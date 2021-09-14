---
description: Obtenga el tamaño asignado o el tamaño total de un archivo mediante la función GetCompressedFileSize o GetFileSize.
ms.assetid: 1894ea01-49ff-41e3-9912-1cd75966bd3f
title: Obtener el tamaño de un archivo disperso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93a1c6a33f0d6913e0e6848e4593ea0e0bf0259
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069885"
---
# <a name="obtaining-the-size-of-a-sparse-file"></a>Obtener el tamaño de un archivo disperso

Use la [**función GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) para obtener el tamaño real asignado en el disco para un archivo disperso. Este total no incluye el tamaño de las regiones que se desasignaron porque se rellenaron con ceros. Use la [**función GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) para determinar el tamaño total de un archivo, incluido el tamaño de las regiones dispersas que se desasignaron.

 

 



