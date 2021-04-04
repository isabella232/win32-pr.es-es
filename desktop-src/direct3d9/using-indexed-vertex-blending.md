---
description: Los Estados de transformación 256-511 están reservados para almacenar hasta 256 matrices que se pueden indexar con índices de 8 bits.
ms.assetid: 4c15cfc5-afdf-48d4-8fd1-b10cbe596a1c
title: Usar la combinación de vértices indizada (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120362e4a86081ff51aee9053d1526a9a08f014a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906436"
---
# <a name="using-indexed-vertex-blending-direct3d-9"></a>Usar la combinación de vértices indizada (Direct3D 9)

Los Estados de transformación 256-511 están reservados para almacenar hasta 256 matrices que se pueden indexar con índices de 8 bits. Use la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) para asignar índices 0-255 a los Estados de transformación correspondientes. En el ejemplo de código siguiente se muestra cómo usar el método [**IDirect3DDevice9:: SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) para establecer la matriz en el estado de la transformación número 256 en una matriz de identidades.


```
D3DMATRIX matBlend1;
D3DXMatrixIdentity( &matBlend1 );
m_pD3DDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matBlend );
```



Para habilitar o deshabilitar la combinación de vértices indexados, establezca el estado de representación de D3DRS \_ INDEXEDVERTEXBLENDENABLE en **true**. Cuando el estado de representación es habilitado, debe pasar los índices de matriz como DWORDs empaquetadas con todos los vértices. Cuando este estado de representación está deshabilitado y la combinación de vértices está habilitada, equivale a tener los índices de matriz 0, 1, 2 y 3 en cada vértice. En el ejemplo de código siguiente se usa el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) para habilitar la combinación de vértices indizada.


```
m_pD3DDevice->SetRenderState( D3DRS_INDEXEDVERTEXBLENDENABLE, TRUE );
```



Para habilitar o deshabilitar la fusión de vértices, establezca el estado de representación [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) en un valor distinto de D3DRS \_ deshabilitar del tipo enumerado [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) . Si este estado de representación no se establece en D3DRS \_ disable, debe pasar el número necesario de pesos para cada vértice. En el ejemplo de código siguiente se usa **IDirect3DDevice9:: SetRenderState** para habilitar la fusión de vértices con tres pesos para cada vértice.


```
m_pD3DDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_3WEIGHTS );
```



## <a name="determining-indexed-vertex-blending-support"></a>Determinar la compatibilidad con la mezcla de vértices indizados

Para determinar el tamaño máximo de la matriz de mezcla de vértices indizados, compruebe el miembro MaxVertexBlendMatrixIndex de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) . En el ejemplo de código siguiente se usa el método [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) para recuperar este tamaño.


```
D3DCAPS9 d3dCaps;
    
m_pD3DDevice->GetDeviceCaps( &d3dCaps );
IndexedMatrixMaxSize = d3dCaps.MaxVertexBlendMatrixIndex;
```



Si el valor establecido en MaxVertexBlendMatrixIndex es 0, el dispositivo no admite matrices indizadas.

> [!Note]  
> Cuando se usa el procesamiento de vértices de software, se pueden usar 256 matrices para la combinación de vértices indexados, con o sin la combinación normal.

 

## <a name="passing-matrix-indices-to-direct3d"></a>Pasar índices de matriz a Direct3D

Los índices de matriz mundial se pueden pasar a Direct3D mediante sombreadores de vértices heredados, FVF o declaraciones.

En el ejemplo de código siguiente se muestra cómo usar los sombreadores de vértices heredados.


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



Cuando se usa un sombreador de vértices heredado, los índices de matriz se pasan junto con las posiciones de los vértices mediante \_ marcas D3DFVF XYZBn. Los índices de matriz se pasan como bytes dentro de un valor DWORD y deben estar presentes inmediatamente después del último peso del vértice. Los pesos de los vértices también se pasan mediante D3DFVF \_ XYZBn. Un valor DWORD empaquetado contiene index3, index2, index1 y index0, donde index0 se encuentra en el byte más bajo de la DWORD. El número de índices de matriz mundial usados es igual al número que se pasa al número de matrices usadas para la fusión, tal y como se define en [**D3DRS \_ VERTEXBLEND**](./d3drenderstatetype.md).

Cuando se usa una declaración, D3DVSDE \_ BLENDINDICES define el registro de vértices de entrada para obtener los índices de matriz. Los índices de matriz se deben pasar como D3DVSDT \_ UBYTE4.

En el ejemplo de código siguiente se muestra cómo usar las declaraciones. Tenga en cuenta que el orden de los componentes ya no es importante a menos que use un sombreador de vértices de función fija.

Esta es la declaración de vértices.


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

[Fusión de vértices indexados](indexed-vertex-blending.md)
</dt> </dl>

 

 
