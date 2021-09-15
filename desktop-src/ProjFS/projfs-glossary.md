---
title: Windows Glosario del sistema de archivos proyectado
description: Términos especiales usados en ProjFS.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: c6eac8faa83e2c898e4b1a3ada5c24ef81151b22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580197"
---
# <a name="windows-projected-file-system-glossary"></a>Windows Glosario del sistema de archivos proyectado

Términos especiales usados en ProjFS.

<dl>
<dt>

<span id="projfs.glossary_backing_store"></span><span id="PROJFS.GLOSSARY_BACKING_STORE"></span>**almacén de respaldo**
</dt>
<dd>

Datos jerárquicos mantenidos por el proveedor que se proyectan en el sistema de archivos como archivos y directorios.
</dd>

<dt>

<span id="projfs.glossary_dirty_placeholder"></span><span id="PROJFS.GLOSSARY_DIRTY_PLACEHOLDER"></span>**marcador de posición dirty**
</dt>
<dd>

Un archivo o directorio que se ha modificado localmente y ya no es una memoria caché de su estado en el almacén del proveedor.  Consulte [Estado de caché en la raíz de virtualización.](cache-state.md)
</dd>

<dt>

<span id="projfs.glossary_full_file_directory"></span><span id="PROJFS.GLOSSARY_FULL_FILE_DIRECTORY"></span>**archivo o directorio completos**
</dt>
<dd>

Un archivo o directorio que se creó en el sistema de archivos local o un archivo que se ha modificado, lo que hace que ya no sea una memoria caché de su estado en el almacén de respaldo.  Consulte [Estado de caché en la raíz de virtualización.](cache-state.md)
</dd>

<dt>

<span id="projfs.glossary_hydrated_placeholder"></span><span id="PROJFS.GLOSSARY_HYDRATED_PLACEHOLDER"></span>**marcador de posición hidratado**
</dt>
<dd>

Archivo cuyo contenido y metadatos se han almacenado en caché en el disco.  Consulte [Estado de caché en la raíz de virtualización.](cache-state.md)
</dd>

<dt>

<span id="projfs.glossary_placeholder"></span><span id="PROJFS.GLOSSARY_PLACEHOLDER"></span>**Marcador**
</dt>
<dd>

Un archivo o directorio que no está totalmente presente en el disco.  Consulte [Estado de caché en la raíz de virtualización.](cache-state.md)
</dd>

<dt>

<span id="projfs.glossary_tombstone"></span><span id="PROJFS.GLOSSARY_TOMBSTONE"></span>**Lápida**
</dt>
<dd>

Marcador de posición oculto especial que representa un elemento que se ha eliminado del sistema de archivos local.  Consulte [Estado de caché en la raíz de virtualización.](cache-state.md)
</dd>

<dt>

<span id="projfs.glossary_virtual_file_directory"></span><span id="PROJFS.GLOSSARY_virtual_file_directory"></span>**archivo o directorio virtual**
</dt>
<dd>

Un archivo o directorio que no existe físicamente en el disco, pero que se proyecta en resultados de enumeración.  Consulte [Estado de caché en la raíz de virtualización.](cache-state.md)
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