---
description: Describe la ubicación del archivo de inclusión.
ms.assetid: a15d363e-0d82-44a9-816b-edf2f60540b3
title: Enumeración D3DXINCLUDE_TYPE (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXINCLUDE_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 51a4ed41203a9f78ee5fef747f088e9def9033c0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547886"
---
# <a name="d3dxinclude_type-enumeration"></a><span data-ttu-id="7868c-103">\_Enumeración de tipo D3DXINCLUDE</span><span class="sxs-lookup"><span data-stu-id="7868c-103">D3DXINCLUDE\_TYPE enumeration</span></span>

<span data-ttu-id="7868c-104">Describe la ubicación del archivo de inclusión.</span><span class="sxs-lookup"><span data-stu-id="7868c-104">Describes the location for the include file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7868c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7868c-105">Syntax</span></span>


```C++
typedef enum D3DXINCLUDE_TYPE { 
  D3DXINC_LOCAL        = 0,
  D3DXINC_SYSTEM       = 1,
  D3DXINC_FORCE_DWORD  = 0x7fffffff
} D3DXINCLUDE_TYPE, *LPD3DXINCLUDE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="7868c-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="7868c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7868c-107"><span id="D3DXINC_LOCAL"></span><span id="d3dxinc_local"></span>**D3DXINC \_ local**</span><span class="sxs-lookup"><span data-stu-id="7868c-107"><span id="D3DXINC_LOCAL"></span><span id="d3dxinc_local"></span>**D3DXINC\_LOCAL**</span></span>
</dt> <dd>

<span data-ttu-id="7868c-108">Busque en el proyecto local el archivo de inclusión.</span><span class="sxs-lookup"><span data-stu-id="7868c-108">Look in the local project for the include file.</span></span>

</dd> <dt>

<span data-ttu-id="7868c-109"><span id="D3DXINC_SYSTEM"></span><span id="d3dxinc_system"></span>**\_Sistema D3DXINC**</span><span class="sxs-lookup"><span data-stu-id="7868c-109"><span id="D3DXINC_SYSTEM"></span><span id="d3dxinc_system"></span>**D3DXINC\_SYSTEM**</span></span>
</dt> <dd>

<span data-ttu-id="7868c-110">Busque el archivo de inclusión en la ruta de acceso del sistema.</span><span class="sxs-lookup"><span data-stu-id="7868c-110">Look in the system path for the include file.</span></span>

</dd> <dt>

<span data-ttu-id="7868c-111"><span id="D3DXINC_FORCE_DWORD"></span><span id="d3dxinc_force_dword"></span>**D3DXINC \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="7868c-111"><span id="D3DXINC_FORCE_DWORD"></span><span id="d3dxinc_force_dword"></span>**D3DXINC\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="7868c-112">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="7868c-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="7868c-113">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7868c-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="7868c-114">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="7868c-114">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7868c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7868c-115">Requirements</span></span>



| <span data-ttu-id="7868c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7868c-116">Requirement</span></span> | <span data-ttu-id="7868c-117">Value</span><span class="sxs-lookup"><span data-stu-id="7868c-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7868c-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7868c-118">Header</span></span><br/> | <dl> <span data-ttu-id="7868c-119"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="7868c-119"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7868c-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="7868c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7868c-121">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="7868c-121">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




