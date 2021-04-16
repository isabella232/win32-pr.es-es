---
description: Windows almacena los datos en las operaciones de lectura y escritura de archivos en los búferes de datos mantenidos por el sistema para optimizar el rendimiento del disco.
ms.assetid: e8c12a1d-f6a4-4850-814d-6f0a712f8f9a
title: Vaciar System-Buffered datos de e/s en el disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0639c5ea909d96a248bb563f1c6a08cd7a526d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546691"
---
# <a name="flushing-system-buffered-io-data-to-disk"></a>Vaciar System-Buffered datos de e/s en el disco

Windows almacena los datos en las operaciones de lectura y escritura de archivos en los búferes de datos mantenidos por el sistema para optimizar el rendimiento del disco. Cuando una aplicación escribe en un archivo, el sistema normalmente almacena en búfer los datos y escribe los datos en el disco de forma periódica. Una aplicación puede obligar al sistema operativo a escribir el contenido de estos búferes de datos en el disco mediante la función [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) . Como alternativa, una aplicación puede especificar que las operaciones de escritura omitan el búfer de datos y escriban directamente en el disco estableciendo la marca de **archivo sin marca de \_ almacenamiento en \_ \_ búfer** cuando se crea o se abre el archivo con la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .

Si hay datos en el búfer interno cuando el archivo está cerrado, el sistema operativo no escribe automáticamente el contenido del búfer en el disco antes de cerrar el archivo. Si la aplicación no obliga al sistema operativo a escribir el búfer en el disco antes de cerrar el archivo, el algoritmo de almacenamiento en caché determina cuándo se escribe el búfer.

> [!Note]  
> El acceso a un búfer de datos mientras una operación de lectura o escritura lo está usando puede dañar el búfer. Las aplicaciones no deben leer, escribir en, reasignar o liberar el búfer de datos que está usando una operación de lectura o escritura hasta que se complete la operación.

 

 

 



