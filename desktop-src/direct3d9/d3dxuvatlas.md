---
description: Define las opciones para realizar cálculos de distancia de poliedro, al ajustar una textura a una superficie curva. Use esta marca para elegir entre cálculos de alta calidad frente a cálculos rápidos al calcular un Atlas de textura.
ms.assetid: 76649c57-e5ae-4e0d-a7ab-f56385a327c2
title: Enumeración D3DXUVATLAS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVATLAS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 64cc116199b688fc9dcd8d6fbf331d85da508948
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717700"
---
# <a name="d3dxuvatlas-enumeration"></a><span data-ttu-id="1cb66-104">Enumeración D3DXUVATLAS</span><span class="sxs-lookup"><span data-stu-id="1cb66-104">D3DXUVATLAS enumeration</span></span>

<span data-ttu-id="1cb66-105">Define las opciones para realizar cálculos de distancia de poliedro, al ajustar una textura a una superficie curva.</span><span class="sxs-lookup"><span data-stu-id="1cb66-105">Defines options for performing geodesic distance calculations, when fitting a texture to a curved surface.</span></span> <span data-ttu-id="1cb66-106">Use esta marca para elegir entre cálculos de alta calidad frente a cálculos rápidos al calcular un Atlas de textura.</span><span class="sxs-lookup"><span data-stu-id="1cb66-106">Use this flag to choose between high quality versus fast calculations when computing a texture atlas.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cb66-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1cb66-107">Syntax</span></span>


```C++
typedef enum _D3DXUVATLAS { 
  D3DXUVATLAS_DEFAULT           = 1,
  D3DXUVATLAS_GEODESIC_FAST     = 2,
  D3DXUVATLAS_GEODESIC_QUALITY  = 3
} D3DXUVATLAS;
```



## <a name="constants"></a><span data-ttu-id="1cb66-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="1cb66-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1cb66-109"><span id="D3DXUVATLAS_DEFAULT"></span><span id="d3dxuvatlas_default"></span>**\_Valor predeterminado de D3DXUVATLAS**</span><span class="sxs-lookup"><span data-stu-id="1cb66-109"><span id="D3DXUVATLAS_DEFAULT"></span><span id="d3dxuvatlas_default"></span>**D3DXUVATLAS\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="1cb66-110">En su lugar, las mallas con más de 25.000 caras tendrán aplicado el método de distancia geodasic rápido, mientras que las mallas con menos de 25.000 caras tendrán aplicado el método de distancia de Poliedro de mayor calidad.</span><span class="sxs-lookup"><span data-stu-id="1cb66-110">Meshes with more than 25k faces will have the fast geodasic distance method applied to them while meshes with fewer than 25k faces will have the higher quality geodesic distance method applied to them instead.</span></span>

</dd> <dt>

<span data-ttu-id="1cb66-111"><span id="D3DXUVATLAS_GEODESIC_FAST"></span><span id="d3dxuvatlas_geodesic_fast"></span>**D3DXUVATLAS \_ poliedro \_ rápido**</span><span class="sxs-lookup"><span data-stu-id="1cb66-111"><span id="D3DXUVATLAS_GEODESIC_FAST"></span><span id="d3dxuvatlas_geodesic_fast"></span>**D3DXUVATLAS\_GEODESIC\_FAST**</span></span>
</dt> <dd>

<span data-ttu-id="1cb66-112">Usa las aproximaciones para mejorar la velocidad de los gráficos a costa de que se agreguen más gráficos a la malla.</span><span class="sxs-lookup"><span data-stu-id="1cb66-112">Uses approximations to improve charting speed at the cost of added stretch or more charts being output for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="1cb66-113"><span id="D3DXUVATLAS_GEODESIC_QUALITY"></span><span id="d3dxuvatlas_geodesic_quality"></span>**\_Calidad de Poliedro de D3DXUVATLAS \_**</span><span class="sxs-lookup"><span data-stu-id="1cb66-113"><span id="D3DXUVATLAS_GEODESIC_QUALITY"></span><span id="d3dxuvatlas_geodesic_quality"></span>**D3DXUVATLAS\_GEODESIC\_QUALITY**</span></span>
</dt> <dd>

<span data-ttu-id="1cb66-114">Proporciona gráficos de mejor calidad, pero requiere más tiempo y memoria de lo rápido.</span><span class="sxs-lookup"><span data-stu-id="1cb66-114">Provides better quality charts, but requires more time and memory than fast.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1cb66-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cb66-115">Requirements</span></span>



| <span data-ttu-id="1cb66-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cb66-116">Requirement</span></span> | <span data-ttu-id="1cb66-117">Value</span><span class="sxs-lookup"><span data-stu-id="1cb66-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1cb66-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1cb66-118">Header</span></span><br/> | <dl> <span data-ttu-id="1cb66-119"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cb66-119"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cb66-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="1cb66-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cb66-121">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="1cb66-121">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




