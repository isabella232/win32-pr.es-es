---
title: Cómo crear un búfer de constantes
description: En este tema se muestra cómo inicializar un búfer de constantes como preparación para la representación.
ms.assetid: 78694ac2-e850-402d-8c99-6afb0bd5d660
keywords:
- búfer de constantes, crear
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1abb6718ad223ff389aa0b7ebf10ad1ec8bacd71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793323"
---
# <a name="how-to-create-a-constant-buffer"></a><span data-ttu-id="3b3bb-104">Cómo: crear un búfer de constantes</span><span class="sxs-lookup"><span data-stu-id="3b3bb-104">How to: Create a Constant Buffer</span></span>

<span data-ttu-id="3b3bb-105">Los [búferes de constantes](overviews-direct3d-11-resources-buffers-intro.md) contienen datos de constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="3b3bb-105">[Constant buffers](overviews-direct3d-11-resources-buffers-intro.md) contain shader constant data.</span></span> <span data-ttu-id="3b3bb-106">En este tema se muestra cómo inicializar un [búfer de constantes](overviews-direct3d-11-resources-buffers-intro.md) como preparación para la representación.</span><span class="sxs-lookup"><span data-stu-id="3b3bb-106">This topic shows how to initialize a [constant buffer](overviews-direct3d-11-resources-buffers-intro.md) in preparation for rendering.</span></span>

<span data-ttu-id="3b3bb-107">**Para inicializar un búfer de constantes**</span><span class="sxs-lookup"><span data-stu-id="3b3bb-107">**To initialize a constant buffer**</span></span>

1.  <span data-ttu-id="3b3bb-108">Defina una estructura que describa los datos constantes del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="3b3bb-108">Define a structure that describes the vertex shader constant data.</span></span>
2.  <span data-ttu-id="3b3bb-109">Asigne memoria para la estructura que definió en el paso uno.</span><span class="sxs-lookup"><span data-stu-id="3b3bb-109">Allocate memory for the structure that you defined in step one.</span></span> <span data-ttu-id="3b3bb-110">Rellene este búfer con datos constantes del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="3b3bb-110">Fill this buffer with vertex shader constant data.</span></span> <span data-ttu-id="3b3bb-111">Puede usar **malloc** o **New** para asignar la memoria, o puede asignar memoria para la estructura de la pila.</span><span class="sxs-lookup"><span data-stu-id="3b3bb-111">You can use **malloc** or **new** to allocate the memory, or you can allocate memory for the structure from the stack.</span></span>
3.  <span data-ttu-id="3b3bb-112">Cree una descripción de búfer rellenando una estructura [**\_ \_ DESC de búfer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) .</span><span class="sxs-lookup"><span data-stu-id="3b3bb-112">Create a buffer description by filling in a [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure.</span></span> <span data-ttu-id="3b3bb-113">Pase la \_ \_ marca de búfer constante de enlace D3D11 \_ al miembro **BindFlags** y pase el tamaño de la estructura de la descripción del búfer de constantes en bytes al miembro **ByteWidth** .</span><span class="sxs-lookup"><span data-stu-id="3b3bb-113">Pass the D3D11\_BIND\_CONSTANT\_BUFFER flag to the **BindFlags** member and pass the size of the constant buffer description structure in bytes to the **ByteWidth** member.</span></span>

    > [!Note]  
    > <span data-ttu-id="3b3bb-114">La \_ marca de \_ búfer constante de enlace D3D11 no se \_ puede combinar con otras marcas.</span><span class="sxs-lookup"><span data-stu-id="3b3bb-114">The D3D11\_BIND\_CONSTANT\_BUFFER flag cannot be combined with any other flags.</span></span>

     

4.  <span data-ttu-id="3b3bb-115">Cree una descripción de los datos de subrecurso rellenando una estructura de [**\_ \_ datos de subrecurso D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) .</span><span class="sxs-lookup"><span data-stu-id="3b3bb-115">Create a subresource data description by filling in a [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure.</span></span> <span data-ttu-id="3b3bb-116">El miembro **pSysMem** de la estructura de **\_ \_ datos del subrecurso D3D11** debe apuntar directamente a los datos constantes del sombreador de vértices que creó en el paso dos.</span><span class="sxs-lookup"><span data-stu-id="3b3bb-116">The **pSysMem** member of the **D3D11\_SUBRESOURCE\_DATA** structure must point directly to the vertex shader constant data that you created in step two.</span></span>
5.  <span data-ttu-id="3b3bb-117">Llame a [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) mientras pasa la estructura de [**\_ \_ DESC del búfer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , la estructura de [**\_ \_ datos del subrecurso D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) y la dirección de un puntero a la interfaz [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) que se va a inicializar.</span><span class="sxs-lookup"><span data-stu-id="3b3bb-117">Call [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) while passing the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure, the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure, and the address of a pointer to the [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) interface to initialize.</span></span>

<span data-ttu-id="3b3bb-118">En estos ejemplos de código se muestra cómo crear un búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="3b3bb-118">These code examples demonstrate how to create a constant buffer.</span></span>

<span data-ttu-id="3b3bb-119">En este ejemplo se da por supuesto que **g \_ pd3dDevice** es un objeto [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) válido y que **g \_ pd3dContext** es un objeto [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) válido.</span><span class="sxs-lookup"><span data-stu-id="3b3bb-119">This example assumes that **g\_pd3dDevice** is a valid [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) object and that **g\_pd3dContext** is a valid [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>


```C++
ID3D11Buffer*   g_pConstantBuffer11 = NULL;

// Define the constant data used to communicate with shaders.
struct VS_CONSTANT_BUFFER
{
    XMFLOAT4X4 mWorldViewProj;                              
    XMFLOAT4 vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;                                            
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
} VS_CONSTANT_BUFFER;

// Supply the vertex shader constant data.
VS_CONSTANT_BUFFER VsConstData;
VsConstData.mWorldViewProj = {...};
VsConstData.vSomeVectorThatMayBeNeededByASpecificShader = XMFLOAT4(1,2,3,4);
VsConstData.fSomeFloatThatMayBeNeededByASpecificShader = 3.0f;
VsConstData.fTime = 1.0f;
VsConstData.fSomeFloatThatMayBeNeededByASpecificShader2 = 2.0f;
VsConstData.fSomeFloatThatMayBeNeededByASpecificShader3 = 4.0f;

// Fill in a buffer description.
D3D11_BUFFER_DESC cbDesc;
cbDesc.ByteWidth = sizeof( VS_CONSTANT_BUFFER );
cbDesc.Usage = D3D11_USAGE_DYNAMIC;
cbDesc.BindFlags = D3D11_BIND_CONSTANT_BUFFER;
cbDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
cbDesc.MiscFlags = 0;
cbDesc.StructureByteStride = 0;

// Fill in the subresource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = &VsConstData;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the buffer.
hr = g_pd3dDevice->CreateBuffer( &cbDesc, &InitData, 
                                 &g_pConstantBuffer11 );

if( FAILED( hr ) )
   return hr;

// Set the buffer.
g_pd3dContext->VSSetConstantBuffers( 0, 1, &g_pConstantBuffer11 );
    
```



<span data-ttu-id="3b3bb-120">En este ejemplo se muestra la definición de CBuffer de HLSL asociada.</span><span class="sxs-lookup"><span data-stu-id="3b3bb-120">This example shows the associated HLSL cbuffer definition.</span></span>

``` syntax
cbuffer VS_CONSTANT_BUFFER : register(b0)
{
    matrix mWorldViewProj;
    float4  vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
};
```

> [!Note]  
> <span data-ttu-id="3b3bb-121">Asegúrese de que coincide con el \_ diseño \_ de memoria del búfer de vs Constant en C++ con el diseño de HLSL.</span><span class="sxs-lookup"><span data-stu-id="3b3bb-121">Make sure to match the VS\_CONSTANT\_BUFFER memory layout in C++ with the HLSL layout.</span></span> <span data-ttu-id="3b3bb-122">Para obtener información sobre cómo HLSL controla el diseño en memoria, consulte [reglas de empaquetado para variables constantes](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).</span><span class="sxs-lookup"><span data-stu-id="3b3bb-122">For info about how HLSL handles layout in memory, see [Packing Rules for Constant Variables](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3b3bb-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3b3bb-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b3bb-124">Búferes</span><span class="sxs-lookup"><span data-stu-id="3b3bb-124">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[<span data-ttu-id="3b3bb-125">Cómo usar Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="3b3bb-125">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 