---
description: Inicializa un color con los valores rojo, verde, azul y alfa proporcionados.
ms.assetid: 87d322f1-4a26-42fd-a1c3-7be220cecf0f
title: Macro D3DCOLOR_RGBA (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_RGBA
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c5047f29a9afbe5bb18db213f90e559b5e11d273
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649397"
---
# <a name="d3dcolor_rgba-macro"></a><span data-ttu-id="a8f97-103">D3DCOLOR \_ rgba (macro)</span><span class="sxs-lookup"><span data-stu-id="a8f97-103">D3DCOLOR\_RGBA macro</span></span>

<span data-ttu-id="a8f97-104">Inicializa un color con los valores rojo, verde, azul y alfa proporcionados.</span><span class="sxs-lookup"><span data-stu-id="a8f97-104">Initializes a color with the supplied red, green, blue, and alpha values.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8f97-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8f97-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_RGBA(
   int r,
   int g,
   int b,
   int a
);
```



## <a name="parameters"></a><span data-ttu-id="a8f97-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8f97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8f97-107">*r*</span><span class="sxs-lookup"><span data-stu-id="a8f97-107">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="a8f97-108">Componente rojo del color.</span><span class="sxs-lookup"><span data-stu-id="a8f97-108">Red component of the color.</span></span> <span data-ttu-id="a8f97-109">Este valor debe estar en el intervalo comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="a8f97-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="a8f97-110">*g*</span><span class="sxs-lookup"><span data-stu-id="a8f97-110">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="a8f97-111">Componente verde del color.</span><span class="sxs-lookup"><span data-stu-id="a8f97-111">Green component of the color.</span></span> <span data-ttu-id="a8f97-112">Este valor debe estar en el intervalo comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="a8f97-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="a8f97-113">*b*</span><span class="sxs-lookup"><span data-stu-id="a8f97-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="a8f97-114">Componente azul del color.</span><span class="sxs-lookup"><span data-stu-id="a8f97-114">Blue component of the color.</span></span> <span data-ttu-id="a8f97-115">Este valor debe estar en el intervalo comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="a8f97-115">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="a8f97-116">*un*</span><span class="sxs-lookup"><span data-stu-id="a8f97-116">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="a8f97-117">Componente alfa del color.</span><span class="sxs-lookup"><span data-stu-id="a8f97-117">Alpha component of the color.</span></span> <span data-ttu-id="a8f97-118">Este valor debe estar en el intervalo comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="a8f97-118">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8f97-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8f97-119">Return value</span></span>

<span data-ttu-id="a8f97-120">Devuelve el valor de [**D3DCOLOR**](d3dcolor.md) que corresponde a los valores RGBA proporcionados.</span><span class="sxs-lookup"><span data-stu-id="a8f97-120">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied RGBA values.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8f97-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8f97-121">Requirements</span></span>



| <span data-ttu-id="a8f97-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8f97-122">Requirement</span></span> | <span data-ttu-id="a8f97-123">Value</span><span class="sxs-lookup"><span data-stu-id="a8f97-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8f97-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8f97-124">Header</span></span><br/> | <dl> <span data-ttu-id="a8f97-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8f97-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8f97-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8f97-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8f97-127">Macros</span><span class="sxs-lookup"><span data-stu-id="a8f97-127">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="a8f97-128">**\_ARGB D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="a8f97-128">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="a8f97-129">**D3DCOLOR \_ XRGB**</span><span class="sxs-lookup"><span data-stu-id="a8f97-129">**D3DCOLOR\_XRGB**</span></span>](d3dcolor-xrgb.md)
</dt> </dl>

 

 




