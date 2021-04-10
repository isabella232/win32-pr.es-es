---
title: Efecto de morfología
description: Use el efecto de morfología para estrechar o aumentar el grosor de los límites de una imagen.
ms.assetid: 4B3CFC51-D556-4729-B433-7307C80291F4
keywords:
- efectos de morfología
- efecto de desactivación
- efecto de mermas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f43cf41810ae0b16c9bc96dd37473a0231fc132c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150635"
---
# <a name="morphology-effect"></a><span data-ttu-id="dcb3b-106">Efecto de morfología</span><span class="sxs-lookup"><span data-stu-id="dcb3b-106">Morphology effect</span></span>

<span data-ttu-id="dcb3b-107">Use el efecto de morfología para estrechar o aumentar el grosor de los límites de una imagen.</span><span class="sxs-lookup"><span data-stu-id="dcb3b-107">Use the morphology effect to thin or thicken edge boundaries in an image.</span></span> <span data-ttu-id="dcb3b-108">Este efecto crea un kernel que es 2 veces los valores de ancho y alto que especifique.</span><span class="sxs-lookup"><span data-stu-id="dcb3b-108">This effect creates a kernel that is 2 times the Width and Height values you specify.</span></span> <span data-ttu-id="dcb3b-109">Este efecto centra el kernel en el píxel que está calculando y devuelve el valor máximo en el kernel (si dilating) o el valor mínimo en el kernel (si Eroding).</span><span class="sxs-lookup"><span data-stu-id="dcb3b-109">This effect centers the kernel on the pixel it is calculating and returns the maximum value in the kernel (if dilating) or minimum value in the kernel (if eroding).</span></span>

<span data-ttu-id="dcb3b-110">El CLSID para este efecto es CLSID \_ D2D1Morphology.</span><span class="sxs-lookup"><span data-stu-id="dcb3b-110">The CLSID for this effect is CLSID\_D2D1Morphology.</span></span>

## <a name="example-images"></a><span data-ttu-id="dcb3b-111">Imágenes de ejemplo</span><span class="sxs-lookup"><span data-stu-id="dcb3b-111">Example images</span></span>

<span data-ttu-id="dcb3b-112">En este ejemplo se muestra el resultado del efecto al utilizar el modo de.</span><span class="sxs-lookup"><span data-stu-id="dcb3b-112">This example shows the output of the effect when using the erode mode.</span></span>



| <span data-ttu-id="dcb3b-113">Antes</span><span class="sxs-lookup"><span data-stu-id="dcb3b-113">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg) |
| <span data-ttu-id="dcb3b-115">Después</span><span class="sxs-lookup"><span data-stu-id="dcb3b-115">After</span></span>                                                      |
| ![la imagen después de la transformación.](images/7-morphology.png) |



 


```C++
ComPtr<ID2D1Effect> morphologyEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Morphology, &morphologyEffect);

morphologyEffect->SetInput(0, bitmap);

morphologyEffect->SetValue(D2D1_MORPHOLOGY_PROP_MODE, D2D1_MORPHOLOGY_MODE_ERODE);
morphologyEffect->SetValue(D2D1_MORPHOLOGY_PROP_WIDTH, 14);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(morphologyEffect.Get());
m_d2dContext->EndDraw(); 
```



## <a name="effect-properties"></a><span data-ttu-id="dcb3b-117">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="dcb3b-117">Effect properties</span></span>



| <span data-ttu-id="dcb3b-118">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="dcb3b-118">Display name and index enumeration</span></span>                          | <span data-ttu-id="dcb3b-119">Tipo y valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="dcb3b-119">Type and default value</span></span>                                                     | <span data-ttu-id="dcb3b-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="dcb3b-120">Description</span></span>                                                                                                                                                       |
|-------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcb3b-121">Mode</span><span class="sxs-lookup"><span data-stu-id="dcb3b-121">Mode</span></span><br/> <span data-ttu-id="dcb3b-122">D2D1 \_ \_ modo de propuesta de morfología \_</span><span class="sxs-lookup"><span data-stu-id="dcb3b-122">D2D1\_MORPHOLOGY\_PROP\_MODE</span></span><br/>     | <span data-ttu-id="dcb3b-123">\_Modo de morfología de D2D1 \_</span><span class="sxs-lookup"><span data-stu-id="dcb3b-123">D2D1\_MORPHOLOGY\_MODE</span></span><br/> <span data-ttu-id="dcb3b-124">D2D1 \_ el \_ modo de morfología \_</span><span class="sxs-lookup"><span data-stu-id="dcb3b-124">D2D1\_MORPHOLOGY\_MODE\_ERODE</span></span><br/> | <span data-ttu-id="dcb3b-125">Modo de morfología.</span><span class="sxs-lookup"><span data-stu-id="dcb3b-125">The morphology mode.</span></span> <span data-ttu-id="dcb3b-126">Los modos disponibles son (Flatten) y Dilate (espesor).</span><span class="sxs-lookup"><span data-stu-id="dcb3b-126">The available modes are erode (flatten) and dilate (thicken).</span></span><br/> <span data-ttu-id="dcb3b-127">Vea [modos de morfología](#morphology-modes) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="dcb3b-127">See [Morphology modes](#morphology-modes) for more info.</span></span><br/> |
| <span data-ttu-id="dcb3b-128">Ancho</span><span class="sxs-lookup"><span data-stu-id="dcb3b-128">Width</span></span><br/> <span data-ttu-id="dcb3b-129">Ancho de la D2D1 \_ morfología \_ \_</span><span class="sxs-lookup"><span data-stu-id="dcb3b-129">D2D1\_MORPHOLOGY\_PROP\_WIDTH</span></span><br/>   | <span data-ttu-id="dcb3b-130">UINT</span><span class="sxs-lookup"><span data-stu-id="dcb3b-130">UINT</span></span><br/> <span data-ttu-id="dcb3b-131">1</span><span class="sxs-lookup"><span data-stu-id="dcb3b-131">1</span></span><br/>                                               | <span data-ttu-id="dcb3b-132">Tamaño del kernel en la dirección X.</span><span class="sxs-lookup"><span data-stu-id="dcb3b-132">Size of the kernel in the X direction.</span></span> <span data-ttu-id="dcb3b-133">Las unidades están en DIP.</span><span class="sxs-lookup"><span data-stu-id="dcb3b-133">The units are in DIPs.</span></span> <span data-ttu-id="dcb3b-134">Los valores deben estar entre 1 y 100, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="dcb3b-134">Values must be between 1 and 100 inclusive.</span></span>                                                         |
| <span data-ttu-id="dcb3b-135">Alto</span><span class="sxs-lookup"><span data-stu-id="dcb3b-135">Height</span></span><br/> <span data-ttu-id="dcb3b-136">Alto de la D2D1 \_ morfología \_ \_</span><span class="sxs-lookup"><span data-stu-id="dcb3b-136">D2D1\_MORPHOLOGY\_PROP\_HEIGHT</span></span><br/> | <span data-ttu-id="dcb3b-137">UINT</span><span class="sxs-lookup"><span data-stu-id="dcb3b-137">UINT</span></span><br/> <span data-ttu-id="dcb3b-138">1</span><span class="sxs-lookup"><span data-stu-id="dcb3b-138">1</span></span><br/>                                               | <span data-ttu-id="dcb3b-139">Tamaño del kernel en la dirección Y.</span><span class="sxs-lookup"><span data-stu-id="dcb3b-139">Size of the kernel in the Y direction.</span></span> <span data-ttu-id="dcb3b-140">Las unidades están en DIP.</span><span class="sxs-lookup"><span data-stu-id="dcb3b-140">The units are in DIPs.</span></span> <span data-ttu-id="dcb3b-141">Los valores deben estar entre 1 y 100, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="dcb3b-141">Values must be between 1 and 100 inclusive.</span></span>                                                         |



 

## <a name="morphology-modes"></a><span data-ttu-id="dcb3b-142">Modos de morfología</span><span class="sxs-lookup"><span data-stu-id="dcb3b-142">Morphology modes</span></span>



| <span data-ttu-id="dcb3b-143">Nombre</span><span class="sxs-lookup"><span data-stu-id="dcb3b-143">Name</span></span>                           | <span data-ttu-id="dcb3b-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="dcb3b-144">Description</span></span>                                                    |
|--------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="dcb3b-145">D2D1 \_ el \_ modo de morfología \_</span><span class="sxs-lookup"><span data-stu-id="dcb3b-145">D2D1\_MORPHOLOGY\_MODE\_ERODE</span></span>  | <span data-ttu-id="dcb3b-146">Se usa el valor máximo de cada canal RGB en el kernel.</span><span class="sxs-lookup"><span data-stu-id="dcb3b-146">The maximum value from each RGB channel in the kernel is used.</span></span> |
| <span data-ttu-id="dcb3b-147">Desreferenciado del modo de \_ morfología D2D1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="dcb3b-147">D2D1\_MORPHOLOGY\_MODE\_DILATE</span></span> | <span data-ttu-id="dcb3b-148">Se usa el valor mínimo de cada canal RGB en el kernel.</span><span class="sxs-lookup"><span data-stu-id="dcb3b-148">The minimum value from each RGB channel in the kernel is used.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="dcb3b-149">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="dcb3b-149">Output bitmap</span></span>

<span data-ttu-id="dcb3b-150">En el modo de tiempo de ejecución, el tamaño del mapa de bits de salida crece:</span><span class="sxs-lookup"><span data-stu-id="dcb3b-150">For DILATE mode, the Output Bitmap size grows:</span></span> 

| <span data-ttu-id="dcb3b-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcb3b-151">Requirement</span></span> | <span data-ttu-id="dcb3b-152">Value</span><span class="sxs-lookup"><span data-stu-id="dcb3b-152">Value</span></span> |
|--------------------------|-----------------------------------------|
| <span data-ttu-id="dcb3b-153">Crecimiento de mapa de bits de salida X =</span><span class="sxs-lookup"><span data-stu-id="dcb3b-153">Output Bitmap Growth X =</span></span> | <span data-ttu-id="dcb3b-154">INT (FLOAT (ancho) \* ((PPP del usuario)/96))</span><span class="sxs-lookup"><span data-stu-id="dcb3b-154">INT(FLOAT(Width) \* ((User DPI) / 96))</span></span>  |
| <span data-ttu-id="dcb3b-155">Crecimiento de mapa de bits de salida Y =</span><span class="sxs-lookup"><span data-stu-id="dcb3b-155">Output Bitmap Growth Y =</span></span> | <span data-ttu-id="dcb3b-156">INT (FLOAT (alto) \* ((PPP del usuario)/96))</span><span class="sxs-lookup"><span data-stu-id="dcb3b-156">INT(FLOAT(Height) \* ((User DPI) / 96))</span></span> |



 

<span data-ttu-id="dcb3b-157">En el modo de disminución, se reduce el tamaño del mapa de bits de salida:</span><span class="sxs-lookup"><span data-stu-id="dcb3b-157">For ERODE mode, the Output Bitmap size shrinks:</span></span>

| <span data-ttu-id="dcb3b-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcb3b-158">Requirement</span></span> | <span data-ttu-id="dcb3b-159">Value</span><span class="sxs-lookup"><span data-stu-id="dcb3b-159">Value</span></span> |
|--------------------------|------------------------------------------|
| <span data-ttu-id="dcb3b-160">Crecimiento de mapa de bits de salida X =</span><span class="sxs-lookup"><span data-stu-id="dcb3b-160">Output Bitmap Growth X =</span></span> | <span data-ttu-id="dcb3b-161">INT (FLOAT (-width) \* ((PPP de usuario)/96))</span><span class="sxs-lookup"><span data-stu-id="dcb3b-161">INT(FLOAT(-Width) \* ((User DPI) / 96))</span></span>  |
| <span data-ttu-id="dcb3b-162">Crecimiento de mapa de bits de salida Y =</span><span class="sxs-lookup"><span data-stu-id="dcb3b-162">Output Bitmap Growth Y =</span></span> | <span data-ttu-id="dcb3b-163">INT (FLOAT (-height) \* ((PPP de usuario)/96))</span><span class="sxs-lookup"><span data-stu-id="dcb3b-163">INT(FLOAT(-Height) \* ((User DPI) / 96))</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="dcb3b-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcb3b-164">Requirements</span></span>



| <span data-ttu-id="dcb3b-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcb3b-165">Requirement</span></span> | <span data-ttu-id="dcb3b-166">Value</span><span class="sxs-lookup"><span data-stu-id="dcb3b-166">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dcb3b-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dcb3b-167">Minimum supported client</span></span> | <span data-ttu-id="dcb3b-168">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="dcb3b-168">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="dcb3b-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dcb3b-169">Minimum supported server</span></span> | <span data-ttu-id="dcb3b-170">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="dcb3b-170">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="dcb3b-171">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dcb3b-171">Header</span></span>                   | <span data-ttu-id="dcb3b-172">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="dcb3b-172">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="dcb3b-173">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dcb3b-173">Library</span></span>                  | <span data-ttu-id="dcb3b-174">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="dcb3b-174">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="dcb3b-175">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dcb3b-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcb3b-176">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="dcb3b-176">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

