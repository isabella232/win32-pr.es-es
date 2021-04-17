---
description: Obtiene el identificador de una anotación buscando su nombre.
ms.assetid: da4e2805-5f06-4a9b-836f-85a8c154c502
title: 'ID3DXBaseEffect:: GetAnnotationByName (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotationByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 00698030488b8f4ae788367f87b8d569476292ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698416"
---
# <a name="id3dxbaseeffectgetannotationbyname-method"></a><span data-ttu-id="2a181-103">ID3DXBaseEffect:: GetAnnotationByName (método)</span><span class="sxs-lookup"><span data-stu-id="2a181-103">ID3DXBaseEffect::GetAnnotationByName method</span></span>

<span data-ttu-id="2a181-104">Obtiene el identificador de una anotación buscando su nombre.</span><span class="sxs-lookup"><span data-stu-id="2a181-104">Gets the handle of an annotation by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a181-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a181-105">Syntax</span></span>


```C++
D3DXHANDLE GetAnnotationByName(
  [in] D3DXHANDLE hObject,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="2a181-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a181-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a181-107">*hObject* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2a181-107">*hObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a181-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2a181-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2a181-109">Identificador de una técnica, un paso o un parámetro de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="2a181-109">Handle of a technique, pass, or top-level parameter.</span></span> <span data-ttu-id="2a181-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="2a181-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a181-111">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2a181-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a181-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a181-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2a181-113">Cadena que contiene el nombre de la anotación.</span><span class="sxs-lookup"><span data-stu-id="2a181-113">String containing the annotation name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a181-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a181-114">Return value</span></span>

<span data-ttu-id="2a181-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2a181-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2a181-116">Devuelve el identificador de la anotación especificada o **null** si no se encuentra el nombre.</span><span class="sxs-lookup"><span data-stu-id="2a181-116">Returns the handle of the specified annotation, or **NULL** if the name was not found.</span></span> <span data-ttu-id="2a181-117">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="2a181-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a181-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a181-118">Requirements</span></span>



| <span data-ttu-id="2a181-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a181-119">Requirement</span></span> | <span data-ttu-id="2a181-120">Value</span><span class="sxs-lookup"><span data-stu-id="2a181-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a181-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2a181-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2a181-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a181-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="2a181-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2a181-123">Library</span></span><br/> | <dl> <span data-ttu-id="2a181-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a181-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2a181-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a181-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a181-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="2a181-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
