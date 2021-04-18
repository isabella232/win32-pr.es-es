---
title: D3DX11_EFFECT_VARIABLE_DESC estructura (D3dx11effect. h)
description: Describe una variable de efecto.
ms.assetid: 9c975ad4-b90e-4e69-b78f-4f5cc61083ff
keywords:
- D3DX11_EFFECT_VARIABLE_DESC estructura de Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_VARIABLE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a83121c930c5a634434161c998c72215e227f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998694"
---
# <a name="d3dx11_effect_variable_desc-structure"></a><span data-ttu-id="35d02-104">D3DX11 de la variable de efecto de la \_ \_ \_ estructura DESC</span><span class="sxs-lookup"><span data-stu-id="35d02-104">D3DX11\_EFFECT\_VARIABLE\_DESC structure</span></span>

<span data-ttu-id="35d02-105">Describe una variable de efecto.</span><span class="sxs-lookup"><span data-stu-id="35d02-105">Describes an effect variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="35d02-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35d02-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_VARIABLE_DESC {
  LPCSTR Name;
  LPCSTR Semantic;
  UINT   Flags;
  UINT   Annotations;
  UINT   BufferOffset;
  UINT   ExplicitBindPoint;
} D3DX11_EFFECT_VARIABLE_DESC;
```



## <a name="members"></a><span data-ttu-id="35d02-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="35d02-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="35d02-108">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="35d02-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="35d02-109">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="35d02-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="35d02-110">Nombre de esta variable, anotación o miembro de estructura.</span><span class="sxs-lookup"><span data-stu-id="35d02-110">Name of this variable, annotation, or structure member.</span></span>

</dd> <dt>

<span data-ttu-id="35d02-111">**Semántica**</span><span class="sxs-lookup"><span data-stu-id="35d02-111">**Semantic**</span></span>
</dt> <dd>

<span data-ttu-id="35d02-112">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="35d02-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="35d02-113">Cadena semántica de esta variable o miembro de estructura (NULL para las anotaciones o si no está presente).</span><span class="sxs-lookup"><span data-stu-id="35d02-113">Semantic string of this variable or structure member (NULL for annotations or if not present).</span></span>

</dd> <dt>

<span data-ttu-id="35d02-114">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="35d02-114">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="35d02-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="35d02-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="35d02-116">Marcas opcionales para las variables de efecto.</span><span class="sxs-lookup"><span data-stu-id="35d02-116">Optional flags for effect variables.</span></span>

</dd> <dt>

<span data-ttu-id="35d02-117">**Anotaciones**</span><span class="sxs-lookup"><span data-stu-id="35d02-117">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="35d02-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="35d02-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="35d02-119">Número de anotaciones en esta variable (siempre es 0 para las anotaciones).</span><span class="sxs-lookup"><span data-stu-id="35d02-119">Number of annotations on this variable (always 0 for annotations).</span></span>

</dd> <dt>

<span data-ttu-id="35d02-120">**BufferOffset**</span><span class="sxs-lookup"><span data-stu-id="35d02-120">**BufferOffset**</span></span>
</dt> <dd>

<span data-ttu-id="35d02-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="35d02-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="35d02-122">Desplazamiento en que contiene CBuffer o tbuffer (siempre es 0 para las anotaciones o variables que no están en búferes de constantes).</span><span class="sxs-lookup"><span data-stu-id="35d02-122">Offset into containing cbuffer or tbuffer (always 0 for annotations or variables not in constant buffers).</span></span>

</dd> <dt>

<span data-ttu-id="35d02-123">**ExplicitBindPoint**</span><span class="sxs-lookup"><span data-stu-id="35d02-123">**ExplicitBindPoint**</span></span>
</dt> <dd>

<span data-ttu-id="35d02-124">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="35d02-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="35d02-125">Se usa si la variable se ha enlazado explícitamente mediante la palabra clave Register.</span><span class="sxs-lookup"><span data-stu-id="35d02-125">Used if the variable has been explicitly bound using the register keyword.</span></span> <span data-ttu-id="35d02-126">Marque las marcas del \_ punto de enlace de variable de efecto de D3DX11 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="35d02-126">Check Flags for D3DX11\_EFFECT\_VARIABLE\_EXPLICIT\_BIND\_POINT.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35d02-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="35d02-127">Remarks</span></span>

<span data-ttu-id="35d02-128">La \_ \_ variable de efecto D3DX11 \_ desc se usa con [**ID3DX11EffectVariable:: GetDesc**](id3dx11effectvariable-getdesc.md).</span><span class="sxs-lookup"><span data-stu-id="35d02-128">D3DX11\_EFFECT\_VARIABLE\_DESC is used with [**ID3DX11EffectVariable::GetDesc**](id3dx11effectvariable-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35d02-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35d02-129">Requirements</span></span>



| <span data-ttu-id="35d02-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="35d02-130">Requirement</span></span> | <span data-ttu-id="35d02-131">Value</span><span class="sxs-lookup"><span data-stu-id="35d02-131">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="35d02-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35d02-132">Header</span></span><br/> | <dl> <span data-ttu-id="35d02-133"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="35d02-133"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35d02-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="35d02-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35d02-135">Effects 11 estructuras</span><span class="sxs-lookup"><span data-stu-id="35d02-135">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

