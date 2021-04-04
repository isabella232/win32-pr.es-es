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
# <a name="using-indexed-vertex-blending-direct3d-9"></a><span data-ttu-id="d26fd-103">Usar la combinación de vértices indizada (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d26fd-103">Using Indexed Vertex Blending (Direct3D 9)</span></span>

<span data-ttu-id="d26fd-104">Los Estados de transformación 256-511 están reservados para almacenar hasta 256 matrices que se pueden indexar con índices de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="d26fd-104">Transform states 256-511 are reserved to store up to 256 matrices that can be indexed using 8-bit indices.</span></span> <span data-ttu-id="d26fd-105">Use la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) para asignar índices 0-255 a los Estados de transformación correspondientes.</span><span class="sxs-lookup"><span data-stu-id="d26fd-105">Use the macro [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) to map indices 0-255 to the corresponding transform states.</span></span> <span data-ttu-id="d26fd-106">En el ejemplo de código siguiente se muestra cómo usar el método [**IDirect3DDevice9:: SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) para establecer la matriz en el estado de la transformación número 256 en una matriz de identidades.</span><span class="sxs-lookup"><span data-stu-id="d26fd-106">The following code example shows how to use the [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) method to set the matrix at transform state number 256 to an identity matrix.</span></span>


```
D3DMATRIX matBlend1;
D3DXMatrixIdentity( &matBlend1 );
m_pD3DDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matBlend );
```



<span data-ttu-id="d26fd-107">Para habilitar o deshabilitar la combinación de vértices indexados, establezca el estado de representación de D3DRS \_ INDEXEDVERTEXBLENDENABLE en **true**.</span><span class="sxs-lookup"><span data-stu-id="d26fd-107">To enable or disable indexed vertex blending, set the D3DRS\_INDEXEDVERTEXBLENDENABLE render state to **TRUE**.</span></span> <span data-ttu-id="d26fd-108">Cuando el estado de representación es habilitado, debe pasar los índices de matriz como DWORDs empaquetadas con todos los vértices.</span><span class="sxs-lookup"><span data-stu-id="d26fd-108">When the render state is enabled ,you must pass matrix indices as packed DWORDs with every vertex.</span></span> <span data-ttu-id="d26fd-109">Cuando este estado de representación está deshabilitado y la combinación de vértices está habilitada, equivale a tener los índices de matriz 0, 1, 2 y 3 en cada vértice.</span><span class="sxs-lookup"><span data-stu-id="d26fd-109">When this render state is disabled and vertex blending is enabled, it is equivalent to having the matrix indices 0, 1, 2, and 3 in every vertex.</span></span> <span data-ttu-id="d26fd-110">En el ejemplo de código siguiente se usa el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) para habilitar la combinación de vértices indizada.</span><span class="sxs-lookup"><span data-stu-id="d26fd-110">The code example below uses the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method to enable indexed vertex blending.</span></span>


```
m_pD3DDevice->SetRenderState( D3DRS_INDEXEDVERTEXBLENDENABLE, TRUE );
```



<span data-ttu-id="d26fd-111">Para habilitar o deshabilitar la fusión de vértices, establezca el estado de representación [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) en un valor distinto de D3DRS \_ deshabilitar del tipo enumerado [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) .</span><span class="sxs-lookup"><span data-stu-id="d26fd-111">To enable or disable vertex blending, set the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) render state to a value other than D3DRS\_DISABLE from the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="d26fd-112">Si este estado de representación no se establece en D3DRS \_ disable, debe pasar el número necesario de pesos para cada vértice.</span><span class="sxs-lookup"><span data-stu-id="d26fd-112">If this render state is not set to D3DRS\_DISABLE, then you must pass the required number of weights for each vertex.</span></span> <span data-ttu-id="d26fd-113">En el ejemplo de código siguiente se usa **IDirect3DDevice9:: SetRenderState** para habilitar la fusión de vértices con tres pesos para cada vértice.</span><span class="sxs-lookup"><span data-stu-id="d26fd-113">The following code example uses **IDirect3DDevice9::SetRenderState** to enable vertex blending with three weights for each vertex.</span></span>


```
m_pD3DDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_3WEIGHTS );
```



## <a name="determining-indexed-vertex-blending-support"></a><span data-ttu-id="d26fd-114">Determinar la compatibilidad con la mezcla de vértices indizados</span><span class="sxs-lookup"><span data-stu-id="d26fd-114">Determining Indexed Vertex Blending Support</span></span>

<span data-ttu-id="d26fd-115">Para determinar el tamaño máximo de la matriz de mezcla de vértices indizados, compruebe el miembro MaxVertexBlendMatrixIndex de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .</span><span class="sxs-lookup"><span data-stu-id="d26fd-115">To determine the maximum size for the indexed vertex blending matrix, check the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure's MaxVertexBlendMatrixIndex member.</span></span> <span data-ttu-id="d26fd-116">En el ejemplo de código siguiente se usa el método [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) para recuperar este tamaño.</span><span class="sxs-lookup"><span data-stu-id="d26fd-116">The code example below uses the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method to retrieve this size.</span></span>


```
D3DCAPS9 d3dCaps;
    
m_pD3DDevice->GetDeviceCaps( &d3dCaps );
IndexedMatrixMaxSize = d3dCaps.MaxVertexBlendMatrixIndex;
```



<span data-ttu-id="d26fd-117">Si el valor establecido en MaxVertexBlendMatrixIndex es 0, el dispositivo no admite matrices indizadas.</span><span class="sxs-lookup"><span data-stu-id="d26fd-117">If the value set in MaxVertexBlendMatrixIndex is 0, the device does not support indexed matrices.</span></span>

> [!Note]  
> <span data-ttu-id="d26fd-118">Cuando se usa el procesamiento de vértices de software, se pueden usar 256 matrices para la combinación de vértices indexados, con o sin la combinación normal.</span><span class="sxs-lookup"><span data-stu-id="d26fd-118">When software vertex processing is used, 256 matrices can be used for indexed vertex blending, with or without normal blending.</span></span>

 

## <a name="passing-matrix-indices-to-direct3d"></a><span data-ttu-id="d26fd-119">Pasar índices de matriz a Direct3D</span><span class="sxs-lookup"><span data-stu-id="d26fd-119">Passing Matrix Indices to Direct3D</span></span>

<span data-ttu-id="d26fd-120">Los índices de matriz mundial se pueden pasar a Direct3D mediante sombreadores de vértices heredados, FVF o declaraciones.</span><span class="sxs-lookup"><span data-stu-id="d26fd-120">World matrix indices can be passed to Direct3D by using legacy vertex shaders - FVF - or declarations.</span></span>

<span data-ttu-id="d26fd-121">En el ejemplo de código siguiente se muestra cómo usar los sombreadores de vértices heredados.</span><span class="sxs-lookup"><span data-stu-id="d26fd-121">The code example below shows how to use legacy vertex shaders.</span></span>


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



<span data-ttu-id="d26fd-122">Cuando se usa un sombreador de vértices heredado, los índices de matriz se pasan junto con las posiciones de los vértices mediante \_ marcas D3DFVF XYZBn.</span><span class="sxs-lookup"><span data-stu-id="d26fd-122">When a legacy vertex shader is used, matrix indices are passed together with vertex positions using D3DFVF\_XYZBn flags.</span></span> <span data-ttu-id="d26fd-123">Los índices de matriz se pasan como bytes dentro de un valor DWORD y deben estar presentes inmediatamente después del último peso del vértice.</span><span class="sxs-lookup"><span data-stu-id="d26fd-123">Matrix indices are passed as bytes inside a DWORD and must be present immediately after the last vertex weight.</span></span> <span data-ttu-id="d26fd-124">Los pesos de los vértices también se pasan mediante D3DFVF \_ XYZBn.</span><span class="sxs-lookup"><span data-stu-id="d26fd-124">Vertex weights are also passed using D3DFVF\_XYZBn.</span></span> <span data-ttu-id="d26fd-125">Un valor DWORD empaquetado contiene index3, index2, index1 y index0, donde index0 se encuentra en el byte más bajo de la DWORD.</span><span class="sxs-lookup"><span data-stu-id="d26fd-125">A packed DWORD contains index3, index2, index1, and index0, where index0 is located in the lowest byte of the DWORD.</span></span> <span data-ttu-id="d26fd-126">El número de índices de matriz mundial usados es igual al número que se pasa al número de matrices usadas para la fusión, tal y como se define en [**D3DRS \_ VERTEXBLEND**](./d3drenderstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="d26fd-126">The number of used world-matrix indices is equal to the number passed to the number of matrices used for blending as defined by [**D3DRS\_VERTEXBLEND**](./d3drenderstatetype.md).</span></span>

<span data-ttu-id="d26fd-127">Cuando se usa una declaración, D3DVSDE \_ BLENDINDICES define el registro de vértices de entrada para obtener los índices de matriz.</span><span class="sxs-lookup"><span data-stu-id="d26fd-127">When a declaration is used, D3DVSDE\_BLENDINDICES defines the input vertex register to get matrix indices from.</span></span> <span data-ttu-id="d26fd-128">Los índices de matriz se deben pasar como D3DVSDT \_ UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="d26fd-128">Matrix indices must be passed as D3DVSDT\_UBYTE4.</span></span>

<span data-ttu-id="d26fd-129">En el ejemplo de código siguiente se muestra cómo usar las declaraciones.</span><span class="sxs-lookup"><span data-stu-id="d26fd-129">The code example below shows how to use declarations.</span></span> <span data-ttu-id="d26fd-130">Tenga en cuenta que el orden de los componentes ya no es importante a menos que use un sombreador de vértices de función fija.</span><span class="sxs-lookup"><span data-stu-id="d26fd-130">Note that the order of the components is no longer important unless using a fixed-function vertex shader.</span></span>

<span data-ttu-id="d26fd-131">Esta es la declaración de vértices.</span><span class="sxs-lookup"><span data-stu-id="d26fd-131">Here is the vertex declaration.</span></span>


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
}
```



<span data-ttu-id="d26fd-132">Esta es la declaración de registro correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d26fd-132">Here is the corresponding register declaration.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d26fd-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d26fd-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d26fd-134">Fusión de vértices indexados</span><span class="sxs-lookup"><span data-stu-id="d26fd-134">Indexed Vertex Blending</span></span>](indexed-vertex-blending.md)
</dt> </dl>

 

 
