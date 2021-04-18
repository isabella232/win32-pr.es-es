---
description: Una aplicación Lee y escribe en un archivo mediante las funciones ReadFile, ReadFileEx, WriteFile y WriteFileEx.
ms.assetid: 14ecb06c-3f80-47b8-9964-6a2c3b572300
title: Leer y escribir en archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd0e6518ce2430e18bbb11033023ee6dc274573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668143"
---
# <a name="reading-from-and-writing-to-files"></a>Leer y escribir en archivos

Una aplicación Lee y escribe en un archivo mediante las funciones [**readfile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex), [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)y [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) . Estas funciones requieren un identificador de un archivo que se va a abrir para lectura y escritura, respectivamente. Leen y escriben un número especificado de bytes en la ubicación indicada por el puntero de archivo. Los datos se leen y escriben exactamente como se especifican; las funciones no dan formato a los datos.

Cuando el puntero de archivo alcanza el final de un archivo y la aplicación intenta leer el archivo, no se produce ningún error, pero no se lee ningún byte. Por lo tanto, la lectura de cero bytes sin un error significa que la aplicación ha alcanzado el final del archivo. La escritura de cero bytes no hace nada.

Para obtener más información, vea los siguientes temas.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                                           | Descripción                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Colocar un puntero de archivo](positioning-a-file-pointer.md)<br/>                                                                         | Windows usa un puntero de archivo para hacer un seguimiento de los bytes leídos o escritos.<br/>                                                       |
| [Leer o escribir en archivos mediante un esquema de Scatter-Gather](reading-from-or-writing-to-files-using-a-scatter-gather-scheme.md)<br/> | Describe un esquema de dispersión y recopilación para leer o escribir fragmentos de datos no contiguos en una sola operación.<br/>                   |
| [Vaciar System-Buffered datos de e/s en el disco](flushing-system-buffered-i-o-data-to-disk.md)<br/>                                           | Windows almacena los datos en las operaciones de lectura y escritura de archivos en los búferes de datos mantenidos por el sistema para optimizar el rendimiento del disco.<br/> |
| [Truncar o extender archivos](truncating-or-extending-files.md)<br/>                                                                   | Una aplicación puede truncar o extender un archivo mediante una llamada a [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).<br/>                             |



 

 

 




