---
title: Acceso a recursos
description: Hay varias maneras de tener acceso a los recursos.
ms.assetid: 83950c4d-5df2-4ed1-9d8f-222a62791c18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69ab7bffd22b2271c4d648c3a95ec8d98656973
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997116"
---
# <a name="accessing-resources"></a><span data-ttu-id="aae87-103">Acceso a recursos</span><span class="sxs-lookup"><span data-stu-id="aae87-103">Accessing Resources</span></span>

<span data-ttu-id="aae87-104">Hay varias maneras de tener acceso a [los recursos](overviews-direct3d-11-resources-types.md).</span><span class="sxs-lookup"><span data-stu-id="aae87-104">There are several ways to access [resources](overviews-direct3d-11-resources-types.md).</span></span> <span data-ttu-id="aae87-105">Independientemente de, Direct3D garantiza que se devuelva cero para cualquier recurso al que se tenga acceso fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="aae87-105">Regardless, Direct3D guarantees to return zero for any resource that is accessed out of bounds.</span></span>

-   [<span data-ttu-id="aae87-106">Acceso por desplazamiento de bytes</span><span class="sxs-lookup"><span data-stu-id="aae87-106">Access By Byte Offset</span></span>](#access-by-byte-offset)
-   [<span data-ttu-id="aae87-107">Acceso por índice</span><span class="sxs-lookup"><span data-stu-id="aae87-107">Access By Index</span></span>](#access-by-index)
-   [<span data-ttu-id="aae87-108">Acceso mediante el método MIPS</span><span class="sxs-lookup"><span data-stu-id="aae87-108">Access By Mips Method</span></span>](#access-by-mips-method)
-   [<span data-ttu-id="aae87-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aae87-109">Related topics</span></span>](#related-topics)

## <a name="access-by-byte-offset"></a><span data-ttu-id="aae87-110">Acceso por desplazamiento de bytes</span><span class="sxs-lookup"><span data-stu-id="aae87-110">Access By Byte Offset</span></span>

<span data-ttu-id="aae87-111">Se puede tener acceso a dos nuevos tipos de búfer con un desplazamiento de bytes:</span><span class="sxs-lookup"><span data-stu-id="aae87-111">Two new buffer types can be accessed using a byte offset:</span></span>

-   <span data-ttu-id="aae87-112">[**ByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) es un búfer de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="aae87-112">[**ByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) is a read-only buffer.</span></span>
-   <span data-ttu-id="aae87-113">[**RWByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) es un búfer de lectura o escritura.</span><span class="sxs-lookup"><span data-stu-id="aae87-113">[**RWByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) is a read or write buffer.</span></span>

## <a name="access-by-index"></a><span data-ttu-id="aae87-114">Acceso por índice</span><span class="sxs-lookup"><span data-stu-id="aae87-114">Access By Index</span></span>

<span data-ttu-id="aae87-115">Los tipos de recursos pueden utilizar un índice para hacer referencia a una ubicación específica en el recurso.</span><span class="sxs-lookup"><span data-stu-id="aae87-115">Resource types can use an index to reference a specific location in the resource.</span></span> <span data-ttu-id="aae87-116">Considere este ejemplo:</span><span class="sxs-lookup"><span data-stu-id="aae87-116">Consider this example:</span></span>


```
uint2 pos;
Texture2D<float4> myTexture;
float4 myVar = myTexture[pos];
```



<span data-ttu-id="aae87-117">En este ejemplo se asignan los 4 valores float que se almacenan en el textura situado en la posición del *PDV* en el recurso de textura 2D de *textura* a la variable *myVar* .</span><span class="sxs-lookup"><span data-stu-id="aae87-117">This example assigns the 4 float values that are stored at the texel located at the *pos* position in the *myTexture* 2D texture resource to the *myVar* variable.</span></span>

> [!Note]  
> <span data-ttu-id="aae87-118">El valor predeterminado para tener acceso a una textura de esta manera es el nivel cero de mipmap (el nivel más detallado).</span><span class="sxs-lookup"><span data-stu-id="aae87-118">The default for accessing a texture in this way is mipmap level zero (the most detailed level).</span></span>

 

> [!Note]  
> <span data-ttu-id="aae87-119">La línea "FLOAT4 myVar = nontexture \[ pos \] ;" es equivalente a "FLOAT4 myVar = cartexture. Load (UInt3 (pos, 0));".</span><span class="sxs-lookup"><span data-stu-id="aae87-119">The "float4 myVar = myTexture\[pos\];" line is equivalent to "float4 myVar = myTexture.Load(uint3(pos,0));".</span></span> <span data-ttu-id="aae87-120">El acceso por índice es una nueva mejora de la sintaxis de HLSL.</span><span class="sxs-lookup"><span data-stu-id="aae87-120">Access by index is a new HLSL syntax enhancement.</span></span>

 

> [!Note]  
> <span data-ttu-id="aae87-121">El compilador en la versión de junio de 2010 del SDK de DirectX y versiones posteriores permite indexar todos los tipos de recursos excepto los [búferes de direcciones de bytes](direct3d-11-advanced-stages-cs-resources.md).</span><span class="sxs-lookup"><span data-stu-id="aae87-121">The compiler in the June 2010 version of the DirectX SDK and later lets you index all resource types except for [byte address buffers](direct3d-11-advanced-stages-cs-resources.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="aae87-122">El compilador 2010 de junio y versiones posteriores permiten declarar variables de recursos locales.</span><span class="sxs-lookup"><span data-stu-id="aae87-122">The June 2010 compiler and later lets you declare local resource variables.</span></span> <span data-ttu-id="aae87-123">Puede asignar recursos definidos globalmente (como mi *textura*) a estas variables y usarlas de la misma manera que sus homólogos globales.</span><span class="sxs-lookup"><span data-stu-id="aae87-123">You can assign globally defined resources (like *myTexture*) to these variables and use them the same way as their global counterparts.</span></span>

 

## <a name="access-by-mips-method"></a><span data-ttu-id="aae87-124">Acceso mediante el método MIPS</span><span class="sxs-lookup"><span data-stu-id="aae87-124">Access By Mips Method</span></span>

<span data-ttu-id="aae87-125">Los objetos de textura tienen un método **MIPS** (por ejemplo, [**Texture2D. MIPS**](/previous-versions/windows/desktop/legacy/ff471560(v=vs.85))), que puede usar para especificar el nivel de mipmap.</span><span class="sxs-lookup"><span data-stu-id="aae87-125">Texture objects have a **mips** method (for example, [**Texture2D.mips**](/previous-versions/windows/desktop/legacy/ff471560(v=vs.85))), which you can use to specify the mipmap level.</span></span> <span data-ttu-id="aae87-126">En este ejemplo se lee el color almacenado en (7, 16) en el nivel 2 de mipmap en una textura 2D:</span><span class="sxs-lookup"><span data-stu-id="aae87-126">This example reads the color stored at (7,16) on mipmap level 2 in a 2D texture:</span></span>


```
uint x = 7;
uint y = 16;
float4 myColor = myTexture.mips[2][uint2(x,y)];
```



<span data-ttu-id="aae87-127">Se trata de una mejora del compilador 2010 de junio y posterior.</span><span class="sxs-lookup"><span data-stu-id="aae87-127">This is an enhancement from the June 2010 compiler and later.</span></span> <span data-ttu-id="aae87-128">La \[ \] \[ expresión "uint2 (x, y) \] " es equivalente a "texturiza. Load (UInt3 (x, y, 2))".</span><span class="sxs-lookup"><span data-stu-id="aae87-128">The "myTexture.mips\[2\]\[uint2(x,y)\]" expression is equivalent to "myTexture.Load(uint3(x,y,2))".</span></span>

## <a name="related-topics"></a><span data-ttu-id="aae87-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aae87-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aae87-130">Información general del sombreador de cálculo</span><span class="sxs-lookup"><span data-stu-id="aae87-130">Compute Shader Overview</span></span>](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 