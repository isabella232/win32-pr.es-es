---
description: Define un volumen.
ms.assetid: 415a96bc-1621-4691-b87a-98ca22f0bf07
title: Estructura D3DBOX (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 882f6aadf0d49284b30132d4f08a9c583e5c9d73
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280269"
---
# <a name="d3dbox-structure"></a><span data-ttu-id="a5b74-103">Estructura D3DBOX</span><span class="sxs-lookup"><span data-stu-id="a5b74-103">D3DBOX structure</span></span>

<span data-ttu-id="a5b74-104">Define un volumen.</span><span class="sxs-lookup"><span data-stu-id="a5b74-104">Defines a volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5b74-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5b74-105">Syntax</span></span>


```C++
typedef struct D3DBOX {
  UINT Left;
  UINT Top;
  UINT Right;
  UINT Bottom;
  UINT Front;
  UINT Back;
} D3DBOX, *LPD3DBOX;
```



## <a name="members"></a><span data-ttu-id="a5b74-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="a5b74-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a5b74-107">**Left**</span><span class="sxs-lookup"><span data-stu-id="a5b74-107">**Left**</span></span>
</dt> <dd>

<span data-ttu-id="a5b74-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5b74-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a5b74-109">Posición del lado izquierdo del cuadro en el eje x.</span><span class="sxs-lookup"><span data-stu-id="a5b74-109">Position of the left side of the box on the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="a5b74-110">**Top** (Principales)</span><span class="sxs-lookup"><span data-stu-id="a5b74-110">**Top**</span></span>
</dt> <dd>

<span data-ttu-id="a5b74-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5b74-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a5b74-112">Posición de la parte superior del cuadro en el eje y.</span><span class="sxs-lookup"><span data-stu-id="a5b74-112">Position of the top of the box on the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="a5b74-113">**Right**</span><span class="sxs-lookup"><span data-stu-id="a5b74-113">**Right**</span></span>
</dt> <dd>

<span data-ttu-id="a5b74-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5b74-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a5b74-115">Posición del lado derecho del cuadro en el eje x.</span><span class="sxs-lookup"><span data-stu-id="a5b74-115">Position of the right side of the box on the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="a5b74-116">**Bottom**</span><span class="sxs-lookup"><span data-stu-id="a5b74-116">**Bottom**</span></span>
</dt> <dd>

<span data-ttu-id="a5b74-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5b74-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a5b74-118">Posición de la parte inferior del cuadro en el eje y.</span><span class="sxs-lookup"><span data-stu-id="a5b74-118">Position of the bottom of the box on the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="a5b74-119">**Front**</span><span class="sxs-lookup"><span data-stu-id="a5b74-119">**Front**</span></span>
</dt> <dd>

<span data-ttu-id="a5b74-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5b74-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a5b74-121">Posición del anverso del cuadro en el eje z.</span><span class="sxs-lookup"><span data-stu-id="a5b74-121">Position of the front of the box on the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="a5b74-122">**Atrás**</span><span class="sxs-lookup"><span data-stu-id="a5b74-122">**Back**</span></span>
</dt> <dd>

<span data-ttu-id="a5b74-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5b74-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a5b74-124">Posición del fondo del cuadro en el eje z.</span><span class="sxs-lookup"><span data-stu-id="a5b74-124">Position of the back of the box on the z-axis.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a5b74-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5b74-125">Remarks</span></span>

<span data-ttu-id="a5b74-126">**D3DBOX** incluye los bordes izquierdo, superior y frontal; sin embargo, no se incluyen los bordes derecho, inferior y trasero.</span><span class="sxs-lookup"><span data-stu-id="a5b74-126">**D3DBOX** includes the left, top, and front edges; however, the right, bottom, and back edges are not included.</span></span> <span data-ttu-id="a5b74-127">Por ejemplo, un cuadro de 100 unidades de ancho y comienza en 0 (por lo tanto, incluidos los puntos hasta 99) se expresaría con un valor de 0 para el miembro izquierdo y un valor de 100 para el miembro de la derecha.</span><span class="sxs-lookup"><span data-stu-id="a5b74-127">For example, a box that is 100 units wide and begins at 0 (thus, including the points up to and including 99) would be expressed with a value of 0 for the Left member and a value of 100 for the Right member.</span></span> <span data-ttu-id="a5b74-128">Tenga en cuenta que el valor 99 no se utiliza para el miembro de la derecha.</span><span class="sxs-lookup"><span data-stu-id="a5b74-128">Note that a value of 99 is not used for the Right member.</span></span>

<span data-ttu-id="a5b74-129">Las restricciones en la ordenación lateral observadas para **D3DBOX** son de izquierda a derecha, de arriba a abajo y de delante a atrás.</span><span class="sxs-lookup"><span data-stu-id="a5b74-129">The restrictions on side ordering observed for **D3DBOX** are left to right, top to bottom, and front to back.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5b74-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5b74-130">Requirements</span></span>



| <span data-ttu-id="a5b74-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5b74-131">Requirement</span></span> | <span data-ttu-id="a5b74-132">Value</span><span class="sxs-lookup"><span data-stu-id="a5b74-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b74-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5b74-133">Header</span></span><br/> | <dl> <span data-ttu-id="a5b74-134"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5b74-134"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5b74-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5b74-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5b74-136">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="a5b74-136">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
