---
description: Windows los datos en operaciones de lectura y escritura de archivos en búferes de datos mantenidos por el sistema para optimizar el rendimiento del disco.
ms.assetid: e8c12a1d-f6a4-4850-814d-6f0a712f8f9a
title: Vaciar System-Buffered datos de E/S en el disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0639c5ea909d96a248bb563f1c6a08cd7a526d98
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069941"
---
# <a name="flushing-system-buffered-io-data-to-disk"></a>Vaciar System-Buffered datos de E/S en el disco

Windows los datos en operaciones de lectura y escritura de archivos en búferes de datos mantenidos por el sistema para optimizar el rendimiento del disco. Cuando una aplicación escribe en un archivo, el sistema normalmente almacena en búfer los datos y los escribe en el disco de forma periódica. Una aplicación puede forzar al sistema operativo a escribir el contenido de estos búferes de datos en el disco mediante la [**función FlushFileBuffers.**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) Como alternativa, una aplicación puede especificar que las operaciones de escritura son omitir el búfer de datos y escribir directamente en el disco estableciendo la marca **FILE \_ FLAG NO \_ \_ BUFFERING** cuando se crea o se abre el archivo mediante la [**función CreateFile.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)

Si hay datos en el búfer interno cuando se cierra el archivo, el sistema operativo no escribe automáticamente el contenido del búfer en el disco antes de cerrar el archivo. Si la aplicación no fuerza al sistema operativo a escribir el búfer en el disco antes de cerrar el archivo, el algoritmo de almacenamiento en caché determina cuándo se escribe el búfer.

> [!Note]  
> El acceso a un búfer de datos mientras se usa una operación de lectura o escritura puede dañar el búfer. Las aplicaciones no deben leer, escribir en, volver asignár ni liberar el búfer de datos que usa una operación de lectura o escritura hasta que se complete la operación.

 

 

 



