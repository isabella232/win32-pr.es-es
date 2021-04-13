---
description: Define las marcas que se usan para controlar el número o las matrices que el sistema aplica al realizar la combinación de vértices multimatrix.
ms.assetid: 5314f455-ce5f-4ff5-81fc-d3dffc8705b7
title: Enumeración D3DVERTEXBLENDFLAGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXBLENDFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0b4d22740a9ad06a9848dc7649d62ac06d37a056
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362546"
---
# <a name="d3dvertexblendflags-enumeration"></a><span data-ttu-id="2f6bf-103">Enumeración D3DVERTEXBLENDFLAGS</span><span class="sxs-lookup"><span data-stu-id="2f6bf-103">D3DVERTEXBLENDFLAGS enumeration</span></span>

<span data-ttu-id="2f6bf-104">Define las marcas que se usan para controlar el número o las matrices que el sistema aplica al realizar la combinación de vértices multimatrix.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-104">Defines flags used to control the number or matrices that the system applies when performing multimatrix vertex blending.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f6bf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f6bf-105">Syntax</span></span>


```C++
typedef enum D3DVERTEXBLENDFLAGS { 
  D3DVBF_DISABLE   = 0,
  D3DVBF_1WEIGHTS  = 1,
  D3DVBF_2WEIGHTS  = 2,
  D3DVBF_3WEIGHTS  = 3,
  D3DVBF_TWEENING  = 255,
  D3DVBF_0WEIGHTS  = 256
} D3DVERTEXBLENDFLAGS, *LPD3DVERTEXBLENDFLAGS;
```



## <a name="constants"></a><span data-ttu-id="2f6bf-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="2f6bf-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2f6bf-107"><span id="D3DVBF_DISABLE"></span><span id="d3dvbf_disable"></span>**Deshabilitación de D3DVBF \_**</span><span class="sxs-lookup"><span data-stu-id="2f6bf-107"><span id="D3DVBF_DISABLE"></span><span id="d3dvbf_disable"></span>**D3DVBF\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="2f6bf-108">Deshabilitar la fusión de vértices; Aplique solo la matriz universal establecida por la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , donde el valor de índice para el estado de transformación es 0.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-108">Disable vertex blending; apply only the world matrix set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation state is 0.</span></span>

</dd> <dt>

<span data-ttu-id="2f6bf-109"><span id="D3DVBF_1WEIGHTS"></span><span id="d3dvbf_1weights"></span>**D3DVBF \_ 1WEIGHTS**</span><span class="sxs-lookup"><span data-stu-id="2f6bf-109"><span id="D3DVBF_1WEIGHTS"></span><span id="d3dvbf_1weights"></span>**D3DVBF\_1WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="2f6bf-110">Habilite la fusión de vértices entre las dos matrices establecidas por la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , donde el valor de índice para los Estados de transformación es 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-110">Enable vertex blending between the two matrices set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation states are 0 and 1.</span></span>

</dd> <dt>

<span data-ttu-id="2f6bf-111"><span id="D3DVBF_2WEIGHTS"></span><span id="d3dvbf_2weights"></span>**D3DVBF \_ 2WEIGHTS**</span><span class="sxs-lookup"><span data-stu-id="2f6bf-111"><span id="D3DVBF_2WEIGHTS"></span><span id="d3dvbf_2weights"></span>**D3DVBF\_2WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="2f6bf-112">Habilite la fusión de vértices entre las tres matrices establecidas por la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , donde el valor de índice para los Estados de transformación es 0, 1 y 2.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-112">Enable vertex blending between the three matrices set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation states are 0, 1, and 2.</span></span>

</dd> <dt>

<span data-ttu-id="2f6bf-113"><span id="D3DVBF_3WEIGHTS"></span><span id="d3dvbf_3weights"></span>**D3DVBF \_ 3WEIGHTS**</span><span class="sxs-lookup"><span data-stu-id="2f6bf-113"><span id="D3DVBF_3WEIGHTS"></span><span id="d3dvbf_3weights"></span>**D3DVBF\_3WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="2f6bf-114">Habilite la fusión de vértices entre las cuatro matrices establecidas por la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , donde el valor de índice para los Estados de transformación es 0, 1, 2 y 3.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-114">Enable vertex blending between the four matrices set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation states are 0, 1, 2, and 3.</span></span>

</dd> <dt>

<span data-ttu-id="2f6bf-115"><span id="D3DVBF_TWEENING"></span><span id="d3dvbf_tweening"></span>**Intercalación de D3DVBF \_**</span><span class="sxs-lookup"><span data-stu-id="2f6bf-115"><span id="D3DVBF_TWEENING"></span><span id="d3dvbf_tweening"></span>**D3DVBF\_TWEENING**</span></span>
</dt> <dd>

<span data-ttu-id="2f6bf-116">La mezcla de vértices se realiza mediante el valor asignado a D3DRS \_ TWEENFACTOR.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-116">Vertex blending is done by using the value assigned to D3DRS\_TWEENFACTOR.</span></span>

</dd> <dt>

<span data-ttu-id="2f6bf-117"><span id="D3DVBF_0WEIGHTS"></span><span id="d3dvbf_0weights"></span>**D3DVBF \_ 0WEIGHTS**</span><span class="sxs-lookup"><span data-stu-id="2f6bf-117"><span id="D3DVBF_0WEIGHTS"></span><span id="d3dvbf_0weights"></span>**D3DVBF\_0WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="2f6bf-118">Use una sola matriz con un peso de 1,0.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-118">Use a single matrix with a weight of 1.0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f6bf-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f6bf-119">Remarks</span></span>

<span data-ttu-id="2f6bf-120">Los miembros de este tipo se usan con el \_ Estado de representación de VERTEXBLEND de D3DRS.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-120">Members of this type are used with the D3DRS\_VERTEXBLEND render state.</span></span>

<span data-ttu-id="2f6bf-121">La combinación de geometría (combinación de vértices multimatriz) requiere que la aplicación use un formato de vértice con pesos de fusión (beta) para cada vértice.</span><span class="sxs-lookup"><span data-stu-id="2f6bf-121">Geometry blending (multimatrix vertex blending) requires that your application use a vertex format that has blending (beta) weights for each vertex.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f6bf-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f6bf-122">Requirements</span></span>



| <span data-ttu-id="2f6bf-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f6bf-123">Requirement</span></span> | <span data-ttu-id="2f6bf-124">Value</span><span class="sxs-lookup"><span data-stu-id="2f6bf-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f6bf-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f6bf-125">Header</span></span><br/> | <dl> <span data-ttu-id="2f6bf-126"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f6bf-126"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f6bf-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f6bf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f6bf-128">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="2f6bf-128">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="2f6bf-129">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="2f6bf-129">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> <dt>

[<span data-ttu-id="2f6bf-130">**D3DTS \_ World**</span><span class="sxs-lookup"><span data-stu-id="2f6bf-130">**D3DTS\_WORLD**</span></span>](d3dts-world.md)
</dt> <dt>

[<span data-ttu-id="2f6bf-131">**D3DTS \_ worlda**</span><span class="sxs-lookup"><span data-stu-id="2f6bf-131">**D3DTS\_WORLDn**</span></span>](d3dts-worldn.md)
</dt> <dt>

[<span data-ttu-id="2f6bf-132">**D3DTS \_ WORLDMATRIX**</span><span class="sxs-lookup"><span data-stu-id="2f6bf-132">**D3DTS\_WORLDMATRIX**</span></span>](d3dts-worldmatrix.md)
</dt> </dl>

 

 
