---
description: Para determinar si Direct3D admite la interpolación de vértices, Compruebe la \_ marca de intercalación D3DVTXPCAPS en el miembro VertexProcessingCaps de la estructura D3DCAPS9.
ms.assetid: b60c7f96-3752-4703-9059-486d9906c508
title: Usar la interpolación de vértices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ca56cc521b5bff01a5d6af5c2d4ab6b02cd49e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906541"
---
# <a name="using-vertex-tweening-direct3d-9"></a><span data-ttu-id="42fbf-103">Usar la interpolación de vértices (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="42fbf-103">Using Vertex Tweening (Direct3D 9)</span></span>

<span data-ttu-id="42fbf-104">Para determinar si Direct3D admite la interpolación de vértices, Compruebe la \_ marca de intercalación D3DVTXPCAPS en el miembro VertexProcessingCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .</span><span class="sxs-lookup"><span data-stu-id="42fbf-104">To determine if Direct3D supports vertex tweening, check for the D3DVTXPCAPS\_TWEENING flag in the VertexProcessingCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span> <span data-ttu-id="42fbf-105">En el ejemplo de código siguiente se usa el método [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) para determinar si se admite la intercalación.</span><span class="sxs-lookup"><span data-stu-id="42fbf-105">The following code example uses the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method to determine if tweening is supported.</span></span>


```
// This example assumes that m_pD3DDevice is 
// a valid pointer to a IDirect3DDevice9 interface.
//
D3DCAPS9 d3dCaps;

m_pD3DDevice->GetDeviceCaps( &d3dCaps );
if( 0 != (d3dCaps.VertexProcessingCaps & D3DVTXPCAPS_TWEENING) )
    // Vertex tweening is supported.
```



<span data-ttu-id="42fbf-106">Para usar la interpolación vectorial, primero debe configurar un tipo de vértice personalizado que use una segunda posición normal o una segunda.</span><span class="sxs-lookup"><span data-stu-id="42fbf-106">To use vector tweening, you must first set up a custom vertex type that uses a second normal or a second position.</span></span> <span data-ttu-id="42fbf-107">En el ejemplo de código siguiente se muestra una declaración de ejemplo que incluye tanto un segundo punto como una segunda posición.</span><span class="sxs-lookup"><span data-stu-id="42fbf-107">The following code example shows a sample declaration that includes both a second point and a second position.</span></span>


```
struct TEX_VERTEX
{
    D3DVECTOR position;
    D3DVECTOR normal;
    D3DVECTOR position2;
    D3DVECTOR normal2;
};

//Create a vertex buffer with the type TEX_VERTEX.
```



<span data-ttu-id="42fbf-108">El siguiente paso consiste en establecer la declaración actual.</span><span class="sxs-lookup"><span data-stu-id="42fbf-108">The next step is to set the current declaration.</span></span> <span data-ttu-id="42fbf-109">En el ejemplo de código siguiente se muestra cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="42fbf-109">The code example below shows how to do this.</span></span>


```
// Create the shader declaration.
D3DVERTEXELEMENT9 decl[] = 
{
    { 0, 0,  D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
    { 0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0 },
    { 0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 1 },
    { 0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 1 },
    D3DDECL_END()
};
```



<span data-ttu-id="42fbf-110">Para obtener más información sobre cómo crear un tipo de vértice personalizado y un búfer de vértices, vea [crear un búfer de vértices (Direct3D 9)](creating-a-vertex-buffer.md).</span><span class="sxs-lookup"><span data-stu-id="42fbf-110">For more information about creating a custom vertex type and a vertex buffer, see [Creating a Vertex Buffer (Direct3D 9)](creating-a-vertex-buffer.md).</span></span>

> [!Note]  
> <span data-ttu-id="42fbf-111">Cuando la interpolación de vértices está habilitada, debe existir una segunda posición o una segunda normal en la declaración actual.</span><span class="sxs-lookup"><span data-stu-id="42fbf-111">When vertex tweening is enabled, a second position or a second normal must be present in the current declaration.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="42fbf-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="42fbf-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42fbf-113">Interpolación de vértices</span><span class="sxs-lookup"><span data-stu-id="42fbf-113">Vertex Tweening</span></span>](vertex-tweening.md)
</dt> </dl>

 

 
