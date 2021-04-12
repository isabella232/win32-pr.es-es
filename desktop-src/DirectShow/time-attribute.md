---
description: El atributo Time especifica la hora a la que un parámetro presupone un nuevo valor, en relación con el inicio de la transición o efecto.
ms.assetid: bb478215-cbd5-4fea-9d88-a1f2b002f3da
title: Atributo de hora
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15a84d40c5e38ed81f8c17cd2d931e3f85e389a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279507"
---
# <a name="time-attribute"></a><span data-ttu-id="145de-103">Atributo de hora</span><span class="sxs-lookup"><span data-stu-id="145de-103">time Attribute</span></span>

> [!Note]  
> <span data-ttu-id="145de-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="145de-104">\[Deprecated.</span></span> <span data-ttu-id="145de-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="145de-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="145de-106">El `time` atributo especifica la hora a la que un parámetro presupone un nuevo valor, en relación con el inicio de la transición o efecto.</span><span class="sxs-lookup"><span data-stu-id="145de-106">The `time` attribute specifies the time at which a parameter assumes a new value, relative to the start of the transition or effect.</span></span>

## <a name="possible-values"></a><span data-ttu-id="145de-107">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="145de-107">Possible Values</span></span>

<span data-ttu-id="145de-108">Debe ser una cadena con el formato *HH: mm: SS. FF* , donde *HH* = hours, *mm* = minutes, *SS* = seconds y *FF* = fracciones de segundo.</span><span class="sxs-lookup"><span data-stu-id="145de-108">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="145de-109">Ejemplo: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="145de-109">Example: 1:04:30.512.</span></span> <span data-ttu-id="145de-110">Se pueden omitir las unidades iniciales.</span><span class="sxs-lookup"><span data-stu-id="145de-110">Leading units can be omitted.</span></span> <span data-ttu-id="145de-111">Por ejemplo, 3:00 (tres minutos) y 45 (45 segundos) son válidos.</span><span class="sxs-lookup"><span data-stu-id="145de-111">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="applies-to"></a><span data-ttu-id="145de-112">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="145de-112">Applies To</span></span>

<span data-ttu-id="145de-113">[**en**](at-element.md), [ **lineal**](linear-element.md)</span><span class="sxs-lookup"><span data-stu-id="145de-113">[**at**](at-element.md), [**linear**](linear-element.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="145de-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="145de-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="145de-115">Atributos XTL</span><span class="sxs-lookup"><span data-stu-id="145de-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> </dl>

 

 



