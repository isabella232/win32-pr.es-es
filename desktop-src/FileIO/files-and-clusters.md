---
description: Un archivo es una unidad de datos del sistema de archivos a la que un usuario puede acceder y administrar.
ms.assetid: 271bad79-c23b-45ee-938c-d17dae89db1a
title: Archivos y clústeres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75384900d5d487ab02bd19c13cc2c25e9a310b3e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069945"
---
# <a name="files-and-clusters"></a>Archivos y clústeres

Un *archivo* es una unidad de datos del sistema de archivos a la que un usuario puede acceder y administrar. Un archivo debe tener un nombre único en su directorio. Consta de una o varias secuencias de bytes que incluyen un conjunto de datos relacionados, además de un conjunto de atributos (también denominados propiedades) que describen el archivo o los datos del archivo. La hora de creación de un archivo es un ejemplo de un atributo de archivo.

Cuando se crea un archivo, se crea una secuencia predeterminada sin nombre para almacenar todos los datos escritos en el archivo mientras está abierto. También puede crear secuencias adicionales dentro del archivo. Estas secuencias adicionales se conocen como secuencias alternativas. En la ilustración siguiente se muestra un archivo con la secuencia predeterminada y dos secuencias alternativas.

![archivo con una secuencia predeterminada y dos secuencias alternativas](images/fig1.png)

Los atributos de archivo no se almacenan en los flujos de datos con los datos de archivo, sino que se almacenan en otro lugar y se administran mediante el sistema operativo.

Todos los datos del sistema de archivos, incluidos el código de arranque del sistema y los directorios, se almacenan mediante el sistema de archivos NTFS en archivos. Otros sistemas de archivos almacenan esta información en regiones de disco externas al sistema de archivos. Una ventaja de almacenar esta información en archivos es que Windows buscar, acceder y mantener la información fácilmente. Otras ventajas son que cada uno de estos archivos puede estar protegido por un descriptor de seguridad y, en caso de daños parciales en el disco, se pueden reubicar rápidamente en una parte más segura del disco.

La unidad de almacenamiento fundamental de todos los sistemas de archivos admitidos es *un clúster,* que es un grupo de sectores. Esto permite que el sistema de archivos optimice la administración de datos de disco independientemente del tamaño del sector de disco establecido por el controlador de disco de hardware. Si el disco que se va a administrar es grande y se mueven y organizan grandes cantidades de datos en una sola operación, el administrador puede ajustar el tamaño del clúster para adaptarlo.

Windows los archivos a través de objetos [de](file-objects.md)archivo, [identificadores de archivo](file-handles.md)y [punteros de archivo](file-pointers.md).

Para obtener más información sobre las secuencias de archivos, vea [File Secuencias](file-streams.md). Para obtener más información sobre los clústeres, vea [Clústeres y extensiones.](clusters-and-extents.md) Para obtener más información sobre cómo acceder a los archivos y administrarlos, vea [File Management](file-management.md) and File [Management Reference](file-management-reference.md).

## <a name="in-this-section"></a>En esta sección



| Tema                                                       | Descripción                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Archivo Secuencias](file-streams.md)<br/>                 | En el sistema de archivos NTFS, las secuencias contienen los datos que se escriben en un archivo y que proporciona más información sobre un archivo que atributos y propiedades.<br/>                                                                                         |
| [Objetos de archivo](file-objects.md)<br/>                 | *Los objetos de* archivo funcionan como la interfaz lógica entre los procesos de kernel y modo de usuario y los datos de archivo que residen en el disco físico.<br/>                                                                                                      |
| [Identificadores de archivo](file-handles.md)<br/>                 | Cuando un proceso abre un archivo mediante la  función [**CreateFile,**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) se asocia un identificador de archivo a él hasta que el proceso finaliza o el identificador se cierra mediante la [**función CloseHandle.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)<br/> |
| [Punteros de archivo](file-pointers.md)<br/>               | Un puntero de archivo es un valor de desplazamiento de 64 bits que especifica el byte siguiente que se va a leer o la ubicación en la que se va a recibir el byte siguiente escrito.<br/>                                                                                                                 |
| [Clústeres y extensiones](clusters-and-extents.md)<br/> | Se puede hacer referencia a los clústeres desde dos perspectivas diferentes: dentro del archivo y en el volumen.<br/>                                                                                                                                                   |



 

 

