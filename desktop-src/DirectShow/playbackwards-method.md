---
description: El método PlayBackwards inicia la reproducción hacia atrás desde la ubicación actual a la velocidad especificada.
ms.assetid: 7f8421e7-f835-4a10-a9c9-0e43de159e4f
title: Método PlayBackwards
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b396c3829569d3f3ad25f0c0e8718dfd23f268
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494200"
---
# <a name="playbackwards-method"></a><span data-ttu-id="0a109-103">Método PlayBackwards</span><span class="sxs-lookup"><span data-stu-id="0a109-103">PlayBackwards Method</span></span>

> [!Note]  
> <span data-ttu-id="0a109-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0a109-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="0a109-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="0a109-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="0a109-106">El `PlayBackwards` método inicia la reproducción hacia atrás desde la ubicación actual a la velocidad especificada.</span><span class="sxs-lookup"><span data-stu-id="0a109-106">The `PlayBackwards` method starts backward playback from the current location at the specified speed.</span></span>

``` syntax
MSWebDVD.PlayBackwards(nSpeed)
```

## <a name="parameters"></a><span data-ttu-id="0a109-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a109-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a109-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*</span><span class="sxs-lookup"><span data-stu-id="0a109-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="0a109-109">Especifica la velocidad a la que se reproducirá como un número.</span><span class="sxs-lookup"><span data-stu-id="0a109-109">Specifies the speed at which to play as a number.</span></span> <span data-ttu-id="0a109-110">Este número es un multiplicador: 1,0 es la velocidad de reproducción normal; 2,0 es la velocidad doble, 0,5 es la velocidad media, etc.</span><span class="sxs-lookup"><span data-stu-id="0a109-110">This number is a multiplier—1.0 is normal playback speed; 2.0 is double speed, 0.5 is half speed, and so on.</span></span> <span data-ttu-id="0a109-111">Cuando **nSpeed** no es igual a 1,0, el audio se silencia y la subimagen se desactiva.</span><span class="sxs-lookup"><span data-stu-id="0a109-111">When **nSpeed** does not equal 1.0, audio is muted and the subpicture is turned off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a109-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a109-112">Return Value</span></span>

<span data-ttu-id="0a109-113">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="0a109-113">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="0a109-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a109-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a109-115">**PlayForwards**</span><span class="sxs-lookup"><span data-stu-id="0a109-115">**PlayForwards**</span></span>](playforwards-method.md)
</dt> </dl>

 

 



