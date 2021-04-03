---
description: Define las funciones de comparación admitidas.
ms.assetid: 999af3eb-a208-4312-acee-373192ea69e4
title: Enumeración D3DCMPFUNC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCMPFUNC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e49f0e058e795e00349020619f1e6d6310dfd94f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914709"
---
# <a name="d3dcmpfunc-enumeration"></a><span data-ttu-id="00672-103">Enumeración D3DCMPFUNC</span><span class="sxs-lookup"><span data-stu-id="00672-103">D3DCMPFUNC enumeration</span></span>

<span data-ttu-id="00672-104">Define las funciones de comparación admitidas.</span><span class="sxs-lookup"><span data-stu-id="00672-104">Defines the supported compare functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="00672-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00672-105">Syntax</span></span>


```C++
typedef enum D3DCMPFUNC { 
  D3DCMP_NEVER         = 1,
  D3DCMP_LESS          = 2,
  D3DCMP_EQUAL         = 3,
  D3DCMP_LESSEQUAL     = 4,
  D3DCMP_GREATER       = 5,
  D3DCMP_NOTEQUAL      = 6,
  D3DCMP_GREATEREQUAL  = 7,
  D3DCMP_ALWAYS        = 8,
  D3DCMP_FORCE_DWORD   = 0x7fffffff
} D3DCMPFUNC, *LPD3DCMPFUNC;
```



## <a name="constants"></a><span data-ttu-id="00672-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="00672-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="00672-107"><span id="D3DCMP_NEVER"></span><span id="d3dcmp_never"></span>**D3DCMP \_ nunca**</span><span class="sxs-lookup"><span data-stu-id="00672-107"><span id="D3DCMP_NEVER"></span><span id="d3dcmp_never"></span>**D3DCMP\_NEVER**</span></span>
</dt> <dd>

<span data-ttu-id="00672-108">Siempre produce un error en la prueba.</span><span class="sxs-lookup"><span data-stu-id="00672-108">Always fail the test.</span></span>

</dd> <dt>

<span data-ttu-id="00672-109"><span id="D3DCMP_LESS"></span><span id="d3dcmp_less"></span>**D3DCMP \_ menos**</span><span class="sxs-lookup"><span data-stu-id="00672-109"><span id="D3DCMP_LESS"></span><span id="d3dcmp_less"></span>**D3DCMP\_LESS**</span></span>
</dt> <dd>

<span data-ttu-id="00672-110">Acepte el nuevo píxel si su valor es menor que el valor del píxel actual.</span><span class="sxs-lookup"><span data-stu-id="00672-110">Accept the new pixel if its value is less than the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="00672-111"><span id="D3DCMP_EQUAL"></span><span id="d3dcmp_equal"></span>**Igual a D3DCMP \_**</span><span class="sxs-lookup"><span data-stu-id="00672-111"><span id="D3DCMP_EQUAL"></span><span id="d3dcmp_equal"></span>**D3DCMP\_EQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="00672-112">Acepte el nuevo píxel si su valor es igual al valor del píxel actual.</span><span class="sxs-lookup"><span data-stu-id="00672-112">Accept the new pixel if its value equals the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="00672-113"><span id="D3DCMP_LESSEQUAL"></span><span id="d3dcmp_lessequal"></span>**D3DCMP \_ LESSEQUAL**</span><span class="sxs-lookup"><span data-stu-id="00672-113"><span id="D3DCMP_LESSEQUAL"></span><span id="d3dcmp_lessequal"></span>**D3DCMP\_LESSEQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="00672-114">Acepte el nuevo píxel si su valor es menor o igual que el valor del píxel actual.</span><span class="sxs-lookup"><span data-stu-id="00672-114">Accept the new pixel if its value is less than or equal to the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="00672-115"><span id="D3DCMP_GREATER"></span><span id="d3dcmp_greater"></span>**D3DCMP \_ mayor**</span><span class="sxs-lookup"><span data-stu-id="00672-115"><span id="D3DCMP_GREATER"></span><span id="d3dcmp_greater"></span>**D3DCMP\_GREATER**</span></span>
</dt> <dd>

<span data-ttu-id="00672-116">Acepte el nuevo píxel si su valor es mayor que el valor del píxel actual.</span><span class="sxs-lookup"><span data-stu-id="00672-116">Accept the new pixel if its value is greater than the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="00672-117"><span id="D3DCMP_NOTEQUAL"></span><span id="d3dcmp_notequal"></span>**\_NOTEQUAL D3DCMP**</span><span class="sxs-lookup"><span data-stu-id="00672-117"><span id="D3DCMP_NOTEQUAL"></span><span id="d3dcmp_notequal"></span>**D3DCMP\_NOTEQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="00672-118">Acepte el nuevo píxel si su valor no es igual al valor del píxel actual.</span><span class="sxs-lookup"><span data-stu-id="00672-118">Accept the new pixel if its value does not equal the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="00672-119"><span id="D3DCMP_GREATEREQUAL"></span><span id="d3dcmp_greaterequal"></span>**D3DCMP \_ mayor criticalthreshold**</span><span class="sxs-lookup"><span data-stu-id="00672-119"><span id="D3DCMP_GREATEREQUAL"></span><span id="d3dcmp_greaterequal"></span>**D3DCMP\_GREATEREQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="00672-120">Acepte el nuevo píxel si su valor es mayor o igual que el valor del píxel actual.</span><span class="sxs-lookup"><span data-stu-id="00672-120">Accept the new pixel if its value is greater than or equal to the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="00672-121"><span id="D3DCMP_ALWAYS"></span><span id="d3dcmp_always"></span>**D3DCMP \_ siempre**</span><span class="sxs-lookup"><span data-stu-id="00672-121"><span id="D3DCMP_ALWAYS"></span><span id="d3dcmp_always"></span>**D3DCMP\_ALWAYS**</span></span>
</dt> <dd>

<span data-ttu-id="00672-122">Pase siempre la prueba.</span><span class="sxs-lookup"><span data-stu-id="00672-122">Always pass the test.</span></span>

</dd> <dt>

<span data-ttu-id="00672-123"><span id="D3DCMP_FORCE_DWORD"></span><span id="d3dcmp_force_dword"></span>**D3DCMP \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="00672-123"><span id="D3DCMP_FORCE_DWORD"></span><span id="d3dcmp_force_dword"></span>**D3DCMP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="00672-124">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="00672-124">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="00672-125">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="00672-125">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="00672-126">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="00672-126">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00672-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00672-127">Remarks</span></span>

<span data-ttu-id="00672-128">Los valores de este tipo enumerado definen las funciones de comparación admitidas para los \_ Estados de representación D3DRS ZFUNC, D3DRS \_ ALPHAFUNC y D3DRS \_ STENCILFUNC.</span><span class="sxs-lookup"><span data-stu-id="00672-128">The values in this enumerated type define the supported compare functions for the D3DRS\_ZFUNC, D3DRS\_ALPHAFUNC, and D3DRS\_STENCILFUNC render states.</span></span>

## <a name="requirements"></a><span data-ttu-id="00672-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00672-129">Requirements</span></span>



| <span data-ttu-id="00672-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="00672-130">Requirement</span></span> | <span data-ttu-id="00672-131">Value</span><span class="sxs-lookup"><span data-stu-id="00672-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00672-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00672-132">Header</span></span><br/> | <dl> <span data-ttu-id="00672-133"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="00672-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00672-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="00672-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00672-135">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="00672-135">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="00672-136">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="00672-136">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
