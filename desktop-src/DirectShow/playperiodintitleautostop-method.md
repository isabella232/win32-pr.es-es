---
description: El método PlayPeriodInTitleAutoStop inicia la reproducción a la hora especificada en el título especificado hasta la hora de detención especificada.
ms.assetid: 0c4df76d-3991-4a6c-a8e5-5fd713eeffc2
title: Método PlayPeriodInTitleAutoStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05899b66b7f1a11f8f5b177d311b9634a52595b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906530"
---
# <a name="playperiodintitleautostop-method"></a><span data-ttu-id="7593d-103">Método PlayPeriodInTitleAutoStop</span><span class="sxs-lookup"><span data-stu-id="7593d-103">PlayPeriodInTitleAutoStop Method</span></span>

> [!Note]  
> <span data-ttu-id="7593d-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7593d-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="7593d-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="7593d-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="7593d-106">El `PlayPeriodInTitleAutoStop` método inicia la reproducción a la hora especificada en el título especificado hasta la hora de detención especificada.</span><span class="sxs-lookup"><span data-stu-id="7593d-106">The `PlayPeriodInTitleAutoStop` method starts playback at the specified time in the specified title until the specified stop time.</span></span>

``` syntax
MSWebDVD.PlayPeriodInTitleAutoStop(iTitle, sStartTime, sEndTime)
```

## <a name="parameters"></a><span data-ttu-id="7593d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7593d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7593d-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span><span class="sxs-lookup"><span data-stu-id="7593d-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="7593d-109">Especifica el título como un entero.</span><span class="sxs-lookup"><span data-stu-id="7593d-109">Specifies the title as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="7593d-110"><span id="sStartTime"></span><span id="sstarttime"></span><span id="SSTARTTIME"></span>*sStartTime*</span><span class="sxs-lookup"><span data-stu-id="7593d-110"><span id="sStartTime"></span><span id="sstarttime"></span><span id="SSTARTTIME"></span>*sStartTime*</span></span>
</dt> <dd>

<span data-ttu-id="7593d-111">Especifica la hora de inicio como una cadena en el formato "HH: mm: SS: FF" (especificando horas, minutos, segundos, fotogramas).</span><span class="sxs-lookup"><span data-stu-id="7593d-111">Specifies the start time as a string in "hh:mm:ss:ff" format (specifying hours, minutes, seconds, frames).</span></span>

</dd> <dt>

<span data-ttu-id="7593d-112"><span id="sEndTime"></span><span id="sendtime"></span><span id="SENDTIME"></span>*sEndTime*</span><span class="sxs-lookup"><span data-stu-id="7593d-112"><span id="sEndTime"></span><span id="sendtime"></span><span id="SENDTIME"></span>*sEndTime*</span></span>
</dt> <dd>

<span data-ttu-id="7593d-113">Especifica la hora de finalización como una cadena con el formato "HH: mm: SS: FF".</span><span class="sxs-lookup"><span data-stu-id="7593d-113">Specifies the end time as a String in "hh:mm:ss:ff" format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7593d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7593d-114">Return Value</span></span>

<span data-ttu-id="7593d-115">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="7593d-115">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="7593d-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="7593d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7593d-117">**PlayChaptersAutoStop**</span><span class="sxs-lookup"><span data-stu-id="7593d-117">**PlayChaptersAutoStop**</span></span>](playchaptersautostop-method.md)
</dt> </dl>

 

 



