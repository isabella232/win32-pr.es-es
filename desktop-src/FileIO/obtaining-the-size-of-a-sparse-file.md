---
description: Obtiene el tamaño asignado o el tamaño total de un archivo mediante la función GetCompressedFileSize o GetFileSize.
ms.assetid: 1894ea01-49ff-41e3-9912-1cd75966bd3f
title: Obtención del tamaño de un archivo disperso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93a1c6a33f0d6913e0e6848e4593ea0e0bf0259
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908193"
---
# <a name="obtaining-the-size-of-a-sparse-file"></a>Obtención del tamaño de un archivo disperso

Utilice la función [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) para obtener el tamaño real asignado en el disco para un archivo disperso. Este total no incluye el tamaño de las regiones que se han desasignado porque se han rellenado con ceros. Use la función [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) para determinar el tamaño total de un archivo, incluido el tamaño de las regiones dispersas que se han desasignado.

 

 



