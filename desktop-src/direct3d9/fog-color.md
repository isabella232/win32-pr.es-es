---
description: El color de niebla para la niebla de píxeles y vértices se establece mediante el estado de representación de FOGCOLOR de D3DRS \_ . Los valores de estado de representación pueden ser cualquier color RGB, especificado como color RGBA. Se omite el componente alfa.
ms.assetid: 76366496-553d-4dbf-868d-d58b5377d36a
title: Color de niebla (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c9ae217a26ab38be5e3f232fb9dfcd4c2977f7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104079877"
---
# <a name="fog-color-direct3d-9"></a><span data-ttu-id="9e860-105">Color de niebla (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9e860-105">Fog Color (Direct3D 9)</span></span>

<span data-ttu-id="9e860-106">El color de niebla para la niebla de píxeles y vértices se establece mediante el estado de representación de FOGCOLOR de D3DRS \_ .</span><span class="sxs-lookup"><span data-stu-id="9e860-106">Fog color for both pixel and vertex fog is set through the D3DRS\_FOGCOLOR render state.</span></span> <span data-ttu-id="9e860-107">Los valores de estado de representación pueden ser cualquier color RGB, especificado como color RGBA.</span><span class="sxs-lookup"><span data-stu-id="9e860-107">The render state values can be any RGB color, specified as an RGBA color.</span></span> <span data-ttu-id="9e860-108">Se omite el componente alfa.</span><span class="sxs-lookup"><span data-stu-id="9e860-108">The alpha component is ignored.</span></span>

<span data-ttu-id="9e860-109">En el siguiente ejemplo de C++ se establece el color de niebla en blanco.</span><span class="sxs-lookup"><span data-stu-id="9e860-109">The following C++ example sets the fog color to white.</span></span>


```
/* For this example, the d3dDevice variable is
* a valid pointer to an IDirect3DDevice9 interface.
*/
HRESULT hr;
hr = d3dDevice->SetRenderState(
                    D3DRS_FOGCOLOR,
                    0x00FFFFFF); // Highest 8 bits are not used.
if(FAILED(hr))
    return hr;
```



<span data-ttu-id="9e860-110">La niebla se aplica de forma diferente en la canalización de función fija y en la canalización programable.</span><span class="sxs-lookup"><span data-stu-id="9e860-110">Fog is applied differently by the fixed function pipeline and the programmable pipeline.</span></span>

1.  <span data-ttu-id="9e860-111">Si el controlador admite D3DPMISCCAPS \_ FOGANDSPECULARALPHA:</span><span class="sxs-lookup"><span data-stu-id="9e860-111">If the driver supports D3DPMISCCAPS\_FOGANDSPECULARALPHA:</span></span>
    -   <span data-ttu-id="9e860-112">Si se usa la canalización de función fija y se \_ establece D3DRS FOGCOLOR, v1. w (en el sombreador de píxeles) es igual al valor establecido en Fog renderstate.</span><span class="sxs-lookup"><span data-stu-id="9e860-112">If the fixed function pipeline is used and D3DRS\_FOGCOLOR is set, v1.w (in the pixel shader) equals the value set in fog renderstate.</span></span>
    -   <span data-ttu-id="9e860-113">Si se usa la canalización programable, v1. w (en el sombreador de píxeles) es igual a 0, incluso si oD1. w se escribe explícitamente en un sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="9e860-113">If the programmable pipeline is used, then v1.w (in the pixel shader) equals 0, even if oD1.w is explicitly written in a vertex shader.</span></span>
2.  <span data-ttu-id="9e860-114">Si el controlador no es compatible con D3DPMISCCAPS \_ FOGANDSPECULARALPHA:</span><span class="sxs-lookup"><span data-stu-id="9e860-114">If the driver does NOT support D3DPMISCCAPS\_FOGANDSPECULARALPHA:</span></span>
    -   <span data-ttu-id="9e860-115">Si se usa la canalización de función fija y se \_ establece D3DRS FOGCOLOR, entonces v1. w (en el sombreador de píxeles) es igual al valor establecido en niebla renderstate.</span><span class="sxs-lookup"><span data-stu-id="9e860-115">If the fixed function pipeline is used and D3DRS\_FOGCOLOR is set, then v1.w (in the pixel shader) equals value set in fog renderstate.</span></span>
    -   <span data-ttu-id="9e860-116">Si oFog se escribe explícitamente en un sombreador de vértices, v1. w (en el sombreador de píxeles) es igual a oFog, fijado entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="9e860-116">If oFog is explicitly written in a vertex shader, v1.w (in the pixel shader) equals oFog, clamped between 0 and 1.</span></span>
    -   <span data-ttu-id="9e860-117">Si no se aplica ninguno de los dos casos anteriores, v1. w (en el sombreador de píxeles) es igual a 0, incluso si oD1. w se escribe explícitamente en un sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="9e860-117">If neither of the above two cases applies, v1.w (in the pixel shader) equals 0, even if oD1.w is explicitly written in a vertex shader.</span></span>

<span data-ttu-id="9e860-118">Para obtener más información, vea [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="9e860-118">For more information, see [D3DPMISCCAPS](d3dpmisccaps.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e860-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9e860-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e860-120">Tipos de niebla</span><span class="sxs-lookup"><span data-stu-id="9e860-120">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 



