---
description: Hay disponible una comprobación de redundancia cíclica (CRC) de archivos con Windows Instalador.
ms.assetid: c895488b-6e60-4175-8865-4ba4b0cb2d9a
title: Comprobación de CRC durante una instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c81b80a9b1900abf6c294911803df155a4c75025f5ad5ef01609af7345b0431e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379920"
---
# <a name="crc-checking-during-an-installation"></a>Comprobación de CRC durante una instalación

Hay disponible una comprobación de redundancia cíclica (CRC) de archivos con Windows Instalador. La comprobación de CRC es un mecanismo de comprobación de errores, similar a una suma de comprobación, que permite a una aplicación determinar si se ha modificado la información de un archivo. Una vez Windows instalador finaliza la copia de un archivo, obtiene un valor CRC de los archivos de origen y de destino. El instalador comprueba el CRC original marcado en el archivo y lo compara con el CRC calculado a partir de la copia. Se produce un error en la comprobación de CRC si el valor de CRC original no es NULL y es diferente del CRC calculado en la copia. Si el CRC original es NULL, no se produce ninguna comprobación.

El Windows realiza una comprobación de CRC en un archivo en los siguientes casos:

-   Si se [establece la propiedad MSICHECKCRCS](msicheckcrcs.md) y **msidbFileAttributesChecksum** se incluye en el campo Atributos del registro del archivo en la [tabla File](file-table.md). El instalador realiza la comprobación de CRC una vez después de instalar, duplicar o mover el archivo.
-   Si se establece la propiedad [MSICHECKCRCS](msicheckcrcs.md) y **msidbFileAttributesChecksum** se incluye en el campo Atributos del registro del archivo en la tabla Archivo [,](file-table.md)el instalador realiza una comprobación de CRC después de aplicar revisiones al archivo.
-   Si **msidbFileAttributesChecksum** se incluye en el campo Atributos del registro del archivo en la tabla [File](file-table.md), el instalador realiza una comprobación de CRC antes de enlazar imágenes.

Si se produce un error en la comprobación antes de enlazar una imagen, el instalador notifica los dos errores siguientes en el archivo de registro y continúa la instalación sin enlazar el archivo.



| Código | Message                                               |
|------|-------------------------------------------------------|
| 2941 | No se puede calcular el CRC para el archivo \[ 2 \] .             |
| 2942 | La acción BindImage no se ha ejecutado en \[ 2 \] archivos. |



 

Si se produce un error en la comprobación después de copiar, duplicar o revisar un archivo sin comprimir, el instalador notifica el siguiente error. Este error también se notifica si se produce un error en la comprobación después de copiar un archivo comprimido. Si el archivo tiene el atributo **msidbFileAttributesVital,** el archivo se considera vital para la instalación y el usuario obtiene la opción de reintentar o cancelar la instalación. Si el archivo se marca como novital en la columna Atributos de la tabla Archivo [,](file-table.md)el usuario puede omitir el error y continuar, reintentar o cancelar la instalación.



| Código | Message                                         |
|------|-------------------------------------------------|
| 1331 | No se pudo copiar correctamente \[ 2 \] archivo: error de CRC. |



 

Tenga en cuenta que solo se mueven los archivos sin comprimir. Si se produce un error en la comprobación después de mover un archivo sin comprimir, el instalador muestra el siguiente error. Si el archivo tiene el **atributo msidbFileAttributesVital,** el archivo se considera vital para la instalación y se produce un error en la instalación. Si el archivo está marcado como novital en la columna Atributos de la tabla Archivo [,](file-table.md)el usuario obtiene la opción de cancelar o omitir el error y continuar con la instalación.



| Código | Message                                         |
|------|-------------------------------------------------|
| 1332 | No se pudo mover correctamente \[ el archivo \] 2: error de CRC. |



 

Si se produce un error en la comprobación después de aplicar una revisión a un archivo sin comprimir, el instalador muestra el siguiente error. Si el archivo tiene el **atributo msidbFileAttributesVital,** el archivo se considera vital para la instalación y se produce un error en la instalación. Si el archivo está marcado como novital en la columna Atributos de la tabla Archivo [,](file-table.md)el usuario obtiene la opción de cancelar o omitir el error y continuar con la instalación.



| Código | Message                                          |
|------|--------------------------------------------------|
| 1333 | No se pudo aplicar correctamente la \[ revisión al archivo 2: \] error de CRC. |



 

 

 



