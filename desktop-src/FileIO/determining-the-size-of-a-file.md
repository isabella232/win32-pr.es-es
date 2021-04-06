---
description: La función GetFileSize recupera el tamaño de un archivo.
ms.assetid: 4d3a3925-72e8-4350-b46d-e2c25791e862
title: Determinar el tamaño de un archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f7205c47fe25b223dbcc12322516ff2b162fcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002093"
---
# <a name="determining-the-size-of-a-file"></a>Determinar el tamaño de un archivo

La función [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) recupera el tamaño de un archivo.

Dado que la implementación del sistema de archivos NTFS de archivos permite varias secuencias dentro de un archivo, cualquier aplicación que escriba que tenga acceso a los archivos debe tener en cuenta la posibilidad de que el creador del archivo pueda incluir varias secuencias en el archivo. Si no se comprueban varias secuencias en un archivo, la aplicación puede subestimar el tamaño total del archivo, entre otros errores.

 

 



