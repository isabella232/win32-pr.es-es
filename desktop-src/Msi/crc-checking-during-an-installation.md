---
description: Hay disponible una comprobación de redundancia cíclica (CRC) de archivos con Windows Installer.
ms.assetid: c895488b-6e60-4175-8865-4ba4b0cb2d9a
title: Comprobación de CRC durante una instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e03bb6754b0259aa8b27333c8137408e7dc956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277984"
---
# <a name="crc-checking-during-an-installation"></a>Comprobación de CRC durante una instalación

Hay disponible una comprobación de redundancia cíclica (CRC) de archivos con Windows Installer. La comprobación de CRC es un mecanismo de comprobación de errores, similar a una suma de comprobación, que permite que una aplicación determine si se ha modificado la información de un archivo. Una vez que la Windows Installer termina de copiar un archivo, obtiene un valor CRC de los archivos de origen y de destino. El instalador comprueba el CRC original marcado en el archivo y lo compara con la CRC calculada a partir de la copia. Se produce un error en la comprobación de CRC si el valor CRC original no es NULL y es diferente del CRC calculado en la copia. Si el CRC original es null, no se realiza ninguna comprobación.

El Windows Installer realiza una comprobación de CRC en un archivo en los casos siguientes:

-   Si se establece la [propiedad MSICHECKCRCS](msicheckcrcs.md) y **msidbFileAttributesChecksum** se incluye en el campo Attributes del registro del archivo en la [tabla File](file-table.md). El instalador realiza la comprobación de CRC una vez después de instalar, duplicar o mover el archivo.
-   Si se establece la [propiedad MSICHECKCRCS](msicheckcrcs.md) y **msidbFileAttributesChecksum** se incluye en el campo Attributes del registro del archivo en la [tabla File](file-table.md), el instalador realiza una comprobación CRC después de aplicar la revisión del archivo.
-   Si el **msidbFileAttributesChecksum** se incluye en el campo atributos del registro del archivo en la [tabla de archivos](file-table.md), el instalador realiza una comprobación de CRC antes de enlazar las imágenes.

Si se produce un error en la comprobación antes de enlazar una imagen, el instalador informa de los dos errores siguientes en el archivo de registro y continúa con la instalación sin enlazar el archivo.



| Código | Message                                               |
|------|-------------------------------------------------------|
| 2941 | No se puede calcular la CRC del archivo \[ 2 \] .             |
| 2942 | La acción BindImage no se ejecutó en el \[ \] archivo 2. |



 

Si se produce un error en la comprobación después de copiar, duplicar o revisar un archivo sin comprimir, el instalador informa del siguiente error. También se muestra este error si se produce un error en la comprobación después de copiar un archivo comprimido. Si el archivo tiene el atributo **msidbFileAttributesVital** , el archivo se considera vital para la instalación y el usuario obtiene la opción de Reintentar o cancelar la instalación. Si el archivo está marcado como no vital en la columna atributos de la [tabla archivo](file-table.md), el usuario puede omitir el error y continuar, reintentar o cancelar la instalación.



| Código | Message                                         |
|------|-------------------------------------------------|
| 1331 | No se pudo copiar correctamente el \[ \] archivo 2: error de CRC. |



 

Tenga en cuenta que solo se mueven los archivos sin comprimir. Si se produce un error en la comprobación después de que se mueva un archivo sin comprimir, el instalador muestra el siguiente error. Si el archivo tiene el atributo **msidbFileAttributesVital** , el archivo se considera vital para la instalación y se produce un error en la instalación. Si el archivo está marcado como no vital en la columna atributos de la [tabla archivo](file-table.md), el usuario obtiene la opción de cancelar o omitir el error y continuar con la instalación.



| Código | Message                                         |
|------|-------------------------------------------------|
| 1332 | No se pudo quitar correctamente el \[ \] archivo 2: error de CRC. |



 

Si se produce un error en la comprobación después de revisar un archivo sin comprimir, el instalador muestra el siguiente error. Si el archivo tiene el atributo **msidbFileAttributesVital** , el archivo se considera vital para la instalación y se produce un error en la instalación. Si el archivo está marcado como no vital en la columna atributos de la [tabla archivo](file-table.md), el usuario obtiene la opción de cancelar o omitir el error y continuar con la instalación.



| Código | Message                                          |
|------|--------------------------------------------------|
| 1333 | No se pudo revisar correctamente el \[ \] archivo 2: error de CRC. |



 

 

 



