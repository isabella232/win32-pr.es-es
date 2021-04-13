---
description: Describe los valores de color.
ms.assetid: 6af8c2ec-bc79-4dc6-b56d-7a7676a50b39
title: Estructura D3DCOLORVALUE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLORVALUE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 1fe2f187921749207bbbf51d7fcfd75357a70858
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362481"
---
# <a name="d3dcolorvalue-structure-d3d9typesh"></a><span data-ttu-id="8134c-103">Estructura D3DCOLORVALUE (D3D9Types. h)</span><span class="sxs-lookup"><span data-stu-id="8134c-103">D3DCOLORVALUE structure (D3D9Types.h)</span></span>

<span data-ttu-id="8134c-104">Describe los valores de color.</span><span class="sxs-lookup"><span data-stu-id="8134c-104">Describes color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="8134c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8134c-105">Syntax</span></span>


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a><span data-ttu-id="8134c-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="8134c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8134c-107">**r**</span><span class="sxs-lookup"><span data-stu-id="8134c-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="8134c-108">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="8134c-108">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="8134c-109">Valor de punto flotante que especifica el componente rojo de un color.</span><span class="sxs-lookup"><span data-stu-id="8134c-109">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="8134c-110">Normalmente, este valor está en el intervalo comprendido entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="8134c-110">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="8134c-111">Un valor de 0,0 indica la ausencia completa del componente rojo, mientras que un valor de 1,0 indica que el rojo está totalmente presente.</span><span class="sxs-lookup"><span data-stu-id="8134c-111">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="8134c-112">**g**</span><span class="sxs-lookup"><span data-stu-id="8134c-112">**g**</span></span>
</dt> <dd>

<span data-ttu-id="8134c-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="8134c-113">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="8134c-114">Valor de punto flotante que especifica el componente verde de un color.</span><span class="sxs-lookup"><span data-stu-id="8134c-114">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="8134c-115">Normalmente, este valor está en el intervalo comprendido entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="8134c-115">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="8134c-116">Un valor de 0,0 indica la ausencia completa del componente verde, mientras que un valor de 1,0 indica que el color verde está totalmente presente.</span><span class="sxs-lookup"><span data-stu-id="8134c-116">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="8134c-117">**b**</span><span class="sxs-lookup"><span data-stu-id="8134c-117">**b**</span></span>
</dt> <dd>

<span data-ttu-id="8134c-118">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="8134c-118">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="8134c-119">Valor de punto flotante que especifica el componente azul de un color.</span><span class="sxs-lookup"><span data-stu-id="8134c-119">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="8134c-120">Normalmente, este valor está en el intervalo comprendido entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="8134c-120">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="8134c-121">Un valor de 0,0 indica la ausencia completa del componente azul, mientras que un valor de 1,0 indica que el azul está totalmente presente.</span><span class="sxs-lookup"><span data-stu-id="8134c-121">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="8134c-122">**un**</span><span class="sxs-lookup"><span data-stu-id="8134c-122">**a**</span></span>
</dt> <dd>

<span data-ttu-id="8134c-123">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="8134c-123">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="8134c-124">Valor de punto flotante que especifica el componente alfa de un color.</span><span class="sxs-lookup"><span data-stu-id="8134c-124">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="8134c-125">Normalmente, este valor está en el intervalo comprendido entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="8134c-125">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="8134c-126">Un valor de 0,0 indica que es completamente transparente, mientras que un valor de 1,0 indica que es totalmente opaco.</span><span class="sxs-lookup"><span data-stu-id="8134c-126">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8134c-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8134c-127">Remarks</span></span>

<span data-ttu-id="8134c-128">Puede establecer los miembros de esta estructura en valores fuera del intervalo de 0 a 1 para implementar algunos efectos inusuales.</span><span class="sxs-lookup"><span data-stu-id="8134c-128">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="8134c-129">Los valores mayores que 1 producen luces fuertes que tienden a lavar una escena.</span><span class="sxs-lookup"><span data-stu-id="8134c-129">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="8134c-130">Los valores negativos producen luces oscuras que realmente quitan la luz de una escena.</span><span class="sxs-lookup"><span data-stu-id="8134c-130">Negative values produce dark lights that actually remove light from a scene.</span></span>

## <a name="requirements"></a><span data-ttu-id="8134c-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8134c-131">Requirements</span></span>



| <span data-ttu-id="8134c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="8134c-132">Requirement</span></span> | <span data-ttu-id="8134c-133">Value</span><span class="sxs-lookup"><span data-stu-id="8134c-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8134c-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8134c-134">Header</span></span><br/> | <dl> <span data-ttu-id="8134c-135"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="8134c-135"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8134c-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="8134c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8134c-137">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="8134c-137">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 




