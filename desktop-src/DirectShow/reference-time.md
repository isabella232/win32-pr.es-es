---
description: El tipo de datos de hora de referencia \_ define las unidades de los tiempos de referencia en DirectShow. Cada unidad de tiempo de referencia es de 100 nanosegundos.
ms.assetid: 862c95bc-2e0a-42c0-b907-45f64f27bd41
title: REFERENCE_TIME (Strmif. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab88576f611674f5b208c5c39d328c77dcf57aec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690853"
---
# <a name="reference_time"></a><span data-ttu-id="d0629-104">tiempo de referencia \_</span><span class="sxs-lookup"><span data-stu-id="d0629-104">REFERENCE\_TIME</span></span>

<span data-ttu-id="d0629-105">El tipo de datos de **\_ hora de referencia** define las unidades de los tiempos de referencia en DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d0629-105">The **REFERENCE\_TIME** data type defines the units for reference times in DirectShow.</span></span> <span data-ttu-id="d0629-106">Cada unidad de tiempo de referencia es de 100 nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="d0629-106">Each unit of reference time is 100 nanoseconds.</span></span>


```C++
typedef LONGLONG REFERENCE_TIME;
```



## <a name="remarks"></a><span data-ttu-id="d0629-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0629-107">Remarks</span></span>

<span data-ttu-id="d0629-108">El tipo de datos de **\_ hora de referencia** es un entero de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d0629-108">The **REFERENCE\_TIME** data type is a 64-bit integer.</span></span>

<span data-ttu-id="d0629-109">Los tiempos de referencia se miden normalmente a partir de una de las siguientes líneas base:</span><span class="sxs-lookup"><span data-stu-id="d0629-109">Reference times are usually measured from one of the following baselines:</span></span>

-   <span data-ttu-id="d0629-110">Una hora de reloj absoluta.</span><span class="sxs-lookup"><span data-stu-id="d0629-110">An absolute clock time.</span></span> <span data-ttu-id="d0629-111">En este caso, la línea base dependerá de la implementación del reloj.</span><span class="sxs-lookup"><span data-stu-id="d0629-111">In this case, the baseline will depend on the implementation of the clock.</span></span> <span data-ttu-id="d0629-112">Para obtener más información, consulte [relojes de referencia](reference-clocks.md).</span><span class="sxs-lookup"><span data-stu-id="d0629-112">For more information, see [Reference Clocks](reference-clocks.md).</span></span>
-   <span data-ttu-id="d0629-113">Relativa al inicio de la reproducción.</span><span class="sxs-lookup"><span data-stu-id="d0629-113">Relative to the start of playback.</span></span>

<span data-ttu-id="d0629-114">Para obtener más información acerca de los tiempos de referencia, consulte [hora y relojes en DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="d0629-114">For more information about reference times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0629-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0629-115">Requirements</span></span>



| <span data-ttu-id="d0629-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0629-116">Requirement</span></span> | <span data-ttu-id="d0629-117">Value</span><span class="sxs-lookup"><span data-stu-id="d0629-117">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0629-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0629-118">Header</span></span><br/> | <dl> <span data-ttu-id="d0629-119"><dt>Strmif. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0629-119"><dt>Strmif.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0629-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0629-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0629-121">Tipos de datos de DirectShow</span><span class="sxs-lookup"><span data-stu-id="d0629-121">DirectShow Data Types</span></span>](directshow-data-types.md)
</dt> </dl>

 

 




