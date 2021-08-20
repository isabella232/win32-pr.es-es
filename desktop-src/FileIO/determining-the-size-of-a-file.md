---
description: La función GetFileSize recupera el tamaño de un archivo.
ms.assetid: 4d3a3925-72e8-4350-b46d-e2c25791e862
title: Determinar el tamaño de un archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cdf4185d0bb695d73dc3afd03bb1ee7d6fe95cf606960fbdc41c4ce0b33b732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150618"
---
# <a name="determining-the-size-of-a-file"></a>Determinar el tamaño de un archivo

La [**función GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) recupera el tamaño de un archivo.

Dado que la implementación del sistema de archivos NTFS de archivos permite varias secuencias dentro de un archivo, cualquier aplicación que escriba que acceda a los archivos debe tener en cuenta la posibilidad de que el creador del archivo pueda incluir varias secuencias en el archivo. Si no se comprueban varias secuencias en un archivo, la aplicación puede subestimar el tamaño total del archivo, entre otros errores.

 

 



