---
description: Un mapa de rugosidad es un objeto IDirect3DTexture9 que usa un formato de píxel especializado.
ms.assetid: 7f405cb9-9512-44da-8a85-4b7d22017284
title: Formatos de píxeles de mapa de rugosidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21bbe4a9999d875e43d33389f86b35d22c81b3bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080261"
---
# <a name="bump-map-pixel-formats-direct3d-9"></a><span data-ttu-id="4897a-103">Formatos de píxeles de mapa de rugosidad (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4897a-103">Bump Map Pixel Formats (Direct3D 9)</span></span>

<span data-ttu-id="4897a-104">Un mapa de rugosidad es un objeto [**IDirect3DTexture9**](/windows/desktop/api) que usa un formato de píxel especializado.</span><span class="sxs-lookup"><span data-stu-id="4897a-104">A bump map is an [**IDirect3DTexture9**](/windows/desktop/api) object that uses a specialized pixel format.</span></span> <span data-ttu-id="4897a-105">En lugar de almacenar los componentes de color rojo, verde y azul, cada píxel de un mapa de rugosidad almacena los valores Delta para usted y v (D<sub>U</sub> y d<sub>v</sub>) y, en ocasiones, un componente de luminancia, L. Estos valores son aplicados por el sistema tal y como se describe en el tema [fórmulas de asignación de rugosidad (Direct3D 9)](bump-mapping-formulas.md) .</span><span class="sxs-lookup"><span data-stu-id="4897a-105">Rather than storing red, green, and blue color components, each pixel in a bump map stores the delta values for u and v (D<sub>U</sub> and D<sub>V</sub>) and sometimes a luminance component, L. These values are applied by the system as described in the [Bump Mapping Formulas (Direct3D 9)](bump-mapping-formulas.md) topic.</span></span>

<span data-ttu-id="4897a-106">Puede especificar un formato de píxel de mapa de rugosidad estableciendo el formato en uno de los siguientes: D3DFMT \_ CxV8U8, D3DFMT \_ V8U8, D3DFMT \_ L6V5U5, D3DFMT \_ X8L8V8U8, D3DFMT \_ Q8W8V8U8 o D3DFMT \_ V16U16.</span><span class="sxs-lookup"><span data-stu-id="4897a-106">You can specify a bump map pixel format by setting the format to one of the following: D3DFMT\_CxV8U8, D3DFMT\_V8U8, D3DFMT\_L6V5U5, D3DFMT\_X8L8V8U8, D3DFMT\_Q8W8V8U8, or D3DFMT\_V16U16.</span></span> <span data-ttu-id="4897a-107">Para obtener descripciones, vea [D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="4897a-107">For descriptions, see [D3DFORMAT](d3dformat.md).</span></span>

<span data-ttu-id="4897a-108">Los componentes D<sub>U</sub> y d<sub>V</sub> de un píxel son valores con signo comprendidos entre-1,0 y + 1,0.</span><span class="sxs-lookup"><span data-stu-id="4897a-108">The D<sub>U</sub> and D<sub>V</sub> components of a pixel are signed values that range from - 1.0 to +1.0.</span></span> <span data-ttu-id="4897a-109">El componente de luminancia, cuando se utiliza, es un valor entero sin signo que va de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="4897a-109">The luminance component, when used, is an unsigned integer value that ranges from 0 to 255.</span></span>

> [!Note]  
> <span data-ttu-id="4897a-110">Antes de seleccionar un formato de píxel de mapa de rugosidad, compruebe si se admite el formato determinado.</span><span class="sxs-lookup"><span data-stu-id="4897a-110">Before picking a bump map pixel format, check if the particular format is supported.</span></span> <span data-ttu-id="4897a-111">Para obtener más información, vea [usar la asignación de rugosidad (Direct3D 9)](using-bump-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="4897a-111">For more information, see [Using Bump Mapping (Direct3D 9)](using-bump-mapping.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4897a-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4897a-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4897a-113">Asignación de rugosidad</span><span class="sxs-lookup"><span data-stu-id="4897a-113">Bump Mapping</span></span>](bump-mapping.md)
</dt> </dl>

 

 



