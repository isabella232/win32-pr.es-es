---
description: Obtiene el identificador de un parámetro de nivel superior o un parámetro de miembro de estructura buscando su nombre.
ms.assetid: fb03685e-e512-4293-80d7-6c2c0fc9ebfd
title: 'ID3DXBaseEffect:: GetParameterByName (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f9f7457ffa3bba867d03cceb3521664fecc9d67d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003968"
---
# <a name="id3dxbaseeffectgetparameterbyname-method"></a><span data-ttu-id="593dd-103">ID3DXBaseEffect:: GetParameterByName (método)</span><span class="sxs-lookup"><span data-stu-id="593dd-103">ID3DXBaseEffect::GetParameterByName method</span></span>

<span data-ttu-id="593dd-104">Obtiene el identificador de un parámetro de nivel superior o un parámetro de miembro de estructura buscando su nombre.</span><span class="sxs-lookup"><span data-stu-id="593dd-104">Gets the handle of a top-level parameter or a structure member parameter by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="593dd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="593dd-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameterByName(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="593dd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="593dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="593dd-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="593dd-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="593dd-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="593dd-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="593dd-109">Identificador del parámetro o **null** para los parámetros de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="593dd-109">Handle of the parameter, or **NULL** for top-level parameters.</span></span> <span data-ttu-id="593dd-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="593dd-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="593dd-111">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="593dd-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="593dd-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="593dd-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="593dd-113">Cadena que contiene el nombre del parámetro.</span><span class="sxs-lookup"><span data-stu-id="593dd-113">String containing the parameter name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="593dd-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="593dd-114">Return value</span></span>

<span data-ttu-id="593dd-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="593dd-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="593dd-116">Devuelve el identificador del parámetro especificado, o **null** si el índice no era válido.</span><span class="sxs-lookup"><span data-stu-id="593dd-116">Returns the handle of the specified parameter, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="593dd-117">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="593dd-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="593dd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="593dd-118">Requirements</span></span>



| <span data-ttu-id="593dd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="593dd-119">Requirement</span></span> | <span data-ttu-id="593dd-120">Value</span><span class="sxs-lookup"><span data-stu-id="593dd-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="593dd-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="593dd-121">Header</span></span><br/>  | <dl> <span data-ttu-id="593dd-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="593dd-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="593dd-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="593dd-123">Library</span></span><br/> | <dl> <span data-ttu-id="593dd-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="593dd-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="593dd-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="593dd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="593dd-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="593dd-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
