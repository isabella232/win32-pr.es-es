---
description: 'Estructura D3DCOLORVALUE (D3D9Types.h): describe los valores de color.'
ms.assetid: 6af8c2ec-bc79-4dc6-b56d-7a7676a50b39
title: Estructura D3DCOLORVALUE (D3D9Types.h)
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
ms.openlocfilehash: c9b55fbf718382e9dca7e3999cce0cabe895a261
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116063"
---
# <a name="d3dcolorvalue-structure-d3d9typesh"></a><span data-ttu-id="3c495-103">Estructura D3DCOLORVALUE (D3D9Types.h)</span><span class="sxs-lookup"><span data-stu-id="3c495-103">D3DCOLORVALUE structure (D3D9Types.h)</span></span>

<span data-ttu-id="3c495-104">Describe los valores de color.</span><span class="sxs-lookup"><span data-stu-id="3c495-104">Describes color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c495-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c495-105">Syntax</span></span>


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a><span data-ttu-id="3c495-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="3c495-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3c495-107">**r**</span><span class="sxs-lookup"><span data-stu-id="3c495-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="3c495-108">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3c495-108">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="3c495-109">Valor de punto flotante que especifica el componente rojo de un color.</span><span class="sxs-lookup"><span data-stu-id="3c495-109">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="3c495-110">Este valor suele estar en el intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="3c495-110">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="3c495-111">Un valor de 0,0 indica la ausencia completa del componente rojo, mientras que un valor de 1,0 indica que el rojo está totalmente presente.</span><span class="sxs-lookup"><span data-stu-id="3c495-111">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="3c495-112">**g**</span><span class="sxs-lookup"><span data-stu-id="3c495-112">**g**</span></span>
</dt> <dd>

<span data-ttu-id="3c495-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3c495-113">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="3c495-114">Valor de punto flotante que especifica el componente verde de un color.</span><span class="sxs-lookup"><span data-stu-id="3c495-114">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="3c495-115">Este valor suele estar en el intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="3c495-115">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="3c495-116">Un valor de 0,0 indica la ausencia completa del componente verde, mientras que un valor de 1,0 indica que el verde está totalmente presente.</span><span class="sxs-lookup"><span data-stu-id="3c495-116">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="3c495-117">**b**</span><span class="sxs-lookup"><span data-stu-id="3c495-117">**b**</span></span>
</dt> <dd>

<span data-ttu-id="3c495-118">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3c495-118">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="3c495-119">Valor de punto flotante que especifica el componente azul de un color.</span><span class="sxs-lookup"><span data-stu-id="3c495-119">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="3c495-120">Este valor suele estar en el intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="3c495-120">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="3c495-121">Un valor de 0,0 indica la ausencia completa del componente azul, mientras que un valor de 1,0 indica que el azul está totalmente presente.</span><span class="sxs-lookup"><span data-stu-id="3c495-121">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="3c495-122">**Un**</span><span class="sxs-lookup"><span data-stu-id="3c495-122">**a**</span></span>
</dt> <dd>

<span data-ttu-id="3c495-123">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3c495-123">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="3c495-124">Valor de punto flotante que especifica el componente alfa de un color.</span><span class="sxs-lookup"><span data-stu-id="3c495-124">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="3c495-125">Este valor suele estar en el intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="3c495-125">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="3c495-126">Un valor de 0,0 indica totalmente transparente, mientras que un valor de 1,0 indica totalmente opaco.</span><span class="sxs-lookup"><span data-stu-id="3c495-126">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c495-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3c495-127">Remarks</span></span>

<span data-ttu-id="3c495-128">Puede establecer los miembros de esta estructura en valores fuera del intervalo de 0 a 1 para implementar algunos efectos inusuales.</span><span class="sxs-lookup"><span data-stu-id="3c495-128">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="3c495-129">Los valores mayores que 1 producen luces fuertes que tienden a apagar una escena.</span><span class="sxs-lookup"><span data-stu-id="3c495-129">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="3c495-130">Los valores negativos generan luces oscuras que realmente quitan la luz de una escena.</span><span class="sxs-lookup"><span data-stu-id="3c495-130">Negative values produce dark lights that actually remove light from a scene.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c495-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c495-131">Requirements</span></span>



| <span data-ttu-id="3c495-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c495-132">Requirement</span></span> | <span data-ttu-id="3c495-133">Value</span><span class="sxs-lookup"><span data-stu-id="3c495-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c495-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c495-134">Header</span></span><br/> | <dl> <span data-ttu-id="3c495-135"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="3c495-135"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c495-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3c495-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c495-137">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="3c495-137">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 




