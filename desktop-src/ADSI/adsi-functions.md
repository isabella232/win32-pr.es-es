---
title: Funciones ADSI
description: Active Directory interfaces de servicio exponen las siguientes funciones auxiliares a los clientes que no usan la automatización.
ms.assetid: 4f0e90e2-afcc-4cf7-a731-9b38a83ca229
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, referencia, funciones
- ADSI de la función
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c814cf4f59a391a3242fa748856eaacb35dbcc53
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356714"
---
# <a name="adsi-functions"></a><span data-ttu-id="1e1ce-105">Funciones ADSI</span><span class="sxs-lookup"><span data-stu-id="1e1ce-105">ADSI Functions</span></span>

<span data-ttu-id="1e1ce-106">Active Directory interfaces de servicio exponen las siguientes funciones auxiliares a los clientes que no usan la automatización.</span><span class="sxs-lookup"><span data-stu-id="1e1ce-106">Active Directory Service Interfaces expose the following helper functions to clients that do not use Automation.</span></span>



| <span data-ttu-id="1e1ce-107">Función</span><span class="sxs-lookup"><span data-stu-id="1e1ce-107">Function</span></span>                                           | <span data-ttu-id="1e1ce-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e1ce-108">Description</span></span>                                                                                        |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e1ce-109">**ADsBuildEnumerator**</span><span class="sxs-lookup"><span data-stu-id="1e1ce-109">**ADsBuildEnumerator**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator)   | <span data-ttu-id="1e1ce-110">Crea un objeto enumerador para el objeto contenedor ADSI especificado.</span><span class="sxs-lookup"><span data-stu-id="1e1ce-110">Creates an enumerator object for the specified ADSI container object.</span></span>                              |
| [<span data-ttu-id="1e1ce-111">**ADsBuildVarArrayInt**</span><span class="sxs-lookup"><span data-stu-id="1e1ce-111">**ADsBuildVarArrayInt**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararrayint) | <span data-ttu-id="1e1ce-112">Compila una matriz de tipo Variant a partir de una matriz de **DWORD** s.</span><span class="sxs-lookup"><span data-stu-id="1e1ce-112">Builds a variant array from an array of **DWORD** s.</span></span>                                                |
| [<span data-ttu-id="1e1ce-113">**ADsBuildVarArrayStr**</span><span class="sxs-lookup"><span data-stu-id="1e1ce-113">**ADsBuildVarArrayStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararraystr) | <span data-ttu-id="1e1ce-114">Compila una matriz de tipo Variant a partir de una matriz de cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="1e1ce-114">Builds a variant array from an array of Unicode strings.</span></span>                                           |
| [<span data-ttu-id="1e1ce-115">**ADsEncodeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="1e1ce-115">**ADsEncodeBinaryData**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) | <span data-ttu-id="1e1ce-116">Convierte un BLOB de datos binarios en el formato adecuado para un filtro de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1e1ce-116">Converts a blob of binary data to the format suitable for a search filter.</span></span>                         |
| [<span data-ttu-id="1e1ce-117">**ADsEnumerateNext**</span><span class="sxs-lookup"><span data-stu-id="1e1ce-117">**ADsEnumerateNext**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)       | <span data-ttu-id="1e1ce-118">Rellena una matriz de tipo Variant con elementos recuperados del objeto de enumerador especificado.</span><span class="sxs-lookup"><span data-stu-id="1e1ce-118">Populates a variant array with elements retrieved from the specified enumerator object.</span></span>            |
| [<span data-ttu-id="1e1ce-119">**ADsFreeEnumerator**</span><span class="sxs-lookup"><span data-stu-id="1e1ce-119">**ADsFreeEnumerator**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator)     | <span data-ttu-id="1e1ce-120">Libera un objeto de enumerador creado previamente por [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator).</span><span class="sxs-lookup"><span data-stu-id="1e1ce-120">Frees an enumerator object previously created by [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator).</span></span> |
| [<span data-ttu-id="1e1ce-121">**ADsGetLastError**</span><span class="sxs-lookup"><span data-stu-id="1e1ce-121">**ADsGetLastError**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror)         | <span data-ttu-id="1e1ce-122">Recupera el último valor de código de error del subproceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="1e1ce-122">Retrieves the last error code value of the calling thread.</span></span>                                         |
| [<span data-ttu-id="1e1ce-123">**ADsGetObject**</span><span class="sxs-lookup"><span data-stu-id="1e1ce-123">**ADsGetObject**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject)               | <span data-ttu-id="1e1ce-124">Enlaza a un objeto ADSI con las credenciales actuales.</span><span class="sxs-lookup"><span data-stu-id="1e1ce-124">Binds to an ADSI object using the current credentials.</span></span>                                             |
| [<span data-ttu-id="1e1ce-125">**ADsOpenObject**</span><span class="sxs-lookup"><span data-stu-id="1e1ce-125">**ADsOpenObject**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)             | <span data-ttu-id="1e1ce-126">Enlaza a un objeto ADSI mediante las credenciales especificadas</span><span class="sxs-lookup"><span data-stu-id="1e1ce-126">Binds to an ADSI object using specified credentials</span></span>                                                |
| [<span data-ttu-id="1e1ce-127">**ADsSetLastError**</span><span class="sxs-lookup"><span data-stu-id="1e1ce-127">**ADsSetLastError**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adssetlasterror)         | <span data-ttu-id="1e1ce-128">Establece el valor del código de error del subproceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="1e1ce-128">Sets the error code value of the calling thread.</span></span>                                                   |
| [<span data-ttu-id="1e1ce-129">**AllocADsMem**</span><span class="sxs-lookup"><span data-stu-id="1e1ce-129">**AllocADsMem**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem)                 | <span data-ttu-id="1e1ce-130">Asigna un bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="1e1ce-130">Allocates a block of memory.</span></span>                                                                       |
| [<span data-ttu-id="1e1ce-131">**AllocADsStr**</span><span class="sxs-lookup"><span data-stu-id="1e1ce-131">**AllocADsStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-allocadsstr)                 | <span data-ttu-id="1e1ce-132">Asigna memoria para una cadena determinada.</span><span class="sxs-lookup"><span data-stu-id="1e1ce-132">Allocates memory for a given string.</span></span>                                                               |
| [<span data-ttu-id="1e1ce-133">**FreeADsMem**</span><span class="sxs-lookup"><span data-stu-id="1e1ce-133">**FreeADsMem**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem)                   | <span data-ttu-id="1e1ce-134">Libera la memoria asignada por [**AllocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem).</span><span class="sxs-lookup"><span data-stu-id="1e1ce-134">Frees the memory allocated by [**AllocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem).</span></span>                                  |
| [<span data-ttu-id="1e1ce-135">**FreeADsStr**</span><span class="sxs-lookup"><span data-stu-id="1e1ce-135">**FreeADsStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-freeadsstr)                   | <span data-ttu-id="1e1ce-136">Libera la memoria asignada para la cadena especificada.</span><span class="sxs-lookup"><span data-stu-id="1e1ce-136">Frees the memory allocated for the given string.</span></span>                                                   |
| [<span data-ttu-id="1e1ce-137">**ReallocADsMem**</span><span class="sxs-lookup"><span data-stu-id="1e1ce-137">**ReallocADsMem**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsmem)             | <span data-ttu-id="1e1ce-138">Asigna el contenido de la memoria existente a una ubicación de memoria recién creada.</span><span class="sxs-lookup"><span data-stu-id="1e1ce-138">Assigns the existing memory content to a newly created memory location.</span></span>                            |
| [<span data-ttu-id="1e1ce-139">**ReallocADsStr**</span><span class="sxs-lookup"><span data-stu-id="1e1ce-139">**ReallocADsStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsstr)             | <span data-ttu-id="1e1ce-140">Reemplaza una cadena existente por otra nueva.</span><span class="sxs-lookup"><span data-stu-id="1e1ce-140">Replaces an existing string with a new one.</span></span>                                                        |



 

<span data-ttu-id="1e1ce-141">Las siguientes funciones ADSI están obsoletas.</span><span class="sxs-lookup"><span data-stu-id="1e1ce-141">The following ADSI functions are obsolete.</span></span>



| <span data-ttu-id="1e1ce-142">Función</span><span class="sxs-lookup"><span data-stu-id="1e1ce-142">Function</span></span>                                                  | <span data-ttu-id="1e1ce-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e1ce-143">Description</span></span> |
|-----------------------------------------------------------|-------------|
| [<span data-ttu-id="1e1ce-144">**AdsFreeAllErrorRecords**</span><span class="sxs-lookup"><span data-stu-id="1e1ce-144">**AdsFreeAllErrorRecords**</span></span>](obsolete-adsi-functions.md) | <span data-ttu-id="1e1ce-145">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="1e1ce-145">Obsolete.</span></span>   |
| [<span data-ttu-id="1e1ce-146">**AdsDecodeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="1e1ce-146">**AdsDecodeBinaryData**</span></span>](obsolete-adsi-functions.md)    | <span data-ttu-id="1e1ce-147">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="1e1ce-147">Obsolete.</span></span>   |
| [<span data-ttu-id="1e1ce-148">**PropVariantToAdsType**</span><span class="sxs-lookup"><span data-stu-id="1e1ce-148">**PropVariantToAdsType**</span></span>](obsolete-adsi-functions.md)   | <span data-ttu-id="1e1ce-149">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="1e1ce-149">Obsolete.</span></span>   |
| [<span data-ttu-id="1e1ce-150">**AdsTypeToPropVariant**</span><span class="sxs-lookup"><span data-stu-id="1e1ce-150">**AdsTypeToPropVariant**</span></span>](obsolete-adsi-functions.md)   | <span data-ttu-id="1e1ce-151">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="1e1ce-151">Obsolete.</span></span>   |
| [<span data-ttu-id="1e1ce-152">**AdsFreeAdsValues**</span><span class="sxs-lookup"><span data-stu-id="1e1ce-152">**AdsFreeAdsValues**</span></span>](obsolete-adsi-functions.md)       | <span data-ttu-id="1e1ce-153">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="1e1ce-153">Obsolete.</span></span>   |
| [<span data-ttu-id="1e1ce-154">**InitAdsMem**</span><span class="sxs-lookup"><span data-stu-id="1e1ce-154">**InitAdsMem**</span></span>](obsolete-adsi-functions.md)             | <span data-ttu-id="1e1ce-155">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="1e1ce-155">Obsolete.</span></span>   |
| [<span data-ttu-id="1e1ce-156">**AssertAdsmemLeaks**</span><span class="sxs-lookup"><span data-stu-id="1e1ce-156">**AssertAdsmemLeaks**</span></span>](obsolete-adsi-functions.md)      | <span data-ttu-id="1e1ce-157">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="1e1ce-157">Obsolete.</span></span>   |
| [<span data-ttu-id="1e1ce-158">**DumpMemorytracker**</span><span class="sxs-lookup"><span data-stu-id="1e1ce-158">**DumpMemorytracker**</span></span>](obsolete-adsi-functions.md)      | <span data-ttu-id="1e1ce-159">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="1e1ce-159">Obsolete.</span></span>   |



 

 

 




