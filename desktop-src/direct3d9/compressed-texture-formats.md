---
description: Esta sección contiene información sobre la organización interna de formatos de textura comprimidos.
ms.assetid: a916d635-2be4-48be-ba70-a743b2969553
title: Formatos de textura comprimidos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcecf6e98d125f3a391ab0e7a7c569a8dbd27d0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807748"
---
# <a name="compressed-texture-formats-direct3d-9"></a><span data-ttu-id="a9bde-103">Formatos de textura comprimidos (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a9bde-103">Compressed Texture Formats (Direct3D 9)</span></span>

<span data-ttu-id="a9bde-104">Esta sección contiene información sobre la organización interna de formatos de textura comprimidos.</span><span class="sxs-lookup"><span data-stu-id="a9bde-104">This section contains information about the internal organization of compressed texture formats.</span></span> <span data-ttu-id="a9bde-105">No necesita estos detalles para usar texturas comprimidas, ya que puede usar las funciones de D3DX para la conversión a y desde formatos comprimidos.</span><span class="sxs-lookup"><span data-stu-id="a9bde-105">You do not need these details to use compressed textures, because you can use D3DX functions for conversion to and from compressed formats.</span></span> <span data-ttu-id="a9bde-106">Sin embargo, esta información resulta útil si desea trabajar directamente con datos de superficie comprimidos.</span><span class="sxs-lookup"><span data-stu-id="a9bde-106">However, this information is useful if you want to operate on compressed surface data directly.</span></span>

<span data-ttu-id="a9bde-107">Direct3D usa un formato de compresión que divide los mapas de textura en bloques textura 4x4.</span><span class="sxs-lookup"><span data-stu-id="a9bde-107">Direct3D uses a compression format that divides texture maps into 4x4 texel blocks.</span></span> <span data-ttu-id="a9bde-108">Si la textura no contiene transparencia (es opaca) o si la transparencia se especifica mediante un alfa de 1 bit, un bloque de 8 bytes representa el bloque de mapa de textura.</span><span class="sxs-lookup"><span data-stu-id="a9bde-108">If the texture contains no transparency - is opaque - or if the transparency is specified by a 1-bit alpha, an 8-byte block represents the texture map block.</span></span> <span data-ttu-id="a9bde-109">Si el mapa de textura contiene textura transparentes, mediante un canal alfa, un bloque de 16 bytes lo representa.</span><span class="sxs-lookup"><span data-stu-id="a9bde-109">If the texture map does contain transparent texels, using an alpha channel, a 16-byte block represents it.</span></span>

-   [<span data-ttu-id="a9bde-110">Texturas alfa opacas y de 1 bit (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a9bde-110">Opaque and 1-Bit Alpha Textures (Direct3D 9)</span></span>](opaque-and-1-bit-alpha-textures.md)
-   [<span data-ttu-id="a9bde-111">Texturas con canales alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a9bde-111">Textures with Alpha Channels (Direct3D 9)</span></span>](textures-with-alpha-channels.md)

<span data-ttu-id="a9bde-112">Cualquier textura única debe especificar que sus datos se almacenan como 64 o 128 bits por grupo de 16 textura.</span><span class="sxs-lookup"><span data-stu-id="a9bde-112">Any single texture must specify that its data is stored as 64 or 128 bits per group of 16 texels.</span></span> <span data-ttu-id="a9bde-113">Si los bloques de 64 bits, es decir, el formato DXT1, se usan para la textura, es posible mezclar los formatos alfa opacos y de 1 bit en cada bloque dentro de la misma textura.</span><span class="sxs-lookup"><span data-stu-id="a9bde-113">If 64-bit blocks - that is, format DXT1 - are used for the texture, it is possible to mix the opaque and 1-bit alpha formats on a per-block basis within the same texture.</span></span> <span data-ttu-id="a9bde-114">En otras palabras, la comparación de la magnitud de entero sin signo de color \_ 0 y el color \_ 1 se realiza de forma única para cada bloque de 16 textura.</span><span class="sxs-lookup"><span data-stu-id="a9bde-114">In other words, the comparison of the unsigned integer magnitude of color\_0 and color\_1 is performed uniquely for each block of 16 texels.</span></span>

<span data-ttu-id="a9bde-115">Cuando se usan bloques de 128 bits, el canal alfa debe especificarse en modo EXPLICIT (Format DXT2 o DXT3) o Interpolated (Format DXT4 o DXT5) para toda la textura.</span><span class="sxs-lookup"><span data-stu-id="a9bde-115">When 128-bit blocks are used, the alpha channel must be specified in either explicit (format DXT2 or DXT3) or interpolated mode (format DXT4 or DXT5) for the entire texture.</span></span> <span data-ttu-id="a9bde-116">Al igual que con el color, cuando se selecciona el modo interpolado, se pueden usar ocho alfa interpolados o el modo alfa interpolado bloque a bloque.</span><span class="sxs-lookup"><span data-stu-id="a9bde-116">As with color, when interpolated mode is selected, either eight interpolated alphas or six interpolated alphas mode can be used on a block-by-block basis.</span></span> <span data-ttu-id="a9bde-117">De nuevo, la comparación de la magnitud de alfa \_ 0 y alfa \_ 1 se realiza de forma exclusiva en bloque por bloque.</span><span class="sxs-lookup"><span data-stu-id="a9bde-117">Again the magnitude comparison of alpha\_0 and alpha\_1 is done uniquely on a block-by-block basis.</span></span>

<span data-ttu-id="a9bde-118">El paso de los formatos DXTn es diferente de lo que se devolvió en DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="a9bde-118">The pitch for DXTn formats is different from what was returned in DirectX 7.0.</span></span> <span data-ttu-id="a9bde-119">El paso se mide ahora en bytes (no en bloques).</span><span class="sxs-lookup"><span data-stu-id="a9bde-119">Pitch is now measured in bytes (not blocks).</span></span> <span data-ttu-id="a9bde-120">Por ejemplo, si tiene un ancho de 16, tendrá un paso de cuatro bloques (4 \* 8 para DXT1, 4 \* 16 para DXT2-5).</span><span class="sxs-lookup"><span data-stu-id="a9bde-120">For example, if you have a width of 16, then you will have a pitch of four blocks (4\*8 for DXT1, 4\*16 for DXT2-5).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9bde-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a9bde-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9bde-122">Recursos de textura comprimidos</span><span class="sxs-lookup"><span data-stu-id="a9bde-122">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 



