---
description: En un volumen del sistema de archivos NTFS, cada archivo y directorio tiene un atributo de compresión.
ms.assetid: 8aca120c-22a7-4dc8-a921-dfcec1277452
title: Atributo Compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e8e86eebe919476851f35f77cf10d6a07035d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913710"
---
# <a name="compression-attribute"></a>Atributo Compression

En un volumen del sistema de archivos NTFS, cada archivo y directorio tiene un *atributo de compresión*. Otros sistemas de archivos también pueden implementar un atributo de compresión para archivos y directorios individuales.

Puede determinar si un sistema de archivos admite un atributo de compresión para archivos y directorios mediante una llamada a la función [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) y examinando el indicador de bits de **compresión de \_ archivo \_ de archivo** .

Utilice la función [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) o [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) para determinar el atributo de compresión de un archivo o directorio.

Si se establece el atributo de compresión de un archivo (**archivo \_ \_ comprimido con atributo**), se comprimen todos los datos del archivo. Si el atributo está desactivado, no se comprime ninguno de los datos del archivo. No hay ningún estado parcialmente comprimido desde una perspectiva de programación de modo de usuario. el atributo Compression es un indicador booleano simple de estado de compresión.

El atributo Compression de un directorio proporciona un atributo de compresión predeterminado para los archivos y subdirectorios recién creados. Cuando se llama a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) o a [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) para crear un nuevo archivo o directorio, el nuevo archivo o directorio hereda el atributo Compression de su directorio principal.

Para modificar el atributo de **archivo \_ \_ comprimido** para un archivo o directorio, debe usar la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con el código de control de [**\_ \_ compresión set de FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Constantes de atributo de archivo**](file-attribute-constants.md)
</dt> </dl>

 

 
