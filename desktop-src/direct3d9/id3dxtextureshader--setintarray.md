---
description: 'Método ID3DXTextureShader::SetIntArray: establece una matriz de enteros.'
ms.assetid: 1ceb8bb0-d168-49cf-8964-8ae582b5ec2e
title: Método ID3DXTextureShader::SetIntArray (D3DX9Shader.h)
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
ms.openlocfilehash: 0ddc00637bddf2810e73be7755a9dcfb8696053e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097493"
---
# <a name="id3dxtextureshadersetintarray-method"></a><span data-ttu-id="2f783-103">Método ID3DXTextureShader::SetIntArray</span><span class="sxs-lookup"><span data-stu-id="2f783-103">ID3DXTextureShader::SetIntArray method</span></span>

<span data-ttu-id="2f783-104">Establece una matriz de enteros.</span><span class="sxs-lookup"><span data-stu-id="2f783-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f783-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f783-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       D3DXHANDLE hConstant,
  [in] const INT        *pn,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="2f783-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f783-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f783-107">*hConstant* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2f783-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f783-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2f783-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2f783-109">Identificador único de la matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="2f783-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="2f783-110">Vea [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="2f783-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f783-111">*pn* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2f783-111">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f783-112">Tipo: **const [**INT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2f783-112">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2f783-113">Matriz de enteros.</span><span class="sxs-lookup"><span data-stu-id="2f783-113">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="2f783-114">*Recuento* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2f783-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f783-115">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f783-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f783-116">Número de enteros de la matriz.</span><span class="sxs-lookup"><span data-stu-id="2f783-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f783-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f783-117">Return value</span></span>

<span data-ttu-id="2f783-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2f783-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2f783-119">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2f783-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2f783-120">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2f783-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f783-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f783-121">Requirements</span></span>



| <span data-ttu-id="2f783-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f783-122">Requirement</span></span> | <span data-ttu-id="2f783-123">Value</span><span class="sxs-lookup"><span data-stu-id="2f783-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f783-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f783-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2f783-125"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="2f783-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2f783-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f783-126">Library</span></span><br/> | <dl> <span data-ttu-id="2f783-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f783-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2f783-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2f783-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f783-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="2f783-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
