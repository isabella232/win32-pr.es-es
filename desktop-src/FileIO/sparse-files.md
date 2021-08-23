---
description: La compresión de archivos de archivos que contienen principalmente ceros hace un uso eficaz del espacio en disco.
ms.assetid: 7326041d-f11e-4b80-ac4e-07173e418ce7
title: Archivos dispersos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb89a8fd3e8c067d5328756e57d511d4c38d615f2bb19c579208462c3f5bdbf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951054"
---
# <a name="sparse-files"></a>Archivos dispersos

Se dice que un archivo en el que gran parte de los datos son ceros contiene *un conjunto de datos disperso.* Los archivos como estos suelen ser muy grandes, por ejemplo, un archivo que contiene datos de imagen que se van a procesar o una matriz dentro de una base de datos de alta velocidad. El problema con los archivos que contienen conjuntos de datos dispersos es que la mayoría del archivo no contiene datos útiles y, debido a esto, son un uso ineficaz del espacio en disco.

La compresión de archivos en el sistema de archivos NTFS es una solución parcial al problema. Todos los datos del archivo que no se escriben explícitamente se establecen explícitamente en cero. La compresión de archivos compacta estos intervalos de ceros. Sin embargo, un inconveniente de la compresión de archivos es que el tiempo de acceso puede aumentar debido a la compresión de datos y la descompresión.

La compatibilidad con archivos dispersos se introduce en el sistema de archivos NTFS como otra manera de hacer que el uso del espacio en disco sea más eficaz. Cuando se habilita la funcionalidad de archivo disperso, el sistema no asigna espacio en la unidad de disco duro a un archivo, excepto en regiones donde contiene datos distintos de cero. Cuando se intenta realizar una operación de escritura en la que una gran cantidad de datos del búfer es ceros, los ceros no se escriben en el archivo. En su lugar, el sistema de archivos crea una lista interna que contiene las ubicaciones de los ceros en el archivo y esta lista se consulta durante todas las operaciones de lectura. Cuando se realiza una operación de lectura en áreas del archivo donde se encontraban ceros, el sistema de archivos devuelve el número adecuado de ceros en el búfer asignado para la operación de lectura. De esta manera, el mantenimiento del archivo disperso es transparente para todos los procesos que acceden a él y es más eficaz que la compresión para este escenario concreto.

El valor de datos predeterminado de un archivo disperso es cero; sin embargo, se puede establecer en otros valores.

Para obtener más información sobre los archivos dispersos, vea los temas siguientes.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                     | Descripción                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Operaciones de archivos dispersos](sparse-file-operations.md)<br/>                           | Determine si un sistema de archivos admite archivos dispersos llamando a la función GetVolumeInformation.<br/>                                                                                |
| [Obtener el tamaño de un archivo disperso](obtaining-the-size-of-a-sparse-file.md)<br/> | Obtenga el tamaño asignado o el tamaño total de un archivo mediante la [**función GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) o [**GetFileSize.**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize)<br/> |
| [Archivos dispersos y cuotas de disco](sparse-files-and-disk-quota.md)<br/>                | Un archivo disperso afecta a las cuotas de usuario por el tamaño nominal del archivo, no la cantidad real asignada de espacio en disco.<br/>                                                                  |



 

 

 




