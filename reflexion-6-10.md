`git log` muestra el historial de commits visibles del proyecto, mientras que `git reflog` registra todos los movimientos locales del repositorio, incluso los que ya no aparecen en ese historial.

Imagina que haces un `git reset --hard` y pierdes varios commits importantes porque no los habías subido. Con `git reflog` puedes ver a qué commit apuntaba tu repositorio antes del reset, copiar ese identificador y volver a él, recuperando todo el trabajo perdido.

Porque `git reflog` no es una garantía permanente: solo guarda el historial local por tiempo limitado y puede borrarse (por limpieza automática o si se pierde el repositorio). Si ejecutas un `reset --hard` y no recuperas los commits a tiempo, puedes perderlos definitivamente, sobre todo si nunca se subieron a remoto.
