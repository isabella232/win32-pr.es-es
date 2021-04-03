---
description: Define si el modo de teselación actual es discreto o continuo.
ms.assetid: d8055a25-6a8e-4018-a993-762f6f0e0cd3
title: Enumeración D3DPATCHEDGESTYLE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPATCHEDGESTYLE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e625b7c4ff12f9859efdcc2b10b551a2223adab6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914749"
---
# <a name="d3dpatchedgestyle-enumeration"></a><span data-ttu-id="bd6b1-103">Enumeración D3DPATCHEDGESTYLE</span><span class="sxs-lookup"><span data-stu-id="bd6b1-103">D3DPATCHEDGESTYLE enumeration</span></span>

<span data-ttu-id="bd6b1-104">Define si el modo de teselación actual es discreto o continuo.</span><span class="sxs-lookup"><span data-stu-id="bd6b1-104">Defines whether the current tessellation mode is discrete or continuous.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd6b1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd6b1-105">Syntax</span></span>


```C++
typedef enum D3DPATCHEDGESTYLE { 
  D3DPATCHEDGE_DISCRETE     = 0,
  D3DPATCHEDGE_CONTINUOUS   = 1,
  D3DPATCHEDGE_FORCE_DWORD  = 0x7fffffff
} D3DPATCHEDGESTYLE, *LPD3DPATCHEDGESTYLE;
```



## <a name="constants"></a><span data-ttu-id="bd6b1-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="bd6b1-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bd6b1-107"><span id="D3DPATCHEDGE_DISCRETE"></span><span id="d3dpatchedge_discrete"></span>**D3DPATCHEDGE \_ discreto**</span><span class="sxs-lookup"><span data-stu-id="bd6b1-107"><span id="D3DPATCHEDGE_DISCRETE"></span><span id="d3dpatchedge_discrete"></span>**D3DPATCHEDGE\_DISCRETE**</span></span>
</dt> <dd>

<span data-ttu-id="bd6b1-108">Estilo de borde discreto.</span><span class="sxs-lookup"><span data-stu-id="bd6b1-108">Discrete edge style.</span></span> <span data-ttu-id="bd6b1-109">En el modo discreto, puede especificar la teselación de punto flotante, pero se truncará en enteros.</span><span class="sxs-lookup"><span data-stu-id="bd6b1-109">In discrete mode, you can specify float tessellation but it will be truncated to integers.</span></span>

</dd> <dt>

<span data-ttu-id="bd6b1-110"><span id="D3DPATCHEDGE_CONTINUOUS"></span><span id="d3dpatchedge_continuous"></span>**D3DPATCHEDGE \_ continuo**</span><span class="sxs-lookup"><span data-stu-id="bd6b1-110"><span id="D3DPATCHEDGE_CONTINUOUS"></span><span id="d3dpatchedge_continuous"></span>**D3DPATCHEDGE\_CONTINUOUS**</span></span>
</dt> <dd>

<span data-ttu-id="bd6b1-111">Estilo de borde continuo.</span><span class="sxs-lookup"><span data-stu-id="bd6b1-111">Continuous edge style.</span></span> <span data-ttu-id="bd6b1-112">En el modo continuo, la teselación se especifica como valores float que se pueden variar suavemente para reducir los artefactos de "sacando".</span><span class="sxs-lookup"><span data-stu-id="bd6b1-112">In continuous mode, tessellation is specified as float values that can be smoothly varied to reduce "popping" artifacts.</span></span>

</dd> <dt>

<span data-ttu-id="bd6b1-113"><span id="D3DPATCHEDGE_FORCE_DWORD"></span><span id="d3dpatchedge_force_dword"></span>**D3DPATCHEDGE \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bd6b1-113"><span id="D3DPATCHEDGE_FORCE_DWORD"></span><span id="d3dpatchedge_force_dword"></span>**D3DPATCHEDGE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="bd6b1-114">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="bd6b1-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="bd6b1-115">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="bd6b1-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="bd6b1-116">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="bd6b1-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd6b1-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bd6b1-117">Remarks</span></span>

<span data-ttu-id="bd6b1-118">Tenga en cuenta que la teselación continua produce un patrón de teselación completamente diferente del discreto para los mismos valores de teselación (esto es más evidente en el modo de trama).</span><span class="sxs-lookup"><span data-stu-id="bd6b1-118">Note that continuous tessellation produces a completely different tessellation pattern from the discrete one for the same tessellation values (this is more apparent in wireframe mode).</span></span> <span data-ttu-id="bd6b1-119">Por lo tanto, 4,0 Continuous no es lo mismo que 4 discretos.</span><span class="sxs-lookup"><span data-stu-id="bd6b1-119">Thus, 4.0 continuous is not the same as 4 discrete.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd6b1-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd6b1-120">Requirements</span></span>



| <span data-ttu-id="bd6b1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd6b1-121">Requirement</span></span> | <span data-ttu-id="bd6b1-122">Value</span><span class="sxs-lookup"><span data-stu-id="bd6b1-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd6b1-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd6b1-123">Header</span></span><br/> | <dl> <span data-ttu-id="bd6b1-124"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd6b1-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd6b1-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd6b1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd6b1-126">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="bd6b1-126">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




