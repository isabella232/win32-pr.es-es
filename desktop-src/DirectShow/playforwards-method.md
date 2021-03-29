---
description: El método PlayForwards inicia la reproducción hacia delante desde la ubicación actual a la velocidad especificada.
ms.assetid: 4f1a3e74-b343-413d-8df7-6c4bea39c62d
title: Método PlayForwards
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10d49d8d6d80613c4dd5b2b8a374002b37d9baa4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806247"
---
# <a name="playforwards-method"></a><span data-ttu-id="6e01a-103">Método PlayForwards</span><span class="sxs-lookup"><span data-stu-id="6e01a-103">PlayForwards Method</span></span>

> [!Note]  
> <span data-ttu-id="6e01a-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6e01a-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="6e01a-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="6e01a-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="6e01a-106">El `PlayForwards` método inicia la reproducción hacia delante desde la ubicación actual a la velocidad especificada.</span><span class="sxs-lookup"><span data-stu-id="6e01a-106">The `PlayForwards` method starts forward playback from the current location at the specified speed.</span></span>

``` syntax
MSWebDVD.PlayForwards(nSpeed)
```

## <a name="parameters"></a><span data-ttu-id="6e01a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e01a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e01a-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*</span><span class="sxs-lookup"><span data-stu-id="6e01a-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="6e01a-109">Especifica la velocidad a la que se reproducirá como valor entero.</span><span class="sxs-lookup"><span data-stu-id="6e01a-109">Specifies the speed at which to play as an Integer value.</span></span> <span data-ttu-id="6e01a-110">Este valor es un multiplicador: 1,0 es la velocidad de reproducción normal; 2,0 es la velocidad doble, 0,5 es la velocidad media, etc.</span><span class="sxs-lookup"><span data-stu-id="6e01a-110">This value is a multiplier—1.0 is normal playback speed; 2.0 is double speed, 0.5 is half speed, and so on.</span></span> <span data-ttu-id="6e01a-111">Cuando **nSpeed** no es igual a 1,0, el audio se silencia y la subimagen se desactiva.</span><span class="sxs-lookup"><span data-stu-id="6e01a-111">When **nSpeed** does not equal 1.0, audio is muted and the subpicture is turned off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e01a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e01a-112">Return Value</span></span>

<span data-ttu-id="6e01a-113">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6e01a-113">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="6e01a-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e01a-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e01a-115">**PlayBackwards**</span><span class="sxs-lookup"><span data-stu-id="6e01a-115">**PlayBackwards**</span></span>](playbackwards-method.md)
</dt> </dl>

 

 



