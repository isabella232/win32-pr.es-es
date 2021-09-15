---
description: Para determinar si Direct3D admite la interpolación de vértices, compruebe la marca TWEENING D3DVTXPCAPS en el miembro VertexProcessingCaps de la estructura \_ D3DCAPS9.
ms.assetid: b60c7f96-3752-4703-9059-486d9906c508
title: Usar interpolación de vértices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ca56cc521b5bff01a5d6af5c2d4ab6b02cd49e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580133"
---
# <a name="using-vertex-tweening-direct3d-9"></a>Usar interpolación de vértices (Direct3D 9)

Para determinar si Direct3D admite la interpolación de vértices, compruebe la marca TWEENING D3DVTXPCAPS en el miembro VertexProcessingCaps de la estructura \_ [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) En el ejemplo de código siguiente se usa el método [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) para determinar si se admite la interpolación.


```
// This example assumes that m_pD3DDevice is 
// a valid pointer to a IDirect3DDevice9 interface.
//
D3DCAPS9 d3dCaps;

m_pD3DDevice->GetDeviceCaps( &d3dCaps );
if( 0 != (d3dCaps.VertexProcessingCaps & D3DVTXPCAPS_TWEENING) )
    // Vertex tweening is supported.
```



Para usar la interpolación de vectores, primero debe configurar un tipo de vértice personalizado que use una segunda posición normal o una segunda. En el ejemplo de código siguiente se muestra una declaración de ejemplo que incluye un segundo punto y una segunda posición.


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



El siguiente paso consiste en establecer la declaración actual. En el ejemplo de código siguiente se muestra cómo hacerlo.


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



Para obtener más información sobre cómo crear un tipo de vértice personalizado y un búfer de vértices, vea Crear un búfer de [vértices (Direct3D 9).](creating-a-vertex-buffer.md)

> [!Note]  
> Cuando la interpolación de vértices está habilitada, debe haber una segunda posición o una segunda normal en la declaración actual.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interpolación de vértices](vertex-tweening.md)
</dt> </dl>

 

 
