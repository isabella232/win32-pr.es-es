---
title: Ejemplo de textura DDS
description: En el caso de una textura sin comprimir, use las marcas DDSD de \_ tono y DDPF \_ RGB; para una textura comprimida, use las \_ marcas DDSD LINEARSIZE y DDPF \_ FourCC.
ms.assetid: 5bf54e8d-1dc5-4782-96c1-132d258fb560
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbaa6f86dddc7e60d7f41fc34d7c9fe994d50e4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714184"
---
# <a name="dds-texture-example"></a><span data-ttu-id="570cf-103">Ejemplo de textura DDS</span><span class="sxs-lookup"><span data-stu-id="570cf-103">DDS Texture Example</span></span>

<span data-ttu-id="570cf-104">En el caso de una textura sin comprimir, use las marcas DDSD de \_ tono y DDPF \_ RGB; para una textura comprimida, use las \_ marcas DDSD LINEARSIZE y DDPF \_ FourCC.</span><span class="sxs-lookup"><span data-stu-id="570cf-104">For an uncompressed texture, use the DDSD\_PITCH and DDPF\_RGB flags; for a compressed texture, use the DDSD\_LINEARSIZE and DDPF\_FOURCC flags.</span></span> <span data-ttu-id="570cf-105">En el caso de una textura mipmapped, use las \_ marcas complejas DDSD MIPMAPCOUNT, DDSCAPS \_ y DDSCAPS también, así como \_ el miembro de número de MIPMAP.</span><span class="sxs-lookup"><span data-stu-id="570cf-105">For a mipmapped texture, use the DDSD\_MIPMAPCOUNT, DDSCAPS\_MIPMAP, and DDSCAPS\_COMPLEX flags also as well as the mipmap count member.</span></span> <span data-ttu-id="570cf-106">Si se generan los mapas MIP, normalmente se escriben todos los niveles por debajo de 1 por 1.</span><span class="sxs-lookup"><span data-stu-id="570cf-106">If mipmaps are generated, all levels down to 1-by-1 are usually written.</span></span>

<span data-ttu-id="570cf-107">En el caso de una textura comprimida, el tamaño de cada imagen de nivel de mipmap es normalmente un cuarto del tamaño de la anterior, con un mínimo de 8 (DXT1) o 16 (DXT2-5) bytes (para las texturas cuadradas).</span><span class="sxs-lookup"><span data-stu-id="570cf-107">For a compressed texture, the size of each mipmap level image is typically one-fourth the size of the previous, with a minimum of 8 (DXT1) or 16 (DXT2-5) bytes (for square textures).</span></span> <span data-ttu-id="570cf-108">Use la fórmula siguiente para calcular el tamaño de cada nivel para una textura no cuadrada:</span><span class="sxs-lookup"><span data-stu-id="570cf-108">Use the following formula to calculate the size of each level for a non-square texture:</span></span>


```
max(1, ( (width + 3) / 4 ) ) x max(1, ( (height + 3) / 4 ) ) x 8(DXT1) or 16(DXT2-5)
```



<span data-ttu-id="570cf-109">En esta tabla se muestra la cantidad de espacio que ocupa cada capa para una textura R8G8B8 de 256 por 256, sin usar la compresión.</span><span class="sxs-lookup"><span data-stu-id="570cf-109">This table lists the amount of space taken up by each layer for a 256-by-256 R8G8B8 texture, without using compression.</span></span>



| <span data-ttu-id="570cf-110">Componentes DDS</span><span class="sxs-lookup"><span data-stu-id="570cf-110">DDS Components</span></span>          | <span data-ttu-id="570cf-111">\# Bytes</span><span class="sxs-lookup"><span data-stu-id="570cf-111">\# Bytes</span></span> |
|-------------------------|----------|
| <span data-ttu-id="570cf-112">header</span><span class="sxs-lookup"><span data-stu-id="570cf-112">header</span></span>                  | <span data-ttu-id="570cf-113">128</span><span class="sxs-lookup"><span data-stu-id="570cf-113">128</span></span>      |
| <span data-ttu-id="570cf-114">imagen principal de 256-por-256</span><span class="sxs-lookup"><span data-stu-id="570cf-114">256-by-256 main image</span></span>   | <span data-ttu-id="570cf-115">196608</span><span class="sxs-lookup"><span data-stu-id="570cf-115">196608</span></span>   |
| <span data-ttu-id="570cf-116">imagen de mipmap 128 por 128</span><span class="sxs-lookup"><span data-stu-id="570cf-116">128-by-128 mipmap image</span></span> | <span data-ttu-id="570cf-117">49152</span><span class="sxs-lookup"><span data-stu-id="570cf-117">49152</span></span>    |
| <span data-ttu-id="570cf-118">imagen de mipmap 64 por 64</span><span class="sxs-lookup"><span data-stu-id="570cf-118">64-by-64 mipmap image</span></span>   | <span data-ttu-id="570cf-119">12288</span><span class="sxs-lookup"><span data-stu-id="570cf-119">12288</span></span>    |
| <span data-ttu-id="570cf-120">imagen de mipmap 32 por 32</span><span class="sxs-lookup"><span data-stu-id="570cf-120">32-by-32 mipmap image</span></span>   | <span data-ttu-id="570cf-121">3072</span><span class="sxs-lookup"><span data-stu-id="570cf-121">3072</span></span>     |
| <span data-ttu-id="570cf-122">imagen de mipmap de 16 por 16</span><span class="sxs-lookup"><span data-stu-id="570cf-122">16-by-16 mipmap image</span></span>   | <span data-ttu-id="570cf-123">768</span><span class="sxs-lookup"><span data-stu-id="570cf-123">768</span></span>      |
| <span data-ttu-id="570cf-124">imagen de mipmap de 8 por 8</span><span class="sxs-lookup"><span data-stu-id="570cf-124">8-by-8 mipmap image</span></span>     | <span data-ttu-id="570cf-125">192</span><span class="sxs-lookup"><span data-stu-id="570cf-125">192</span></span>      |
| <span data-ttu-id="570cf-126">imagen de mipmap de 4 por 4</span><span class="sxs-lookup"><span data-stu-id="570cf-126">4-by-4 mipmap image</span></span>     | <span data-ttu-id="570cf-127">48</span><span class="sxs-lookup"><span data-stu-id="570cf-127">48</span></span>       |
| <span data-ttu-id="570cf-128">imagen de mipmap 2 por 2</span><span class="sxs-lookup"><span data-stu-id="570cf-128">2-by-2 mipmap image</span></span>     | <span data-ttu-id="570cf-129">12</span><span class="sxs-lookup"><span data-stu-id="570cf-129">12</span></span>       |
| <span data-ttu-id="570cf-130">imagen de mipmap 1 por 1</span><span class="sxs-lookup"><span data-stu-id="570cf-130">1-by-1 mipmap image</span></span>     | <span data-ttu-id="570cf-131">3</span><span class="sxs-lookup"><span data-stu-id="570cf-131">3</span></span>        |



 

<span data-ttu-id="570cf-132">En esta tabla se muestra la cantidad de espacio que ocupa cada capa de la misma textura mediante compresión (DXT1).</span><span class="sxs-lookup"><span data-stu-id="570cf-132">This table lists the amount of space taken up by each layer for the same texture using compression (DXT1).</span></span>



| <span data-ttu-id="570cf-133">Componentes DDS</span><span class="sxs-lookup"><span data-stu-id="570cf-133">DDS Components</span></span>         | <span data-ttu-id="570cf-134">\# Bytes</span><span class="sxs-lookup"><span data-stu-id="570cf-134">\# Bytes</span></span> |
|------------------------|----------|
| <span data-ttu-id="570cf-135">header</span><span class="sxs-lookup"><span data-stu-id="570cf-135">header</span></span>                 | <span data-ttu-id="570cf-136">128</span><span class="sxs-lookup"><span data-stu-id="570cf-136">128</span></span>      |
| <span data-ttu-id="570cf-137">imagen principal de 256-por-64</span><span class="sxs-lookup"><span data-stu-id="570cf-137">256-by-64 main image</span></span>   | <span data-ttu-id="570cf-138">8192</span><span class="sxs-lookup"><span data-stu-id="570cf-138">8192</span></span>     |
| <span data-ttu-id="570cf-139">imagen de mipmap 128 por 32</span><span class="sxs-lookup"><span data-stu-id="570cf-139">128-by-32 mipmap image</span></span> | <span data-ttu-id="570cf-140">2048</span><span class="sxs-lookup"><span data-stu-id="570cf-140">2048</span></span>     |
| <span data-ttu-id="570cf-141">imagen de mipmap 64 por 16</span><span class="sxs-lookup"><span data-stu-id="570cf-141">64-by-16 mipmap image</span></span>  | <span data-ttu-id="570cf-142">512</span><span class="sxs-lookup"><span data-stu-id="570cf-142">512</span></span>      |
| <span data-ttu-id="570cf-143">imagen de mipmap 32 por 8</span><span class="sxs-lookup"><span data-stu-id="570cf-143">32-by-8 mipmap image</span></span>   | <span data-ttu-id="570cf-144">128</span><span class="sxs-lookup"><span data-stu-id="570cf-144">128</span></span>      |
| <span data-ttu-id="570cf-145">imagen de mipmap de 16 por 4</span><span class="sxs-lookup"><span data-stu-id="570cf-145">16-by-4 mipmap image</span></span>   | <span data-ttu-id="570cf-146">32</span><span class="sxs-lookup"><span data-stu-id="570cf-146">32</span></span>       |
| <span data-ttu-id="570cf-147">imagen de mipmap de 8 por 2</span><span class="sxs-lookup"><span data-stu-id="570cf-147">8-by-2 mipmap image</span></span>    | <span data-ttu-id="570cf-148">16</span><span class="sxs-lookup"><span data-stu-id="570cf-148">16</span></span>       |
| <span data-ttu-id="570cf-149">imagen de mipmap de 4 por 1</span><span class="sxs-lookup"><span data-stu-id="570cf-149">4-by-1 mipmap image</span></span>    | <span data-ttu-id="570cf-150">8</span><span class="sxs-lookup"><span data-stu-id="570cf-150">8</span></span>        |
| <span data-ttu-id="570cf-151">imagen de mipmap 2 por 1</span><span class="sxs-lookup"><span data-stu-id="570cf-151">2-by-1 mipmap image</span></span>    | <span data-ttu-id="570cf-152">8</span><span class="sxs-lookup"><span data-stu-id="570cf-152">8</span></span>        |
| <span data-ttu-id="570cf-153">imagen de mipmap 1 por 1</span><span class="sxs-lookup"><span data-stu-id="570cf-153">1-by-1 mipmap image</span></span>    | <span data-ttu-id="570cf-154">8</span><span class="sxs-lookup"><span data-stu-id="570cf-154">8</span></span>        |



 

<span data-ttu-id="570cf-155">En esta tabla se muestra la cantidad de espacio que ocupa cada capa de la misma textura con un formato de compresión de DXGI (en este caso BC3 \_ UNORM) que, por lo tanto, requiere el encabezado extendido:</span><span class="sxs-lookup"><span data-stu-id="570cf-155">This table lists the amount of space taken up by each layer for the same texture using a DXGI compression format (in this case BC3\_UNORM) that therefore requires the extended header:</span></span>



| <span data-ttu-id="570cf-156">Componentes DDS</span><span class="sxs-lookup"><span data-stu-id="570cf-156">DDS Components</span></span>                                                | <span data-ttu-id="570cf-157">\# Bytes</span><span class="sxs-lookup"><span data-stu-id="570cf-157">\# Bytes</span></span> |
|---------------------------------------------------------------|----------|
| <span data-ttu-id="570cf-158">header (FourCC establecido en "contenido DX10")</span><span class="sxs-lookup"><span data-stu-id="570cf-158">header (FourCC set to "DX10")</span></span>                                 | <span data-ttu-id="570cf-159">128</span><span class="sxs-lookup"><span data-stu-id="570cf-159">128</span></span>      |
| <span data-ttu-id="570cf-160">encabezado extendido (formato de DXGI establecido en \_ formato de dxgi \_ BC3 \_ UNORM)</span><span class="sxs-lookup"><span data-stu-id="570cf-160">extended header (DXGI format set to DXGI\_FORMAT\_BC3\_UNORM)</span></span> | <span data-ttu-id="570cf-161">20</span><span class="sxs-lookup"><span data-stu-id="570cf-161">20</span></span>       |
| <span data-ttu-id="570cf-162">imagen principal de 256-por-64</span><span class="sxs-lookup"><span data-stu-id="570cf-162">256-by-64 main image</span></span>                                          | <span data-ttu-id="570cf-163">16384</span><span class="sxs-lookup"><span data-stu-id="570cf-163">16384</span></span>    |
| <span data-ttu-id="570cf-164">imagen de mipmap 128 por 32</span><span class="sxs-lookup"><span data-stu-id="570cf-164">128-by-32 mipmap image</span></span>                                        | <span data-ttu-id="570cf-165">4096</span><span class="sxs-lookup"><span data-stu-id="570cf-165">4096</span></span>     |
| <span data-ttu-id="570cf-166">imagen de mipmap 64 por 16</span><span class="sxs-lookup"><span data-stu-id="570cf-166">64-by-16 mipmap image</span></span>                                         | <span data-ttu-id="570cf-167">1024</span><span class="sxs-lookup"><span data-stu-id="570cf-167">1024</span></span>     |
| <span data-ttu-id="570cf-168">imagen de mipmap 32 por 8</span><span class="sxs-lookup"><span data-stu-id="570cf-168">32-by-8 mipmap image</span></span>                                          | <span data-ttu-id="570cf-169">256</span><span class="sxs-lookup"><span data-stu-id="570cf-169">256</span></span>      |
| <span data-ttu-id="570cf-170">imagen de mipmap de 16 por 4</span><span class="sxs-lookup"><span data-stu-id="570cf-170">16-by-4 mipmap image</span></span>                                          | <span data-ttu-id="570cf-171">64</span><span class="sxs-lookup"><span data-stu-id="570cf-171">64</span></span>       |
| <span data-ttu-id="570cf-172">imagen de mipmap de 8 por 2</span><span class="sxs-lookup"><span data-stu-id="570cf-172">8-by-2 mipmap image</span></span>                                           | <span data-ttu-id="570cf-173">32</span><span class="sxs-lookup"><span data-stu-id="570cf-173">32</span></span>       |
| <span data-ttu-id="570cf-174">imagen de mipmap de 4 por 1</span><span class="sxs-lookup"><span data-stu-id="570cf-174">4-by-1 mipmap image</span></span>                                           | <span data-ttu-id="570cf-175">16</span><span class="sxs-lookup"><span data-stu-id="570cf-175">16</span></span>       |
| <span data-ttu-id="570cf-176">imagen de mipmap 2 por 1</span><span class="sxs-lookup"><span data-stu-id="570cf-176">2-by-1 mipmap image</span></span>                                           | <span data-ttu-id="570cf-177">16</span><span class="sxs-lookup"><span data-stu-id="570cf-177">16</span></span>       |
| <span data-ttu-id="570cf-178">imagen de mipmap 1 por 1</span><span class="sxs-lookup"><span data-stu-id="570cf-178">1-by-1 mipmap image</span></span>                                           | <span data-ttu-id="570cf-179">16</span><span class="sxs-lookup"><span data-stu-id="570cf-179">16</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="570cf-180">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="570cf-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="570cf-181">Guía de programación para DDS</span><span class="sxs-lookup"><span data-stu-id="570cf-181">Programming Guide for DDS</span></span>](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




