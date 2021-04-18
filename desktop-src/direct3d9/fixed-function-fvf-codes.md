---
description: Un código FVF describe el contenido de los vértices almacenados intercalados en un único flujo de datos.
ms.assetid: 1a616f42-ec24-44ab-872f-7ea43646dd00
title: Códigos FVF de función fija (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd10b655c0692881e5d93b6c716ec9bcd8a76c45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705191"
---
# <a name="fixed-function-fvf-codes-direct3d-9"></a><span data-ttu-id="fd73f-103">Códigos FVF de función fija (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fd73f-103">Fixed Function FVF Codes (Direct3D 9)</span></span>

<span data-ttu-id="fd73f-104">Un código FVF describe el contenido de los vértices almacenados intercalados en un único flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="fd73f-104">A FVF code describes the contents of vertices stored interleaved in a single data stream.</span></span> <span data-ttu-id="fd73f-105">Normalmente, especifica los datos que va a procesar la canalización de procesamiento de vértices de función fija.</span><span class="sxs-lookup"><span data-stu-id="fd73f-105">It generally specifies data to be processed by the fixed function vertex processing pipeline.</span></span> <span data-ttu-id="fd73f-106">Se trata de una declaración de vértice de estilo anterior; para ver el estilo de declaración de vértices actual, vea [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="fd73f-106">This is an older-style vertex declaration; to see the current vertex declaration style, see [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

<span data-ttu-id="fd73f-107">Las aplicaciones Direct3D pueden definir vértices del modelo de varias maneras diferentes.</span><span class="sxs-lookup"><span data-stu-id="fd73f-107">Direct3D applications can define model vertices in several different ways.</span></span> <span data-ttu-id="fd73f-108">La compatibilidad con definiciones de vértices flexibles, también conocidas como formatos de vértices flexibles o códigos de formato de vértices flexibles, permite que la aplicación use solo los componentes de vértice que necesita, lo que elimina los componentes que no se usan.</span><span class="sxs-lookup"><span data-stu-id="fd73f-108">Support for flexible vertex definitions, also known as flexible vertex formats or flexible vertex format codes, makes it possible for your application to use only the vertex components it needs, eliminating those components that aren't used.</span></span> <span data-ttu-id="fd73f-109">Al usar solo los componentes de vértice necesarios, la aplicación puede conservar memoria y minimizar el ancho de banda de procesamiento necesario para representar los modelos.</span><span class="sxs-lookup"><span data-stu-id="fd73f-109">By using only the needed vertex components, your application can conserve memory and minimize the processing bandwidth required to render models.</span></span> <span data-ttu-id="fd73f-110">Describe cómo se da formato a los vértices mediante una combinación de códigos [D3DFVF](d3dfvf.md) .</span><span class="sxs-lookup"><span data-stu-id="fd73f-110">You describe how your vertices are formatted by using a combination of [D3DFVF](d3dfvf.md) codes.</span></span>

<span data-ttu-id="fd73f-111">La especificación FVF incluye formatos para el tamaño de punto, especificado por D3DFVF \_ PSIZE.</span><span class="sxs-lookup"><span data-stu-id="fd73f-111">The FVF specification includes formats for point size, specified by D3DFVF\_PSIZE.</span></span> <span data-ttu-id="fd73f-112">Este tamaño se expresa en unidades de espacio de la cámara para los vértices no transformados y encendidos (TL) y en unidades de espacio de dispositivo para los vértices de TL.</span><span class="sxs-lookup"><span data-stu-id="fd73f-112">This size is expressed in camera space units for non-transformed and lit (TL) vertices, and in device-space units for TL vertices.</span></span>

<span data-ttu-id="fd73f-113">Los métodos de representación de la interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) proporcionan a las aplicaciones de C++ métodos que aceptan una combinación de estas marcas y las usan para determinar cómo representar primitivas.</span><span class="sxs-lookup"><span data-stu-id="fd73f-113">The rendering methods of the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface provide C++ applications with methods that accept a combination of these flags, and use them to determine how to render primitives.</span></span> <span data-ttu-id="fd73f-114">Básicamente, estas marcas indican al sistema qué componentes de vértices-posición, pesos de fusión de vértices, normal, colores y el número y el formato de las coordenadas de textura (la aplicación usa y, indirectamente, qué partes de la canalización de representación desea que se apliquen a Direct3D).</span><span class="sxs-lookup"><span data-stu-id="fd73f-114">Basically, these flags tell the system which vertex components - position, vertex blending weights, normal, colors, and the number and format of texture coordinates - your application uses and, indirectly, which parts of the rendering pipeline you want Direct3D to apply to them.</span></span> <span data-ttu-id="fd73f-115">Además, la presencia o ausencia de una marca de formato de vértice determinado se comunica con el sistema en el que los campos de componente de vértice están presentes en la memoria y que se han omitido.</span><span class="sxs-lookup"><span data-stu-id="fd73f-115">In addition, the presence or absence of a particular vertex format flag communicates to the system which vertex component fields are present in memory and which you've omitted.</span></span>

<span data-ttu-id="fd73f-116">Para determinar las limitaciones de los dispositivos, puede consultar en un dispositivo los valores de D3DFVFCAPS \_ DONOTSTRIPELEMENTS y D3DFVFCAPS \_ TEXCOORDCOUNTMASK en el miembro FVFCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="fd73f-116">To determine device limitations, you can query a device for the values of D3DFVFCAPS\_DONOTSTRIPELEMENTS and D3DFVFCAPS\_TEXCOORDCOUNTMASK in the FVFCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

<span data-ttu-id="fd73f-117">Las coordenadas de textura se pueden declarar en formatos diferentes, lo que permite direccionar las texturas usando tan solo una coordenada o hasta cuatro coordenadas de textura (para las coordenadas de textura proyectadas en 2D).</span><span class="sxs-lookup"><span data-stu-id="fd73f-117">Texture coordinates can be declared in different formats, allowing textures to be addressed using as few as one coordinate or as many as four texture coordinates (for 2D projected texture coordinates).</span></span> <span data-ttu-id="fd73f-118">Para obtener más información, vea [formatos de coordenadas de textura (Direct3D 9)](texture-coordinate-formats.md).</span><span class="sxs-lookup"><span data-stu-id="fd73f-118">For more information, see [Texture Coordinate Formats (Direct3D 9)](texture-coordinate-formats.md).</span></span> <span data-ttu-id="fd73f-119">Utilice el conjunto de macros [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) para crear patrones de bits que identifiquen los formatos de coordenadas de textura que usa el formato de vértice.</span><span class="sxs-lookup"><span data-stu-id="fd73f-119">Use the [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) set of macros to create bit patterns that identify the texture coordinate formats that your vertex format uses.</span></span>

<span data-ttu-id="fd73f-120">Ninguna aplicación usará todos los componentes.</span><span class="sxs-lookup"><span data-stu-id="fd73f-120">No application will use every component.</span></span> <span data-ttu-id="fd73f-121">Los campos de vectores de vértices y homogéneos recíprocos (RHW) son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="fd73f-121">The reciprocal homogeneous W (RHW) and vertex normal fields are mutually exclusive.</span></span> <span data-ttu-id="fd73f-122">Además, la mayoría de las aplicaciones intentan usar los ocho conjuntos de coordenadas de textura, pero Direct3D tiene esta capacidad.</span><span class="sxs-lookup"><span data-stu-id="fd73f-122">Nor will most applications try to use all eight sets of texture coordinates, but Direct3D has this capacity.</span></span> <span data-ttu-id="fd73f-123">Existen varias restricciones en cuanto a las marcas que puede usar con otras marcas.</span><span class="sxs-lookup"><span data-stu-id="fd73f-123">There are several restrictions on which flags you can use with other flags.</span></span> <span data-ttu-id="fd73f-124">Por ejemplo, no puede usar los \_ marcadores D3DFVF XYZ y D3DFVF \_ XYZRHW juntos, ya que esto indicaría que la aplicación está describiendo la posición de un vértice con vértices sin transformar y transformados.</span><span class="sxs-lookup"><span data-stu-id="fd73f-124">For example, you cannot use the D3DFVF\_XYZ and D3DFVF\_XYZRHW flags together, as this would indicate that your application is describing a vertex's position with both untransformed and transformed vertices.</span></span>

<span data-ttu-id="fd73f-125">Para usar la combinación de vértices indizada, la \_ marca D3DFVF LASTBETA \_ UBYTE4 debe aparecer al final de la declaración FVF.</span><span class="sxs-lookup"><span data-stu-id="fd73f-125">To use indexed vertex blending, the D3DFVF\_LASTBETA\_UBYTE4 flag should appear at the end of the FVF declaration.</span></span> <span data-ttu-id="fd73f-126">La presencia de esta marca indica que el quinto peso de la mezcla se tratará como DWORD en lugar de como float.</span><span class="sxs-lookup"><span data-stu-id="fd73f-126">The presence of this flag indicates that the fifth blending weight will be treated as a DWORD instead of float.</span></span> <span data-ttu-id="fd73f-127">Para obtener más información, vea [fusión de vértices indizados (Direct3D 9)](indexed-vertex-blending.md).</span><span class="sxs-lookup"><span data-stu-id="fd73f-127">For more information, see [Indexed Vertex Blending (Direct3D 9)](indexed-vertex-blending.md).</span></span>

<span data-ttu-id="fd73f-128">En los siguientes ejemplos de código se muestra la diferencia entre un código FVF que usa la \_ marca D3DFVF LASTBETA \_ UBYTE4 y otro que no lo es.</span><span class="sxs-lookup"><span data-stu-id="fd73f-128">The following code samples shows the difference between an FVF code that uses the D3DFVF\_LASTBETA\_UBYTE4 flag and one that doesn't.</span></span> <span data-ttu-id="fd73f-129">La marca D3DFVF \_ XYZB3 está presente cuando se usan cuatro índices de mezcla porque siempre resta la suma de los tres primeros del número uno para obtener el cuarto (Blend ₄ = 1-(Blend ₁ + Blend ₂ + Blend ₃)).</span><span class="sxs-lookup"><span data-stu-id="fd73f-129">The flag D3DFVF\_XYZB3 is present when four blending indices are used because you always subtract the sum of the first three from the number one to obtain the fourth (blend₄ = 1 - (blend₁ + blend₂ + blend₃)).</span></span>


```
#define D3DFVF_BLENDVERTEX (D3DFVF_XYZB3|D3DFVF_NORMAL|D3DFVF_TEX1)

struct BLENDVERTEX
{
    D3DXVECTOR3 v;       // Referenced as v0 in the vertex shader
    FLOAT       blend1;  // Referenced as v1.x in the vertex shader
    FLOAT       blend2;  // Referenced as v1.y in the vertex shader
    FLOAT       blend3;  // Referenced as v1.z in the vertex shader
                         // v1.w = 1.0 - (v1.x + v1.y + v1.z)
    D3DXVECTOR3 n;       // Referenced as v3 in the vertex shader
    FLOAT       tu, tv;  // Referenced as v7 in the vertex shader
};
```



<span data-ttu-id="fd73f-130">El FVF que se define a continuación usa la \_ marca D3DFVF Last \_ UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="fd73f-130">The FVF defined below uses the D3DFVF\_LAST\_UBYTE4 flag.</span></span>


```
#define D3DFVF_BLENDVERTEX (D3DFVF_XYZB4 | D3DFVF_LASTBETA_UBYTE4 |D3DFVF_NORMAL|D3DFVF_TEX1)

struct BLENDVERTEX
{
    D3DXVECTOR3 v;       // Referenced as v0 in the vertex shader
    FLOAT       blend1;  // Referenced as v1.x in the vertex shader
    FLOAT       blend2;  // Referenced as v1.y in the vertex shader
    FLOAT       blend3;  // Referenced as v1.z in the vertex shader
                         // v1.w = 1.0 - (v1.x + v1.y + v1.z)
    DWORD       indices; // Referenced as v2.xyzw in the vertex shader 
    D3DXVECTOR3 n;       // Referenced as v3 in the vertex shader
    FLOAT       tu, tv;  // Referenced as v7 in the vertex shader
};
```



## <a name="related-topics"></a><span data-ttu-id="fd73f-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fd73f-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd73f-132">Declaración de vértice</span><span class="sxs-lookup"><span data-stu-id="fd73f-132">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 
