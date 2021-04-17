---
description: Define constantes que describen los formatos de búfer de profundidad.
ms.assetid: 5e5ce48b-8859-43e0-a9b4-5972cf6bf781
title: Enumeración D3DZBUFFERTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DZBUFFERTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 271a278f48c10a89fa6f552c3e1a7b4a83f274f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718261"
---
# <a name="d3dzbuffertype-enumeration"></a><span data-ttu-id="0bd22-103">Enumeración D3DZBUFFERTYPE</span><span class="sxs-lookup"><span data-stu-id="0bd22-103">D3DZBUFFERTYPE enumeration</span></span>

<span data-ttu-id="0bd22-104">Define constantes que describen los formatos de búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="0bd22-104">Defines constants that describe depth-buffer formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bd22-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0bd22-105">Syntax</span></span>


```C++
typedef enum D3DZBUFFERTYPE { 
  D3DZB_FALSE        = 0,
  D3DZB_TRUE         = 1,
  D3DZB_USEW         = 2,
  D3DZB_FORCE_DWORD  = 0x7fffffff
} D3DZBUFFERTYPE, *LPD3DZBUFFERTYPE;
```



## <a name="constants"></a><span data-ttu-id="0bd22-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="0bd22-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0bd22-107"><span id="D3DZB_FALSE"></span><span id="d3dzb_false"></span>**D3DZB \_ false**</span><span class="sxs-lookup"><span data-stu-id="0bd22-107"><span id="D3DZB_FALSE"></span><span id="d3dzb_false"></span>**D3DZB\_FALSE**</span></span>
</dt> <dd>

<span data-ttu-id="0bd22-108">Deshabilite el almacenamiento en búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="0bd22-108">Disable depth buffering.</span></span>

</dd> <dt>

<span data-ttu-id="0bd22-109"><span id="D3DZB_TRUE"></span><span id="d3dzb_true"></span>**D3DZB \_ true**</span><span class="sxs-lookup"><span data-stu-id="0bd22-109"><span id="D3DZB_TRUE"></span><span id="d3dzb_true"></span>**D3DZB\_TRUE**</span></span>
</dt> <dd>

<span data-ttu-id="0bd22-110">Habilite el almacenamiento en búfer de z.</span><span class="sxs-lookup"><span data-stu-id="0bd22-110">Enable z-buffering.</span></span>

</dd> <dt>

<span data-ttu-id="0bd22-111"><span id="D3DZB_USEW"></span><span id="d3dzb_usew"></span>**D3DZB \_ USEW**</span><span class="sxs-lookup"><span data-stu-id="0bd22-111"><span id="D3DZB_USEW"></span><span id="d3dzb_usew"></span>**D3DZB\_USEW**</span></span>
</dt> <dd>

<span data-ttu-id="0bd22-112">Habilite el almacenamiento en búfer.</span><span class="sxs-lookup"><span data-stu-id="0bd22-112">Enable w-buffering.</span></span>

</dd> <dt>

<span data-ttu-id="0bd22-113"><span id="D3DZB_FORCE_DWORD"></span><span id="d3dzb_force_dword"></span>**D3DZB \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0bd22-113"><span id="D3DZB_FORCE_DWORD"></span><span id="d3dzb_force_dword"></span>**D3DZB\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="0bd22-114">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="0bd22-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="0bd22-115">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0bd22-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="0bd22-116">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="0bd22-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0bd22-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0bd22-117">Remarks</span></span>

<span data-ttu-id="0bd22-118">Los miembros de este tipo enumerado se usan con el \_ Estado de representación de ZENABLE de D3DRS.</span><span class="sxs-lookup"><span data-stu-id="0bd22-118">Members of this enumerated type are used with the D3DRS\_ZENABLE render state.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bd22-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bd22-119">Requirements</span></span>



| <span data-ttu-id="0bd22-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bd22-120">Requirement</span></span> | <span data-ttu-id="0bd22-121">Value</span><span class="sxs-lookup"><span data-stu-id="0bd22-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bd22-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0bd22-122">Header</span></span><br/> | <dl> <span data-ttu-id="0bd22-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bd22-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bd22-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="0bd22-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bd22-125">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="0bd22-125">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="0bd22-126">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="0bd22-126">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
