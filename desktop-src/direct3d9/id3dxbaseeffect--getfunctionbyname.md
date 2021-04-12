---
description: Obtiene el identificador de una función buscando su nombre.
ms.assetid: 1e2e2dae-5084-47f3-9812-3dbf609bd70b
title: 'ID3DXBaseEffect:: GetFunctionByName (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunctionByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e1cd9ec56ff5df3bff293ade0669b4cd7c8dad5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362781"
---
# <a name="id3dxbaseeffectgetfunctionbyname-method"></a><span data-ttu-id="d9423-103">ID3DXBaseEffect:: GetFunctionByName (método)</span><span class="sxs-lookup"><span data-stu-id="d9423-103">ID3DXBaseEffect::GetFunctionByName method</span></span>

<span data-ttu-id="d9423-104">Obtiene el identificador de una función buscando su nombre.</span><span class="sxs-lookup"><span data-stu-id="d9423-104">Gets the handle of a function by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9423-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9423-105">Syntax</span></span>


```C++
D3DXHANDLE GetFunctionByName(
  [in] LPCSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="d9423-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9423-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9423-107">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d9423-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9423-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9423-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9423-109">Cadena que contiene el nombre de la función.</span><span class="sxs-lookup"><span data-stu-id="d9423-109">String containing the function name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9423-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9423-110">Return value</span></span>

<span data-ttu-id="d9423-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d9423-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d9423-112">Devuelve el identificador de la función especificada, o **null** si no se encuentra el nombre.</span><span class="sxs-lookup"><span data-stu-id="d9423-112">Returns the handle of the specified function, or **NULL** if the name was not found.</span></span> <span data-ttu-id="d9423-113">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="d9423-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9423-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9423-114">Requirements</span></span>



| <span data-ttu-id="d9423-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9423-115">Requirement</span></span> | <span data-ttu-id="d9423-116">Value</span><span class="sxs-lookup"><span data-stu-id="d9423-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9423-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d9423-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d9423-118"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9423-118"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="d9423-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d9423-119">Library</span></span><br/> | <dl> <span data-ttu-id="d9423-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9423-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d9423-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9423-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9423-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="d9423-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
