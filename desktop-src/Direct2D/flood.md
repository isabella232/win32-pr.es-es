---
title: Efecto de saturación
description: Utilice el efecto de saturación para generar un mapa de bits basado en el color y el valor alfa especificados. Puede usar este efecto si desea un color específico como entrada para un efecto, como un color de fondo.
ms.assetid: F80A6DC0-E18C-4324-BE4A-FE40C5722988
keywords:
- efecto de saturación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92d34a41c0913a0d250fc24467b37b0d347b4ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996775"
---
# <a name="flood-effect"></a><span data-ttu-id="8ebf0-105">Efecto de saturación</span><span class="sxs-lookup"><span data-stu-id="8ebf0-105">Flood effect</span></span>

<span data-ttu-id="8ebf0-106">Utilice el efecto de saturación para generar un mapa de bits basado en el color y el valor alfa especificados.</span><span class="sxs-lookup"><span data-stu-id="8ebf0-106">Use the flood effect to generate a bitmap based on the specified color and alpha value.</span></span> <span data-ttu-id="8ebf0-107">Puede usar este efecto si desea un color específico como entrada para un efecto, como un color de fondo.</span><span class="sxs-lookup"><span data-stu-id="8ebf0-107">You can use this effect when you want a specific color as an input for an effect, like a background color.</span></span>

> [!Note]  
> <span data-ttu-id="8ebf0-108">El efecto pasa a lo largo del valor de color especificado según lo especificado.</span><span class="sxs-lookup"><span data-stu-id="8ebf0-108">The effect passes along the specified color value as specified.</span></span> <span data-ttu-id="8ebf0-109">Debe multiplicar manualmente los valores si planea pasar el resultado a efectos que esperan una entrada previamente multiplicada.</span><span class="sxs-lookup"><span data-stu-id="8ebf0-109">You must manually pre-multiply the values if you plan to pass the output to effects that expect a pre-multiplied input.</span></span>

 

<span data-ttu-id="8ebf0-110">El CLSID para este efecto es CLSID \_ D2D1Flood.</span><span class="sxs-lookup"><span data-stu-id="8ebf0-110">The CLSID for this effect is CLSID\_D2D1Flood.</span></span>

<span data-ttu-id="8ebf0-111">El efecto de saturación no tiene ninguna imagen de entrada.</span><span class="sxs-lookup"><span data-stu-id="8ebf0-111">The flood effect has no input image.</span></span>

-   [<span data-ttu-id="8ebf0-112">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="8ebf0-112">Example image</span></span>](#example-image)
-   [<span data-ttu-id="8ebf0-113">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="8ebf0-113">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="8ebf0-114">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="8ebf0-114">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="8ebf0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ebf0-115">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="8ebf0-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8ebf0-116">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="8ebf0-117">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="8ebf0-117">Example image</span></span>

![imagen de ejemplo del efecto de saturación que presenta el color verde.](images/20-flood.png)


```C++
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(0.0f, 1.0f, 0.0f, 1.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(floodEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="8ebf0-119">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="8ebf0-119">Effect properties</span></span>



| <span data-ttu-id="8ebf0-120">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="8ebf0-120">Display name and index enumeration</span></span>                   | <span data-ttu-id="8ebf0-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ebf0-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ebf0-122">Color</span><span class="sxs-lookup"><span data-stu-id="8ebf0-122">Color</span></span><br/> <span data-ttu-id="8ebf0-123">COLOR de D2D1 \_ inundaciones \_ \_</span><span class="sxs-lookup"><span data-stu-id="8ebf0-123">D2D1\_FLOOD\_PROP\_COLOR</span></span><br/> | <span data-ttu-id="8ebf0-124">Color y opacidad del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="8ebf0-124">The color and opacity of the bitmap.</span></span> <span data-ttu-id="8ebf0-125">Esta propiedad es un D2D1 \_ Vector \_ 4F.</span><span class="sxs-lookup"><span data-stu-id="8ebf0-125">This property is a D2D1\_VECTOR\_4F.</span></span> <span data-ttu-id="8ebf0-126">Los valores individuales de cada canal son de tipo FLOAT, unbounded y sin unidades.</span><span class="sxs-lookup"><span data-stu-id="8ebf0-126">The individual values for each channel are of type FLOAT, unbounded and unitless.</span></span> <span data-ttu-id="8ebf0-127">El efecto no modifica los valores de los canales.</span><span class="sxs-lookup"><span data-stu-id="8ebf0-127">The effect doesn't modify the values for the channels.</span></span><br/> <span data-ttu-id="8ebf0-128">Los valores RGBA para cada canal oscilan entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="8ebf0-128">The RGBA values for each channel range from 0 to 1.</span></span><br/> <span data-ttu-id="8ebf0-129">El tipo es D2D1 \_ Vector \_ 4F.</span><span class="sxs-lookup"><span data-stu-id="8ebf0-129">The type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="8ebf0-130">El valor predeterminado es {0.0 f, 0.0 f, 0.0 f, 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="8ebf0-130">The default value is {0.0f, 0.0f, 0.0f, 1.0f}.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="8ebf0-131">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="8ebf0-131">Output bitmap</span></span>

<span data-ttu-id="8ebf0-132">Este efecto genera un mapa de bits de tamaño lógico infinito.</span><span class="sxs-lookup"><span data-stu-id="8ebf0-132">This effect generates a logically infinite sized bitmap.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ebf0-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ebf0-133">Requirements</span></span>



| <span data-ttu-id="8ebf0-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ebf0-134">Requirement</span></span> | <span data-ttu-id="8ebf0-135">Value</span><span class="sxs-lookup"><span data-stu-id="8ebf0-135">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8ebf0-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ebf0-136">Minimum supported client</span></span> | <span data-ttu-id="8ebf0-137">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="8ebf0-137">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="8ebf0-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ebf0-138">Minimum supported server</span></span> | <span data-ttu-id="8ebf0-139">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="8ebf0-139">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="8ebf0-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ebf0-140">Header</span></span>                   | <span data-ttu-id="8ebf0-141">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="8ebf0-141">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="8ebf0-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8ebf0-142">Library</span></span>                  | <span data-ttu-id="8ebf0-143">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="8ebf0-143">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="8ebf0-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8ebf0-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ebf0-145">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="8ebf0-145">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

