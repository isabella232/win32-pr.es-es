---
title: Obtener información sobre los descomprimores y los descomprimores
description: Obtener información sobre los descomprimores y los descomprimores
ms.assetid: 2f1edfd0-dd30-42ea-a5ae-24265d3f8af3
keywords:
- Administrador de compresión de vídeo (VCM), obtención de información sobre los ingerentes
- VCM (administrador de compresión de vídeo), obtención de información sobre los resaltes
- Función ICGetInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b023a8f82fa92aa78a2a2dcf47a8f6c9447f943ac0f68440c6d7aff3123fc84e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038445"
---
# <a name="obtaining-information-about-compressors-and-decompressors"></a>Obtener información sobre los descomprimores y los descomprimores

En el ejemplo siguiente se usa [**la función ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) para obtener información sobre un descompresión o un descompresión.


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



 

 




