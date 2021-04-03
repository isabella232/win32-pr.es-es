---
description: El atributo mlength especifica la duración de un archivo de código fuente. Este valor debe ser la duración real o se pueden producir errores de representación.
ms.assetid: f33ce85c-df61-4248-8dea-677162fa1a07
title: Atributo mlength
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35eadc288e29d99df0e6af7f06e1404d86f6a938
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997620"
---
# <a name="mlength-attribute"></a><span data-ttu-id="74867-104">Atributo mlength</span><span class="sxs-lookup"><span data-stu-id="74867-104">mlength Attribute</span></span>

> [!Note]  
> <span data-ttu-id="74867-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="74867-105">\[Deprecated.</span></span> <span data-ttu-id="74867-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="74867-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="74867-107">El `mlength` atributo especifica la duración de un archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="74867-107">The `mlength` attribute specifies the duration of a source file.</span></span> <span data-ttu-id="74867-108">Este valor debe ser la duración real o se pueden producir errores de representación.</span><span class="sxs-lookup"><span data-stu-id="74867-108">This value must be the actual duration, or rendering errors may occur.</span></span>

## <a name="applies-to"></a><span data-ttu-id="74867-109">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="74867-109">Applies To</span></span>

[<span data-ttu-id="74867-110">**clip**</span><span class="sxs-lookup"><span data-stu-id="74867-110">**clip**</span></span>](clip-element.md)

## <a name="possible-values"></a><span data-ttu-id="74867-111">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="74867-111">Possible Values</span></span>

<span data-ttu-id="74867-112">Debe ser una cadena con el formato *HH: mm: SS. FF* , donde *HH* = hours, *mm* = minutes, *SS* = seconds y *FF* = fracciones de segundo.</span><span class="sxs-lookup"><span data-stu-id="74867-112">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="74867-113">Ejemplo: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="74867-113">Example: 1:04:30.512.</span></span> <span data-ttu-id="74867-114">Se pueden omitir las unidades iniciales.</span><span class="sxs-lookup"><span data-stu-id="74867-114">Leading units can be omitted.</span></span> <span data-ttu-id="74867-115">Por ejemplo, 3:00 (tres minutos) y 45 (45 segundos) son válidos.</span><span class="sxs-lookup"><span data-stu-id="74867-115">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="see-also"></a><span data-ttu-id="74867-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="74867-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74867-117">Atributos XTL</span><span class="sxs-lookup"><span data-stu-id="74867-117">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="74867-118">**IAMTimelineSrc::SetMediaLength**</span><span class="sxs-lookup"><span data-stu-id="74867-118">**IAMTimelineSrc::SetMediaLength**</span></span>](iamtimelinesrc-setmedialength.md)
</dt> </dl>

 

 



