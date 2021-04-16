---
description: El método PlayAtTimeInTitle inicia la reproducción en el momento especificado dentro del título especificado.
ms.assetid: 82726885-8393-409b-b8a1-29a8e9e9ac65
title: Método PlayAtTimeInTitle
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c40373b4327b6df5fc341ca392c223d464a70a8b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494201"
---
# <a name="playattimeintitle-method"></a><span data-ttu-id="7e771-103">Método PlayAtTimeInTitle</span><span class="sxs-lookup"><span data-stu-id="7e771-103">PlayAtTimeInTitle Method</span></span>

> [!Note]  
> <span data-ttu-id="7e771-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7e771-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="7e771-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="7e771-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="7e771-106">El `PlayAtTimeInTitle` método inicia la reproducción en el momento especificado dentro del título especificado.</span><span class="sxs-lookup"><span data-stu-id="7e771-106">The `PlayAtTimeInTitle` method starts playback at the specified time within the specified title.</span></span>

``` syntax
MSWebDVD.PlayAtTimeInTitle(sTime, iTitle)
```

## <a name="parameters"></a><span data-ttu-id="7e771-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e771-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e771-108"><span id="sTime"></span><span id="stime"></span><span id="STIME"></span>*sTime*</span><span class="sxs-lookup"><span data-stu-id="7e771-108"><span id="sTime"></span><span id="stime"></span><span id="STIME"></span>*sTime*</span></span>
</dt> <dd>

<span data-ttu-id="7e771-109">Especifica la hora a la que se inicia la reproducción como una cadena.</span><span class="sxs-lookup"><span data-stu-id="7e771-109">Specifies the time at which to start playback as a string.</span></span> <span data-ttu-id="7e771-110">La cadena debe tener el formato "HH: mm: SS: FF" (especificando horas, minutos, segundos, fotogramas).</span><span class="sxs-lookup"><span data-stu-id="7e771-110">The string must be in the format "hh:mm:ss:ff" (specifying hours, minutes, seconds, frames).</span></span>

</dd> <dt>

<span data-ttu-id="7e771-111"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span><span class="sxs-lookup"><span data-stu-id="7e771-111"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="7e771-112">Especifica el índice del título como un entero.</span><span class="sxs-lookup"><span data-stu-id="7e771-112">Specifies the index of the title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e771-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e771-113">Return Value</span></span>

<span data-ttu-id="7e771-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="7e771-114">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="7e771-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e771-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e771-116">**CurrentTitle**</span><span class="sxs-lookup"><span data-stu-id="7e771-116">**CurrentTitle**</span></span>](currenttitle-property.md)
</dt> <dt>

[<span data-ttu-id="7e771-117">**PlayAtTime**</span><span class="sxs-lookup"><span data-stu-id="7e771-117">**PlayAtTime**</span></span>](playattime-method.md)
</dt> <dt>

[<span data-ttu-id="7e771-118">**TitlesAvailable**</span><span class="sxs-lookup"><span data-stu-id="7e771-118">**TitlesAvailable**</span></span>](titlesavailable-property.md)
</dt> </dl>

 

 



