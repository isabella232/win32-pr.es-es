---
description: Define los modos de selección admitidos.
ms.assetid: b669307c-0d40-4ecb-8a2e-8bd1d9c65647
title: Enumeración D3DCULL (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCULL
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e88aa1baf86b2b03177cc686bf83299311065283
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707803"
---
# <a name="d3dcull-enumeration"></a><span data-ttu-id="a9dcf-103">Enumeración D3DCULL</span><span class="sxs-lookup"><span data-stu-id="a9dcf-103">D3DCULL enumeration</span></span>

<span data-ttu-id="a9dcf-104">Define los modos de selección admitidos.</span><span class="sxs-lookup"><span data-stu-id="a9dcf-104">Defines the supported culling modes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9dcf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9dcf-105">Syntax</span></span>


```C++
typedef enum D3DCULL { 
  D3DCULL_NONE         = 1,
  D3DCULL_CW           = 2,
  D3DCULL_CCW          = 3,
  D3DCULL_FORCE_DWORD  = 0x7fffffff
} D3DCULL, *LPD3DCULL;
```



## <a name="constants"></a><span data-ttu-id="a9dcf-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="a9dcf-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a9dcf-107"><span id="D3DCULL_NONE"></span><span id="d3dcull_none"></span>**D3DCULL \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="a9dcf-107"><span id="D3DCULL_NONE"></span><span id="d3dcull_none"></span>**D3DCULL\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="a9dcf-108">No revierta caras.</span><span class="sxs-lookup"><span data-stu-id="a9dcf-108">Do not cull back faces.</span></span>

</dd> <dt>

<span data-ttu-id="a9dcf-109"><span id="D3DCULL_CW"></span><span id="d3dcull_cw"></span>**D3DCULL \_ CW**</span><span class="sxs-lookup"><span data-stu-id="a9dcf-109"><span id="D3DCULL_CW"></span><span id="d3dcull_cw"></span>**D3DCULL\_CW**</span></span>
</dt> <dd>

<span data-ttu-id="a9dcf-110">Reactivar caras con vértices hacia la derecha.</span><span class="sxs-lookup"><span data-stu-id="a9dcf-110">Cull back faces with clockwise vertices.</span></span>

</dd> <dt>

<span data-ttu-id="a9dcf-111"><span id="D3DCULL_CCW"></span><span id="d3dcull_ccw"></span>**D3DCULL \_ CCW**</span><span class="sxs-lookup"><span data-stu-id="a9dcf-111"><span id="D3DCULL_CCW"></span><span id="d3dcull_ccw"></span>**D3DCULL\_CCW**</span></span>
</dt> <dd>

<span data-ttu-id="a9dcf-112">Reactivar caras con vértices en sentido contrario a las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="a9dcf-112">Cull back faces with counterclockwise vertices.</span></span>

</dd> <dt>

<span data-ttu-id="a9dcf-113"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a9dcf-113"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="a9dcf-114">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="a9dcf-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="a9dcf-115">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a9dcf-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="a9dcf-116">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="a9dcf-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9dcf-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9dcf-117">Remarks</span></span>

<span data-ttu-id="a9dcf-118">El estado de representación de D3DRS CULLMODE usa los valores de este tipo enumerado \_ .</span><span class="sxs-lookup"><span data-stu-id="a9dcf-118">The values in this enumerated type are used by the D3DRS\_CULLMODE render state.</span></span> <span data-ttu-id="a9dcf-119">Los modos de selección de datos definen cómo se seleccionan los rostros al representar una geometría.</span><span class="sxs-lookup"><span data-stu-id="a9dcf-119">The culling modes define how back faces are culled when rendering a geometry.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9dcf-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9dcf-120">Requirements</span></span>



| <span data-ttu-id="a9dcf-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9dcf-121">Requirement</span></span> | <span data-ttu-id="a9dcf-122">Value</span><span class="sxs-lookup"><span data-stu-id="a9dcf-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9dcf-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9dcf-123">Header</span></span><br/> | <dl> <span data-ttu-id="a9dcf-124"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9dcf-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9dcf-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9dcf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9dcf-126">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="a9dcf-126">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="a9dcf-127">**D3DCAPS9**</span><span class="sxs-lookup"><span data-stu-id="a9dcf-127">**D3DCAPS9**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[<span data-ttu-id="a9dcf-128">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="a9dcf-128">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
