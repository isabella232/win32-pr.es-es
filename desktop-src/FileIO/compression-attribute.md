---
description: En un volumen del sistema de archivos NTFS, cada archivo y directorio tiene un atributo de compresión.
ms.assetid: 8aca120c-22a7-4dc8-a921-dfcec1277452
title: Atributo de compresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99fb42aaa30fc3e5d2ef36da85bae194950c587d024510b18233f3c83504ab88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982155"
---
# <a name="compression-attribute"></a>Atributo de compresión

En un volumen del sistema de archivos NTFS, cada archivo y directorio tiene un *atributo de compresión*. Otros sistemas de archivos también pueden implementar un atributo de compresión para archivos y directorios individuales.

Puede determinar si un sistema de archivos admite un atributo de compresión para archivos y directorios llamando a la función [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) y examinando la marca de bits **FILE FILE \_ \_ COMPRESSION.**

Use la [**función GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) o [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) para determinar el atributo de compresión de un archivo o directorio.

Si se establece el atributo de compresión de un archivo **(FILE \_ ATTRIBUTE \_ COMPRESSED),** se comprimen todos los datos del archivo. Si el atributo está claro, no se comprime ninguno de los datos del archivo. No hay ningún estado parcialmente comprimido desde una perspectiva de programación en modo de usuario; el atributo de compresión es un simple indicador booleano del estado de compresión.

El atributo de compresión de un directorio proporciona un atributo de compresión predeterminado para los subdirectorios y archivos recién creados. Cuando se llama a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) [**o CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) para crear un nuevo archivo o directorio, el nuevo archivo o directorio hereda el atributo de compresión de su directorio primario.

Para modificar el **atributo FILE \_ ATTRIBUTE \_ COMPRESSED** de un archivo o directorio, debe usar la [**función DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con el código de control [**FSCTL SET \_ \_ COMPRESSION.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Constantes de atributo de archivo**](file-attribute-constants.md)
</dt> </dl>

 

 
