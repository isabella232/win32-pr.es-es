---
description: Un archivo es una unidad de datos del sistema de archivos a la que un usuario puede tener acceso y administrar.
ms.assetid: 271bad79-c23b-45ee-938c-d17dae89db1a
title: Archivos y clústeres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75384900d5d487ab02bd19c13cc2c25e9a310b3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276184"
---
# <a name="files-and-clusters"></a>Archivos y clústeres

Un *archivo* es una unidad de datos del sistema de archivos a la que un usuario puede tener acceso y administrar. Un archivo debe tener un nombre único en su directorio. Consta de una o más secuencias de bytes que contienen un conjunto de datos relacionados, además de un conjunto de atributos (también denominados propiedades) que describen el archivo o los datos del archivo. La hora de creación de un archivo es un ejemplo de un atributo de archivo.

Cuando se crea un archivo, se crea una secuencia predeterminada sin nombre para almacenar todos los datos escritos en el archivo mientras está abierto. También puede crear secuencias adicionales dentro del archivo. Estas secuencias adicionales se denominan secuencias alternativas. En la ilustración siguiente se muestra un archivo con la secuencia predeterminada y dos flujos alternativos.

![archivo con una secuencia predeterminada y dos flujos alternativos](images/fig1.png)

Los atributos de archivo no se almacenan en los flujos de datos con los datos de archivo, sino que se almacenan en otro lugar y se administran mediante el sistema operativo.

Todos los datos del sistema de archivos, incluidos el código y los directorios de arranque del sistema, se almacenan en los archivos del sistema de archivos NTFS. Otros sistemas de archivos almacenan esta información en regiones de disco externas al sistema de archivos. Una ventaja de almacenar esta información en los archivos es que Windows puede ubicar, tener acceso y mantener la información fácilmente. Otras ventajas son que cada uno de estos archivos puede estar protegido por un descriptor de seguridad y, en el caso de daños parciales en el disco, se pueden reubicar rápidamente en una parte más segura del disco.

La unidad de almacenamiento fundamental de todos los sistemas de archivos admitidos es un *clúster*, que es un grupo de sectores. Esto permite que el sistema de archivos optimice la administración de los datos de disco independientemente del tamaño del sector del disco establecido por el controlador de disco de hardware. Si el disco que se va a administrar es grande y se mueven grandes cantidades de datos y se organizan en una sola operación, el administrador puede ajustar el tamaño del clúster para que se adapte a esto.

Windows administra los archivos a través de [objetos de archivo](file-objects.md), [identificadores de archivo](file-handles.md)y [punteros de archivo](file-pointers.md).

Para obtener más información sobre las secuencias de archivos, consulte [secuencias de archivo](file-streams.md). Para obtener más información sobre los clústeres, consulte [clústeres y extensiones](clusters-and-extents.md). Para obtener más información sobre cómo obtener acceso a los archivos y administrarlos, consulte [Administración](file-management.md) de archivos y [referencia de administración de archivos](file-management-reference.md).

## <a name="in-this-section"></a>En esta sección



| Tema                                                       | Descripción                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Secuencias de archivo](file-streams.md)<br/>                 | En el sistema de archivos NTFS, las secuencias contienen los datos que se escriben en un archivo y que proporcionan más información sobre un archivo que los atributos y las propiedades.<br/>                                                                                         |
| [Objetos de archivo](file-objects.md)<br/>                 | Los *objetos de archivo* funcionan como la interfaz lógica entre los procesos de kernel y de modo de usuario y los datos de archivo que residen en el disco físico.<br/>                                                                                                      |
| [Identificadores de archivo](file-handles.md)<br/>                 | Cuando un proceso abre un archivo mediante la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , se asocia un *identificador de archivo* hasta que el proceso finaliza o el identificador se cierra con la función [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .<br/> |
| [Punteros de archivo](file-pointers.md)<br/>               | Un puntero de archivo es un valor de desplazamiento de 64 bits que especifica el siguiente byte que se va a leer o la ubicación en la que se va a recibir el siguiente byte escrito.<br/>                                                                                                                 |
| [Clústeres y extensiones](clusters-and-extents.md)<br/> | Se puede hacer referencia a los clústeres desde dos perspectivas diferentes: dentro del archivo y en el volumen.<br/>                                                                                                                                                   |



 

 

