---
description: Inicializa un color con los valores rojo, verde y azul proporcionados.
ms.assetid: 832a4a78-c166-4e45-a907-57730da1c2c8
title: Macro D3DCOLOR_XRGB (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_XRGB
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 4932e34979b0913f27874e57cfa881f18fb16364
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424348"
---
# <a name="d3dcolor_xrgb-macro"></a><span data-ttu-id="36988-103">D3DCOLOR \_ XRGB (macro)</span><span class="sxs-lookup"><span data-stu-id="36988-103">D3DCOLOR\_XRGB macro</span></span>

<span data-ttu-id="36988-104">Inicializa un color con los valores rojo, verde y azul proporcionados.</span><span class="sxs-lookup"><span data-stu-id="36988-104">Initializes a color with the supplied red, green, and blue values.</span></span>

## <a name="syntax"></a><span data-ttu-id="36988-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36988-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_XRGB(
   int r,
   int g,
   int b
);
```



## <a name="parameters"></a><span data-ttu-id="36988-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="36988-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36988-107">*r*</span><span class="sxs-lookup"><span data-stu-id="36988-107">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="36988-108">Componente rojo del color.</span><span class="sxs-lookup"><span data-stu-id="36988-108">Red component of the color.</span></span> <span data-ttu-id="36988-109">Este valor debe estar en el intervalo comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="36988-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="36988-110">*g*</span><span class="sxs-lookup"><span data-stu-id="36988-110">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="36988-111">Componente verde del color.</span><span class="sxs-lookup"><span data-stu-id="36988-111">Green component of the color.</span></span> <span data-ttu-id="36988-112">Este valor debe estar en el intervalo comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="36988-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="36988-113">*b*</span><span class="sxs-lookup"><span data-stu-id="36988-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="36988-114">Componente azul del color.</span><span class="sxs-lookup"><span data-stu-id="36988-114">Blue component of the color.</span></span> <span data-ttu-id="36988-115">Este valor debe estar en el intervalo comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="36988-115">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36988-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="36988-116">Return value</span></span>

<span data-ttu-id="36988-117">Devuelve el valor de [**D3DCOLOR**](d3dcolor.md) que corresponde a los valores RGB proporcionados.</span><span class="sxs-lookup"><span data-stu-id="36988-117">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied RGB values.</span></span>

## <a name="requirements"></a><span data-ttu-id="36988-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36988-118">Requirements</span></span>



| <span data-ttu-id="36988-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="36988-119">Requirement</span></span> | <span data-ttu-id="36988-120">Value</span><span class="sxs-lookup"><span data-stu-id="36988-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="36988-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="36988-121">Header</span></span><br/> | <dl> <span data-ttu-id="36988-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="36988-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36988-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="36988-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36988-124">Macros</span><span class="sxs-lookup"><span data-stu-id="36988-124">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="36988-125">**\_ARGB D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="36988-125">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="36988-126">**D3DCOLOR \_ RGBA**</span><span class="sxs-lookup"><span data-stu-id="36988-126">**D3DCOLOR\_RGBA**</span></span>](d3dcolor-rgba.md)
</dt> </dl>

 

 




