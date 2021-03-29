---
description: Cada archivo y directorio de un volumen que admite la compresión de archivos y directorios individuales tiene un estado de compresión.
ms.assetid: 9db1b2e2-864e-45b5-8227-400cad75222e
title: Estado de compresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e182921a6c5e1b79c08fbafb6a8104c4bd8ca1cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277057"
---
# <a name="compression-state"></a>Estado de compresión

Cada archivo y directorio de un volumen que admite la compresión de archivos y directorios individuales tiene un *Estado de compresión*.

Mientras que el atributo de compresión de un archivo o directorio indica simplemente si el archivo o el directorio está comprimido o no comprimido, el estado de compresión también especifica el formato de los datos comprimidos.

Use el código de control de [**\_ \_ compresión de FSCTL obtener**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) para determinar el estado de compresión de un archivo o directorio.

El estado de compresión se codifica como un valor de 16 bits. Un valor de estado de compresión de formato de compresión \_ \_ None indica que un archivo no está comprimido. Un valor de formato de compresión \_ \_ predeterminado indica que se comprime un archivo con el formato de compresión predeterminado. Cualquier otro valor indica que se comprime un archivo con el formato de compresión especificado por el valor de estado de compresión.

Use el código de control de [**\_ \_ compresión Set Compression**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) para establecer el estado de compresión de un archivo o directorio. Esta operación también establece el atributo Compression del archivo o directorio.

Al establecer el estado de compresión de un archivo en un valor distinto de cero, se comprime el archivo con el formato de compresión codificado por el valor de estado de compresión. Al establecer el estado de compresión de un archivo en cero, se descomprime el archivo. Se trata de operaciones sincrónicas. El archivo se comprime o se descomprime inmediatamente al establecer su estado de compresión.

Establecer el estado de compresión de un directorio no provoca ninguna compresión o descompresión inmediata. En su lugar, el establecimiento del estado de compresión de un directorio establece un estado de compresión predeterminado que se asignará a todos los archivos y subdirectorios recién creados.

 

 
