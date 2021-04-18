---
title: Glosario del sistema de archivos previsto de Windows
description: Términos especiales usados en ProjFS.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: c6eac8faa83e2c898e4b1a3ada5c24ef81151b22
ms.sourcegitcommit: a48b68a75323edfb902eb04fbe6d0ecba6988c21
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/21/2020
ms.locfileid: "105720135"
---
# <a name="windows-projected-file-system-glossary"></a>Glosario del sistema de archivos previsto de Windows

Términos especiales usados en ProjFS.

<dl>
<dt>

<span id="projfs.glossary_backing_store"></span><span id="PROJFS.GLOSSARY_BACKING_STORE"></span>**memoria auxiliar**
</dt>
<dd>

Datos jerárquicos mantenidos por el proveedor que se proyectan en el sistema de archivos como archivos y directorios.
</dd>

<dt>

<span id="projfs.glossary_dirty_placeholder"></span><span id="PROJFS.GLOSSARY_DIRTY_PLACEHOLDER"></span>**marcador de posición modificado**
</dt>
<dd>

Archivo o directorio que se ha modificado localmente y que ya no es una caché de su estado en el almacén del proveedor.  Consulte [Estado de la caché en la raíz de virtualización](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_full_file_directory"></span><span id="PROJFS.GLOSSARY_FULL_FILE_DIRECTORY"></span>**archivo/directorio completo**
</dt>
<dd>

Un archivo o directorio creado en el sistema de archivos local, o un archivo que se ha modificado, de modo que ya no es una caché de su estado en la memoria auxiliar.  Consulte [Estado de la caché en la raíz de virtualización](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_hydrated_placeholder"></span><span id="PROJFS.GLOSSARY_HYDRATED_PLACEHOLDER"></span>**marcador de posición hidratado**
</dt>
<dd>

Archivo cuyo contenido y sus metadatos se han almacenado en memoria caché en el disco.  Consulte [Estado de la caché en la raíz de virtualización](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_placeholder"></span><span id="PROJFS.GLOSSARY_PLACEHOLDER"></span>**falso**
</dt>
<dd>

Archivo o directorio que no está totalmente presente en el disco.  Consulte [Estado de la caché en la raíz de virtualización](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_tombstone"></span><span id="PROJFS.GLOSSARY_TOMBSTONE"></span>**exclusión**
</dt>
<dd>

Marcador de posición oculto especial que representa un elemento que se ha eliminado del sistema de archivos local.  Consulte [Estado de la caché en la raíz de virtualización](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_virtual_file_directory"></span><span id="PROJFS.GLOSSARY_virtual_file_directory"></span>**directorio/archivo virtual**
</dt>
<dd>

Archivo o directorio que no existe físicamente en el disco, sino que se proyecta en los resultados de la enumeración.  Consulte [Estado de la caché en la raíz de virtualización](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_virtualization_instance"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_INSTANCE"></span>**instancia de virtualización**
</dt>
<dd>

Objeto en memoria que administra la comunicación entre el proveedor y ProjFS para el conjunto de archivos y directorios ubicados en una raíz de virtualización determinada.
</dd>

<dt>

<span id="projfs.glossary_virtualization_root"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_ROOT"></span>**raíz de virtualización**
</dt>
<dd>

Directorio del sistema de archivos en el que se proyectan los datos del proveedor.
</dd>

</dl>

<!--
<dt>

<span id="projfs.glossary_"></span><span id="PROJFS.GLOSSARY_"></span>**TERM**
</dt>
<dd>

DEFINITION
</dd>
-->