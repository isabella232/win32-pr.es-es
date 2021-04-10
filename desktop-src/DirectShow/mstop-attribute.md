---
description: El atributo mstop especifica la hora de detención de un clip, relativa al archivo multimedia original.
ms.assetid: 01559d29-9c7b-4842-a1f7-16552adbda43
title: Atributo mstop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a63f52a1b912392165293e008074cf64a03b9751
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151985"
---
# <a name="mstop-attribute"></a><span data-ttu-id="c72fb-103">Atributo mstop</span><span class="sxs-lookup"><span data-stu-id="c72fb-103">mstop Attribute</span></span>

> [!Note]  
> <span data-ttu-id="c72fb-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="c72fb-104">\[Deprecated.</span></span> <span data-ttu-id="c72fb-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c72fb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c72fb-106">El `mstop` atributo especifica la hora de detención de un clip, relativa al archivo multimedia original.</span><span class="sxs-lookup"><span data-stu-id="c72fb-106">The `mstop` attribute specifies the stop time of a clip, relative to the original media file.</span></span>

## <a name="applies-to"></a><span data-ttu-id="c72fb-107">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="c72fb-107">Applies To</span></span>

[<span data-ttu-id="c72fb-108">**clip**</span><span class="sxs-lookup"><span data-stu-id="c72fb-108">**clip**</span></span>](clip-element.md)

## <a name="possible-values"></a><span data-ttu-id="c72fb-109">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="c72fb-109">Possible Values</span></span>

<span data-ttu-id="c72fb-110">Debe ser una cadena con el formato *HH: mm: SS. FF* , donde *HH* = hours, *mm* = minutes, *SS* = seconds y *FF* = fracciones de segundo.</span><span class="sxs-lookup"><span data-stu-id="c72fb-110">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="c72fb-111">Ejemplo: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="c72fb-111">Example: 1:04:30.512.</span></span> <span data-ttu-id="c72fb-112">Se pueden omitir las unidades iniciales.</span><span class="sxs-lookup"><span data-stu-id="c72fb-112">Leading units can be omitted.</span></span> <span data-ttu-id="c72fb-113">Por ejemplo, 3:00 (tres minutos) y 45 (45 segundos) son válidos.</span><span class="sxs-lookup"><span data-stu-id="c72fb-113">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="see-also"></a><span data-ttu-id="c72fb-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="c72fb-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c72fb-115">Atributos XTL</span><span class="sxs-lookup"><span data-stu-id="c72fb-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="c72fb-116">**IAMTimelineSrc::SetMediaTimes**</span><span class="sxs-lookup"><span data-stu-id="c72fb-116">**IAMTimelineSrc::SetMediaTimes**</span></span>](iamtimelinesrc-setmediatimes.md)
</dt> </dl>

 

 



