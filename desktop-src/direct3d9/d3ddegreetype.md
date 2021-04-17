---
description: Define el grado de las variables de la ecuación que describe una curva.
ms.assetid: 52a9c57e-a48d-4d8a-a208-97a3d09e7abf
title: Enumeración D3DDEGREETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEGREETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 773ef3a8dd8fc5f4657119c2021c5723e54a3bd7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717677"
---
# <a name="d3ddegreetype-enumeration"></a><span data-ttu-id="02a6b-103">Enumeración D3DDEGREETYPE</span><span class="sxs-lookup"><span data-stu-id="02a6b-103">D3DDEGREETYPE enumeration</span></span>

<span data-ttu-id="02a6b-104">Define el grado de las variables de la ecuación que describe una curva.</span><span class="sxs-lookup"><span data-stu-id="02a6b-104">Defines the degree of the variables in the equation that describes a curve.</span></span>

## <a name="syntax"></a><span data-ttu-id="02a6b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02a6b-105">Syntax</span></span>


```C++
typedef enum D3DDEGREETYPE { 
  D3DDEGREE_LINEAR     = 1,
  D3DDEGREE_QUADRATIC  = 2,
  D3DDEGREE_CUBIC      = 3,
  D3DDEGREE_QUINTIC    = 5,
  D3DCULL_FORCE_DWORD  = 0x7fffffff
} D3DDEGREETYPE, *LPD3DDEGREETYPE;
```



## <a name="constants"></a><span data-ttu-id="02a6b-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="02a6b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="02a6b-107"><span id="D3DDEGREE_LINEAR"></span><span id="d3ddegree_linear"></span>**\_Lineal D3DDEGREE**</span><span class="sxs-lookup"><span data-stu-id="02a6b-107"><span id="D3DDEGREE_LINEAR"></span><span id="d3ddegree_linear"></span>**D3DDEGREE\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="02a6b-108">La curva se describe mediante variables de primer orden.</span><span class="sxs-lookup"><span data-stu-id="02a6b-108">Curve is described by variables of first order.</span></span>

</dd> <dt>

<span data-ttu-id="02a6b-109"><span id="D3DDEGREE_QUADRATIC"></span><span id="d3ddegree_quadratic"></span>**D3DDEGREE \_ cuadrático**</span><span class="sxs-lookup"><span data-stu-id="02a6b-109"><span id="D3DDEGREE_QUADRATIC"></span><span id="d3ddegree_quadratic"></span>**D3DDEGREE\_QUADRATIC**</span></span>
</dt> <dd>

<span data-ttu-id="02a6b-110">La curva se describe mediante variables de segundo orden.</span><span class="sxs-lookup"><span data-stu-id="02a6b-110">Curve is described by variables of second order.</span></span>

</dd> <dt>

<span data-ttu-id="02a6b-111"><span id="D3DDEGREE_CUBIC"></span><span id="d3ddegree_cubic"></span>**D3DDEGREE \_ cúbico**</span><span class="sxs-lookup"><span data-stu-id="02a6b-111"><span id="D3DDEGREE_CUBIC"></span><span id="d3ddegree_cubic"></span>**D3DDEGREE\_CUBIC**</span></span>
</dt> <dd>

<span data-ttu-id="02a6b-112">La curva se describe mediante variables de tercer orden.</span><span class="sxs-lookup"><span data-stu-id="02a6b-112">Curve is described by variables of third order.</span></span>

</dd> <dt>

<span data-ttu-id="02a6b-113"><span id="D3DDEGREE_QUINTIC"></span><span id="d3ddegree_quintic"></span>**D3DDEGREE \_ quintal**</span><span class="sxs-lookup"><span data-stu-id="02a6b-113"><span id="D3DDEGREE_QUINTIC"></span><span id="d3ddegree_quintic"></span>**D3DDEGREE\_QUINTIC**</span></span>
</dt> <dd>

<span data-ttu-id="02a6b-114">La curva se describe mediante variables de cuarto orden.</span><span class="sxs-lookup"><span data-stu-id="02a6b-114">Curve is described by variables of fourth order.</span></span>

</dd> <dt>

<span data-ttu-id="02a6b-115"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="02a6b-115"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="02a6b-116">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="02a6b-116">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="02a6b-117">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="02a6b-117">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="02a6b-118">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="02a6b-118">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02a6b-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02a6b-119">Remarks</span></span>

<span data-ttu-id="02a6b-120">Los valores de esta enumeración se utilizan para describir las curvas usadas por las revisiones de rectángulo y triángulo.</span><span class="sxs-lookup"><span data-stu-id="02a6b-120">The values in this enumeration are used to describe the curves used by rectangle and triangle patches.</span></span> <span data-ttu-id="02a6b-121">Para obtener más información, vea D3DRS \_ CULLMODE.</span><span class="sxs-lookup"><span data-stu-id="02a6b-121">For more information, see D3DRS\_CULLMODE.</span></span>

## <a name="requirements"></a><span data-ttu-id="02a6b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02a6b-122">Requirements</span></span>



| <span data-ttu-id="02a6b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="02a6b-123">Requirement</span></span> | <span data-ttu-id="02a6b-124">Value</span><span class="sxs-lookup"><span data-stu-id="02a6b-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="02a6b-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="02a6b-125">Header</span></span><br/> | <dl> <span data-ttu-id="02a6b-126"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="02a6b-126"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02a6b-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="02a6b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02a6b-128">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="02a6b-128">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="02a6b-129">**D3DCAPS9**</span><span class="sxs-lookup"><span data-stu-id="02a6b-129">**D3DCAPS9**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[<span data-ttu-id="02a6b-130">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="02a6b-130">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
