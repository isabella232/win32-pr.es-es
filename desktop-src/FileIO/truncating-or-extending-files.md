---
description: Una aplicación puede truncar o extender un archivo mediante una llamada a SetEndOfFile.
ms.assetid: 23a0242d-50e9-4324-bb09-505afe383a80
title: Truncar o extender archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daf8a2d4e7e346bfea41285be97d6d756e2a6b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688284"
---
# <a name="truncating-or-extending-files"></a>Truncar o extender archivos

Una aplicación puede truncar o extender un archivo mediante una llamada a [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile). Esta función establece el marcador de fin de archivo en la posición actual del puntero de archivo.

Tenga en cuenta que cuando se extiende un archivo, no se define el contenido entre las ubicaciones de fin de archivo antiguas y nuevas.

 

 



