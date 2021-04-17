---
description: El calificador de contratipo contiene el valor entero para el tipo de contador de propiedad para las propiedades de \_ las clases PerfRawData de Win32. CookingType contiene las constantes para los tipos de fórmula de propiedad de \_ las clases PerfFormattedData de Win32.
ms.assetid: aa79fcdb-503f-4928-b2b7-f07baeaf9fb5
ms.tgt_platform: multiple
title: Calificador de tipo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterType
api_type:
- NA
api_location: ''
ms.openlocfilehash: 883ee7aa2f230756d62294d46e6402fe7f962d4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677627"
---
# <a name="countertype-qualifier"></a><span data-ttu-id="f9550-104">Calificador de tipo</span><span class="sxs-lookup"><span data-stu-id="f9550-104">CounterType Qualifier</span></span>

<span data-ttu-id="f9550-105">El calificador de **contratipo** contiene el valor entero para el tipo de contador de propiedad para las propiedades de las clases [**\_ PerfRawData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="f9550-105">The **CounterType** qualifier contains the integer value for the property counter type for properties in [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes.</span></span> <span data-ttu-id="f9550-106">**CookingType** contiene las constantes para los tipos de fórmula de propiedad de las clases [**\_ PerfFormattedData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) .</span><span class="sxs-lookup"><span data-stu-id="f9550-106">The **CookingType** contains the constants for property formula types in [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes.</span></span>

<span data-ttu-id="f9550-107">Para obtener más información y un desglose de los tipos de contador por función, vea [tipos de contadores](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="f9550-107">For more information and a breakdown of counter types by function, see [Counter Types](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).</span></span>



| <span data-ttu-id="f9550-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="f9550-108">CounterType</span></span> | <span data-ttu-id="f9550-109">CookingType</span><span class="sxs-lookup"><span data-stu-id="f9550-109">CookingType</span></span>                              |
|-------------|------------------------------------------|
| <span data-ttu-id="f9550-110">0</span><span class="sxs-lookup"><span data-stu-id="f9550-110">0</span></span>           | <span data-ttu-id="f9550-111">contador de rendimiento \_ \_ RAWCOUNT \_ Hex</span><span class="sxs-lookup"><span data-stu-id="f9550-111">PERF\_COUNTER\_RAWCOUNT\_HEX</span></span>             |
| <span data-ttu-id="f9550-112">256</span><span class="sxs-lookup"><span data-stu-id="f9550-112">256</span></span>         | <span data-ttu-id="f9550-113">contador de rendimiento de \_ \_ \_ RAWCOUNT grande \_ Hex</span><span class="sxs-lookup"><span data-stu-id="f9550-113">PERF\_COUNTER\_LARGE\_RAWCOUNT\_HEX</span></span>      |
| <span data-ttu-id="f9550-114">2816</span><span class="sxs-lookup"><span data-stu-id="f9550-114">2816</span></span>        | <span data-ttu-id="f9550-115">\_texto del contador de rendimiento \_</span><span class="sxs-lookup"><span data-stu-id="f9550-115">PERF\_COUNTER\_TEXT</span></span>                      |
| <span data-ttu-id="f9550-116">65536</span><span class="sxs-lookup"><span data-stu-id="f9550-116">65536</span></span>       | <span data-ttu-id="f9550-117">contador de rendimiento \_ \_ RAWCOUNT</span><span class="sxs-lookup"><span data-stu-id="f9550-117">PERF\_COUNTER\_RAWCOUNT</span></span>                  |
| <span data-ttu-id="f9550-118">65792</span><span class="sxs-lookup"><span data-stu-id="f9550-118">65792</span></span>       | <span data-ttu-id="f9550-119">contador de rendimiento \_ \_ grande \_ RAWCOUNT</span><span class="sxs-lookup"><span data-stu-id="f9550-119">PERF\_COUNTER\_LARGE\_RAWCOUNT</span></span>           |
| <span data-ttu-id="f9550-120">73728</span><span class="sxs-lookup"><span data-stu-id="f9550-120">73728</span></span>       | <span data-ttu-id="f9550-121">RENDIMIENTO \_ doble \_ sin formato</span><span class="sxs-lookup"><span data-stu-id="f9550-121">PERF\_DOUBLE\_RAW</span></span>                        |
| <span data-ttu-id="f9550-122">4195328</span><span class="sxs-lookup"><span data-stu-id="f9550-122">4195328</span></span>     | <span data-ttu-id="f9550-123">\_Delta de contador de rendimiento \_</span><span class="sxs-lookup"><span data-stu-id="f9550-123">PERF\_COUNTER\_DELTA</span></span>                     |
| <span data-ttu-id="f9550-124">4195584</span><span class="sxs-lookup"><span data-stu-id="f9550-124">4195584</span></span>     | <span data-ttu-id="f9550-125">\_ \_ diferencia grande de contador de rendimiento \_</span><span class="sxs-lookup"><span data-stu-id="f9550-125">PERF\_COUNTER\_LARGE\_DELTA</span></span>              |
| <span data-ttu-id="f9550-126">4260864</span><span class="sxs-lookup"><span data-stu-id="f9550-126">4260864</span></span>     | <span data-ttu-id="f9550-127">\_contador de ejemplo de rendimiento \_</span><span class="sxs-lookup"><span data-stu-id="f9550-127">PERF\_SAMPLE\_COUNTER</span></span>                    |
| <span data-ttu-id="f9550-128">4523008</span><span class="sxs-lookup"><span data-stu-id="f9550-128">4523008</span></span>     | <span data-ttu-id="f9550-129">tipo de contador de rendimiento \_ \_ QUEUELEN \_</span><span class="sxs-lookup"><span data-stu-id="f9550-129">PERF\_COUNTER\_QUEUELEN\_TYPE</span></span>            |
| <span data-ttu-id="f9550-130">4523264</span><span class="sxs-lookup"><span data-stu-id="f9550-130">4523264</span></span>     | <span data-ttu-id="f9550-131">\_tipo de \_ \_ QUEUELEN grande de contador \_ de rendimiento</span><span class="sxs-lookup"><span data-stu-id="f9550-131">PERF\_COUNTER\_LARGE\_QUEUELEN\_TYPE</span></span>     |
| <span data-ttu-id="f9550-132">5571840</span><span class="sxs-lookup"><span data-stu-id="f9550-132">5571840</span></span>     | <span data-ttu-id="f9550-133">Contador de rendimiento de \_ \_ \_ tipo QUEUELEN de 100 NS \_</span><span class="sxs-lookup"><span data-stu-id="f9550-133">PERF\_COUNTER\_100NS\_QUEUELEN\_TYPE</span></span>     |
| <span data-ttu-id="f9550-134">6620416</span><span class="sxs-lookup"><span data-stu-id="f9550-134">6620416</span></span>     | <span data-ttu-id="f9550-135">\_tipo de \_ \_ QUEUELEN de \_ tiempo \_ del contador de rendimiento</span><span class="sxs-lookup"><span data-stu-id="f9550-135">PERF\_COUNTER\_OBJ\_TIME\_QUEUELEN\_TYPE</span></span> |
| <span data-ttu-id="f9550-136">272696320</span><span class="sxs-lookup"><span data-stu-id="f9550-136">272696320</span></span>   | <span data-ttu-id="f9550-137">contador \_ de rendimiento \_</span><span class="sxs-lookup"><span data-stu-id="f9550-137">PERF\_COUNTER\_COUNTER</span></span>                   |
| <span data-ttu-id="f9550-138">272696576</span><span class="sxs-lookup"><span data-stu-id="f9550-138">272696576</span></span>   | <span data-ttu-id="f9550-139">\_recuento masivo de contadores de rendimiento \_ \_</span><span class="sxs-lookup"><span data-stu-id="f9550-139">PERF\_COUNTER\_BULK\_COUNT</span></span>               |
| <span data-ttu-id="f9550-140">537003008</span><span class="sxs-lookup"><span data-stu-id="f9550-140">537003008</span></span>   | <span data-ttu-id="f9550-141">fracción de rendimiento \_ sin procesar \_</span><span class="sxs-lookup"><span data-stu-id="f9550-141">PERF\_RAW\_FRACTION</span></span>                      |
| <span data-ttu-id="f9550-142">541132032</span><span class="sxs-lookup"><span data-stu-id="f9550-142">541132032</span></span>   | <span data-ttu-id="f9550-143">\_temporizador de contadores de rendimiento \_</span><span class="sxs-lookup"><span data-stu-id="f9550-143">PERF\_COUNTER\_TIMER</span></span>                     |
| <span data-ttu-id="f9550-144">541525248</span><span class="sxs-lookup"><span data-stu-id="f9550-144">541525248</span></span>   | <span data-ttu-id="f9550-145">\_ \_ temporizador del sistema de precisión de rendimiento \_</span><span class="sxs-lookup"><span data-stu-id="f9550-145">PERF\_PRECISION\_SYSTEM\_TIMER</span></span>           |
| <span data-ttu-id="f9550-146">542180608</span><span class="sxs-lookup"><span data-stu-id="f9550-146">542180608</span></span>   | <span data-ttu-id="f9550-147">\_Temporizador de 100NSEC de rendimiento \_</span><span class="sxs-lookup"><span data-stu-id="f9550-147">PERF\_100NSEC\_TIMER</span></span>                     |
| <span data-ttu-id="f9550-148">542573824</span><span class="sxs-lookup"><span data-stu-id="f9550-148">542573824</span></span>   | <span data-ttu-id="f9550-149">\_Temporizador de \_ 100 de precisión de rendimiento \_</span><span class="sxs-lookup"><span data-stu-id="f9550-149">PERF\_PRECISION\_100NS\_TIMER</span></span>            |
| <span data-ttu-id="f9550-150">543229184</span><span class="sxs-lookup"><span data-stu-id="f9550-150">543229184</span></span>   | <span data-ttu-id="f9550-151">\_temporizador de \_ tiempo de Perf \_</span><span class="sxs-lookup"><span data-stu-id="f9550-151">PERF\_OBJ\_TIME\_TIMER</span></span>                   |
| <span data-ttu-id="f9550-152">543622400</span><span class="sxs-lookup"><span data-stu-id="f9550-152">543622400</span></span>   | <span data-ttu-id="f9550-153">\_temporizador de \_ objeto de precisión de rendimiento \_</span><span class="sxs-lookup"><span data-stu-id="f9550-153">PERF\_PRECISION\_OBJECT\_TIMER</span></span>           |
| <span data-ttu-id="f9550-154">549585920</span><span class="sxs-lookup"><span data-stu-id="f9550-154">549585920</span></span>   | <span data-ttu-id="f9550-155">\_fracción de ejemplo de rendimiento \_</span><span class="sxs-lookup"><span data-stu-id="f9550-155">PERF\_SAMPLE\_FRACTION</span></span>                   |
| <span data-ttu-id="f9550-156">557909248</span><span class="sxs-lookup"><span data-stu-id="f9550-156">557909248</span></span>   | <span data-ttu-id="f9550-157">\_ \_ INV del contador de rendimiento \_</span><span class="sxs-lookup"><span data-stu-id="f9550-157">PERF\_COUNTER\_TIMER\_INV</span></span>                |
| <span data-ttu-id="f9550-158">558957824</span><span class="sxs-lookup"><span data-stu-id="f9550-158">558957824</span></span>   | <span data-ttu-id="f9550-159">\_INV 100NSEC \_ del temporizador \_ de rendimiento</span><span class="sxs-lookup"><span data-stu-id="f9550-159">PERF\_100NSEC\_TIMER\_INV</span></span>                |
| <span data-ttu-id="f9550-160">574686464</span><span class="sxs-lookup"><span data-stu-id="f9550-160">574686464</span></span>   | <span data-ttu-id="f9550-161">contador de rendimiento de \_ \_ varios \_ temporizadores</span><span class="sxs-lookup"><span data-stu-id="f9550-161">PERF\_COUNTER\_MULTI\_TIMER</span></span>              |
| <span data-ttu-id="f9550-162">575735040</span><span class="sxs-lookup"><span data-stu-id="f9550-162">575735040</span></span>   | <span data-ttu-id="f9550-163">\_ \_ Temporizador múltiple de rendimiento 100NSEC \_</span><span class="sxs-lookup"><span data-stu-id="f9550-163">PERF\_100NSEC\_MULTI\_TIMER</span></span>              |
| <span data-ttu-id="f9550-164">591463680</span><span class="sxs-lookup"><span data-stu-id="f9550-164">591463680</span></span>   | <span data-ttu-id="f9550-165">contador de rendimiento de \_ \_ varios \_ temporizadores \_</span><span class="sxs-lookup"><span data-stu-id="f9550-165">PERF\_COUNTER\_MULTI\_TIMER\_INV</span></span>         |
| <span data-ttu-id="f9550-166">592512256</span><span class="sxs-lookup"><span data-stu-id="f9550-166">592512256</span></span>   | <span data-ttu-id="f9550-167">\_Inv de \_ \_ temporizador múltiple \_ de rendimiento 100NSEC</span><span class="sxs-lookup"><span data-stu-id="f9550-167">PERF\_100NSEC\_MULTI\_TIMER\_INV</span></span>         |
| <span data-ttu-id="f9550-168">805438464</span><span class="sxs-lookup"><span data-stu-id="f9550-168">805438464</span></span>   | <span data-ttu-id="f9550-169">\_temporizador de promedio de rendimiento \_</span><span class="sxs-lookup"><span data-stu-id="f9550-169">PERF\_AVERAGE\_TIMER</span></span>                     |
| <span data-ttu-id="f9550-170">807666944</span><span class="sxs-lookup"><span data-stu-id="f9550-170">807666944</span></span>   | <span data-ttu-id="f9550-171">\_tiempo transcurrido de rendimiento \_</span><span class="sxs-lookup"><span data-stu-id="f9550-171">PERF\_ELAPSED\_TIME</span></span>                      |
| <span data-ttu-id="f9550-172">1073742336</span><span class="sxs-lookup"><span data-stu-id="f9550-172">1073742336</span></span>  | <span data-ttu-id="f9550-173">contador de rendimiento \_ \_ NoData</span><span class="sxs-lookup"><span data-stu-id="f9550-173">PERF\_COUNTER\_NODATA</span></span>                    |
| <span data-ttu-id="f9550-174">1073874176</span><span class="sxs-lookup"><span data-stu-id="f9550-174">1073874176</span></span>  | <span data-ttu-id="f9550-175">media de rendimiento en \_ \_ masa</span><span class="sxs-lookup"><span data-stu-id="f9550-175">PERF\_AVERAGE\_BULK</span></span>                      |
| <span data-ttu-id="f9550-176">1073939457</span><span class="sxs-lookup"><span data-stu-id="f9550-176">1073939457</span></span>  | <span data-ttu-id="f9550-177">\_base de ejemplo de rendimiento \_</span><span class="sxs-lookup"><span data-stu-id="f9550-177">PERF\_SAMPLE\_BASE</span></span>                       |
| <span data-ttu-id="f9550-178">1073939458</span><span class="sxs-lookup"><span data-stu-id="f9550-178">1073939458</span></span>  | <span data-ttu-id="f9550-179">\_base de promedio de rendimiento \_</span><span class="sxs-lookup"><span data-stu-id="f9550-179">PERF\_AVERAGE\_BASE</span></span>                      |
| <span data-ttu-id="f9550-180">1073939459</span><span class="sxs-lookup"><span data-stu-id="f9550-180">1073939459</span></span>  | <span data-ttu-id="f9550-181">\_base sin procesar de rendimiento \_</span><span class="sxs-lookup"><span data-stu-id="f9550-181">PERF\_RAW\_BASE</span></span>                          |
| <span data-ttu-id="f9550-182">1073939712</span><span class="sxs-lookup"><span data-stu-id="f9550-182">1073939712</span></span>  | <span data-ttu-id="f9550-183">marca de tiempo de precisión de rendimiento \_ \_</span><span class="sxs-lookup"><span data-stu-id="f9550-183">PERF\_PRECISION\_TIMESTAMP</span></span>               |
| <span data-ttu-id="f9550-184">1073939715</span><span class="sxs-lookup"><span data-stu-id="f9550-184">1073939715</span></span>  | <span data-ttu-id="f9550-185">\_ \_ base sin formato de alto rendimiento \_</span><span class="sxs-lookup"><span data-stu-id="f9550-185">PERF\_LARGE\_RAW\_BASE</span></span>                   |
| <span data-ttu-id="f9550-186">1107494144</span><span class="sxs-lookup"><span data-stu-id="f9550-186">1107494144</span></span>  | <span data-ttu-id="f9550-187">contador de rendimiento de \_ \_ varias \_ bases</span><span class="sxs-lookup"><span data-stu-id="f9550-187">PERF\_COUNTER\_MULTI\_BASE</span></span>               |
| <span data-ttu-id="f9550-188">2147483648</span><span class="sxs-lookup"><span data-stu-id="f9550-188">2147483648</span></span>  | <span data-ttu-id="f9550-189">\_tipo de \_ histograma del contador de rendimiento \_</span><span class="sxs-lookup"><span data-stu-id="f9550-189">PERF\_COUNTER\_HISTOGRAM\_TYPE</span></span>           |



 

## <a name="requirements"></a><span data-ttu-id="f9550-190">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9550-190">Requirements</span></span>



| <span data-ttu-id="f9550-191">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9550-191">Requirement</span></span> | <span data-ttu-id="f9550-192">Value</span><span class="sxs-lookup"><span data-stu-id="f9550-192">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f9550-193">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9550-193">Minimum supported client</span></span><br/> | <span data-ttu-id="f9550-194">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9550-194">Windows Vista</span></span><br/>       |
| <span data-ttu-id="f9550-195">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9550-195">Minimum supported server</span></span><br/> | <span data-ttu-id="f9550-196">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9550-196">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9550-197">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9550-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9550-198">Calificadores específicos de las clases de rendimiento de WMI</span><span class="sxs-lookup"><span data-stu-id="f9550-198">Qualifiers Specific to WMI Performance Classes</span></span>](qualifiers-specific-to-wmi-performance-classes.md)
</dt> </dl>

 

