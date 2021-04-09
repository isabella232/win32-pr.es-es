---
description: Inicializa un color con los valores de punto flotante rojo, verde, azul y alfa proporcionados.
ms.assetid: 61825e33-4150-47cd-97f2-2144434a45e2
title: Macro D3DCOLOR_COLORVALUE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_COLORVALUE
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 3d5bb780a5999d8931335da1e9f49ad8af88dc12
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103820962"
---
# <a name="d3dcolor_colorvalue-macro"></a><span data-ttu-id="c6b8c-103">D3DCOLOR \_ COLORVALUE (macro)</span><span class="sxs-lookup"><span data-stu-id="c6b8c-103">D3DCOLOR\_COLORVALUE macro</span></span>

<span data-ttu-id="c6b8c-104">Inicializa un color con los valores de punto flotante rojo, verde, azul y alfa proporcionados.</span><span class="sxs-lookup"><span data-stu-id="c6b8c-104">Initializes a color with the supplied red, green, blue, and alpha floating-point values.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6b8c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c6b8c-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_COLORVALUE(
   float r,
   float g,
   float b,
   float a
);
```



## <a name="parameters"></a><span data-ttu-id="c6b8c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6b8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6b8c-107">*r*</span><span class="sxs-lookup"><span data-stu-id="c6b8c-107">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="c6b8c-108">Componente rojo del color.</span><span class="sxs-lookup"><span data-stu-id="c6b8c-108">Red component of the color.</span></span> <span data-ttu-id="c6b8c-109">Este valor debe ser un valor de punto flotante en el intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="c6b8c-109">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="c6b8c-110">*g*</span><span class="sxs-lookup"><span data-stu-id="c6b8c-110">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="c6b8c-111">Componente verde del color.</span><span class="sxs-lookup"><span data-stu-id="c6b8c-111">Green component of the color.</span></span> <span data-ttu-id="c6b8c-112">Este valor debe ser un valor de punto flotante en el intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="c6b8c-112">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="c6b8c-113">*b*</span><span class="sxs-lookup"><span data-stu-id="c6b8c-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="c6b8c-114">Componente azul del color.</span><span class="sxs-lookup"><span data-stu-id="c6b8c-114">Blue component of the color.</span></span> <span data-ttu-id="c6b8c-115">Este valor debe ser un valor de punto flotante en el intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="c6b8c-115">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="c6b8c-116">*un*</span><span class="sxs-lookup"><span data-stu-id="c6b8c-116">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="c6b8c-117">Componente alfa del color.</span><span class="sxs-lookup"><span data-stu-id="c6b8c-117">Alpha component of the color.</span></span> <span data-ttu-id="c6b8c-118">Este valor debe ser un valor de punto flotante en el intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="c6b8c-118">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6b8c-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6b8c-119">Return value</span></span>

<span data-ttu-id="c6b8c-120">Devuelve el valor de [**D3DCOLOR**](d3dcolor.md) que corresponde a los valores RGBA proporcionados.</span><span class="sxs-lookup"><span data-stu-id="c6b8c-120">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied RGBA values.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6b8c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6b8c-121">Requirements</span></span>



| <span data-ttu-id="c6b8c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6b8c-122">Requirement</span></span> | <span data-ttu-id="c6b8c-123">Value</span><span class="sxs-lookup"><span data-stu-id="c6b8c-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6b8c-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c6b8c-124">Header</span></span><br/> | <dl> <span data-ttu-id="c6b8c-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6b8c-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6b8c-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6b8c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6b8c-127">Macros</span><span class="sxs-lookup"><span data-stu-id="c6b8c-127">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




