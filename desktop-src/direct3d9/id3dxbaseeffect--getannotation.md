---
description: Obtiene el identificador de una anotación.
ms.assetid: 433d73b7-9371-4d76-8b34-a64c608eb1a3
title: 'ID3DXBaseEffect:: GetAnnotation (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotation
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: aad446e436478c8c7673a1919879983437fd9602
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718520"
---
# <a name="id3dxbaseeffectgetannotation-method"></a><span data-ttu-id="65df1-103">ID3DXBaseEffect:: GetAnnotation (método)</span><span class="sxs-lookup"><span data-stu-id="65df1-103">ID3DXBaseEffect::GetAnnotation method</span></span>

<span data-ttu-id="65df1-104">Obtiene el identificador de una anotación.</span><span class="sxs-lookup"><span data-stu-id="65df1-104">Gets the handle of an annotation.</span></span>

## <a name="syntax"></a><span data-ttu-id="65df1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65df1-105">Syntax</span></span>


```C++
D3DXHANDLE GetAnnotation(
  [in] D3DXHANDLE hObject,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="65df1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65df1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65df1-107">*hObject* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="65df1-107">*hObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65df1-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="65df1-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="65df1-109">Identificador de una técnica, un paso o un parámetro de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="65df1-109">Handle of a technique, pass, or top-level parameter.</span></span> <span data-ttu-id="65df1-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="65df1-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="65df1-111">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="65df1-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65df1-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65df1-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="65df1-113">Índice de anotación.</span><span class="sxs-lookup"><span data-stu-id="65df1-113">Annotation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65df1-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65df1-114">Return value</span></span>

<span data-ttu-id="65df1-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="65df1-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="65df1-116">Devuelve el identificador de la anotación especificada o **null** si el índice no era válido.</span><span class="sxs-lookup"><span data-stu-id="65df1-116">Returns the handle of the specified annotation, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="65df1-117">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="65df1-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="65df1-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65df1-118">Remarks</span></span>

<span data-ttu-id="65df1-119">Las anotaciones son datos específicos del usuario que se pueden adjuntar a cualquier técnica, paso o parámetro.</span><span class="sxs-lookup"><span data-stu-id="65df1-119">Annotations are user-specific data that can be attached to any technique, pass, or parameter.</span></span> <span data-ttu-id="65df1-120">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="65df1-120">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="65df1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65df1-121">Requirements</span></span>



| <span data-ttu-id="65df1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="65df1-122">Requirement</span></span> | <span data-ttu-id="65df1-123">Value</span><span class="sxs-lookup"><span data-stu-id="65df1-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="65df1-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65df1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="65df1-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="65df1-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="65df1-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="65df1-126">Library</span></span><br/> | <dl> <span data-ttu-id="65df1-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65df1-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="65df1-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="65df1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65df1-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="65df1-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
