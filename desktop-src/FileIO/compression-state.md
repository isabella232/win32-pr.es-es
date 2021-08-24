---
description: Cada archivo y directorio de un volumen que admite la compresión de archivos y directorios individuales tiene un estado de compresión.
ms.assetid: 9db1b2e2-864e-45b5-8227-400cad75222e
title: Estado de compresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19abfe0deecb951c00dacb00c64dd8dcf7af56d37fe9112095cdce403619f843
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582425"
---
# <a name="compression-state"></a>Estado de compresión

Cada archivo y directorio de un volumen que admite la compresión de archivos y directorios individuales tiene un *estado de compresión*.

Mientras que el atributo de compresión de un archivo o directorio indica simplemente si el archivo o directorio está comprimido o no comprimido, el estado de compresión también especifica el formato de los datos comprimidos.

Use el código de control [**\_ FSCTL GET \_ COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) para determinar el estado de compresión de un archivo o directorio.

El estado de compresión se codifica como un valor de 16 bits. Un valor de estado de compresión de COMPRESSION \_ FORMAT NONE indica que un archivo no está \_ comprimido. Un valor de COMPRESSION \_ FORMAT DEFAULT indica que un archivo está comprimido con el formato de compresión \_ predeterminado. Cualquier otro valor indica que un archivo está comprimido, utilizando el formato de compresión especificado por el valor de estado de compresión.

Use el código de control [**FSCTL \_ SET \_ COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) para establecer el estado de compresión de un archivo o directorio. Esta operación también establece el atributo de compresión del archivo o directorio.

Al establecer el estado de compresión de un archivo en un valor distinto de cero, se comprime el archivo con el formato de compresión codificado por el valor de estado de compresión. Al establecer el estado de compresión de un archivo en cero, se descomprime el archivo. Se trata de operaciones sincrónicas. El archivo se comprime o descomprime inmediatamente cuando se establece su estado de compresión.

Establecer el estado de compresión de un directorio no provoca ninguna compresión o descompresión inmediatas. En su lugar, al establecer el estado de compresión de un directorio se establece un estado de compresión predeterminado que se dará a todos los archivos y subdirectorios recién creados.

 

 
