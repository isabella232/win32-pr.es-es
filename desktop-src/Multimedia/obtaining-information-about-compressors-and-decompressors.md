---
title: Obtener información sobre los descomprimores y los descomprimores
description: Obtener información sobre los descomprimores y los descomprimores
ms.assetid: 2f1edfd0-dd30-42ea-a5ae-24265d3f8af3
keywords:
- Administrador de compresión de vídeo (VCM), obtención de información sobre los resaltes
- VCM (administrador de compresión de vídeo), obtención de información sobre los resaltes
- Función ICGetInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 874793233ef0aec4de5b372573fb8dcd79f5d875
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169633"
---
# <a name="obtaining-information-about-compressors-and-decompressors"></a>Obtener información sobre los descomprimores y los descomprimores

En el ejemplo siguiente se usa [**la función ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) para obtener información sobre un descomprimidor o un descomprimidor.


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



En el ejemplo siguiente se usan las macros [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) e [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) para mostrar un cuadro de diálogo Acerca de para el descomprimidor o el descomprimidor, si el cuadro de diálogo existe.


```C++
// If the compressor has an About dialog box, display it.

if ( ICQueryAbout(hIC)) ICAbout(hIC, hwndApp); 
 
```



 

 




