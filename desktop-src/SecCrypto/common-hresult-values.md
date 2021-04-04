---
description: Los valores HRESULT siguientes son los más comunes. Se incluyen más valores en el archivo de encabezado Winerror. h.
ms.assetid: ce52efc3-92c7-40e4-ac49-0c54049e169f
title: Valores HRESULT comunes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a64d042d9531d026cda548b2a699ed60c0bebd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908598"
---
# <a name="common-hresult-values"></a><span data-ttu-id="d458c-104">Valores HRESULT comunes</span><span class="sxs-lookup"><span data-stu-id="d458c-104">Common HRESULT Values</span></span>

<span data-ttu-id="d458c-105">Los valores HRESULT siguientes son los más comunes.</span><span class="sxs-lookup"><span data-stu-id="d458c-105">The following HRESULT values are the most common.</span></span> <span data-ttu-id="d458c-106">Se incluyen más valores en el archivo de encabezado Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="d458c-106">More values are contained in the header file Winerror.h.</span></span>

<span data-ttu-id="d458c-107">Estos son los valores que aparecen ordenados alfabéticamente por nombre.</span><span class="sxs-lookup"><span data-stu-id="d458c-107">Here are the values listed alphabetically by name.</span></span>



| <span data-ttu-id="d458c-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="d458c-108">Name</span></span>            | <span data-ttu-id="d458c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d458c-109">Description</span></span>                         | <span data-ttu-id="d458c-110">Value</span><span class="sxs-lookup"><span data-stu-id="d458c-110">Value</span></span>      |
|-----------------|-------------------------------------|------------|
| <span data-ttu-id="d458c-111">S \_ correcto</span><span class="sxs-lookup"><span data-stu-id="d458c-111">S\_OK</span></span>           | <span data-ttu-id="d458c-112">Operación correcta</span><span class="sxs-lookup"><span data-stu-id="d458c-112">Operation successful</span></span>                | <span data-ttu-id="d458c-113">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d458c-113">0x00000000</span></span> |
| <span data-ttu-id="d458c-114">E \_ anular</span><span class="sxs-lookup"><span data-stu-id="d458c-114">E\_ABORT</span></span>        | <span data-ttu-id="d458c-115">Operación anulada</span><span class="sxs-lookup"><span data-stu-id="d458c-115">Operation aborted</span></span>                   | <span data-ttu-id="d458c-116">0x80004004</span><span class="sxs-lookup"><span data-stu-id="d458c-116">0x80004004</span></span> |
| <span data-ttu-id="d458c-117">E \_ ACCESSDENIED</span><span class="sxs-lookup"><span data-stu-id="d458c-117">E\_ACCESSDENIED</span></span> | <span data-ttu-id="d458c-118">Error general de acceso denegado</span><span class="sxs-lookup"><span data-stu-id="d458c-118">General access denied error</span></span>         | <span data-ttu-id="d458c-119">0x80070005</span><span class="sxs-lookup"><span data-stu-id="d458c-119">0x80070005</span></span> |
| <span data-ttu-id="d458c-120">E \_ FAIL</span><span class="sxs-lookup"><span data-stu-id="d458c-120">E\_FAIL</span></span>         | <span data-ttu-id="d458c-121">Error no especificado</span><span class="sxs-lookup"><span data-stu-id="d458c-121">Unspecified failure</span></span>                 | <span data-ttu-id="d458c-122">0x80004005</span><span class="sxs-lookup"><span data-stu-id="d458c-122">0x80004005</span></span> |
| <span data-ttu-id="d458c-123">\_identificador E</span><span class="sxs-lookup"><span data-stu-id="d458c-123">E\_HANDLE</span></span>       | <span data-ttu-id="d458c-124">Identificador no válido</span><span class="sxs-lookup"><span data-stu-id="d458c-124">Handle that is not valid</span></span>            | <span data-ttu-id="d458c-125">0x80070006</span><span class="sxs-lookup"><span data-stu-id="d458c-125">0x80070006</span></span> |
| <span data-ttu-id="d458c-126">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d458c-126">E\_INVALIDARG</span></span>   | <span data-ttu-id="d458c-127">Uno o varios argumentos no son válidos</span><span class="sxs-lookup"><span data-stu-id="d458c-127">One or more arguments are not valid</span></span> | <span data-ttu-id="d458c-128">0x80070057</span><span class="sxs-lookup"><span data-stu-id="d458c-128">0x80070057</span></span> |
| <span data-ttu-id="d458c-129">E \_ NOinterface</span><span class="sxs-lookup"><span data-stu-id="d458c-129">E\_NOINTERFACE</span></span>  | <span data-ttu-id="d458c-130">No se admite esta interfaz</span><span class="sxs-lookup"><span data-stu-id="d458c-130">No such interface supported</span></span>         | <span data-ttu-id="d458c-131">0x80004002</span><span class="sxs-lookup"><span data-stu-id="d458c-131">0x80004002</span></span> |
| <span data-ttu-id="d458c-132">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="d458c-132">E\_NOTIMPL</span></span>      | <span data-ttu-id="d458c-133">No implementado</span><span class="sxs-lookup"><span data-stu-id="d458c-133">Not implemented</span></span>                     | <span data-ttu-id="d458c-134">0x80004001</span><span class="sxs-lookup"><span data-stu-id="d458c-134">0x80004001</span></span> |
| <span data-ttu-id="d458c-135">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="d458c-135">E\_OUTOFMEMORY</span></span>  | <span data-ttu-id="d458c-136">No se pudo asignar la memoria necesaria</span><span class="sxs-lookup"><span data-stu-id="d458c-136">Failed to allocate necessary memory</span></span> | <span data-ttu-id="d458c-137">0x8007000E</span><span class="sxs-lookup"><span data-stu-id="d458c-137">0x8007000E</span></span> |
| <span data-ttu-id="d458c-138">\_puntero E</span><span class="sxs-lookup"><span data-stu-id="d458c-138">E\_POINTER</span></span>      | <span data-ttu-id="d458c-139">Puntero no válido</span><span class="sxs-lookup"><span data-stu-id="d458c-139">Pointer that is not valid</span></span>           | <span data-ttu-id="d458c-140">0x80004003</span><span class="sxs-lookup"><span data-stu-id="d458c-140">0x80004003</span></span> |
| <span data-ttu-id="d458c-141">E \_ inesperado</span><span class="sxs-lookup"><span data-stu-id="d458c-141">E\_UNEXPECTED</span></span>   | <span data-ttu-id="d458c-142">Error inesperado</span><span class="sxs-lookup"><span data-stu-id="d458c-142">Unexpected failure</span></span>                  | <span data-ttu-id="d458c-143">0x8000FFFF</span><span class="sxs-lookup"><span data-stu-id="d458c-143">0x8000FFFF</span></span> |



 

<span data-ttu-id="d458c-144">Estos son los valores que se muestran en orden numérico por valor.</span><span class="sxs-lookup"><span data-stu-id="d458c-144">Here are the values listed in numeric order by value.</span></span>



| <span data-ttu-id="d458c-145">Value</span><span class="sxs-lookup"><span data-stu-id="d458c-145">Value</span></span>      | <span data-ttu-id="d458c-146">Nombre</span><span class="sxs-lookup"><span data-stu-id="d458c-146">Name</span></span>            | <span data-ttu-id="d458c-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="d458c-147">Description</span></span>                         |
|------------|-----------------|-------------------------------------|
| <span data-ttu-id="d458c-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d458c-148">0x00000000</span></span> | <span data-ttu-id="d458c-149">S \_ correcto</span><span class="sxs-lookup"><span data-stu-id="d458c-149">S\_OK</span></span>           | <span data-ttu-id="d458c-150">Operación correcta</span><span class="sxs-lookup"><span data-stu-id="d458c-150">Operation successful</span></span>                |
| <span data-ttu-id="d458c-151">0x80004001</span><span class="sxs-lookup"><span data-stu-id="d458c-151">0x80004001</span></span> | <span data-ttu-id="d458c-152">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="d458c-152">E\_NOTIMPL</span></span>      | <span data-ttu-id="d458c-153">No implementado</span><span class="sxs-lookup"><span data-stu-id="d458c-153">Not implemented</span></span>                     |
| <span data-ttu-id="d458c-154">0x80004002</span><span class="sxs-lookup"><span data-stu-id="d458c-154">0x80004002</span></span> | <span data-ttu-id="d458c-155">E \_ NOinterface</span><span class="sxs-lookup"><span data-stu-id="d458c-155">E\_NOINTERFACE</span></span>  | <span data-ttu-id="d458c-156">No se admite esta interfaz</span><span class="sxs-lookup"><span data-stu-id="d458c-156">No such interface supported</span></span>         |
| <span data-ttu-id="d458c-157">0x80004003</span><span class="sxs-lookup"><span data-stu-id="d458c-157">0x80004003</span></span> | <span data-ttu-id="d458c-158">\_puntero E</span><span class="sxs-lookup"><span data-stu-id="d458c-158">E\_POINTER</span></span>      | <span data-ttu-id="d458c-159">Puntero no válido</span><span class="sxs-lookup"><span data-stu-id="d458c-159">Pointer that is not valid</span></span>           |
| <span data-ttu-id="d458c-160">0x80004004</span><span class="sxs-lookup"><span data-stu-id="d458c-160">0x80004004</span></span> | <span data-ttu-id="d458c-161">E \_ anular</span><span class="sxs-lookup"><span data-stu-id="d458c-161">E\_ABORT</span></span>        | <span data-ttu-id="d458c-162">Operación anulada</span><span class="sxs-lookup"><span data-stu-id="d458c-162">Operation aborted</span></span>                   |
| <span data-ttu-id="d458c-163">0x80004005</span><span class="sxs-lookup"><span data-stu-id="d458c-163">0x80004005</span></span> | <span data-ttu-id="d458c-164">E \_ FAIL</span><span class="sxs-lookup"><span data-stu-id="d458c-164">E\_FAIL</span></span>         | <span data-ttu-id="d458c-165">Error no especificado</span><span class="sxs-lookup"><span data-stu-id="d458c-165">Unspecified failure</span></span>                 |
| <span data-ttu-id="d458c-166">0x8000FFFF</span><span class="sxs-lookup"><span data-stu-id="d458c-166">0x8000FFFF</span></span> | <span data-ttu-id="d458c-167">E \_ inesperado</span><span class="sxs-lookup"><span data-stu-id="d458c-167">E\_UNEXPECTED</span></span>   | <span data-ttu-id="d458c-168">Error inesperado</span><span class="sxs-lookup"><span data-stu-id="d458c-168">Unexpected failure</span></span>                  |
| <span data-ttu-id="d458c-169">0x80070005</span><span class="sxs-lookup"><span data-stu-id="d458c-169">0x80070005</span></span> | <span data-ttu-id="d458c-170">E \_ ACCESSDENIED</span><span class="sxs-lookup"><span data-stu-id="d458c-170">E\_ACCESSDENIED</span></span> | <span data-ttu-id="d458c-171">Error general de acceso denegado</span><span class="sxs-lookup"><span data-stu-id="d458c-171">General access denied error</span></span>         |
| <span data-ttu-id="d458c-172">0x80070006</span><span class="sxs-lookup"><span data-stu-id="d458c-172">0x80070006</span></span> | <span data-ttu-id="d458c-173">\_identificador E</span><span class="sxs-lookup"><span data-stu-id="d458c-173">E\_HANDLE</span></span>       | <span data-ttu-id="d458c-174">Identificador no válido</span><span class="sxs-lookup"><span data-stu-id="d458c-174">Handle that is not valid</span></span>            |
| <span data-ttu-id="d458c-175">0x8007000E</span><span class="sxs-lookup"><span data-stu-id="d458c-175">0x8007000E</span></span> | <span data-ttu-id="d458c-176">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="d458c-176">E\_OUTOFMEMORY</span></span>  | <span data-ttu-id="d458c-177">No se pudo asignar la memoria necesaria</span><span class="sxs-lookup"><span data-stu-id="d458c-177">Failed to allocate necessary memory</span></span> |
| <span data-ttu-id="d458c-178">0x80070057</span><span class="sxs-lookup"><span data-stu-id="d458c-178">0x80070057</span></span> | <span data-ttu-id="d458c-179">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d458c-179">E\_INVALIDARG</span></span>   | <span data-ttu-id="d458c-180">Uno o varios argumentos no son válidos</span><span class="sxs-lookup"><span data-stu-id="d458c-180">One or more arguments are not valid</span></span> |



 

 

 



