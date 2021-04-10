---
description: Describe una técnica utilizada por un efecto.
ms.assetid: 7ba2dbb3-8039-4d1c-ad9d-130d9bf3d80a
title: D3DXTECHNIQUE_DESC estructura (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTECHNIQUE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 35dd483a983f17371d6a77e6c020b3a45d9e9360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083716"
---
# <a name="d3dxtechnique_desc-structure"></a><span data-ttu-id="b5831-103">D3DXTECHNIQUE \_ DESC (estructura)</span><span class="sxs-lookup"><span data-stu-id="b5831-103">D3DXTECHNIQUE\_DESC structure</span></span>

<span data-ttu-id="b5831-104">Describe una técnica utilizada por un efecto.</span><span class="sxs-lookup"><span data-stu-id="b5831-104">Describes a technique used by an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5831-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5831-105">Syntax</span></span>


```C++
typedef struct D3DXTECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DXTECHNIQUE_DESC, *LPD3DXTECHNIQUE_DESC;
```



## <a name="members"></a><span data-ttu-id="b5831-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="b5831-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b5831-107">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="b5831-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="b5831-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5831-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b5831-109">Cadena que contiene el nombre de la técnica.</span><span class="sxs-lookup"><span data-stu-id="b5831-109">String that contains the technique name.</span></span>

</dd> <dt>

<span data-ttu-id="b5831-110">**Paso**</span><span class="sxs-lookup"><span data-stu-id="b5831-110">**Passes**</span></span>
</dt> <dd>

<span data-ttu-id="b5831-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5831-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b5831-112">Número de pasos de representación que requiere la técnica.</span><span class="sxs-lookup"><span data-stu-id="b5831-112">Number of rendering passes the technique requires.</span></span> <span data-ttu-id="b5831-113">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="b5831-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b5831-114">**Anotaciones**</span><span class="sxs-lookup"><span data-stu-id="b5831-114">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="b5831-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5831-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b5831-116">Número de anotaciones.</span><span class="sxs-lookup"><span data-stu-id="b5831-116">The number of annotations.</span></span> <span data-ttu-id="b5831-117">Consulte [Agregar información a los parámetros de efectos con \_ anotaciones](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="b5831-117">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5831-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5831-118">Remarks</span></span>

<span data-ttu-id="b5831-119">Algunas tarjetas de vídeo pueden representar dos texturas en un solo paso.</span><span class="sxs-lookup"><span data-stu-id="b5831-119">Some video cards can render two textures in a single pass.</span></span> <span data-ttu-id="b5831-120">Sin embargo, si una tarjeta no tiene esta capacidad, a menudo es posible representar el mismo efecto en dos pasos, utilizando una textura para cada paso.</span><span class="sxs-lookup"><span data-stu-id="b5831-120">However, if a card does not have this capability, it is often possible to render the same effect in two passes, using one texture for each pass.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5831-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5831-121">Requirements</span></span>



| <span data-ttu-id="b5831-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5831-122">Requirement</span></span> | <span data-ttu-id="b5831-123">Value</span><span class="sxs-lookup"><span data-stu-id="b5831-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5831-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5831-124">Header</span></span><br/> | <dl> <span data-ttu-id="b5831-125"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5831-125"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5831-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5831-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5831-127">Estructuras de efectos</span><span class="sxs-lookup"><span data-stu-id="b5831-127">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
