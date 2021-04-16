---
description: La propiedad FramesPerSecond recupera la velocidad de fotogramas de vídeo para el título actual del DVD.
ms.assetid: c5d36308-1447-4636-9b3a-4a3f93d27789
title: Propiedad FramesPerSecond
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e00ec3281d88a2901f630c9231edbf1e76a89c23
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677105"
---
# <a name="framespersecond-property"></a><span data-ttu-id="1ed47-103">Propiedad FramesPerSecond</span><span class="sxs-lookup"><span data-stu-id="1ed47-103">FramesPerSecond Property</span></span>

> [!Note]  
> <span data-ttu-id="1ed47-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1ed47-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="1ed47-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="1ed47-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="1ed47-106">La `FramesPerSecond` propiedad recupera la velocidad de fotogramas de vídeo del título actual del DVD.</span><span class="sxs-lookup"><span data-stu-id="1ed47-106">The `FramesPerSecond` property retrieves the video frame rate for the current DVD title.</span></span>

``` syntax
[ iFramesPerSec = ] MSWebDVD.FramesPerSecond
```

## <a name="return-value"></a><span data-ttu-id="1ed47-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ed47-107">Return Value</span></span>

<span data-ttu-id="1ed47-108">Devuelve un valor entero que representa la velocidad de fotogramas de vídeo; 25 o 30 fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="1ed47-108">Returns an integer value representing the video frame rate; either 25 or 30 frames per second.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ed47-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1ed47-109">Remarks</span></span>

<span data-ttu-id="1ed47-110">Esta propiedad es de solo lectura y no tiene ningún valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1ed47-110">This property is read-only with no default value.</span></span> <span data-ttu-id="1ed47-111">Las señales de vídeo NTSC se muestran en 30 fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="1ed47-111">NTSC video signals are displayed at 30 frames per second.</span></span> <span data-ttu-id="1ed47-112">PAL se muestra en 25 fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="1ed47-112">PAL is displayed at 25 frames per second.</span></span> <span data-ttu-id="1ed47-113">Un disco se codifica para reproducirse en NTSC o PAL, pero no puede reproducirse en ambos.</span><span class="sxs-lookup"><span data-stu-id="1ed47-113">A disc is encoded to play on either NTSC or PAL, but cannot play on both.</span></span>

 

 



