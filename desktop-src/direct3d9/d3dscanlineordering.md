---
description: Marcas que indican el método que el rasterizador utiliza para crear una imagen en una superficie.
ms.assetid: 55cf790e-ebe9-4791-a2be-a90fc76bae57
title: Enumeración D3DSCANLINEORDERING (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSCANLINEORDERING
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2eaed36577f881266c12b0a927cfcdc2494f0d57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718536"
---
# <a name="d3dscanlineordering-enumeration"></a><span data-ttu-id="1cc05-103">Enumeración D3DSCANLINEORDERING</span><span class="sxs-lookup"><span data-stu-id="1cc05-103">D3DSCANLINEORDERING enumeration</span></span>

<span data-ttu-id="1cc05-104">Marcas que indican el método que el rasterizador utiliza para crear una imagen en una superficie.</span><span class="sxs-lookup"><span data-stu-id="1cc05-104">Flags indicating the method the rasterizer uses to create an image on a surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cc05-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1cc05-105">Syntax</span></span>


```C++
typedef enum D3DSCANLINEORDERING { 
  D3DSCANLINEORDERING_PROGRESSIVE  = 1,
  D3DSCANLINEORDERING_INTERLACED   = 2
} D3DSCANLINEORDERING, *LPD3DSCANLINEORDERING;
```



## <a name="constants"></a><span data-ttu-id="1cc05-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="1cc05-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1cc05-107"><span id="D3DSCANLINEORDERING_PROGRESSIVE"></span><span id="d3dscanlineordering_progressive"></span>**\_Progresiva D3DSCANLINEORDERING**</span><span class="sxs-lookup"><span data-stu-id="1cc05-107"><span id="D3DSCANLINEORDERING_PROGRESSIVE"></span><span id="d3dscanlineordering_progressive"></span>**D3DSCANLINEORDERING\_PROGRESSIVE**</span></span>
</dt> <dd>

<span data-ttu-id="1cc05-108">La imagen se crea desde la primera Scanline hasta la última sin omitir ninguna.</span><span class="sxs-lookup"><span data-stu-id="1cc05-108">The image is created from the first scanline to the last without skipping any.</span></span>

</dd> <dt>

<span data-ttu-id="1cc05-109"><span id="D3DSCANLINEORDERING_INTERLACED"></span><span id="d3dscanlineordering_interlaced"></span>**D3DSCANLINEORDERING \_ entrelazado**</span><span class="sxs-lookup"><span data-stu-id="1cc05-109"><span id="D3DSCANLINEORDERING_INTERLACED"></span><span id="d3dscanlineordering_interlaced"></span>**D3DSCANLINEORDERING\_INTERLACED**</span></span>
</dt> <dd>

<span data-ttu-id="1cc05-110">La imagen se crea mediante el método entrelazado, en el que las líneas impares se dibujan en las pasadas con números impares y las líneas pares se dibujan en pasos con número par.</span><span class="sxs-lookup"><span data-stu-id="1cc05-110">The image is created using the interlaced method in which odd-numbered lines are drawn on odd-numbered passes and even lines are drawn on even-numbered passes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1cc05-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1cc05-111">Remarks</span></span>

<span data-ttu-id="1cc05-112">Esta enumeración se usa como miembro en [**D3DDISPLAYMODEFILTER**](d3ddisplaymodefilter.md) y [**D3DDISPLAYMODEEX**](d3ddisplaymodeex.md).</span><span class="sxs-lookup"><span data-stu-id="1cc05-112">This enumeration is used as a member in [**D3DDISPLAYMODEFILTER**](d3ddisplaymodefilter.md) and [**D3DDISPLAYMODEEX**](d3ddisplaymodeex.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1cc05-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cc05-113">Requirements</span></span>



| <span data-ttu-id="1cc05-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cc05-114">Requirement</span></span> | <span data-ttu-id="1cc05-115">Value</span><span class="sxs-lookup"><span data-stu-id="1cc05-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1cc05-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1cc05-116">Header</span></span><br/> | <dl> <span data-ttu-id="1cc05-117"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cc05-117"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cc05-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="1cc05-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cc05-119">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="1cc05-119">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




