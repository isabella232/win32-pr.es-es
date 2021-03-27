---
title: Tipo de textura
description: Use la siguiente sintaxis para declarar una variable de textura.
ms.assetid: 54db5432-dab8-4a4d-a4de-93c6fa640535
keywords:
- Tipo de textura HLSL
topic_type:
- apiref
api_name:
- Texture type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89568dc5cf24af38f916375795eea052c8b39200
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2020
ms.locfileid: "103789135"
---
# <a name="texture-type"></a><span data-ttu-id="68ea9-104">Tipo de textura</span><span class="sxs-lookup"><span data-stu-id="68ea9-104">Texture type</span></span>

<span data-ttu-id="68ea9-105">Use la siguiente sintaxis para declarar una variable de textura.</span><span class="sxs-lookup"><span data-stu-id="68ea9-105">Use the following syntax to declare a texture variable.</span></span>

|                |
|----------------|
| <span data-ttu-id="68ea9-106">**Nombre del tipo;**</span><span class="sxs-lookup"><span data-stu-id="68ea9-106">**Type Name;**</span></span> |

## <a name="parameters"></a><span data-ttu-id="68ea9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68ea9-107">Parameters</span></span>
| <span data-ttu-id="68ea9-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="68ea9-108">Item</span></span>                                                                                     | <span data-ttu-id="68ea9-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="68ea9-109">Description</span></span>                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68ea9-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Automáticamente**</span><span class="sxs-lookup"><span data-stu-id="68ea9-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span><br/> | <span data-ttu-id="68ea9-111">Uno de los siguientes tipos: Texture (sin tipo, para compatibilidad con versiones anteriores), Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, TextureCube.</span><span class="sxs-lookup"><span data-stu-id="68ea9-111">One of the following types: texture (untyped, for backwards compatibility), Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, TextureCube.</span></span> <span data-ttu-id="68ea9-112">El tamaño del elemento debe ajustarse a las cantidades de 4 32 bits.</span><span class="sxs-lookup"><span data-stu-id="68ea9-112">The element size must fit into 4 32-bit quantities.</span></span><br/> |
| <span data-ttu-id="68ea9-113"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span><span class="sxs-lookup"><span data-stu-id="68ea9-113"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/> | <span data-ttu-id="68ea9-114">Cadena ASCII que identifica de forma única el nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="68ea9-114">An ASCII string that uniquely identifies the variable name.</span></span><br/>                                                                                                                                                   |
## <a name="remarks"></a><span data-ttu-id="68ea9-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68ea9-115">Remarks</span></span>

<span data-ttu-id="68ea9-116">El uso de una textura consta de tres partes.</span><span class="sxs-lookup"><span data-stu-id="68ea9-116">There are three parts to using a texture.</span></span>

1.  <span data-ttu-id="68ea9-117">Declarar una variable de textura.</span><span class="sxs-lookup"><span data-stu-id="68ea9-117">Declaring a texture variable.</span></span> <span data-ttu-id="68ea9-118">Esto se hace con la sintaxis mostrada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="68ea9-118">This is done with the syntax shown above.</span></span> <span data-ttu-id="68ea9-119">Por ejemplo, se trata de declaraciones válidas.</span><span class="sxs-lookup"><span data-stu-id="68ea9-119">For example, these are valid declarations.</span></span>

    ```
    texture g_MeshTexture;
    ```

    <span data-ttu-id="68ea9-120">\- o -</span><span class="sxs-lookup"><span data-stu-id="68ea9-120">\- or -</span></span>

    ```
    Texture2D g_MeshTexture;
    ```

2.  <span data-ttu-id="68ea9-121">Declarar e inicializar un objeto de muestra.</span><span class="sxs-lookup"><span data-stu-id="68ea9-121">Declaring and initializing a sampler object.</span></span> <span data-ttu-id="68ea9-122">Esto se hace con una sintaxis ligeramente diferente en Direct3D 9 y Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="68ea9-122">This is done with slightly different syntax in Direct3D 9 and Direct3D 10.</span></span> <span data-ttu-id="68ea9-123">Para obtener más información sobre la sintaxis de objetos de muestra, vea [tipo de muestra (DirectX HLSL)](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="68ea9-123">For details about sampler object syntax, see [Sampler Type (DirectX HLSL)](dx-graphics-hlsl-sampler.md).</span></span>
3.  <span data-ttu-id="68ea9-124">Invocar una función de textura en un sombreador.</span><span class="sxs-lookup"><span data-stu-id="68ea9-124">Invoking a texture function in a shader.</span></span>

<span data-ttu-id="68ea9-125">Diferencias entre Direct3D 9 y Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="68ea9-125">Differences between Direct3D 9 and Direct3D 10:</span></span>

<span data-ttu-id="68ea9-126">Direct3D 9 usa [funciones de textura intrínsecas](dx-graphics-hlsl-intrinsic-functions.md) para realizar operaciones de textura.</span><span class="sxs-lookup"><span data-stu-id="68ea9-126">Direct3D 9 uses [intrinsic texture functions](dx-graphics-hlsl-intrinsic-functions.md) to perform texture operations.</span></span> <span data-ttu-id="68ea9-127">Este ejemplo está en el [ejemplo BasicHLSL](/previous-versions/windows/desktop/bb153287(v%3Dvs.85)) y usa [tex2D (s, t) (DirectX HLSL)](dx-graphics-hlsl-tex2d.md) para realizar el muestreo de textura.</span><span class="sxs-lookup"><span data-stu-id="68ea9-127">This example is from the [BasicHLSL Sample](/previous-versions/windows/desktop/bb153287(v%3Dvs.85)) and uses [tex2D(s, t) (DirectX HLSL)](dx-graphics-hlsl-tex2d.md) to perform texture sampling.</span></span>

<code>Output.RGBColor = tex2D(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

<span data-ttu-id="68ea9-128">En su lugar, Direct3D 10 usa [objetos de textura con plantilla](dx-graphics-hlsl-to-type.md) .</span><span class="sxs-lookup"><span data-stu-id="68ea9-128">Direct3D 10 uses [templated texture objects](dx-graphics-hlsl-to-type.md) instead.</span></span> <span data-ttu-id="68ea9-129">Este es un ejemplo de la operación de textura equivalente.</span><span class="sxs-lookup"><span data-stu-id="68ea9-129">Here is an example of the equivalent texture operation.</span></span>

<code>Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

## <a name="see-also"></a><span data-ttu-id="68ea9-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="68ea9-130">See also</span></span>

[<span data-ttu-id="68ea9-131">Tipos de datos (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="68ea9-131">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
