---
description: Una aplicación lee y escribe en un archivo mediante las funciones ReadFile, ReadFileEx, WriteFile y WriteFileEx.
ms.assetid: 14ecb06c-3f80-47b8-9964-6a2c3b572300
title: Leer y escribir en archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b88de3510a681839a9592bed4755de6249f79db117d94985ddb00320381b92c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119533325"
---
# <a name="reading-from-and-writing-to-files"></a>Leer y escribir en archivos

Una aplicación lee y escribe en un archivo mediante las funciones [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx,**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)y [**WriteFileEx.**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) Estas funciones requieren que se abra un identificador de un archivo para leer y escribir, respectivamente. Leen y escriben un número especificado de bytes en la ubicación indicada por el puntero de archivo. Los datos se leen y escriben exactamente según lo especificado; las funciones no formatearán los datos.

Cuando el puntero de archivo alcanza el final de un archivo y la aplicación intenta leerlo, no se produce ningún error, pero no se leen bytes. Por lo tanto, leer cero bytes sin un error significa que la aplicación ha llegado al final del archivo. Escribir cero bytes no hace nada.

Para obtener más información, vea los temas siguientes:

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                                           | Descripción                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Colocar un puntero de archivo](positioning-a-file-pointer.md)<br/>                                                                         | Windows un puntero de archivo para realizar un seguimiento de los bytes leídos o escritos.<br/>                                                       |
| [Lectura o escritura en archivos mediante un esquema Scatter-Gather datos](reading-from-or-writing-to-files-using-a-scatter-gather-scheme.md)<br/> | Describe un esquema de dispersión y recopilación para leer o escribir fragmentos de datos no continuos en una operación.<br/>                   |
| [Vaciado de System-Buffered datos de E/S en el disco](flushing-system-buffered-i-o-data-to-disk.md)<br/>                                           | Windows los datos en operaciones de lectura y escritura de archivos en búferes de datos mantenidos por el sistema para optimizar el rendimiento del disco.<br/> |
| [Truncamiento o extensión de archivos](truncating-or-extending-files.md)<br/>                                                                   | Una aplicación puede truncar o extender un archivo llamando a [**SetEndOfFile.**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile)<br/>                             |



 

 

 




