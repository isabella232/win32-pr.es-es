---
description: Direct3D usa una forma de filtrado de textura lineal denominada filtrado bilineal.
ms.assetid: vs|directx_sdk|~\linear_texture_filtering.htm
title: Filtrado de textura lineal (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7940bd693ec42ef4f48920a5a362fad5f5b0bf02
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537599"
---
# <a name="linear-texture-filtering-direct3d-9"></a><span data-ttu-id="079e2-103">Filtrado de textura lineal (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="079e2-103">Linear Texture Filtering (Direct3D 9)</span></span>

<span data-ttu-id="079e2-104">Direct3D usa una forma de filtrado de textura lineal denominada filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="079e2-104">Direct3D uses a form of linear texture filtering called bilinear filtering.</span></span> <span data-ttu-id="079e2-105">Al igual que [el muestreo de punto más cercano (Direct3D 9)](nearest-point-sampling.md), el filtrado de textura bilineal calcula primero una dirección textura, que normalmente no es una dirección entera.</span><span class="sxs-lookup"><span data-stu-id="079e2-105">Like [Nearest-Point Sampling (Direct3D 9)](nearest-point-sampling.md), bilinear texture filtering first computes a texel address, which is usually not an integer address.</span></span> <span data-ttu-id="079e2-106">A continuación, el filtrado bilineal busca el textura cuya dirección de entero está más cercana a la dirección calculada.</span><span class="sxs-lookup"><span data-stu-id="079e2-106">Bilinear filtering then finds the texel whose integer address is closest to the computed address.</span></span> <span data-ttu-id="079e2-107">Además, el módulo de representación de Direct3D calcula una media ponderada de los textura que están inmediatamente por encima, a la izquierda y a la derecha del punto de ejemplo más próximo.</span><span class="sxs-lookup"><span data-stu-id="079e2-107">In addition, the Direct3D rendering module computes a weighted average of the texels that are immediately above, below, to the left of, and to the right of the nearest sample point.</span></span>

<span data-ttu-id="079e2-108">Seleccione el filtrado de textura bilineal invocando el método [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) .</span><span class="sxs-lookup"><span data-stu-id="079e2-108">Select bilinear texture filtering by invoking the [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) method.</span></span> <span data-ttu-id="079e2-109">Establezca el valor del primer parámetro en el número de índice entero (0-7) de la textura para la que está seleccionando un método de filtrado de textura.</span><span class="sxs-lookup"><span data-stu-id="079e2-109">Set the value of the first parameter to the integer index number (0-7) of the texture for which you are selecting a texture filtering method.</span></span> <span data-ttu-id="079e2-110">Pase D3DSAMP \_ MAGFILTER, D3DSAMP \_ MINFILTER o D3DSAMP \_ MIPFILTER para el segundo parámetro con el fin de establecer el filtro de ampliación, minificación o mipmapping.</span><span class="sxs-lookup"><span data-stu-id="079e2-110">Pass D3DSAMP\_MAGFILTER, D3DSAMP\_MINFILTER, or D3DSAMP\_MIPFILTER for the second parameter to set the magnification, minification, or mipmapping filter.</span></span> <span data-ttu-id="079e2-111">Pase D3DTEXF \_ linear en el tercer parámetro.</span><span class="sxs-lookup"><span data-stu-id="079e2-111">Pass D3DTEXF\_LINEAR in the third parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="079e2-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="079e2-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="079e2-113">Filtrado de textura</span><span class="sxs-lookup"><span data-stu-id="079e2-113">Texture Filtering</span></span>](texture-filtering.md)
</dt> </dl>

 

 
