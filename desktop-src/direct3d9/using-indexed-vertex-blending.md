---
description: Los estados de transformación 256-511 están reservados para almacenar hasta 256 matrices que se pueden indexar mediante índices de 8 bits.
ms.assetid: 4c15cfc5-afdf-48d4-8fd1-b10cbe596a1c
title: Uso de la combinación de vértices indexados (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120362e4a86081ff51aee9053d1526a9a08f014a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473235"
---
# <a name="using-indexed-vertex-blending-direct3d-9"></a>Uso de la combinación de vértices indexados (Direct3D 9)

Los estados de transformación 256-511 están reservados para almacenar hasta 256 matrices que se pueden indexar mediante índices de 8 bits. Use la macro [**D3DTS \_ WORLDMATRIX para**](d3dts-worldmatrix.md) asignar índices de 0 a 255 a los estados de transformación correspondientes. En el ejemplo de código siguiente se muestra cómo usar el método [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) para establecer la matriz en el número de estado de transformación 256 en una matriz de identidad.


```
D3DMATRIX matBlend1;
D3DXMatrixIdentity( &matBlend1 );
m_pD3DDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matBlend );
```



Para habilitar o deshabilitar la mezcla de vértices indexados, establezca el estado de representación \_ INDEXEDVERTEXBLENDENABLE de D3DRS en **TRUE.** Cuando el estado de representación está habilitado, debe pasar índices de matriz como DWORD empaquetados con cada vértice. Cuando este estado de representación está deshabilitado y la fusión de vértices está habilitada, equivale a tener los índices de matriz 0, 1, 2 y 3 en cada vértice. En el ejemplo de código siguiente se [**usa el método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) para habilitar la mezcla de vértices indexados.


```
m_pD3DDevice->SetRenderState( D3DRS_INDEXEDVERTEXBLENDENABLE, TRUE );
```



Para habilitar o deshabilitar la mezcla de vértices, establezca el estado de representación [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) en un valor distinto de D3DRS DISABLE del tipo enumerado \_ [**D3DVERTEXBLENDFLAGS.**](./d3dvertexblendflags.md) Si este estado de representación no se establece en D3DRS DISABLE, debe pasar el número necesario de \_ pesos para cada vértice. En el ejemplo de código siguiente se **usa IDirect3DDevice9::SetRenderState** para habilitar la mezcla de vértices con tres pesos para cada vértice.


```
m_pD3DDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_3WEIGHTS );
```



## <a name="determining-indexed-vertex-blending-support"></a>Determinar la compatibilidad con la mezcla de vértices indexados

Para determinar el tamaño máximo de la matriz de mezcla de vértices indexados, compruebe el miembro MaxVertexBlendMatrixIndex de la estructura [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) En el ejemplo de código siguiente se [**usa el método IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) para recuperar este tamaño.


```
D3DCAPS9 d3dCaps;
    
m_pD3DDevice->GetDeviceCaps( &d3dCaps );
IndexedMatrixMaxSize = d3dCaps.MaxVertexBlendMatrixIndex;
```



Si el valor establecido en MaxVertexBlendMatrixIndex es 0, el dispositivo no admite matrices indizadas.

> [!Note]  
> Cuando se usa el procesamiento de vértices de software, se pueden usar 256 matrices para la mezcla de vértices indexados, con o sin mezcla normal.

 

## <a name="passing-matrix-indices-to-direct3d"></a>Pasar índices de matriz a Direct3D

Los índices de matriz mundial se pueden pasar a Direct3D mediante sombreadores de vértices heredados (FVF) o declaraciones.

En el ejemplo de código siguiente se muestra cómo usar sombreadores de vértices heredados.


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
};
    
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZB2 | D3DFVF_LASTBETA_UBYTE4 |
                             D3DFVF_NORMAL);
```



Cuando se usa un sombreador de vértices heredado, los índices de matriz se pasan junto con posiciones de vértice mediante marcas \_ XYZBn D3DFVF. Los índices de matriz se pasan como bytes dentro de un DWORD y deben estar presentes inmediatamente después del último peso del vértice. Los pesos de vértice también se pasan mediante D3DFVF \_ XYZBn. Una DWORD empaquetada contiene index3, index2, index1 e index0, donde index0 se encuentra en el byte más bajo de DWORD. El número de índices de matriz mundial usados es igual al número pasado al número de matrices usadas para la mezcla, tal como se define en [**D3DRS \_ VERTEXBLEND**](./d3drenderstatetype.md).

Cuando se usa una declaración, D3DVSDE BLENDINDICES define el registro de vértices de entrada del que obtener \_ índices de matriz. Los índices de matriz se deben pasar como D3DVSDT \_ UBYTE4.

En el ejemplo de código siguiente se muestra cómo usar declaraciones. Tenga en cuenta que el orden de los componentes ya no es importante a menos que se use un sombreador de vértices de función fija.

Esta es la declaración de vértice.


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
}
```



Esta es la declaración de registro correspondiente.


```
// Create the shader declaration.
D3DVERTEXELEMENT9 decl[] = 
{
    { 0, 0,  D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
    { 0, 12, D3DDECLTYPE_FLOAT1, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BLENDWEIGHT, 0 },
    { 0, 16, D3DDECLTYPE_UBYTE4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BLENDINDICES, 0 },
    { 0, 20, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0 },
    D3DDECL_END()
};
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mezcla de vértices indexados](indexed-vertex-blending.md)
</dt> </dl>

 

 
