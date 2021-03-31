---
title: Obtener información acerca de los compresores y descompresores
description: Obtener información acerca de los compresores y descompresores
ms.assetid: 2f1edfd0-dd30-42ea-a5ae-24265d3f8af3
keywords:
- Administrador de compresión de vídeo (VCM), obtener información sobre los compresores
- VCM (Administrador de compresión de vídeo), obtener información sobre los compresores
- ICGetInfo función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 874793233ef0aec4de5b372573fb8dcd79f5d875
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418483"
---
# <a name="obtaining-information-about-compressors-and-decompressors"></a><span data-ttu-id="11459-106">Obtener información acerca de los compresores y descompresores</span><span class="sxs-lookup"><span data-stu-id="11459-106">Obtaining Information About Compressors and Decompressors</span></span>

<span data-ttu-id="11459-107">En el ejemplo siguiente se usa la función [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) para obtener información sobre un compresor o descompresor.</span><span class="sxs-lookup"><span data-stu-id="11459-107">The following example uses the [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) function to obtain information about a compressor or decompressor.</span></span>


```C++
ICINFO ICInfo; 
ICGetInfo(hIC, &ICInfo, sizeof(ICInfo)); 
 
```



<span data-ttu-id="11459-108">En el ejemplo siguiente se usan las macros [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) y [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) para obtener los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="11459-108">The following example uses the [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) and [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) macros to obtain the default values.</span></span>


```C++
DWORD dwKeyFrameRate, dwQuality; 
dwKeyFrameRate = ICGetDefaultKeyFrameRate(hIC); 
dwQuality = ICGetDefaultQuality(hIC); 
 
```



<span data-ttu-id="11459-109">En el ejemplo siguiente se usan las macros [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) y [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) para mostrar un cuadro de diálogo acerca de para el compresor o descompresor, si el cuadro de diálogo existe.</span><span class="sxs-lookup"><span data-stu-id="11459-109">The following example uses the [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) and [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) macros to display an About dialog box for the compressor or decompressor, if the dialog box exists.</span></span>


```C++
// If the compressor has an About dialog box, display it.

if ( ICQueryAbout(hIC)) ICAbout(hIC, hwndApp); 
 
```



 

 




