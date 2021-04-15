---
description: Define un color de material básico que se puede aplicar a una malla completa o a las caras individuales de una malla. La potencia es el exponente especular del material.
ms.assetid: vs|directx_sdk|~\material.htm
title: Material
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54c13d201152350a8a61950bb609f73cbdb2a3aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494279"
---
# <a name="material"></a><span data-ttu-id="8013a-104">Material</span><span class="sxs-lookup"><span data-stu-id="8013a-104">Material</span></span>

<span data-ttu-id="8013a-105">Define un color de material básico que se puede aplicar a una malla completa o a las caras individuales de una malla.</span><span class="sxs-lookup"><span data-stu-id="8013a-105">Defines a basic material color that can be applied to either a complete mesh or a mesh's individual faces.</span></span> <span data-ttu-id="8013a-106">La potencia es el exponente especular del material.</span><span class="sxs-lookup"><span data-stu-id="8013a-106">The power is the specular exponent of the material.</span></span>

``` syntax
template Material
{
    < 3D82AB4D-62DA-11CF-AB39-0020AF71E433 >
    ColorRGBA faceColor;
    FLOAT power;
    ColorRGB specularColor;
    ColorRGB emissiveColor;
    [...]
} 
```

<span data-ttu-id="8013a-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="8013a-107">Where:</span></span>

-   <span data-ttu-id="8013a-108">color faceColor.</span><span class="sxs-lookup"><span data-stu-id="8013a-108">faceColor - Face color.</span></span> <span data-ttu-id="8013a-109">Una plantilla ColorRGBA.</span><span class="sxs-lookup"><span data-stu-id="8013a-109">A ColorRGBA template.</span></span> <span data-ttu-id="8013a-110">Vea [**ColorRGBA**](colorrgba.md).</span><span class="sxs-lookup"><span data-stu-id="8013a-110">See [**ColorRGBA**](colorrgba.md).</span></span>
-   <span data-ttu-id="8013a-111">exponente de color especular de material de energía.</span><span class="sxs-lookup"><span data-stu-id="8013a-111">power - Material specular color exponent.</span></span>
-   <span data-ttu-id="8013a-112">specularColor: color especular de material.</span><span class="sxs-lookup"><span data-stu-id="8013a-112">specularColor - Material specular color.</span></span> <span data-ttu-id="8013a-113">Una plantilla ColorRGB.</span><span class="sxs-lookup"><span data-stu-id="8013a-113">A ColorRGB template.</span></span> <span data-ttu-id="8013a-114">Vea [**ColorRGB**](colorrgb.md).</span><span class="sxs-lookup"><span data-stu-id="8013a-114">See [**ColorRGB**](colorrgb.md).</span></span>
-   <span data-ttu-id="8013a-115">emissiveColor: material emisor color.</span><span class="sxs-lookup"><span data-stu-id="8013a-115">emissiveColor - Material emissive color.</span></span> <span data-ttu-id="8013a-116">Una plantilla ColorRGB.</span><span class="sxs-lookup"><span data-stu-id="8013a-116">A ColorRGB template.</span></span> <span data-ttu-id="8013a-117">Vea [**ColorRGB**](colorrgb.md).</span><span class="sxs-lookup"><span data-stu-id="8013a-117">See [**ColorRGB**](colorrgb.md).</span></span>

> [!Note]  
> <span data-ttu-id="8013a-118">El color ambiente requiere un componente alfa.</span><span class="sxs-lookup"><span data-stu-id="8013a-118">The ambient color requires an alpha component.</span></span>

 

<span data-ttu-id="8013a-119">[**TextureFilename**](texturefilename.md) es un objeto de datos opcional.</span><span class="sxs-lookup"><span data-stu-id="8013a-119">[**TextureFilename**](texturefilename.md) is an optional data object.</span></span> <span data-ttu-id="8013a-120">Si este objeto no está presente, la superficie no tiene textura.</span><span class="sxs-lookup"><span data-stu-id="8013a-120">If this object is not present, the face is untextured.</span></span>

## <a name="see-also"></a><span data-ttu-id="8013a-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="8013a-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="8013a-122">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="8013a-122">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> </dl>

 

 



