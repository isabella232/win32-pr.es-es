---
title: Efecto de mosaico
description: Use el efecto de mosaico para repetir la región especificada de la imagen.
ms.assetid: C7505DBF-5F79-4407-84C4-634EA7EC06B7
keywords:
- efecto de mosaico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5def48ab30cadb28673179f6eec5d7ffa7e19e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079452"
---
# <a name="tile-effect"></a><span data-ttu-id="9f726-104">Efecto de mosaico</span><span class="sxs-lookup"><span data-stu-id="9f726-104">Tile effect</span></span>

<span data-ttu-id="9f726-105">Use el efecto de mosaico para repetir la región especificada de la imagen.</span><span class="sxs-lookup"><span data-stu-id="9f726-105">Use the tile effect to repeat the specified region of the image.</span></span>

<span data-ttu-id="9f726-106">El CLSID para este efecto es CLSID \_ D2D1Tile.</span><span class="sxs-lookup"><span data-stu-id="9f726-106">The CLSID for this effect is CLSID\_D2D1Tile.</span></span>

## <a name="example-image"></a><span data-ttu-id="9f726-107">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="9f726-107">Example image</span></span>



| <span data-ttu-id="9f726-108">Antes</span><span class="sxs-lookup"><span data-stu-id="9f726-108">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg) |
| <span data-ttu-id="9f726-110">Después</span><span class="sxs-lookup"><span data-stu-id="9f726-110">After</span></span>                                                      |
| ![la imagen después de la transformación.](images/9-tile.png)       |



 


```C++
ComPtr<ID2D1Effect> tileEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Tile, &tileEffect);

tileEffect->SetInput(0, bitmap);

tileEffect->SetValue(D2D1_TILE_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tileEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="9f726-112">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="9f726-112">Effect properties</span></span>



| <span data-ttu-id="9f726-113">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="9f726-113">Display name and index enumeration</span></span>                | <span data-ttu-id="9f726-114">Tipo y valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="9f726-114">Type and default value</span></span>                                              | <span data-ttu-id="9f726-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f726-115">Description</span></span>                                                                                                                                        |
|---------------------------------------------------|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f726-116">Rect</span><span class="sxs-lookup"><span data-stu-id="9f726-116">Rect</span></span><br/> <span data-ttu-id="9f726-117">D2D1 \_ icono \_ prop \_ .</span><span class="sxs-lookup"><span data-stu-id="9f726-117">D2D1\_TILE\_PROP\_RECT</span></span><br/> | <span data-ttu-id="9f726-118">D2D1 \_ Vector \_ 4F</span><span class="sxs-lookup"><span data-stu-id="9f726-118">D2D1\_VECTOR\_4F</span></span><br/> <span data-ttu-id="9f726-119">{0.0 f, 0.0 f, 100,0 f, 100,0 f}</span><span class="sxs-lookup"><span data-stu-id="9f726-119">{0.0f, 0.0f, 100.0f, 100.0f}</span></span><br/> | <span data-ttu-id="9f726-120">Región de la imagen que se va a colocar en mosaico.</span><span class="sxs-lookup"><span data-stu-id="9f726-120">The region of the image to be tiled.</span></span> <span data-ttu-id="9f726-121">Esta propiedad es una \_ 4F de vector D2D1 \_ definida como: (izquierda, superior, derecha, inferior).</span><span class="sxs-lookup"><span data-stu-id="9f726-121">This property is a D2D1\_VECTOR\_4F defined as: (left, top, right, bottom).</span></span> <span data-ttu-id="9f726-122">Las unidades están en DIP.</span><span class="sxs-lookup"><span data-stu-id="9f726-122">The units are in DIPs.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="9f726-123">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="9f726-123">Output bitmap</span></span>

<span data-ttu-id="9f726-124">Este efecto genera un mapa de bits de tamaño lógico infinito.</span><span class="sxs-lookup"><span data-stu-id="9f726-124">This effect generates a logically infinite sized bitmap.</span></span>

<span data-ttu-id="9f726-125">Puede colocar una imagen en mosaico y generar un tamaño determinado sin efectos adicionales si establece el tamaño al llamar a [**ID2D1DeviceContext::D rawimage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)).</span><span class="sxs-lookup"><span data-stu-id="9f726-125">You can tile an image and output a certain size without any additional effects by setting the size when you call [**ID2D1DeviceContext::DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f726-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f726-126">Requirements</span></span>



| <span data-ttu-id="9f726-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f726-127">Requirement</span></span> | <span data-ttu-id="9f726-128">Value</span><span class="sxs-lookup"><span data-stu-id="9f726-128">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9f726-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f726-129">Minimum supported client</span></span> | <span data-ttu-id="9f726-130">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="9f726-130">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="9f726-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f726-131">Minimum supported server</span></span> | <span data-ttu-id="9f726-132">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="9f726-132">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="9f726-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f726-133">Header</span></span>                   | <span data-ttu-id="9f726-134">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="9f726-134">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="9f726-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9f726-135">Library</span></span>                  | <span data-ttu-id="9f726-136">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="9f726-136">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="9f726-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9f726-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f726-138">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="9f726-138">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

