---
description: Las coordenadas de textura en Direct3D pueden incluir uno, dos, tres o cuatro elementos de punto flotante para direccionar texturas con distintos niveles de dimensión.
ms.assetid: d841af62-41b0-4b80-960b-4630b9a7210c
title: Formatos de coordenadas de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c95eada1cf21f0a4db38589794b08b88023e72d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806860"
---
# <a name="texture-coordinate-formats-direct3d-9"></a><span data-ttu-id="629fc-103">Formatos de coordenadas de textura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="629fc-103">Texture Coordinate Formats (Direct3D 9)</span></span>

<span data-ttu-id="629fc-104">Las coordenadas de textura en Direct3D pueden incluir uno, dos, tres o cuatro elementos de punto flotante para direccionar texturas con distintos niveles de dimensión.</span><span class="sxs-lookup"><span data-stu-id="629fc-104">Texture coordinates in Direct3D can include one, two, three, or four floating point elements to address textures with varying levels of dimension.</span></span> <span data-ttu-id="629fc-105">Una textura 1D: una superficie de textura con dimensiones de textura 1 por n se dirige mediante una coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="629fc-105">A 1D texture - a texture surface with dimensions of 1-by-n texels - is addressed by one texture coordinate.</span></span> <span data-ttu-id="629fc-106">El caso más común, las texturas 2D, se direccionan con dos coordenadas de textura que se suelen denominar ti y v.</span><span class="sxs-lookup"><span data-stu-id="629fc-106">The most common case, 2D textures, are addressed with two texture coordinates commonly called u and v.</span></span> <span data-ttu-id="629fc-107">Direct3D admite dos tipos de texturas 3D, mapas de entorno cúbico y texturas de volumen.</span><span class="sxs-lookup"><span data-stu-id="629fc-107">Direct3D supports two types of 3D textures, cubic-environment maps and volume textures.</span></span> <span data-ttu-id="629fc-108">Los mapas de entorno cúbicos no son realmente 3D, pero se dirigen con un vector de 3 elementos.</span><span class="sxs-lookup"><span data-stu-id="629fc-108">Cubic environment maps aren't truly 3D, but they are addressed with a 3-element vector.</span></span> <span data-ttu-id="629fc-109">Para obtener más información, vea [asignación de entorno cúbica (Direct3D 9)](cubic-environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="629fc-109">For details, see [Cubic Environment Mapping (Direct3D 9)](cubic-environment-mapping.md).</span></span>

<span data-ttu-id="629fc-110">Como se describe en [códigos FVF de función fija (Direct3D 9)](fixed-function-fvf-codes.md), las aplicaciones codifican las coordenadas de textura en el formato de vértice.</span><span class="sxs-lookup"><span data-stu-id="629fc-110">As described in [Fixed Function FVF Codes (Direct3D 9)](fixed-function-fvf-codes.md), applications encode texture coordinates in the vertex format.</span></span> <span data-ttu-id="629fc-111">El formato de vértice puede incluir varios conjuntos de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="629fc-111">The vertex format can include multiple sets of texture coordinates.</span></span> <span data-ttu-id="629fc-112">Use el \_ TEX0 D3DFVF a través de D3DFVF \_ TEX8 [D3DFVF](d3dfvf.md) para describir un formato de vértice que no incluya coordenadas de textura o un máximo de ocho conjuntos.</span><span class="sxs-lookup"><span data-stu-id="629fc-112">Use the D3DFVF\_TEX0 through D3DFVF\_TEX8 [D3DFVF](d3dfvf.md) to describe a vertex format that includes no texture coordinates, or as many as eight sets.</span></span>

<span data-ttu-id="629fc-113">Cada conjunto de coordenadas de textura puede tener entre uno y cuatro elementos.</span><span class="sxs-lookup"><span data-stu-id="629fc-113">Each texture coordinate set can have between one and four elements.</span></span> <span data-ttu-id="629fc-114">Las marcas de D3DFVF \_ TEXTUREFORMAT1 a D3DFVF \_ TEXTUREFORMAT4 describen el número de elementos de una coordenada de textura de un conjunto, pero estas marcas no se usan por sí mismas.</span><span class="sxs-lookup"><span data-stu-id="629fc-114">The D3DFVF\_TEXTUREFORMAT1 through D3DFVF\_TEXTUREFORMAT4 flags describe the number of elements in a texture coordinate in a set, but these flags aren't used by themselves.</span></span> <span data-ttu-id="629fc-115">En lugar de ello, el conjunto de macros de [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) utiliza estas marcas para crear patrones de bits que describen el número de elementos utilizados por un conjunto determinado de coordenadas de textura en el formato de vértice.</span><span class="sxs-lookup"><span data-stu-id="629fc-115">Rather, the [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) set of macros use these flags to create bit patterns that describe the number of elements used by a particular set of texture coordinates in the vertex format.</span></span> <span data-ttu-id="629fc-116">Estas macros aceptan un solo parámetro que identifica el índice del conjunto de coordenadas cuyo número de elementos se está definiendo.</span><span class="sxs-lookup"><span data-stu-id="629fc-116">These macros accept a single parameter that identifies the index of the coordinate set whose number of elements is being defined.</span></span> <span data-ttu-id="629fc-117">En el ejemplo siguiente se muestra cómo se utilizan estas macros.</span><span class="sxs-lookup"><span data-stu-id="629fc-117">The following example illustrates how these macros are used.</span></span>


```
// This vertex format contains two sets of texture coordinates.
// The first set (index 0) has 2 elements, and the second set 
// has 1 element. The description for this vertex format would be: 
//     dwFVF = D3DFVF_XYZ  | D3DFVF_NORMAL | D3DFVF_DIFFUSE | D3DFVF_TEX2 |
//             D3DFVF_TEXCOORDSIZE2(0) | D3DFVF_TEXCOORDSIZE1(1); 
//
typedef struct CVF
{
    D3DVECTOR position;
    D3DVECTOR normal;
    D3DCOLOR  diffuse;
    float     u, v;   // 1st set, 2D
    float     t;      // 2nd set, 1D
} CustomVertexFormat;
```



> [!Note]  
> <span data-ttu-id="629fc-118">Con la excepción de los mapas de entorno cúbico y las texturas de volumen, los rasterizadores no pueden direccionar las texturas mediante el uso de más de dos elementos.</span><span class="sxs-lookup"><span data-stu-id="629fc-118">With the exception of cubic-environment maps and volume textures, rasterizers cannot address textures by using any more than two elements.</span></span> <span data-ttu-id="629fc-119">Las aplicaciones pueden proporcionar hasta tres elementos para una coordenada de textura, pero solo si la textura es un mapa de cubo, una textura de volumen o la \_ marca de transformación de textura proyectada D3DTTFF.</span><span class="sxs-lookup"><span data-stu-id="629fc-119">Applications can supply up to three elements for a texture coordinate, but only if the texture is a cube map, a volume texture, or the D3DTTFF\_PROJECTED texture transform flag is used.</span></span> <span data-ttu-id="629fc-120">La \_ marca proyectada D3DTTFF hace que el rasterizador Divida los dos primeros elementos por el tercer elemento (o n).</span><span class="sxs-lookup"><span data-stu-id="629fc-120">The D3DTTFF\_PROJECTED flag causes the rasterizer to divide the first two elements by the third (or n) element.</span></span> <span data-ttu-id="629fc-121">Para obtener más información, vea [transformaciones de coordenadas de textura (Direct3D 9)](texture-coordinate-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="629fc-121">For more information, see [Texture Coordinate Transformations (Direct3D 9)](texture-coordinate-transformations.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="629fc-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="629fc-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="629fc-123">Coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="629fc-123">Texture Coordinates</span></span>](texture-coordinates.md)
</dt> </dl>

 

 



