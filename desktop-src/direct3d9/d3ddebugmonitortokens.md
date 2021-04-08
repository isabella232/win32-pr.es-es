---
description: Define los tokens del monitor de depuración.
ms.assetid: c0df4c9f-a232-45cf-b543-e95ee84a4a8d
title: Enumeración D3DDEBUGMONITORTOKENS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEBUGMONITORTOKENS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 82c3ecfa7d197e1ab912dbafe0d26fcb2281e605
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003780"
---
# <a name="d3ddebugmonitortokens-enumeration"></a><span data-ttu-id="d528a-103">Enumeración D3DDEBUGMONITORTOKENS</span><span class="sxs-lookup"><span data-stu-id="d528a-103">D3DDEBUGMONITORTOKENS enumeration</span></span>

<span data-ttu-id="d528a-104">Define los tokens del monitor de depuración.</span><span class="sxs-lookup"><span data-stu-id="d528a-104">Defines the debug monitor tokens.</span></span>

## <a name="syntax"></a><span data-ttu-id="d528a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d528a-105">Syntax</span></span>


```C++
typedef enum D3DDEBUGMONITORTOKENS { 
  D3DDMT_ENABLE       = 0,
  D3DDMT_DISABLE      = 1,
  D3DDMT_FORCE_DWORD  = 0x7fffffff
} D3DDEBUGMONITORTOKENS, *LPD3DDEBUGMONITORTOKENS;
```



## <a name="constants"></a><span data-ttu-id="d528a-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="d528a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d528a-107"><span id="D3DDMT_ENABLE"></span><span id="d3ddmt_enable"></span>**\_Habilitación de D3DDMT**</span><span class="sxs-lookup"><span data-stu-id="d528a-107"><span id="D3DDMT_ENABLE"></span><span id="d3ddmt_enable"></span>**D3DDMT\_ENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="d528a-108">Habilite el monitor de depuración.</span><span class="sxs-lookup"><span data-stu-id="d528a-108">Enable the debug monitor.</span></span>

</dd> <dt>

<span data-ttu-id="d528a-109"><span id="D3DDMT_DISABLE"></span><span id="d3ddmt_disable"></span>**Deshabilitación de D3DDMT \_**</span><span class="sxs-lookup"><span data-stu-id="d528a-109"><span id="D3DDMT_DISABLE"></span><span id="d3ddmt_disable"></span>**D3DDMT\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="d528a-110">Deshabilite el monitor de depuración.</span><span class="sxs-lookup"><span data-stu-id="d528a-110">Disable the debug monitor.</span></span>

</dd> <dt>

<span data-ttu-id="d528a-111"><span id="D3DDMT_FORCE_DWORD"></span><span id="d3ddmt_force_dword"></span>**D3DDMT \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="d528a-111"><span id="D3DDMT_FORCE_DWORD"></span><span id="d3ddmt_force_dword"></span>**D3DDMT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="d528a-112">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="d528a-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="d528a-113">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d528a-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="d528a-114">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d528a-114">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d528a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d528a-115">Remarks</span></span>

<span data-ttu-id="d528a-116">Los valores de este tipo enumerado se usan en el estado de representación de D3DRS \_ DEBUGMONITORTOKEN y solo son relevantes para las compilaciones de depuración.</span><span class="sxs-lookup"><span data-stu-id="d528a-116">The values in this enumerated type are used by the D3DRS\_DEBUGMONITORTOKEN render state and are only relevant for debug builds.</span></span>

## <a name="requirements"></a><span data-ttu-id="d528a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d528a-117">Requirements</span></span>



| <span data-ttu-id="d528a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d528a-118">Requirement</span></span> | <span data-ttu-id="d528a-119">Value</span><span class="sxs-lookup"><span data-stu-id="d528a-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d528a-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d528a-120">Header</span></span><br/> | <dl> <span data-ttu-id="d528a-121"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d528a-121"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d528a-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d528a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d528a-123">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="d528a-123">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="d528a-124">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="d528a-124">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
