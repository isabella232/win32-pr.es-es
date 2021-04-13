---
title: Efecto de Atlas
description: Puede usar este efecto para generar una parte de una imagen, pero conservar la región fuera de la parte para su uso en operaciones posteriores.
ms.assetid: D35E32CB-4DF7-408F-A717-1E421DDC8763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f9e1d4c6df0698d47a35eb2cbdaf670b98ed125
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492125"
---
# <a name="atlas-effect"></a><span data-ttu-id="d3039-103">Efecto de Atlas</span><span class="sxs-lookup"><span data-stu-id="d3039-103">Atlas effect</span></span>

<span data-ttu-id="d3039-104">Puede usar este efecto para generar una parte de una imagen, pero conservar la región fuera de la parte para su uso en operaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d3039-104">You can use this effect to output a portion of an image but retain the region outside of the portion for use in subsequent operations.</span></span>

<span data-ttu-id="d3039-105">El CLSID para este efecto es CLSID \_ D2D1Atlas.</span><span class="sxs-lookup"><span data-stu-id="d3039-105">The CLSID for this effect is CLSID\_D2D1Atlas.</span></span>

<span data-ttu-id="d3039-106">El efecto de Atlas es útil si desea cargar una imagen grande formada por muchas imágenes más pequeñas, como varios marcos de un Sprite.</span><span class="sxs-lookup"><span data-stu-id="d3039-106">The atlas effect is useful if you want to load a large image made up of many smaller images, such as various frames of a sprite.</span></span>

<span data-ttu-id="d3039-107">Para crear la salida del efecto:</span><span class="sxs-lookup"><span data-stu-id="d3039-107">To create the output the effect:</span></span>

1.  <span data-ttu-id="d3039-108">Recorta la entrada a la propiedad *InputRect* especificada.</span><span class="sxs-lookup"><span data-stu-id="d3039-108">Crops the input to the given *InputRect* property.</span></span>
2.  <span data-ttu-id="d3039-109">Traduce el origen del resultado a (0,0).</span><span class="sxs-lookup"><span data-stu-id="d3039-109">Translates the origin of the result to (0,0).</span></span>

> [!Note]  
> <span data-ttu-id="d3039-110">La propiedad *InputPaddingRect* solo debe ser mayor si y solo si los píxeles entre los dos rectángulos son negros transparentes en la entrada.</span><span class="sxs-lookup"><span data-stu-id="d3039-110">The *InputPaddingRect* property should only be larger if and only if the pixels between the two rectangles are transparent black on the input.</span></span> <span data-ttu-id="d3039-111">Esto puede dar lugar a que Direct2D ejecute el gráfico de forma más óptima.</span><span class="sxs-lookup"><span data-stu-id="d3039-111">This may result in Direct2D executing the graph more optimally.</span></span>

 

<span data-ttu-id="d3039-112">Este es un ejemplo del efecto.</span><span class="sxs-lookup"><span data-stu-id="d3039-112">Here is an example of the effect.</span></span> <span data-ttu-id="d3039-113">Esta imagen es pequeña y sencilla con fines ilustrativos.</span><span class="sxs-lookup"><span data-stu-id="d3039-113">This image is small and simple for illustration purposes.</span></span>

![imagen de entrada.](images/atlas.png)

<span data-ttu-id="d3039-115">La imagen anterior es la entrada al efecto.</span><span class="sxs-lookup"><span data-stu-id="d3039-115">The preceding image is the input to the effect.</span></span> <span data-ttu-id="d3039-116">En el código siguiente se crea un efecto de Atlas, se establece la entrada, se establece el rectángulo de entrada y, a continuación, se dibuja la salida.</span><span class="sxs-lookup"><span data-stu-id="d3039-116">The code here creates an atlas effect, sets the input, sets the input rectangle, and then draws the output.</span></span>


```C++
ComPtr<ID2D1Effect> atlasEffect;

// Create the Atlas Effect.
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Atlas, &atlasEffect));

// Set the input.
atlasEffect->SetInputEffect(0, inputImage.Get());

// The images here are 150 x 150 pixels.
float size = 150.0f;

// Compensate for the padding between images.
float padding = 10.0f;

// The input rectangle.  150 x 150 pixels with 10 pixel padding
D2D1_Vector_4F inputRect = D2D1::Vector4F(size + (padding * 2), padding, size, size);

DX::ThrowIfFailed(atlasEffect->SetValue(D2D1_ATLAS_PROP_INPUT_RECT, inputRect));

// Draw the image
m_d2dContext->DrawImage(atlasEffect.Get());
```



<span data-ttu-id="d3039-117">El código anterior selecciona un rectángulo que está alrededor del segundo triángulo.</span><span class="sxs-lookup"><span data-stu-id="d3039-117">The preceding code selects a rectangle that is around the second triangle.</span></span> <span data-ttu-id="d3039-118">Se omite el relleno alrededor de él.</span><span class="sxs-lookup"><span data-stu-id="d3039-118">The padding around it is ignored.</span></span> <span data-ttu-id="d3039-119">Esta es la imagen resultante.</span><span class="sxs-lookup"><span data-stu-id="d3039-119">Here is the resulting image.</span></span>

![imagen de salida.](images/atlas2.png)

> [!Note]  
> <span data-ttu-id="d3039-121">Se trata de una situación en la que puede optar por especificar un *InputPaddingRect* porque el relleno es negro transparente.</span><span class="sxs-lookup"><span data-stu-id="d3039-121">This is a situation where you may choose to specify a *InputPaddingRect* because the padding is transparent black.</span></span> <span data-ttu-id="d3039-122">El rectángulo sería `D2D1::Vector4F(size + (padding * 2), 0, size + padding, size + padding);` .</span><span class="sxs-lookup"><span data-stu-id="d3039-122">The rectangle would be `D2D1::Vector4F(size + (padding * 2), 0, size + padding, size + padding);`.</span></span>

 

## <a name="effect-properties"></a><span data-ttu-id="d3039-123">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="d3039-123">Effect properties</span></span>



| <span data-ttu-id="d3039-124">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="d3039-124">Display name and index enumeration</span></span>                                             | <span data-ttu-id="d3039-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3039-125">Description</span></span>                                                                                                                                                                  |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3039-126">InputRect</span><span class="sxs-lookup"><span data-stu-id="d3039-126">InputRect</span></span><br/> <span data-ttu-id="d3039-127">D2D1 \_ \_ Rect de \_ entrada de Atlas \_ de la</span><span class="sxs-lookup"><span data-stu-id="d3039-127">D2D1\_ATLAS\_PROP\_INPUT\_RECT</span></span><br/>                 | <span data-ttu-id="d3039-128">Parte de la imagen que se pasa al siguiente efecto.</span><span class="sxs-lookup"><span data-stu-id="d3039-128">The portion of the image passed to the next effect.</span></span><br/> <span data-ttu-id="d3039-129">El tipo es D2D1 \_ Vector \_ 4F.</span><span class="sxs-lookup"><span data-stu-id="d3039-129">Type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="d3039-130">El valor predeterminado es (-FLT \_ Max,-FLT \_ Max, FLT \_ Max, FLT \_ máx.).</span><span class="sxs-lookup"><span data-stu-id="d3039-130">Default value is (-FLT\_MAX, -FLT\_MAX, FLT\_MAX, FLT\_MAX).</span></span> <br/> |
| <span data-ttu-id="d3039-131">InputPaddingRect</span><span class="sxs-lookup"><span data-stu-id="d3039-131">InputPaddingRect</span></span><br/> <span data-ttu-id="d3039-132">\_Rect de \_ \_ relleno de \_ entrada \_ de D2D1 Atlas</span><span class="sxs-lookup"><span data-stu-id="d3039-132">D2D1\_ATLAS\_PROP\_INPUT\_PADDING\_RECT</span></span><br/> | <span data-ttu-id="d3039-133">Tamaño máximo muestreado para el rectángulo de salida.</span><span class="sxs-lookup"><span data-stu-id="d3039-133">The maximum size sampled for the output rectangle.</span></span><br/> <span data-ttu-id="d3039-134">El tipo es D2D1 \_ Vector \_ 4F.</span><span class="sxs-lookup"><span data-stu-id="d3039-134">Type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="d3039-135">El valor predeterminado es (-FLT \_ Max,-FLT \_ Max, FLT \_ Max, FLT \_ máx.).</span><span class="sxs-lookup"><span data-stu-id="d3039-135">Default value is (-FLT\_MAX, -FLT\_MAX, FLT\_MAX, FLT\_MAX).</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="d3039-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3039-136">Requirements</span></span>



| <span data-ttu-id="d3039-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3039-137">Requirement</span></span> | <span data-ttu-id="d3039-138">Value</span><span class="sxs-lookup"><span data-stu-id="d3039-138">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d3039-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3039-139">Minimum supported client</span></span> | <span data-ttu-id="d3039-140">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="d3039-140">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d3039-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3039-141">Minimum supported server</span></span> | <span data-ttu-id="d3039-142">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="d3039-142">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d3039-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d3039-143">Header</span></span>                   | <span data-ttu-id="d3039-144">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="d3039-144">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="d3039-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d3039-145">Library</span></span>                  | <span data-ttu-id="d3039-146">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="d3039-146">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="d3039-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d3039-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3039-148">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="d3039-148">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

