---
description: La compresión de archivos que contienen principalmente ceros hace un uso eficaz del espacio en disco.
ms.assetid: 7326041d-f11e-4b80-ac4e-07173e418ce7
title: Archivos dispersos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c282ca89c9dc9e44800a2a7fc969c3f883006b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666625"
---
# <a name="sparse-files"></a>Archivos dispersos

Se dice que un archivo en el que muchos de los datos son ceros contiene un *conjunto de datos dispersos*. Los archivos como estos suelen ser muy grandes, por ejemplo, un archivo que contiene datos de imagen que se van a procesar o una matriz en una base de datos de alta velocidad. El problema con los archivos que contienen conjuntos de datos dispersos es que la mayoría del archivo no contiene datos útiles y, debido a ello, son un uso ineficaz del espacio en disco.

La compresión de archivos en el sistema de archivos NTFS es una solución parcial del problema. Todos los datos del archivo que no se escriben explícitamente se establecen explícitamente en cero. La compresión de archivos compacta estos intervalos de ceros. Sin embargo, un inconveniente de la compresión de archivos es que el tiempo de acceso puede aumentar debido a la compresión y descompresión de datos.

La compatibilidad con archivos dispersos se incluye en el sistema de archivos NTFS como otra manera de aumentar la eficacia del uso del espacio en disco. Cuando está habilitada la funcionalidad de archivos dispersos, el sistema no asigna espacio en la unidad de disco duro a un archivo, excepto en las regiones donde contiene datos distintos de cero. Cuando se intenta realizar una operación de escritura en la que una gran cantidad de datos en el búfer es ceros, los ceros no se escriben en el archivo. En su lugar, el sistema de archivos crea una lista interna que contiene las ubicaciones de los ceros en el archivo y esta lista se consulta durante todas las operaciones de lectura. Cuando se realiza una operación de lectura en áreas del archivo donde se encuentran ceros, el sistema de archivos devuelve el número adecuado de ceros en el búfer asignado para la operación de lectura. De esta manera, el mantenimiento del archivo disperso es transparente para todos los procesos que tienen acceso a él y es más eficaz que la compresión para este escenario concreto.

El valor de datos predeterminado de un archivo disperso es cero; sin embargo, se puede establecer en otros valores.

Para obtener más información acerca de los archivos dispersos, vea los temas siguientes.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                     | Descripción                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Operaciones de archivos dispersos](sparse-file-operations.md)<br/>                           | Determine si un sistema de archivos admite archivos dispersos mediante una llamada a la función GetVolumeInformation.<br/>                                                                                |
| [Obtención del tamaño de un archivo disperso](obtaining-the-size-of-a-sparse-file.md)<br/> | Obtiene el tamaño asignado o el tamaño total de un archivo mediante la función [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) o [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) .<br/> |
| [Archivos dispersos y cuotas de disco](sparse-files-and-disk-quota.md)<br/>                | Un archivo disperso afecta a las cuotas de usuario por el tamaño nominal del archivo, no por la cantidad de espacio en disco real asignada.<br/>                                                                  |



 

 

 




