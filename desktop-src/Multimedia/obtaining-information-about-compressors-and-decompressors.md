---
title: Obtener información acerca de los descomprimores y los descompresores
description: Obtener información acerca de los descomprimores y los descompresores
ms.assetid: 2f1edfd0-dd30-42ea-a5ae-24265d3f8af3
keywords:
- Administrador de compresión de vídeo (VCM), obtención de información sobre los resaltes
- VCM (administrador de compresión de vídeo), obtención de información sobre los resaltes
- Función ICGetInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 874793233ef0aec4de5b372573fb8dcd79f5d875
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370405"
---
# <a name="obtaining-information-about-compressors-and-decompressors"></a>Obtener información acerca de los descomprimores y los descompresores

En el ejemplo siguiente se usa [**la función ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) para obtener información sobre un descomprimidor o descompresión.


```C++
ICINFO ICInfo; 
ICGetInfo(hIC, &ICInfo, sizeof(ICInfo)); 
 
```



En el ejemplo siguiente se usan las macros [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) [**e ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) para obtener los valores predeterminados.


```C++
DWORD dwKeyFrameRate, dwQuality; 
dwKeyFrameRate = ICGetDefaultKeyFrameRate(hIC); 
dwQuality = ICGetDefaultQuality(hIC); 
 
```



En el ejemplo siguiente se usan las macros [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) y [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) para mostrar un cuadro de diálogo Acerca de para el descomprimidor o el descompresión, si el cuadro de diálogo existe.


```C++
// If the compressor has an About dialog box, display it.

if ( ICQueryAbout(hIC)) ICAbout(hIC, hwndApp); 
 
```



 

 




