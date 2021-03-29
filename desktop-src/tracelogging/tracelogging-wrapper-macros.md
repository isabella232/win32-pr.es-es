---
title: Macros de contenedor de TraceLogging
description: Enumera las macros de contenedor para los proveedores de TraceLogging.
ms.assetid: 806F43F3-D376-4DBD-A4C5-B5F01E5D009D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dc28b3a35074089b1f5c613b041534b8b282423
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779687"
---
# <a name="tracelogging-wrapper-macros"></a><span data-ttu-id="6f613-103">Macros de contenedor de TraceLogging</span><span class="sxs-lookup"><span data-stu-id="6f613-103">TraceLogging Wrapper Macros</span></span>

<span data-ttu-id="6f613-104">Enumera las macros de contenedor para los proveedores de TraceLogging.</span><span class="sxs-lookup"><span data-stu-id="6f613-104">Lists the wrapper macros for TraceLogging providers.</span></span>

<span data-ttu-id="6f613-105">Para registrar eventos mediante proveedores de TraceLogging, debe usar las macros TraceLogging Write [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) o [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity).</span><span class="sxs-lookup"><span data-stu-id="6f613-105">In order to record events using TraceLogging providers, you need to use the TraceLogging write macros [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) or [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity).</span></span> <span data-ttu-id="6f613-106">Ambas macros requieren que se ajusten los datos de eventos en una macro contenedora.</span><span class="sxs-lookup"><span data-stu-id="6f613-106">Both of these macros require you to wrap any event data in a wrapper macro.</span></span> <span data-ttu-id="6f613-107">Hay varias macros de contenedor diferentes para los distintos tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="6f613-107">There are several different wrapper macros for different data types.</span></span> <span data-ttu-id="6f613-108">Para obtener una lista completa de las macros de TraceLogging, vea [macros de TraceLogging](trace-logging-macros.md).</span><span class="sxs-lookup"><span data-stu-id="6f613-108">For a complete list of TraceLogging macros, see [TraceLogging Macros](trace-logging-macros.md).</span></span>

<span data-ttu-id="6f613-109">Además de las macros de contenedor anteriores, hay varias macros disponibles para los tipos de datos individuales.</span><span class="sxs-lookup"><span data-stu-id="6f613-109">In addition to the wrapper macros above, several macros are available for individual data types.</span></span> <span data-ttu-id="6f613-110">Todas estas macros tienen el mismo formato que la macro [TraceLoggingValue](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue) .</span><span class="sxs-lookup"><span data-stu-id="6f613-110">All of these macros have the same format as the [TraceLoggingValue](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue) macro.</span></span> <span data-ttu-id="6f613-111">Puede usar la macro TraceLoggingValue para detectar automáticamente la macro de contenedor adecuada que se va a usar o usar directamente la macro específica.</span><span class="sxs-lookup"><span data-stu-id="6f613-111">You can use the TraceLoggingValue macro to automatically detect the appropriate wrapper macro to use, or use the specific macro directly.</span></span>

-   [<span data-ttu-id="6f613-112">**TraceLoggingBinary**</span><span class="sxs-lookup"><span data-stu-id="6f613-112">**TraceLoggingBinary**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingbinary)
-   [<span data-ttu-id="6f613-113">**TraceLoggingChannel**</span><span class="sxs-lookup"><span data-stu-id="6f613-113">**TraceLoggingChannel**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingchannel)
-   [<span data-ttu-id="6f613-114">**TraceLoggingCustomAttribute**</span><span class="sxs-lookup"><span data-stu-id="6f613-114">**TraceLoggingCustomAttribute**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingcustomattribute)
-   [<span data-ttu-id="6f613-115">**TraceLoggingDescription**</span><span class="sxs-lookup"><span data-stu-id="6f613-115">**TraceLoggingDescription**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingdescription)
-   [<span data-ttu-id="6f613-116">**TraceLoggingEventTag**</span><span class="sxs-lookup"><span data-stu-id="6f613-116">**TraceLoggingEventTag**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingeventtag)
-   [<span data-ttu-id="6f613-117">**TraceLoggingKeyword**</span><span class="sxs-lookup"><span data-stu-id="6f613-117">**TraceLoggingKeyword**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingkeyword)
-   [<span data-ttu-id="6f613-118">**TraceLoggingLevel**</span><span class="sxs-lookup"><span data-stu-id="6f613-118">**TraceLoggingLevel**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogginglevel)
-   [<span data-ttu-id="6f613-119">**TraceLoggingOpcode**</span><span class="sxs-lookup"><span data-stu-id="6f613-119">**TraceLoggingOpcode**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingopcode)
-   [<span data-ttu-id="6f613-120">**TraceLoggingSocketAddress**</span><span class="sxs-lookup"><span data-stu-id="6f613-120">**TraceLoggingSocketAddress**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingsocketaddress)
-   [<span data-ttu-id="6f613-121">**TraceLoggingStruct**</span><span class="sxs-lookup"><span data-stu-id="6f613-121">**TraceLoggingStruct**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingstruct)
-   [<span data-ttu-id="6f613-122">**TraceLoggingValue**</span><span class="sxs-lookup"><span data-stu-id="6f613-122">**TraceLoggingValue**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue)

> [!Note]
>
> <span data-ttu-id="6f613-123">**TraceLoggingOptionGroup** es específicamente para su uso dentro del \_ proveedor de definición de TRACELOGGING \_ .</span><span class="sxs-lookup"><span data-stu-id="6f613-123">**TraceLoggingOptionGroup** is specifically for use inside of TRACELOGGING\_DEFINE\_PROVIDER.</span></span>
>
> -   [<span data-ttu-id="6f613-124">**TraceLoggingOptionGroup**</span><span class="sxs-lookup"><span data-stu-id="6f613-124">**TraceLoggingOptionGroup**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup)

 

<span data-ttu-id="6f613-125">Estas son las macros de contenedor individuales.</span><span class="sxs-lookup"><span data-stu-id="6f613-125">Here are the individual wrapper macros.</span></span>

-   <span data-ttu-id="6f613-126">TraceLoggingInt8</span><span class="sxs-lookup"><span data-stu-id="6f613-126">TraceLoggingInt8</span></span>

-   <span data-ttu-id="6f613-127">TraceLoggingUInt8</span><span class="sxs-lookup"><span data-stu-id="6f613-127">TraceLoggingUInt8</span></span>

-   <span data-ttu-id="6f613-128">TraceLoggingInt16</span><span class="sxs-lookup"><span data-stu-id="6f613-128">TraceLoggingInt16</span></span>

-   <span data-ttu-id="6f613-129">TraceLoggingUInt16</span><span class="sxs-lookup"><span data-stu-id="6f613-129">TraceLoggingUInt16</span></span>

-   <span data-ttu-id="6f613-130">TraceLoggingInt32</span><span class="sxs-lookup"><span data-stu-id="6f613-130">TraceLoggingInt32</span></span>

-   <span data-ttu-id="6f613-131">TraceLoggingUInt32</span><span class="sxs-lookup"><span data-stu-id="6f613-131">TraceLoggingUInt32</span></span>

-   <span data-ttu-id="6f613-132">TraceLoggingInt64</span><span class="sxs-lookup"><span data-stu-id="6f613-132">TraceLoggingInt64</span></span>

-   <span data-ttu-id="6f613-133">TraceLoggingUInt64</span><span class="sxs-lookup"><span data-stu-id="6f613-133">TraceLoggingUInt64</span></span>

-   <span data-ttu-id="6f613-134">TraceLoggingFloat32</span><span class="sxs-lookup"><span data-stu-id="6f613-134">TraceLoggingFloat32</span></span>

-   <span data-ttu-id="6f613-135">TraceLoggingFloat64</span><span class="sxs-lookup"><span data-stu-id="6f613-135">TraceLoggingFloat64</span></span>

-   <span data-ttu-id="6f613-136">TraceLoggingBool</span><span class="sxs-lookup"><span data-stu-id="6f613-136">TraceLoggingBool</span></span>

-   <span data-ttu-id="6f613-137">TraceLoggingFileTime</span><span class="sxs-lookup"><span data-stu-id="6f613-137">TraceLoggingFileTime</span></span>

-   <span data-ttu-id="6f613-138">TraceLoggingGuid</span><span class="sxs-lookup"><span data-stu-id="6f613-138">TraceLoggingGuid</span></span>

-   <span data-ttu-id="6f613-139">TraceLoggingPointer</span><span class="sxs-lookup"><span data-stu-id="6f613-139">TraceLoggingPointer</span></span>

-   <span data-ttu-id="6f613-140">TraceLoggingSystemTime</span><span class="sxs-lookup"><span data-stu-id="6f613-140">TraceLoggingSystemTime</span></span>

-   <span data-ttu-id="6f613-141">TraceLoggingHexInt8</span><span class="sxs-lookup"><span data-stu-id="6f613-141">TraceLoggingHexInt8</span></span>

-   <span data-ttu-id="6f613-142">TraceLoggingHexUInt8</span><span class="sxs-lookup"><span data-stu-id="6f613-142">TraceLoggingHexUInt8</span></span>

-   <span data-ttu-id="6f613-143">TraceLoggingHexInt32</span><span class="sxs-lookup"><span data-stu-id="6f613-143">TraceLoggingHexInt32</span></span>

-   <span data-ttu-id="6f613-144">TraceLoggingHexUInt32</span><span class="sxs-lookup"><span data-stu-id="6f613-144">TraceLoggingHexUInt32</span></span>

-   <span data-ttu-id="6f613-145">TraceLoggingHexInt64</span><span class="sxs-lookup"><span data-stu-id="6f613-145">TraceLoggingHexInt64</span></span>

-   <span data-ttu-id="6f613-146">TraceLoggingHexUInt64</span><span class="sxs-lookup"><span data-stu-id="6f613-146">TraceLoggingHexUInt64</span></span>

-   <span data-ttu-id="6f613-147">TraceLoggingWchar</span><span class="sxs-lookup"><span data-stu-id="6f613-147">TraceLoggingWchar</span></span>

-   <span data-ttu-id="6f613-148">TraceLoggingChar</span><span class="sxs-lookup"><span data-stu-id="6f613-148">TraceLoggingChar</span></span>

-   <span data-ttu-id="6f613-149">TraceLoggingIntPtr</span><span class="sxs-lookup"><span data-stu-id="6f613-149">TraceLoggingIntPtr</span></span>

-   <span data-ttu-id="6f613-150">TraceLoggingUIntPtr</span><span class="sxs-lookup"><span data-stu-id="6f613-150">TraceLoggingUIntPtr</span></span>

-   <span data-ttu-id="6f613-151">TraceLoggingBoolean</span><span class="sxs-lookup"><span data-stu-id="6f613-151">TraceLoggingBoolean</span></span>

-   <span data-ttu-id="6f613-152">TraceLoggingHexInt16</span><span class="sxs-lookup"><span data-stu-id="6f613-152">TraceLoggingHexInt16</span></span>

-   <span data-ttu-id="6f613-153">TraceLoggingHexUInt16</span><span class="sxs-lookup"><span data-stu-id="6f613-153">TraceLoggingHexUInt16</span></span>

-   <span data-ttu-id="6f613-154">TraceLoggingPid</span><span class="sxs-lookup"><span data-stu-id="6f613-154">TraceLoggingPid</span></span>

-   <span data-ttu-id="6f613-155">TraceLoggingTid</span><span class="sxs-lookup"><span data-stu-id="6f613-155">TraceLoggingTid</span></span>

-   <span data-ttu-id="6f613-156">TraceLoggingPort</span><span class="sxs-lookup"><span data-stu-id="6f613-156">TraceLoggingPort</span></span>

-   <span data-ttu-id="6f613-157">TraceLoggingWinError</span><span class="sxs-lookup"><span data-stu-id="6f613-157">TraceLoggingWinError</span></span>

-   <span data-ttu-id="6f613-158">TraceLoggingNTStatus</span><span class="sxs-lookup"><span data-stu-id="6f613-158">TraceLoggingNTStatus</span></span>

-   <span data-ttu-id="6f613-159">TraceLoggingHResult</span><span class="sxs-lookup"><span data-stu-id="6f613-159">TraceLoggingHResult</span></span>

-   <span data-ttu-id="6f613-160">TraceLoggingSocketAddress</span><span class="sxs-lookup"><span data-stu-id="6f613-160">TraceLoggingSocketAddress</span></span>

-   <span data-ttu-id="6f613-161">TraceLoggingSid</span><span class="sxs-lookup"><span data-stu-id="6f613-161">TraceLoggingSid</span></span>

-   <span data-ttu-id="6f613-162">TraceLoggingString</span><span class="sxs-lookup"><span data-stu-id="6f613-162">TraceLoggingString</span></span>

-   <span data-ttu-id="6f613-163">TraceLoggingWideString</span><span class="sxs-lookup"><span data-stu-id="6f613-163">TraceLoggingWideString</span></span>

-   <span data-ttu-id="6f613-164">TraceLoggingCountedString</span><span class="sxs-lookup"><span data-stu-id="6f613-164">TraceLoggingCountedString</span></span>

-   <span data-ttu-id="6f613-165">TraceLoggingCountedWideString</span><span class="sxs-lookup"><span data-stu-id="6f613-165">TraceLoggingCountedWideString</span></span>

-   <span data-ttu-id="6f613-166">TraceLoggingAnsiString</span><span class="sxs-lookup"><span data-stu-id="6f613-166">TraceLoggingAnsiString</span></span>

-   <span data-ttu-id="6f613-167">TraceLoggingUnicodeString</span><span class="sxs-lookup"><span data-stu-id="6f613-167">TraceLoggingUnicodeString</span></span>

-   <span data-ttu-id="6f613-168">TraceLoggingBinary (datos vacíos \* , tamaño de los datos en bytes \[ , \] nombre opcional) los parámetros de esta macro difieren de los anteriores.</span><span class="sxs-lookup"><span data-stu-id="6f613-168">TraceLoggingBinary(void \*data, size of the data in bytes, \[optional\] name ) The parameters to this macro differ from those above.</span></span> <span data-ttu-id="6f613-169">Si se especifica el parámetro *Name* , debe ser un literal de cadena (no una variable) y no puede contener caracteres nulos incrustados.</span><span class="sxs-lookup"><span data-stu-id="6f613-169">If the *name* parameter is specified, it must be a string literal (not a variable) and may not contain any embedded null characters.</span></span> <span data-ttu-id="6f613-170">Si no se proporciona el parámetro *Name* , se genera automáticamente un nombre.</span><span class="sxs-lookup"><span data-stu-id="6f613-170">If the *name* parameter is not provided, a name is generated automatically.</span></span>

<span data-ttu-id="6f613-171">La API de TraceLogging también hace que varias macros estén disponibles para las matrices.</span><span class="sxs-lookup"><span data-stu-id="6f613-171">The TraceLogging API also makes several macros available for arrays.</span></span> <span data-ttu-id="6f613-172">Estas matrices pueden tener una longitud fija o ser de longitud variable, en función de la macro de contenedor que elija usar.</span><span class="sxs-lookup"><span data-stu-id="6f613-172">These arrays can either have a fixed length or be of a variable length, depending on the wrapper macro you choose to use.</span></span> <span data-ttu-id="6f613-173">Todas estas macros de contenedor siguen este formato.</span><span class="sxs-lookup"><span data-stu-id="6f613-173">All of these wrapper macros follow this format.</span></span>

`TraceLoggingBooleanArray(pVals, cVals, name, desc, tags)`

<span data-ttu-id="6f613-174">El parámetro *pVals* apunta a la matriz de datos y *cVals* indica el número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="6f613-174">The parameter *pVals* points to the array of data and *cVals* indicates the number of elements in the array.</span></span> <span data-ttu-id="6f613-175">*cVals* debe ser una constante y no puede ser una variable.</span><span class="sxs-lookup"><span data-stu-id="6f613-175">*cVals* must be a constant and cannot be a variable.</span></span> <span data-ttu-id="6f613-176">Al igual que con las macros de contenedor de valor único, *Name*, **DESC** y *Tags* son parámetros opcionales y deben seguir las mismas restricciones que se explican con la macro **TraceLoggingValue** .</span><span class="sxs-lookup"><span data-stu-id="6f613-176">As with the single value wrapper macros, *name*, **desc**, and *tags* are optional parameters and must follow the same restrictions as explained with the **TraceLoggingValue** macro.</span></span>

-   <span data-ttu-id="6f613-177">TraceLoggingInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-177">TraceLoggingInt8FixedArray</span></span>

-   <span data-ttu-id="6f613-178">TraceLoggingUInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-178">TraceLoggingUInt8FixedArray</span></span>

-   <span data-ttu-id="6f613-179">TraceLoggingInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-179">TraceLoggingInt16FixedArray</span></span>

-   <span data-ttu-id="6f613-180">TraceLoggingUInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-180">TraceLoggingUInt16FixedArray</span></span>

-   <span data-ttu-id="6f613-181">TraceLoggingInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-181">TraceLoggingInt32FixedArray</span></span>

-   <span data-ttu-id="6f613-182">TraceLoggingUInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-182">TraceLoggingUInt32FixedArray</span></span>

-   <span data-ttu-id="6f613-183">TraceLoggingInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-183">TraceLoggingInt64FixedArray</span></span>

-   <span data-ttu-id="6f613-184">TraceLoggingUInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-184">TraceLoggingUInt64FixedArray</span></span>

-   <span data-ttu-id="6f613-185">TraceLoggingFloat32FixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-185">TraceLoggingFloat32FixedArray</span></span>

-   <span data-ttu-id="6f613-186">TraceLoggingFloat64FixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-186">TraceLoggingFloat64FixedArray</span></span>

-   <span data-ttu-id="6f613-187">TraceLoggingBoolFixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-187">TraceLoggingBoolFixedArray</span></span>

-   <span data-ttu-id="6f613-188">TraceLoggingGuidFixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-188">TraceLoggingGuidFixedArray</span></span>

-   <span data-ttu-id="6f613-189">TraceLoggingPointerFixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-189">TraceLoggingPointerFixedArray</span></span>

-   <span data-ttu-id="6f613-190">TraceLoggingFileTimeFixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-190">TraceLoggingFileTimeFixedArray</span></span>

-   <span data-ttu-id="6f613-191">TraceLoggingSystemTimeFixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-191">TraceLoggingSystemTimeFixedArray</span></span>

-   <span data-ttu-id="6f613-192">TraceLoggingHexInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-192">TraceLoggingHexInt8FixedArray</span></span>

-   <span data-ttu-id="6f613-193">TraceLoggingHexUInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-193">TraceLoggingHexUInt8FixedArray</span></span>

-   <span data-ttu-id="6f613-194">TraceLoggingHexInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-194">TraceLoggingHexInt32FixedArray</span></span>

-   <span data-ttu-id="6f613-195">TraceLoggingHexUInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-195">TraceLoggingHexUInt32FixedArray</span></span>

-   <span data-ttu-id="6f613-196">TraceLoggingHexInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-196">TraceLoggingHexInt64FixedArray</span></span>

-   <span data-ttu-id="6f613-197">TraceLoggingHexUInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-197">TraceLoggingHexUInt64FixedArray</span></span>

-   <span data-ttu-id="6f613-198">TraceLoggingWcharFixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-198">TraceLoggingWcharFixedArray</span></span>

-   <span data-ttu-id="6f613-199">TraceLoggingCharFixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-199">TraceLoggingCharFixedArray</span></span>

-   <span data-ttu-id="6f613-200">TraceLoggingIntPtrFixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-200">TraceLoggingIntPtrFixedArray</span></span>

-   <span data-ttu-id="6f613-201">TraceLoggingUIntPtrFixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-201">TraceLoggingUIntPtrFixedArray</span></span>

-   <span data-ttu-id="6f613-202">TraceLoggingBooleanFixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-202">TraceLoggingBooleanFixedArray</span></span>

-   <span data-ttu-id="6f613-203">TraceLoggingHexInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-203">TraceLoggingHexInt16FixedArray</span></span>

-   <span data-ttu-id="6f613-204">TraceLoggingHexUInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="6f613-204">TraceLoggingHexUInt16FixedArray</span></span>

-   <span data-ttu-id="6f613-205">TraceLoggingInt8Array</span><span class="sxs-lookup"><span data-stu-id="6f613-205">TraceLoggingInt8Array</span></span>

-   <span data-ttu-id="6f613-206">TraceLoggingUInt8Array</span><span class="sxs-lookup"><span data-stu-id="6f613-206">TraceLoggingUInt8Array</span></span>

-   <span data-ttu-id="6f613-207">TraceLoggingInt16Array</span><span class="sxs-lookup"><span data-stu-id="6f613-207">TraceLoggingInt16Array</span></span>

-   <span data-ttu-id="6f613-208">TraceLoggingUInt16Array</span><span class="sxs-lookup"><span data-stu-id="6f613-208">TraceLoggingUInt16Array</span></span>

-   <span data-ttu-id="6f613-209">TraceLoggingInt32Array</span><span class="sxs-lookup"><span data-stu-id="6f613-209">TraceLoggingInt32Array</span></span>

-   <span data-ttu-id="6f613-210">TraceLoggingUInt32Array</span><span class="sxs-lookup"><span data-stu-id="6f613-210">TraceLoggingUInt32Array</span></span>

-   <span data-ttu-id="6f613-211">TraceLoggingInt64Array</span><span class="sxs-lookup"><span data-stu-id="6f613-211">TraceLoggingInt64Array</span></span>

-   <span data-ttu-id="6f613-212">TraceLoggingUInt64Array</span><span class="sxs-lookup"><span data-stu-id="6f613-212">TraceLoggingUInt64Array</span></span>

-   <span data-ttu-id="6f613-213">TraceLoggingFloat32Array</span><span class="sxs-lookup"><span data-stu-id="6f613-213">TraceLoggingFloat32Array</span></span>

-   <span data-ttu-id="6f613-214">TraceLoggingFloat64Array</span><span class="sxs-lookup"><span data-stu-id="6f613-214">TraceLoggingFloat64Array</span></span>

-   <span data-ttu-id="6f613-215">TraceLoggingBoolArray</span><span class="sxs-lookup"><span data-stu-id="6f613-215">TraceLoggingBoolArray</span></span>

-   <span data-ttu-id="6f613-216">TraceLoggingGuidArray</span><span class="sxs-lookup"><span data-stu-id="6f613-216">TraceLoggingGuidArray</span></span>

-   <span data-ttu-id="6f613-217">TraceLoggingPointerArray</span><span class="sxs-lookup"><span data-stu-id="6f613-217">TraceLoggingPointerArray</span></span>

-   <span data-ttu-id="6f613-218">TraceLoggingFileTimeArray</span><span class="sxs-lookup"><span data-stu-id="6f613-218">TraceLoggingFileTimeArray</span></span>

-   <span data-ttu-id="6f613-219">TraceLoggingSystemTimeArray</span><span class="sxs-lookup"><span data-stu-id="6f613-219">TraceLoggingSystemTimeArray</span></span>

-   <span data-ttu-id="6f613-220">TraceLoggingHexInt8Array</span><span class="sxs-lookup"><span data-stu-id="6f613-220">TraceLoggingHexInt8Array</span></span>

-   <span data-ttu-id="6f613-221">TraceLoggingHexUInt8Array</span><span class="sxs-lookup"><span data-stu-id="6f613-221">TraceLoggingHexUInt8Array</span></span>

-   <span data-ttu-id="6f613-222">TraceLoggingHexInt32Array</span><span class="sxs-lookup"><span data-stu-id="6f613-222">TraceLoggingHexInt32Array</span></span>

-   <span data-ttu-id="6f613-223">TraceLoggingHexUInt32Array</span><span class="sxs-lookup"><span data-stu-id="6f613-223">TraceLoggingHexUInt32Array</span></span>

-   <span data-ttu-id="6f613-224">TraceLoggingHexInt64Array</span><span class="sxs-lookup"><span data-stu-id="6f613-224">TraceLoggingHexInt64Array</span></span>

-   <span data-ttu-id="6f613-225">TraceLoggingHexUInt64Array</span><span class="sxs-lookup"><span data-stu-id="6f613-225">TraceLoggingHexUInt64Array</span></span>

-   <span data-ttu-id="6f613-226">TraceLoggingWcharArray</span><span class="sxs-lookup"><span data-stu-id="6f613-226">TraceLoggingWcharArray</span></span>

-   <span data-ttu-id="6f613-227">TraceLoggingCharArray</span><span class="sxs-lookup"><span data-stu-id="6f613-227">TraceLoggingCharArray</span></span>

-   <span data-ttu-id="6f613-228">TraceLoggingIntPtrArray</span><span class="sxs-lookup"><span data-stu-id="6f613-228">TraceLoggingIntPtrArray</span></span>

-   <span data-ttu-id="6f613-229">TraceLoggingUIntPtrArray</span><span class="sxs-lookup"><span data-stu-id="6f613-229">TraceLoggingUIntPtrArray</span></span>

-   <span data-ttu-id="6f613-230">TraceLoggingBooleanArray</span><span class="sxs-lookup"><span data-stu-id="6f613-230">TraceLoggingBooleanArray</span></span>

-   <span data-ttu-id="6f613-231">TraceLoggingHexInt16Array</span><span class="sxs-lookup"><span data-stu-id="6f613-231">TraceLoggingHexInt16Array</span></span>

-   <span data-ttu-id="6f613-232">TraceLoggingHexUInt16Array</span><span class="sxs-lookup"><span data-stu-id="6f613-232">TraceLoggingHexUInt16Array</span></span>

 

 




