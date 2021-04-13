---
description: La propiedad Volume establece o recupera el volumen del altavoz para la salida de la secuencia de audio.
ms.assetid: b6e22d07-525b-4af2-898c-ce3ed16ea9c1
title: Volume (Propiedad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9c85bc2d20a613e61d454f75b9663284188c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543766"
---
# <a name="volume-property"></a><span data-ttu-id="36b19-103">Volume (Propiedad)</span><span class="sxs-lookup"><span data-stu-id="36b19-103">Volume Property</span></span>

> [!Note]  
> <span data-ttu-id="36b19-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="36b19-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="36b19-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="36b19-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="36b19-106">La `Volume` propiedad establece o recupera el volumen del altavoz de la salida de la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="36b19-106">The `Volume` property sets or retrieves the speaker volume for the audio stream output.</span></span>

``` syntax
[ iVolume = ] MSWebDVD.Volume
```

## <a name="return-value"></a><span data-ttu-id="36b19-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="36b19-107">Return Value</span></span>

<span data-ttu-id="36b19-108">Devuelve el nivel de volumen como atenuación en decibelios como un entero.</span><span class="sxs-lookup"><span data-stu-id="36b19-108">Returns the volume level as attenuation in decibels as an Integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="36b19-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="36b19-109">Remarks</span></span>

<span data-ttu-id="36b19-110">Esta propiedad es de lectura/escritura con un valor predeterminado de 0.</span><span class="sxs-lookup"><span data-stu-id="36b19-110">This property is read/write with a default value of 0.</span></span> <span data-ttu-id="36b19-111">El volumen completo es 0 y 10.000 es el silencio; la escala es logarítmica.</span><span class="sxs-lookup"><span data-stu-id="36b19-111">Full volume is 0, and 10,000 is silence; the scale is logarithmic.</span></span> <span data-ttu-id="36b19-112">Multiplique el nivel de decibelios deseado por 100 (por ejemplo 10.000 = 100 dB).</span><span class="sxs-lookup"><span data-stu-id="36b19-112">Multiply the desired decibel level by 100 (for example 10,000 = 100 dB).</span></span>

 

 



