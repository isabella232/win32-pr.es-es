---
title: Ejemplo de textura de volumen DDS
description: En el caso de una textura de volumen, utilice DDSCAPS \_ Complex, DDSCAPS2 \_ Volume, DDSD \_ Depth, flags y set y dwDepth. Una textura de volumen es una extensión de una textura estándar para Direct3D 9; una textura de volumen se puede definir con o sin mapas MIP.
ms.assetid: c1675a6d-129a-4e95-993f-e1be905781cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03d82faa8041f2b5c99ef57ee2386ff5de84d787
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714183"
---
# <a name="dds-volume-texture-example"></a><span data-ttu-id="ea22d-104">Ejemplo de textura de volumen DDS</span><span class="sxs-lookup"><span data-stu-id="ea22d-104">DDS Volume Texture Example</span></span>

<span data-ttu-id="ea22d-105">En el caso de una textura de volumen, utilice DDSCAPS \_ Complex, DDSCAPS2 \_ Volume, DDSD \_ Depth, flags y set y dwDepth.</span><span class="sxs-lookup"><span data-stu-id="ea22d-105">For a volume texture, use the DDSCAPS\_COMPLEX, DDSCAPS2\_VOLUME, DDSD\_DEPTH, flags and set and dwDepth.</span></span> <span data-ttu-id="ea22d-106">Una textura de volumen es una extensión de una textura estándar para Direct3D 9; una textura de volumen se puede definir con o sin mapas MIP.</span><span class="sxs-lookup"><span data-stu-id="ea22d-106">A volume texture is an extension of a standard texture for Direct3D 9; a volume texture is can be defined with or without mipmaps.</span></span>

<span data-ttu-id="ea22d-107">En el caso de los volúmenes sin mipmaps, cada segmento de profundidad se escribe en el archivo en orden.</span><span class="sxs-lookup"><span data-stu-id="ea22d-107">For volumes without mipmaps, each depth slice is written to the file in order.</span></span> <span data-ttu-id="ea22d-108">Si se incluyen los mapas MIP, todos los segmentos de profundidad de un nivel de mipmap determinado se escriben juntos, con cada nivel que contiene la mitad de los segmentos que el nivel anterior con un mínimo de 1.</span><span class="sxs-lookup"><span data-stu-id="ea22d-108">If mipmaps are included, all depth slices for a given mipmap level are written together, with each level containing half as many slices as the previous level with a minimum of 1.</span></span>

<span data-ttu-id="ea22d-109">Por ejemplo, un mapa de volumen 64 por 64 por 4 con un formato de píxel de R8G8B8 (3 bytes por píxel) con todos los niveles de mipmap contendrá lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ea22d-109">For example, a 64-by-64-by-4 volume map using a pixel format of R8G8B8 (3 bytes per pixel) with all mipmap levels would contain the following:</span></span>



| <span data-ttu-id="ea22d-110">Componentes DDS</span><span class="sxs-lookup"><span data-stu-id="ea22d-110">DDS Components</span></span>                      | <span data-ttu-id="ea22d-111">\# Bytes</span><span class="sxs-lookup"><span data-stu-id="ea22d-111">\# Bytes</span></span>    |
|-------------------------------------|-------------|
| <span data-ttu-id="ea22d-112">header</span><span class="sxs-lookup"><span data-stu-id="ea22d-112">header</span></span>                              | <span data-ttu-id="ea22d-113">128 bytes</span><span class="sxs-lookup"><span data-stu-id="ea22d-113">128 bytes</span></span>   |
| <span data-ttu-id="ea22d-114">64-por-64 segmento 1 de 4 imagen principal.</span><span class="sxs-lookup"><span data-stu-id="ea22d-114">64-by-64 slice 1 of 4 main image.</span></span>   | <span data-ttu-id="ea22d-115">12288 bytes</span><span class="sxs-lookup"><span data-stu-id="ea22d-115">12288 bytes</span></span> |
| <span data-ttu-id="ea22d-116">64-por-64 segmento 2 de 4 imagen principal.</span><span class="sxs-lookup"><span data-stu-id="ea22d-116">64-by-64 slice 2 of 4 main image.</span></span>   | <span data-ttu-id="ea22d-117">12288 bytes</span><span class="sxs-lookup"><span data-stu-id="ea22d-117">12288 bytes</span></span> |
| <span data-ttu-id="ea22d-118">64-por-64 segmento 3 de 4 imagen principal.</span><span class="sxs-lookup"><span data-stu-id="ea22d-118">64-by-64 slice 3 of 4 main image.</span></span>   | <span data-ttu-id="ea22d-119">12288 bytes</span><span class="sxs-lookup"><span data-stu-id="ea22d-119">12288 bytes</span></span> |
| <span data-ttu-id="ea22d-120">64-por-64 segmento 4 de 4 imagen principal.</span><span class="sxs-lookup"><span data-stu-id="ea22d-120">64-by-64 slice 4 of 4 main image.</span></span>   | <span data-ttu-id="ea22d-121">12288 bytes</span><span class="sxs-lookup"><span data-stu-id="ea22d-121">12288 bytes</span></span> |
| <span data-ttu-id="ea22d-122">32-por-32 segmento 1 de 2 imagen de mipmap.</span><span class="sxs-lookup"><span data-stu-id="ea22d-122">32-by-32 slice 1 of 2 mipmap image.</span></span> | <span data-ttu-id="ea22d-123">3072 bytes</span><span class="sxs-lookup"><span data-stu-id="ea22d-123">3072 bytes</span></span>  |
| <span data-ttu-id="ea22d-124">32-por-32 segmento 2 de 2 imágenes de mipmap.</span><span class="sxs-lookup"><span data-stu-id="ea22d-124">32-by-32 slice 2 of 2 mipmap image.</span></span> | <span data-ttu-id="ea22d-125">3072 bytes</span><span class="sxs-lookup"><span data-stu-id="ea22d-125">3072 bytes</span></span>  |
| <span data-ttu-id="ea22d-126">segmento 1 de 16 por 16 de 1 imagen de mipmap.</span><span class="sxs-lookup"><span data-stu-id="ea22d-126">16-by-16 slice 1 of 1 mipmap image.</span></span> | <span data-ttu-id="ea22d-127">768 bytes</span><span class="sxs-lookup"><span data-stu-id="ea22d-127">768 bytes</span></span>   |
| <span data-ttu-id="ea22d-128">8 por 8 segmento 1 de 1 imagen de mipmap.</span><span class="sxs-lookup"><span data-stu-id="ea22d-128">8-by-8 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="ea22d-129">192 bytes</span><span class="sxs-lookup"><span data-stu-id="ea22d-129">192 bytes</span></span>   |
| <span data-ttu-id="ea22d-130">4 por 4 segmento 1 de 1 imagen de mipmap.</span><span class="sxs-lookup"><span data-stu-id="ea22d-130">4-by-4 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="ea22d-131">48 bytes</span><span class="sxs-lookup"><span data-stu-id="ea22d-131">48 bytes</span></span>    |
| <span data-ttu-id="ea22d-132">2-por 2 segmento 1 de 1 imagen de mipmap.</span><span class="sxs-lookup"><span data-stu-id="ea22d-132">2-by-2 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="ea22d-133">12 bytes</span><span class="sxs-lookup"><span data-stu-id="ea22d-133">12 bytes</span></span>    |
| <span data-ttu-id="ea22d-134">1 por 1 segmento 1 de 1 imagen de mipmap.</span><span class="sxs-lookup"><span data-stu-id="ea22d-134">1-by-1 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="ea22d-135">3 bytes</span><span class="sxs-lookup"><span data-stu-id="ea22d-135">3 bytes</span></span>     |



 

<span data-ttu-id="ea22d-136">Tenga en cuenta que el nivel de mipmap más pequeño es solo 3 bytes porque el valor de bitCount es 24 y no hay ninguna compresión agregada en este nivel.</span><span class="sxs-lookup"><span data-stu-id="ea22d-136">Note that the smallest mipmap level is only 3 bytes because the bitcount is 24 and there is no added compression at this level.</span></span>

<span data-ttu-id="ea22d-137">Se ha agregado compatibilidad con las texturas de volumen en DirectX 8.</span><span class="sxs-lookup"><span data-stu-id="ea22d-137">Support for volume textures was added in DirectX 8.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea22d-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ea22d-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea22d-139">Guía de programación para DDS</span><span class="sxs-lookup"><span data-stu-id="ea22d-139">Programming Guide for DDS</span></span>](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




