---
description: Una aplicación puede truncar o extender un archivo llamando a SetEndOfFile.
ms.assetid: 23a0242d-50e9-4324-bb09-505afe383a80
title: Truncamiento o extensión de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daf8a2d4e7e346bfea41285be97d6d756e2a6b26
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069818"
---
# <a name="truncating-or-extending-files"></a>Truncamiento o extensión de archivos

Una aplicación puede truncar o extender un archivo llamando a [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile). Esta función establece el marcador de fin de archivo en la posición actual del puntero de archivo.

Tenga en cuenta que cuando se extiende un archivo, no se define el contenido entre las ubicaciones de fin de archivo anterior y nueva.

 

 



