---
description: Construye patrones de bits que se usan para identificar formatos de coordenadas de textura dentro de una descripción de FVF. Los resultados de estas macros se pueden combinar en una descripción de FVF mediante el operador OR.
ms.assetid: c3076d7c-7935-40ee-b513-7ff6551a535f
title: D3DFVF_TEXCOORDSIZEN (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFVF_TEXCOORDSIZEN
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 58288667954e3414aa3d8ae1550e02e7216ffb4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707940"
---
# <a name="d3dfvf_texcoordsizen"></a><span data-ttu-id="9e550-104">D3DFVF \_ TEXCOORDSIZEN</span><span class="sxs-lookup"><span data-stu-id="9e550-104">D3DFVF\_TEXCOORDSIZEN</span></span>

<span data-ttu-id="9e550-105">Construye patrones de bits que se usan para identificar formatos de coordenadas de textura dentro de una descripción de FVF.</span><span class="sxs-lookup"><span data-stu-id="9e550-105">Constructs bit patterns that are used to identify texture coordinate formats within a FVF description.</span></span> <span data-ttu-id="9e550-106">Los resultados de estas macros se pueden combinar en una descripción de FVF mediante el operador OR.</span><span class="sxs-lookup"><span data-stu-id="9e550-106">The results of these macros can be combined within a FVF description by using the OR operator.</span></span>

``` syntax
#define D3DFVF_TEXCOORDSIZEN(CoordIndex) 
#define D3DFVF_TEXCOORDSIZE1(CoordIndex) (D3DFVF_TEXTUREFORMAT1 << (CoordIndex*2 + 16)) 
#define D3DFVF_TEXCOORDSIZE2(CoordIndex) (D3DFVF_TEXTUREFORMAT2) 
#define D3DFVF_TEXCOORDSIZE3(CoordIndex) (D3DFVF_TEXTUREFORMAT3 << (CoordIndex*2 + 16)) 
#define D3DFVF_TEXCOORDSIZE4(CoordIndex) (D3DFVF_TEXTUREFORMAT4 << (CoordIndex*2 + 16))
```

## <a name="parameters"></a><span data-ttu-id="9e550-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9e550-107">Parameters</span></span>



| <span data-ttu-id="9e550-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9e550-108">Parameter</span></span>                                                                                                    | <span data-ttu-id="9e550-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e550-109">Description</span></span>                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e550-110"><span id="CoordIndex"></span><span id="coordindex"></span><span id="COORDINDEX"></span>CoordIndex</span><span class="sxs-lookup"><span data-stu-id="9e550-110"><span id="CoordIndex"></span><span id="coordindex"></span><span id="COORDINDEX"></span>CoordIndex</span></span><br/> | <span data-ttu-id="9e550-111">Valor que identifica el conjunto de coordenadas de textura en el que se aplica el tamaño de la coordenada de textura (1-, 2-, 3-o 4Dimensional).</span><span class="sxs-lookup"><span data-stu-id="9e550-111">Value that identifies the texture coordinate set at which the texture coordinate size (1-, 2-, 3-, or 4Dimensional) applies.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="9e550-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e550-112">Remarks</span></span>

<span data-ttu-id="9e550-113">Las macros de **D3DFVF \_ TEXCOORDSIZEN** usan las siguientes constantes.</span><span class="sxs-lookup"><span data-stu-id="9e550-113">The **D3DFVF\_TEXCOORDSIZEN** macros use the following constants.</span></span>


```C++
#define D3DFVF_TEXTUREFORMAT1 3 // one floating point value
#define D3DFVF_TEXTUREFORMAT2 0 // two floating point values
#define D3DFVF_TEXTUREFORMAT3 1 // three floating point values
#define D3DFVF_TEXTUREFORMAT4 2 // four floating point values
```



<span data-ttu-id="9e550-114">La descripción de FVF siguiente identifica un formato de vértice que tiene una posición; un normal; colores difusos y especulares; y dos conjuntos de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="9e550-114">The following FVF description identifies a vertex format that has a position; a normal; diffuse and specular colors; and two sets of texture coordinates.</span></span> <span data-ttu-id="9e550-115">El primer conjunto de coordenadas de textura incluye un elemento único y el segundo conjunto incluye dos elementos:</span><span class="sxs-lookup"><span data-stu-id="9e550-115">The first set of texture coordinates includes a single element, and the second set includes two elements:</span></span>


```C++
DWORD dwFVF = D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE |
              D3DFVF_SPECULAR | D3DFVF_TEX2 |
              D3DFVF_TEXCOORDSIZE1(0) |  // Uses 1D texture coordinates for
                                         // texture coordinate set 1 (index 0).
              D3DFVF_TEXCOORDSIZE2(1);   // And 2D texture coordinates for 
                                         // texture coordinate set 2 (index 1).
```



## <a name="requirements"></a><span data-ttu-id="9e550-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e550-116">Requirements</span></span>



| <span data-ttu-id="9e550-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e550-117">Requirement</span></span> | <span data-ttu-id="9e550-118">Value</span><span class="sxs-lookup"><span data-stu-id="9e550-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e550-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e550-119">Header</span></span><br/> | <dl> <span data-ttu-id="9e550-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e550-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e550-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e550-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e550-122">Macros</span><span class="sxs-lookup"><span data-stu-id="9e550-122">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="9e550-123">D3DFVF</span><span class="sxs-lookup"><span data-stu-id="9e550-123">D3DFVF</span></span>](d3dfvf.md)
</dt> </dl>

 

 




