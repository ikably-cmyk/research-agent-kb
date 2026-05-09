# /pending-upload — Buzón temporal de markdowns

Esta carpeta contiene markdowns que aún NO han sido subidos manualmente al data source "Protocolos Laser Dental y PBM" en MindStudio UI.

## Cómo funciona

1. El pipeline (cron diario o Telegram bot) procesa un paper y genera un markdown.
2. El markdown se pushea a /kb/ (fuente de verdad permanente).
3. El mismo markdown se copia a /pending-upload/ (buzón temporal).
4. El audit diario cuenta los archivos aquí y manda email a Isaac con la lista.
5. Isaac descarga los archivos, los arrastra a MindStudio UI, y los borra de /pending-upload/.

## Estado actual

Si esta carpeta tiene archivos, hay papers esperando subida manual.
Si está vacía, todo está al día.
