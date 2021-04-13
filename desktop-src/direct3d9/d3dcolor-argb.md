---
description: Inicializa un color con los valores alfa, rojo, verde y azul proporcionados.
ms.assetid: e862ba1b-fdcf-4058-8835-e58b4fc5e21a
title: Macro D3DCOLOR_ARGB (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_ARGB
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: bd0138c435c15c0c2ac026487471554e0edf0afa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362484"
---
# <a name="d3dcolor_argb-macro"></a><span data-ttu-id="3b540-103">D3DCOLOR ( \_ macro) ARGB</span><span class="sxs-lookup"><span data-stu-id="3b540-103">D3DCOLOR\_ARGB macro</span></span>

<span data-ttu-id="3b540-104">Inicializa un color con los valores alfa, rojo, verde y azul proporcionados.</span><span class="sxs-lookup"><span data-stu-id="3b540-104">Initializes a color with the supplied alpha, red, green, and blue values.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b540-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b540-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_ARGB(
   int a,
   int r,
   int g,
   int b
);
```



## <a name="parameters"></a><span data-ttu-id="3b540-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b540-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b540-107">*un*</span><span class="sxs-lookup"><span data-stu-id="3b540-107">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="3b540-108">Componente alfa del color.</span><span class="sxs-lookup"><span data-stu-id="3b540-108">Alpha component of the color.</span></span> <span data-ttu-id="3b540-109">Este valor debe estar en el intervalo comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="3b540-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="3b540-110">*r*</span><span class="sxs-lookup"><span data-stu-id="3b540-110">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="3b540-111">Componente rojo del color.</span><span class="sxs-lookup"><span data-stu-id="3b540-111">Red component of the color.</span></span> <span data-ttu-id="3b540-112">Este valor debe estar en el intervalo comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="3b540-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="3b540-113">*g*</span><span class="sxs-lookup"><span data-stu-id="3b540-113">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="3b540-114">Componente verde del color.</span><span class="sxs-lookup"><span data-stu-id="3b540-114">Green component of the color.</span></span> <span data-ttu-id="3b540-115">Este valor debe estar en el intervalo comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="3b540-115">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="3b540-116">*b*</span><span class="sxs-lookup"><span data-stu-id="3b540-116">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="3b540-117">Componente azul del color.</span><span class="sxs-lookup"><span data-stu-id="3b540-117">Blue component of the color.</span></span> <span data-ttu-id="3b540-118">Este valor debe estar en el intervalo comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="3b540-118">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b540-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b540-119">Return value</span></span>

<span data-ttu-id="3b540-120">Devuelve el valor de [D3DCOLOR](d3dcolor.md) que corresponde a los valores ARGB proporcionados.</span><span class="sxs-lookup"><span data-stu-id="3b540-120">Returns the [D3DCOLOR](d3dcolor.md) value that corresponds to the supplied ARGB values.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b540-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b540-121">Requirements</span></span>



| <span data-ttu-id="3b540-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b540-122">Requirement</span></span> | <span data-ttu-id="3b540-123">Value</span><span class="sxs-lookup"><span data-stu-id="3b540-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b540-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b540-124">Header</span></span><br/> | <dl> <span data-ttu-id="3b540-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b540-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b540-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b540-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b540-127">Macros</span><span class="sxs-lookup"><span data-stu-id="3b540-127">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="3b540-128">**D3DCOLOR \_ RGBA**</span><span class="sxs-lookup"><span data-stu-id="3b540-128">**D3DCOLOR\_RGBA**</span></span>](d3dcolor-rgba.md)
</dt> <dt>

[<span data-ttu-id="3b540-129">**D3DCOLOR \_ XRGB**</span><span class="sxs-lookup"><span data-stu-id="3b540-129">**D3DCOLOR\_XRGB**</span></span>](d3dcolor-xrgb.md)
</dt> </dl>

 

 




