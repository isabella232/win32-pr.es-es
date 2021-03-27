---
title: D3DX11_EFFECT_TYPE_DESC estructura (D3dx11effect. h)
description: Describe un tipo de variable de efecto.
ms.assetid: bf2aa5b7-c68c-42bb-ae70-2fe16f8669a4
keywords:
- D3DX11_EFFECT_TYPE_DESC estructura de Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_TYPE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae0f4e8af391fed5717f47bb4b80398129cb98ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914798"
---
# <a name="d3dx11_effect_type_desc-structure"></a><span data-ttu-id="7c034-104">Tipo de efecto de D3DX11 ( \_ \_ \_ estructura DESC)</span><span class="sxs-lookup"><span data-stu-id="7c034-104">D3DX11\_EFFECT\_TYPE\_DESC structure</span></span>

<span data-ttu-id="7c034-105">Describe un tipo de variable de efecto.</span><span class="sxs-lookup"><span data-stu-id="7c034-105">Describes an effect-variable type.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c034-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c034-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_TYPE_DESC {
  LPCSTR                      TypeName;
  D3D10_SHADER_VARIABLE_CLASS Class;
  D3D10_SHADER_VARIABLE_TYPE  Type;
  UINT                        Elements;
  UINT                        Members;
  UINT                        Rows;
  UINT                        Columns;
  UINT                        PackedSize;
  UINT                        UnpackedSize;
  UINT                        Stride;
} D3DX11_EFFECT_TYPE_DESC;
```



## <a name="members"></a><span data-ttu-id="7c034-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7c034-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7c034-108">**TypeName**</span><span class="sxs-lookup"><span data-stu-id="7c034-108">**TypeName**</span></span>
</dt> <dd>

<span data-ttu-id="7c034-109">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7c034-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="7c034-110">Nombre del tipo, por ejemplo "FLOAT4" o "@ struct".</span><span class="sxs-lookup"><span data-stu-id="7c034-110">Name of the type, for example "float4" or "MyStruct".</span></span>

</dd> <dt>

<span data-ttu-id="7c034-111">**Clase**</span><span class="sxs-lookup"><span data-stu-id="7c034-111">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="7c034-112">Tipo: **[ **D3D10 \_ clase de \_ variable \_ de sombreador**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)**</span><span class="sxs-lookup"><span data-stu-id="7c034-112">Type: **[**D3D10\_SHADER\_VARIABLE\_CLASS**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)**</span></span>

</dd> <dd>

<span data-ttu-id="7c034-113">La clase variable (consulte [**\_ \_ \_ clase de variable de sombreador D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)).</span><span class="sxs-lookup"><span data-stu-id="7c034-113">The variable class (see [**D3D10\_SHADER\_VARIABLE\_CLASS**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)).</span></span>

</dd> <dt>

<span data-ttu-id="7c034-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7c034-114">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="7c034-115">Tipo: **[ **D3D10 \_ tipo de \_ variable \_ de sombreador**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)**</span><span class="sxs-lookup"><span data-stu-id="7c034-115">Type: **[**D3D10\_SHADER\_VARIABLE\_TYPE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)**</span></span>

</dd> <dd>

<span data-ttu-id="7c034-116">El tipo de variable (vea [**D3D10 (tipo de \_ \_ variable \_ de sombreador**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)).</span><span class="sxs-lookup"><span data-stu-id="7c034-116">The variable type (see [**D3D10\_SHADER\_VARIABLE\_TYPE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)).</span></span>

</dd> <dt>

<span data-ttu-id="7c034-117">**Elementos**</span><span class="sxs-lookup"><span data-stu-id="7c034-117">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="7c034-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7c034-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="7c034-119">Número de elementos de este tipo (0 si no es una matriz).</span><span class="sxs-lookup"><span data-stu-id="7c034-119">Number of elements in this type (0 if not an array).</span></span>

</dd> <dt>

<span data-ttu-id="7c034-120">**Miembros**</span><span class="sxs-lookup"><span data-stu-id="7c034-120">**Members**</span></span>
</dt> <dd>

<span data-ttu-id="7c034-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7c034-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="7c034-122">Número de miembros (0 si no es una estructura).</span><span class="sxs-lookup"><span data-stu-id="7c034-122">Number of members (0 if not a structure).</span></span>

</dd> <dt>

<span data-ttu-id="7c034-123">**Filas**</span><span class="sxs-lookup"><span data-stu-id="7c034-123">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="7c034-124">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7c034-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="7c034-125">Número de filas de este tipo (0 si no es un primitivo numérico).</span><span class="sxs-lookup"><span data-stu-id="7c034-125">Number of rows in this type (0 if not a numeric primitive).</span></span>

</dd> <dt>

<span data-ttu-id="7c034-126">**Columnas**</span><span class="sxs-lookup"><span data-stu-id="7c034-126">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="7c034-127">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7c034-127">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="7c034-128">Número de columnas de este tipo (0 si no es un primitivo numérico).</span><span class="sxs-lookup"><span data-stu-id="7c034-128">Number of columns in this type (0 if not a numeric primitive).</span></span>

</dd> <dt>

<span data-ttu-id="7c034-129">**PackedSize**</span><span class="sxs-lookup"><span data-stu-id="7c034-129">**PackedSize**</span></span>
</dt> <dd>

<span data-ttu-id="7c034-130">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7c034-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="7c034-131">Número de bytes necesarios para representar este tipo de datos, cuando está estrechamente empaquetado.</span><span class="sxs-lookup"><span data-stu-id="7c034-131">Number of bytes required to represent this data type, when tightly packed.</span></span>

</dd> <dt>

<span data-ttu-id="7c034-132">**UnpackedSize**</span><span class="sxs-lookup"><span data-stu-id="7c034-132">**UnpackedSize**</span></span>
</dt> <dd>

<span data-ttu-id="7c034-133">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7c034-133">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="7c034-134">Número de bytes ocupado por este tipo de datos, cuando se dispone en un búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="7c034-134">Number of bytes occupied by this data type, when laid out in a constant buffer.</span></span>

</dd> <dt>

<span data-ttu-id="7c034-135">**STRI**</span><span class="sxs-lookup"><span data-stu-id="7c034-135">**Stride**</span></span>
</dt> <dd>

<span data-ttu-id="7c034-136">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7c034-136">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="7c034-137">Número de bytes que se van a buscar entre los elementos, cuando se disponen en un búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="7c034-137">Number of bytes to seek between elements, when laid out in a constant buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c034-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c034-138">Remarks</span></span>

<span data-ttu-id="7c034-139">\_ \_ Tipo de efecto D3DX11 \_ desc se usa con [ **ID3DX11EffectType:: GetDesc**](id3dx11effecttype-getdesc.md)</span><span class="sxs-lookup"><span data-stu-id="7c034-139">D3DX11\_EFFECT\_TYPE\_DESC is used with [**ID3DX11EffectType::GetDesc**](id3dx11effecttype-getdesc.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="7c034-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c034-140">Requirements</span></span>



| <span data-ttu-id="7c034-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c034-141">Requirement</span></span> | <span data-ttu-id="7c034-142">Value</span><span class="sxs-lookup"><span data-stu-id="7c034-142">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c034-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c034-143">Header</span></span><br/> | <dl> <span data-ttu-id="7c034-144"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c034-144"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c034-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c034-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c034-146">Effects 11 estructuras</span><span class="sxs-lookup"><span data-stu-id="7c034-146">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

