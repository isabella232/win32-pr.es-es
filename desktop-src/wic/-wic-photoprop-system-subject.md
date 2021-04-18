---
description: La Directiva de metadatos de la fotografía para la propiedad System. Subject.
ms.assetid: 5ab7c74b-8a5e-4329-8a49-291470d406cc
title: Directiva de metadatos de la foto System. Subject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceabbab95a52a1155db949dbc60b4525dd5f9d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706834"
---
# <a name="systemsubject-photo-metadata-policy"></a><span data-ttu-id="052d1-103">Directiva de metadatos de la foto System. Subject</span><span class="sxs-lookup"><span data-stu-id="052d1-103">System.Subject Photo Metadata Policy</span></span>

<span data-ttu-id="052d1-104">La Directiva de metadatos de la fotografía para la propiedad [System. Subject](../properties/props-system-subject.md) .</span><span class="sxs-lookup"><span data-stu-id="052d1-104">The photo metadata policy for the [System.Subject](../properties/props-system-subject.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="052d1-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="052d1-105">PKEY</span></span>

<span data-ttu-id="052d1-106">\_Asunto PKEY</span><span class="sxs-lookup"><span data-stu-id="052d1-106">PKEY\_Subject</span></span>

### <a name="containers"></a><span data-ttu-id="052d1-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="052d1-107">Containers</span></span>

<span data-ttu-id="052d1-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="052d1-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="052d1-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="052d1-109">Read-Only</span></span>

<span data-ttu-id="052d1-110">No</span><span class="sxs-lookup"><span data-stu-id="052d1-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="052d1-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="052d1-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="052d1-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="052d1-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="052d1-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="052d1-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="052d1-114">VT \_ LPWStr o VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="052d1-114">Either VT\_LPWSTR or VT\_LPWSTR</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="052d1-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="052d1-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="052d1-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="052d1-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="052d1-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="052d1-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="052d1-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="052d1-118">Read Paths</span></span>



| <span data-ttu-id="052d1-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="052d1-119">Order</span></span> | <span data-ttu-id="052d1-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="052d1-120">Path</span></span>                     | <span data-ttu-id="052d1-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="052d1-121">Disk Format</span></span>    |
|-------|--------------------------|----------------|
| <span data-ttu-id="052d1-122">1</span><span class="sxs-lookup"><span data-stu-id="052d1-122">1</span></span>     | <span data-ttu-id="052d1-123">/app1/IFD/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="052d1-123">/app1/ifd/{ushort=40095}</span></span> | <span data-ttu-id="052d1-124">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="052d1-124">unicode\_bytes</span></span> |
| <span data-ttu-id="052d1-125">2</span><span class="sxs-lookup"><span data-stu-id="052d1-125">2</span></span>     | <span data-ttu-id="052d1-126">/app1/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="052d1-126">/app1/ifd/{ushort=270}</span></span>   | <span data-ttu-id="052d1-127">ascii</span><span class="sxs-lookup"><span data-stu-id="052d1-127">ascii</span></span>          |



 

### <a name="write-paths"></a><span data-ttu-id="052d1-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="052d1-128">Write Paths</span></span>



| <span data-ttu-id="052d1-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="052d1-129">Order</span></span> | <span data-ttu-id="052d1-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="052d1-130">Path</span></span>                     | <span data-ttu-id="052d1-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="052d1-131">Disk Format</span></span>    |
|-------|--------------------------|----------------|
| <span data-ttu-id="052d1-132">1</span><span class="sxs-lookup"><span data-stu-id="052d1-132">1</span></span>     | <span data-ttu-id="052d1-133">/app1/IFD/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="052d1-133">/app1/ifd/{ushort=40095}</span></span> | <span data-ttu-id="052d1-134">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="052d1-134">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="052d1-135">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="052d1-135">Remove Paths</span></span>



| <span data-ttu-id="052d1-136">Pedido</span><span class="sxs-lookup"><span data-stu-id="052d1-136">Order</span></span> | <span data-ttu-id="052d1-137">Ruta</span><span class="sxs-lookup"><span data-stu-id="052d1-137">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="052d1-138">1</span><span class="sxs-lookup"><span data-stu-id="052d1-138">1</span></span>     | <span data-ttu-id="052d1-139">/app1/IFD/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="052d1-139">/app1/ifd/{ushort=40095}</span></span> |
| <span data-ttu-id="052d1-140">2</span><span class="sxs-lookup"><span data-stu-id="052d1-140">2</span></span>     | <span data-ttu-id="052d1-141">/app1/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="052d1-141">/app1/ifd/{ushort=270}</span></span>   |



 

### <a name="tiff-policy"></a><span data-ttu-id="052d1-142">Directiva TIFF</span><span class="sxs-lookup"><span data-stu-id="052d1-142">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="052d1-143">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="052d1-143">Read Paths</span></span>



| <span data-ttu-id="052d1-144">Pedido</span><span class="sxs-lookup"><span data-stu-id="052d1-144">Order</span></span> | <span data-ttu-id="052d1-145">Ruta</span><span class="sxs-lookup"><span data-stu-id="052d1-145">Path</span></span>                | <span data-ttu-id="052d1-146">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="052d1-146">Disk Format</span></span>    |
|-------|---------------------|----------------|
| <span data-ttu-id="052d1-147">1</span><span class="sxs-lookup"><span data-stu-id="052d1-147">1</span></span>     | <span data-ttu-id="052d1-148">/IFD/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="052d1-148">/ifd/{ushort=40095}</span></span> | <span data-ttu-id="052d1-149">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="052d1-149">unicode\_bytes</span></span> |
| <span data-ttu-id="052d1-150">2</span><span class="sxs-lookup"><span data-stu-id="052d1-150">2</span></span>     | <span data-ttu-id="052d1-151">/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="052d1-151">/ifd/{ushort=270}</span></span>   | <span data-ttu-id="052d1-152">ascii</span><span class="sxs-lookup"><span data-stu-id="052d1-152">ascii</span></span>          |



 

### <a name="write-paths"></a><span data-ttu-id="052d1-153">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="052d1-153">Write Paths</span></span>



| <span data-ttu-id="052d1-154">Pedido</span><span class="sxs-lookup"><span data-stu-id="052d1-154">Order</span></span> | <span data-ttu-id="052d1-155">Ruta</span><span class="sxs-lookup"><span data-stu-id="052d1-155">Path</span></span>                | <span data-ttu-id="052d1-156">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="052d1-156">Disk Format</span></span>    |
|-------|---------------------|----------------|
| <span data-ttu-id="052d1-157">1</span><span class="sxs-lookup"><span data-stu-id="052d1-157">1</span></span>     | <span data-ttu-id="052d1-158">/IFD/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="052d1-158">/ifd/{ushort=40095}</span></span> | <span data-ttu-id="052d1-159">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="052d1-159">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="052d1-160">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="052d1-160">Remove Paths</span></span>



| <span data-ttu-id="052d1-161">Pedido</span><span class="sxs-lookup"><span data-stu-id="052d1-161">Order</span></span> | <span data-ttu-id="052d1-162">Ruta</span><span class="sxs-lookup"><span data-stu-id="052d1-162">Path</span></span>                |
|-------|---------------------|
| <span data-ttu-id="052d1-163">1</span><span class="sxs-lookup"><span data-stu-id="052d1-163">1</span></span>     | <span data-ttu-id="052d1-164">/IFD/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="052d1-164">/ifd/{ushort=40095}</span></span> |
| <span data-ttu-id="052d1-165">2</span><span class="sxs-lookup"><span data-stu-id="052d1-165">2</span></span>     | <span data-ttu-id="052d1-166">/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="052d1-166">/ifd/{ushort=270}</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="052d1-167">Observaciones</span><span class="sxs-lookup"><span data-stu-id="052d1-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="052d1-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="052d1-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="052d1-169">System. Subject</span><span class="sxs-lookup"><span data-stu-id="052d1-169">System.Subject</span></span>](../properties/props-system-subject.md)
</dt> </dl>

 

 
