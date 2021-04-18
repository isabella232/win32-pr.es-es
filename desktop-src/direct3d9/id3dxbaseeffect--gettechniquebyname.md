---
description: Obtiene el identificador de una técnica buscando su nombre.
ms.assetid: 34871229-ad63-4575-8c60-f27d7f7dddce
title: 'ID3DXBaseEffect:: GetTechniqueByName (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechniqueByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5827527bf5151b121958c3f5803ef8a7e74f8d60
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718509"
---
# <a name="id3dxbaseeffectgettechniquebyname-method"></a><span data-ttu-id="56dd1-103">ID3DXBaseEffect:: GetTechniqueByName (método)</span><span class="sxs-lookup"><span data-stu-id="56dd1-103">ID3DXBaseEffect::GetTechniqueByName method</span></span>

<span data-ttu-id="56dd1-104">Obtiene el identificador de una técnica buscando su nombre.</span><span class="sxs-lookup"><span data-stu-id="56dd1-104">Gets the handle of a technique by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="56dd1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56dd1-105">Syntax</span></span>


```C++
D3DXHANDLE GetTechniqueByName(
  [in] LPCSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="56dd1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="56dd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56dd1-107">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="56dd1-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56dd1-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="56dd1-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="56dd1-109">Cadena que contiene el nombre de la técnica.</span><span class="sxs-lookup"><span data-stu-id="56dd1-109">String containing the technique name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56dd1-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="56dd1-110">Return value</span></span>

<span data-ttu-id="56dd1-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="56dd1-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="56dd1-112">Devuelve el identificador de la primera técnica que tiene el nombre especificado, o **null** si no se encuentra el nombre.</span><span class="sxs-lookup"><span data-stu-id="56dd1-112">Returns the handle of the first technique that has the specified name, or **NULL** if the name was not found.</span></span> <span data-ttu-id="56dd1-113">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="56dd1-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="56dd1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56dd1-114">Requirements</span></span>



| <span data-ttu-id="56dd1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="56dd1-115">Requirement</span></span> | <span data-ttu-id="56dd1-116">Value</span><span class="sxs-lookup"><span data-stu-id="56dd1-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="56dd1-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56dd1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="56dd1-118"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="56dd1-118"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="56dd1-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="56dd1-119">Library</span></span><br/> | <dl> <span data-ttu-id="56dd1-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56dd1-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="56dd1-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="56dd1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56dd1-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="56dd1-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
