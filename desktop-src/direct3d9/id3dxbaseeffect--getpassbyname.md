---
description: Obtiene el identificador de un paso buscando su nombre.
ms.assetid: 24d043a2-5c87-4a59-80d4-0c81bd7a0b3e
title: 'ID3DXBaseEffect:: GetPassByName (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 2cd96a9d91f0e822b3e869bd8f0c965f0f951f44
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718513"
---
# <a name="id3dxbaseeffectgetpassbyname-method"></a><span data-ttu-id="f176f-103">ID3DXBaseEffect:: GetPassByName (método)</span><span class="sxs-lookup"><span data-stu-id="f176f-103">ID3DXBaseEffect::GetPassByName method</span></span>

<span data-ttu-id="f176f-104">Obtiene el identificador de un paso buscando su nombre.</span><span class="sxs-lookup"><span data-stu-id="f176f-104">Gets the handle of a pass by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="f176f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f176f-105">Syntax</span></span>


```C++
D3DXHANDLE GetPassByName(
  [in] D3DXHANDLE hTechnique,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="f176f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f176f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f176f-107">*hTechnique* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f176f-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f176f-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f176f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f176f-109">Identificador de la técnica primaria.</span><span class="sxs-lookup"><span data-stu-id="f176f-109">Handle of the parent technique.</span></span> <span data-ttu-id="f176f-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="f176f-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="f176f-111">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f176f-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f176f-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f176f-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f176f-113">Cadena que contiene el nombre del paso.</span><span class="sxs-lookup"><span data-stu-id="f176f-113">String containing the pass name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f176f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f176f-114">Return value</span></span>

<span data-ttu-id="f176f-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f176f-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f176f-116">Devuelve el identificador del primer paso dentro de la técnica especificada que tiene el nombre especificado, o **null** si no se encuentra el nombre.</span><span class="sxs-lookup"><span data-stu-id="f176f-116">Returns the handle of the first pass inside the specified technique that has the specified name, or **NULL** if the name was not found.</span></span> <span data-ttu-id="f176f-117">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="f176f-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f176f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f176f-118">Requirements</span></span>



| <span data-ttu-id="f176f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f176f-119">Requirement</span></span> | <span data-ttu-id="f176f-120">Value</span><span class="sxs-lookup"><span data-stu-id="f176f-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f176f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f176f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f176f-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f176f-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="f176f-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f176f-123">Library</span></span><br/> | <dl> <span data-ttu-id="f176f-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f176f-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f176f-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f176f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f176f-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="f176f-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
