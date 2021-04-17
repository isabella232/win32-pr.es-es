---
description: Establece una matriz de enteros.
ms.assetid: 1ceb8bb0-d168-49cf-8964-8ae582b5ec2e
title: 'ID3DXTextureShader:: SetIntArray (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetIntArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d2e43ac1451ec776339d7aba1a4b0288e948f43d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718236"
---
# <a name="id3dxtextureshadersetintarray-method"></a><span data-ttu-id="2fc10-103">ID3DXTextureShader:: SetIntArray (método)</span><span class="sxs-lookup"><span data-stu-id="2fc10-103">ID3DXTextureShader::SetIntArray method</span></span>

<span data-ttu-id="2fc10-104">Establece una matriz de enteros.</span><span class="sxs-lookup"><span data-stu-id="2fc10-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fc10-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2fc10-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       D3DXHANDLE hConstant,
  [in] const INT        *pn,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="2fc10-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2fc10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fc10-107">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2fc10-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc10-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2fc10-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2fc10-109">Identificador único de la matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="2fc10-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="2fc10-110">Vea [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="2fc10-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fc10-111">*PN* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2fc10-111">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc10-112">Tipo: **const [**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2fc10-112">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2fc10-113">Matriz de enteros.</span><span class="sxs-lookup"><span data-stu-id="2fc10-113">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="2fc10-114">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2fc10-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc10-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2fc10-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2fc10-116">Número de enteros de la matriz.</span><span class="sxs-lookup"><span data-stu-id="2fc10-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fc10-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2fc10-117">Return value</span></span>

<span data-ttu-id="2fc10-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2fc10-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2fc10-119">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2fc10-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2fc10-120">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2fc10-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fc10-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fc10-121">Requirements</span></span>



| <span data-ttu-id="2fc10-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fc10-122">Requirement</span></span> | <span data-ttu-id="2fc10-123">Value</span><span class="sxs-lookup"><span data-stu-id="2fc10-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fc10-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2fc10-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2fc10-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fc10-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2fc10-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2fc10-126">Library</span></span><br/> | <dl> <span data-ttu-id="2fc10-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2fc10-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2fc10-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="2fc10-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fc10-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="2fc10-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
