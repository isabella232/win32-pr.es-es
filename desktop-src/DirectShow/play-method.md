---
description: El método play reproduce el título actual del DVD.
ms.assetid: fe9dc266-5b12-479d-85cb-50cc6bb9d580
title: Play (método) (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f62323c9c86be476a35977dadf554bbfca3bca91
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537125"
---
# <a name="play-method-directshow"></a><span data-ttu-id="82fa4-103">Play (método) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="82fa4-103">Play Method (DirectShow)</span></span>

> [!Note]  
> <span data-ttu-id="82fa4-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="82fa4-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="82fa4-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="82fa4-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="82fa4-106">El `Play` método reproduce el título actual del DVD.</span><span class="sxs-lookup"><span data-stu-id="82fa4-106">The `Play` method plays the current DVD title.</span></span>

``` syntax
MSWebDVD.Play()
```

## <a name="return-value"></a><span data-ttu-id="82fa4-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82fa4-107">Return Value</span></span>

<span data-ttu-id="82fa4-108">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="82fa4-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82fa4-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82fa4-109">Remarks</span></span>

<span data-ttu-id="82fa4-110">Si la reproducción está pausada o detenida y [**EnableResetOnStop**](enableresetonstop-property.md) es true, al llamar a **Play** se reanudará la reproducción a velocidad normal en la ubicación actual.</span><span class="sxs-lookup"><span data-stu-id="82fa4-110">If playback is paused or stopped and [**EnableResetOnStop**](enableresetonstop-property.md) is true, then calling **Play** will resume playback at normal speed at the current location.</span></span> <span data-ttu-id="82fa4-111">Si se detiene la reproducción y **EnableResetOnStop** es false, la llamada a **Play** hará que el disco empiece a reproducirse al principio del primer título.</span><span class="sxs-lookup"><span data-stu-id="82fa4-111">If playback is stopped and **EnableResetOnStop** is false, then calling **Play** will cause the disc to start playing at the beginning of the first title.</span></span>

## <a name="see-also"></a><span data-ttu-id="82fa4-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="82fa4-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82fa4-113">**Reanudar**</span><span class="sxs-lookup"><span data-stu-id="82fa4-113">**Resume**</span></span>](resume-method.md)
</dt> </dl>

 

 



