---
description: Define la ubicación a la que se debe tener acceso a un componente de color o color para los cálculos de iluminación.
ms.assetid: 76061d47-a31c-4008-aa8d-a0464dd3423f
title: Enumeración D3DMATERIALCOLORSOURCE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIALCOLORSOURCE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8877eece8e33c6508768b22c989e992cf8178823
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707935"
---
# <a name="d3dmaterialcolorsource-enumeration"></a><span data-ttu-id="3b790-103">Enumeración D3DMATERIALCOLORSOURCE</span><span class="sxs-lookup"><span data-stu-id="3b790-103">D3DMATERIALCOLORSOURCE enumeration</span></span>

<span data-ttu-id="3b790-104">Define la ubicación a la que se debe tener acceso a un componente de color o color para los cálculos de iluminación.</span><span class="sxs-lookup"><span data-stu-id="3b790-104">Defines the location at which a color or color component must be accessed for lighting calculations.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b790-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b790-105">Syntax</span></span>


```C++
typedef enum D3DMATERIALCOLORSOURCE { 
  D3DMCS_MATERIAL     = 0,
  D3DMCS_COLOR1       = 1,
  D3DMCS_COLOR2       = 2,
  D3DMCS_FORCE_DWORD  = 0x7fffffff
} D3DMATERIALCOLORSOURCE, *LPD3DMATERIALCOLORSOURCE;
```



## <a name="constants"></a><span data-ttu-id="3b790-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="3b790-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3b790-107"><span id="D3DMCS_MATERIAL"></span><span id="d3dmcs_material"></span>**\_Material D3DMCS**</span><span class="sxs-lookup"><span data-stu-id="3b790-107"><span id="D3DMCS_MATERIAL"></span><span id="d3dmcs_material"></span>**D3DMCS\_MATERIAL**</span></span>
</dt> <dd>

<span data-ttu-id="3b790-108">Usar el color del material actual.</span><span class="sxs-lookup"><span data-stu-id="3b790-108">Use the color from the current material.</span></span>

</dd> <dt>

<span data-ttu-id="3b790-109"><span id="D3DMCS_COLOR1"></span><span id="d3dmcs_color1"></span>**D3DMCS \_ COLOR1**</span><span class="sxs-lookup"><span data-stu-id="3b790-109"><span id="D3DMCS_COLOR1"></span><span id="d3dmcs_color1"></span>**D3DMCS\_COLOR1**</span></span>
</dt> <dd>

<span data-ttu-id="3b790-110">Usar el color de vértice difuso.</span><span class="sxs-lookup"><span data-stu-id="3b790-110">Use the diffuse vertex color.</span></span>

</dd> <dt>

<span data-ttu-id="3b790-111"><span id="D3DMCS_COLOR2"></span><span id="d3dmcs_color2"></span>**D3DMCS \_ COLOR2**</span><span class="sxs-lookup"><span data-stu-id="3b790-111"><span id="D3DMCS_COLOR2"></span><span id="d3dmcs_color2"></span>**D3DMCS\_COLOR2**</span></span>
</dt> <dd>

<span data-ttu-id="3b790-112">Usar el color de vértice especular.</span><span class="sxs-lookup"><span data-stu-id="3b790-112">Use the specular vertex color.</span></span>

</dd> <dt>

<span data-ttu-id="3b790-113"><span id="D3DMCS_FORCE_DWORD"></span><span id="d3dmcs_force_dword"></span>**D3DMCS \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="3b790-113"><span id="D3DMCS_FORCE_DWORD"></span><span id="d3dmcs_force_dword"></span>**D3DMCS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="3b790-114">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="3b790-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="3b790-115">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3b790-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="3b790-116">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="3b790-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b790-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b790-117">Remarks</span></span>

<span data-ttu-id="3b790-118">Estas marcas se utilizan para establecer el valor de los siguientes Estados de representación en el tipo enumerado [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) .</span><span class="sxs-lookup"><span data-stu-id="3b790-118">These flags are used to set the value of the following render states in the [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) enumerated type.</span></span>

-   <span data-ttu-id="3b790-119">D3DRS \_ AMBIENTMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="3b790-119">D3DRS\_AMBIENTMATERIALSOURCE</span></span>
-   <span data-ttu-id="3b790-120">D3DRS \_ DIFFUSEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="3b790-120">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>
-   <span data-ttu-id="3b790-121">D3DRS \_ EMISSIVEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="3b790-121">D3DRS\_EMISSIVEMATERIALSOURCE</span></span>
-   <span data-ttu-id="3b790-122">D3DRS \_ SPECULARMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="3b790-122">D3DRS\_SPECULARMATERIALSOURCE</span></span>

## <a name="requirements"></a><span data-ttu-id="3b790-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b790-123">Requirements</span></span>



| <span data-ttu-id="3b790-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b790-124">Requirement</span></span> | <span data-ttu-id="3b790-125">Value</span><span class="sxs-lookup"><span data-stu-id="3b790-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b790-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b790-126">Header</span></span><br/> | <dl> <span data-ttu-id="3b790-127"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b790-127"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b790-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b790-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b790-129">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="3b790-129">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="3b790-130">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="3b790-130">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
