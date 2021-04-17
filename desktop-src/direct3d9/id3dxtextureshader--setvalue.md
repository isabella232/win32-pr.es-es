---
description: Establece la tabla de constantes con los datos en el búfer.
ms.assetid: 55cf5456-8f23-405d-9329-8ff737c5c139
title: 'ID3DXTextureShader:: SetValue (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetValue
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2f18902c73f44bc4294e5152f8da5ea3e37f27ba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670217"
---
# <a name="id3dxtextureshadersetvalue-method"></a><span data-ttu-id="f8545-103">ID3DXTextureShader:: SetValue (método)</span><span class="sxs-lookup"><span data-stu-id="f8545-103">ID3DXTextureShader::SetValue method</span></span>

<span data-ttu-id="f8545-104">Establece la tabla de constantes con los datos en el búfer.</span><span class="sxs-lookup"><span data-stu-id="f8545-104">Sets the constant table with the data in the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8545-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8545-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in] D3DXHANDLE hConstant,
  [in] LPCVOID    pData,
  [in] UINT       Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="f8545-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8545-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8545-107">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f8545-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8545-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f8545-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f8545-109">Identificador único de una constante.</span><span class="sxs-lookup"><span data-stu-id="f8545-109">Unique identifier to a constant.</span></span> <span data-ttu-id="f8545-110">Vea [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="f8545-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8545-111">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f8545-111">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8545-112">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8545-112">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f8545-113">Un puntero a un búfer que contiene los datos de constante.</span><span class="sxs-lookup"><span data-stu-id="f8545-113">A pointer to a buffer containing the constant data.</span></span>

</dd> <dt>

<span data-ttu-id="f8545-114">*Bytes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f8545-114">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8545-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8545-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f8545-116">Tamaño del búfer, en bytes.</span><span class="sxs-lookup"><span data-stu-id="f8545-116">Size of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8545-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8545-117">Return value</span></span>

<span data-ttu-id="f8545-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f8545-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f8545-119">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f8545-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f8545-120">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f8545-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8545-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8545-121">Requirements</span></span>



| <span data-ttu-id="f8545-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8545-122">Requirement</span></span> | <span data-ttu-id="f8545-123">Value</span><span class="sxs-lookup"><span data-stu-id="f8545-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8545-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8545-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f8545-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8545-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f8545-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f8545-126">Library</span></span><br/> | <dl> <span data-ttu-id="f8545-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8545-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f8545-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8545-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8545-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="f8545-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
