---
title: Luminancia a efecto alfa
description: Use la luminancia para el efecto alfa para establecer el canal alfa en la luminancia de la imagen y establezca los canales de color en 0.
ms.assetid: B380DE5A-C097-47E0-8E0F-E3C9D2BA44B0
keywords:
- luminancia a efecto alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb4c6fb78a1d49498b2adab6716d41e93d30deb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104558401"
---
# <a name="luminance-to-alpha-effect"></a><span data-ttu-id="fdb03-104">Luminancia a efecto alfa</span><span class="sxs-lookup"><span data-stu-id="fdb03-104">Luminance to alpha effect</span></span>

<span data-ttu-id="fdb03-105">Use la luminancia para el efecto alfa para establecer el canal alfa en la luminancia de la imagen y establezca los canales de color en 0.</span><span class="sxs-lookup"><span data-stu-id="fdb03-105">Use the luminance to alpha effect to set the alpha channel to the luminance of the image and sets the color channels to 0.</span></span> <span data-ttu-id="fdb03-106">Puede usar la salida de este efecto para crear una superposición semitransparente basada en el brillo de la imagen de entrada.</span><span class="sxs-lookup"><span data-stu-id="fdb03-106">You can use the output of this effect to make a semitransparent overlay based on the brightness of the input image.</span></span> <span data-ttu-id="fdb03-107">También puede utilizarlo para crear una máscara de imagen.</span><span class="sxs-lookup"><span data-stu-id="fdb03-107">Or you can use it to make an image mask.</span></span>

> [!Note]  
> <span data-ttu-id="fdb03-108">Este efecto no tiene propiedades.</span><span class="sxs-lookup"><span data-stu-id="fdb03-108">This effect has no properties.</span></span>

 

<span data-ttu-id="fdb03-109">El CLSID para este efecto es CLSID \_ D2D1LuminanceToAlpha.</span><span class="sxs-lookup"><span data-stu-id="fdb03-109">The CLSID for this effect is CLSID\_D2D1LuminanceToAlpha.</span></span>

## <a name="example-image"></a><span data-ttu-id="fdb03-110">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="fdb03-110">Example image</span></span>

<span data-ttu-id="fdb03-111">En este ejemplo se muestra la salida de la luminancia al efecto alfa compuesto sobre una superficie blanca para mostrar la opacidad.</span><span class="sxs-lookup"><span data-stu-id="fdb03-111">This example shows the output of the luminance to alpha effect composited over a white surface to show opacity.</span></span>



| <span data-ttu-id="fdb03-112">Antes</span><span class="sxs-lookup"><span data-stu-id="fdb03-112">Before</span></span>                                                            |
|-------------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg)        |
| <span data-ttu-id="fdb03-114">Después</span><span class="sxs-lookup"><span data-stu-id="fdb03-114">After</span></span>                                                             |
| ![la imagen después de la transformación.](images/18-luminancetoalpha.png) |



 


```C++
ComPtr<ID2D1Effect> luminanceToAlphaEffect;
m_d2dContext->CreateEffect(CLSID_D2D1LuminanceToAlpha, &luminanceToAlphaEffect);

luminanceToAlphaEffect->SetInput(0, bitmap);

// LuminanceToAlpha result is composited on top of a white surface to show opacity.
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);
floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(1.0f, 1.0f, 1.0f, 1.0f));

ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInputEffect(0, floodEffect.Get());
compositeEffect->SetInputEffect(1, luminanceToAlphaEffect.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="fdb03-116">Este efecto establece el canal alfa de la salida en la luminancia de la imagen de entrada mediante esta matriz de colores.</span><span class="sxs-lookup"><span data-stu-id="fdb03-116">This effect sets the alpha channel of the output to the luminance of the input image using this color matrix.</span></span>

![matriz de colores que el efecto utiliza para establecer el canal alfa.](images/luminance-to-alpha-math1.png)

<span data-ttu-id="fdb03-118">Este efecto consume y genera imágenes alfa premultiplicadas.</span><span class="sxs-lookup"><span data-stu-id="fdb03-118">This effect consumes and outputs premultiplied alpha images.</span></span> <span data-ttu-id="fdb03-119">El efecto no funcionará en imágenes alfa rectas a menos que sean totalmente opacas.</span><span class="sxs-lookup"><span data-stu-id="fdb03-119">The effect won't work on straight alpha images unless they are fully opaque.</span></span>

> [!Note]
>
> <span data-ttu-id="fdb03-120">Dado que las imágenes se almacenan en un formato compensado para la gamma, antes de calcular la luminancia de una imagen, primero debe realizar una corrección de gamma inversa para obtener los valores de color verdaderos de la imagen.</span><span class="sxs-lookup"><span data-stu-id="fdb03-120">Because images are stored in a gamma-compensated format, before you calculate the luminance for an image you should first perform inverse gamma correction to get the true color values for the image.</span></span> <span data-ttu-id="fdb03-121">Puesto que las imágenes se almacenan normalmente en gamma 2,2, puede usar el efecto de transferencia gamma con un exponente de (1/2.2) y, a continuación, utilizar la salida de ese efecto.</span><span class="sxs-lookup"><span data-stu-id="fdb03-121">Since images are normally stored at 2.2 gamma, you can use the Gamma transfer effect with an exponent of (1/2.2) and then use the output of that effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fdb03-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdb03-122">Requirements</span></span>



| <span data-ttu-id="fdb03-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdb03-123">Requirement</span></span> | <span data-ttu-id="fdb03-124">Value</span><span class="sxs-lookup"><span data-stu-id="fdb03-124">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fdb03-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fdb03-125">Minimum supported client</span></span> | <span data-ttu-id="fdb03-126">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="fdb03-126">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="fdb03-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fdb03-127">Minimum supported server</span></span> | <span data-ttu-id="fdb03-128">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="fdb03-128">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="fdb03-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fdb03-129">Header</span></span>                   | <span data-ttu-id="fdb03-130">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="fdb03-130">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="fdb03-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fdb03-131">Library</span></span>                  | <span data-ttu-id="fdb03-132">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="fdb03-132">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="output-bitmap"></a><span data-ttu-id="fdb03-133">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="fdb03-133">Output bitmap</span></span>

<span data-ttu-id="fdb03-134">La salida tiene el mismo tamaño que la imagen de entrada.</span><span class="sxs-lookup"><span data-stu-id="fdb03-134">The output is the same size as the input image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fdb03-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fdb03-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdb03-136">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="fdb03-136">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
