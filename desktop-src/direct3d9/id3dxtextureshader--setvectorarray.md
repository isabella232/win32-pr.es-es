---
description: Establece una matriz de vectores 4D.
ms.assetid: 45bc5cb1-b44a-468b-8c80-a639da8a033f
title: 'ID3DXTextureShader:: SetVectorArray (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetVectorArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c91a012cda9d1aa992682b5cb5aa769bf41de180
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670227"
---
# <a name="id3dxtextureshadersetvectorarray-method"></a><span data-ttu-id="4d957-103">ID3DXTextureShader:: SetVectorArray (método)</span><span class="sxs-lookup"><span data-stu-id="4d957-103">ID3DXTextureShader::SetVectorArray method</span></span>

<span data-ttu-id="4d957-104">Establece una matriz de vectores 4D.</span><span class="sxs-lookup"><span data-stu-id="4d957-104">Sets an array of 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d957-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d957-105">Syntax</span></span>


```C++
HRESULT SetVectorArray(
  [in]       D3DXHANDLE  hConstant,
  [in] const D3DXVECTOR4 *pVector,
  [in]       UINT        Count
);
```



## <a name="parameters"></a><span data-ttu-id="4d957-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d957-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d957-107">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4d957-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d957-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="4d957-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="4d957-109">Identificador único de la matriz de constantes de vector.</span><span class="sxs-lookup"><span data-stu-id="4d957-109">Unique identifier to the array of vector constants.</span></span> <span data-ttu-id="4d957-110">Vea [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="4d957-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d957-111">*pVector* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4d957-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d957-112">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="4d957-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="4d957-113">Matriz de vectores 4D.</span><span class="sxs-lookup"><span data-stu-id="4d957-113">Array of 4D vectors.</span></span> <span data-ttu-id="4d957-114">Vea [**D3DXVECTOR4**](d3dxvector4.md).</span><span class="sxs-lookup"><span data-stu-id="4d957-114">See [**D3DXVECTOR4**](d3dxvector4.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d957-115">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4d957-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d957-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4d957-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4d957-117">Número de vectores de la matriz.</span><span class="sxs-lookup"><span data-stu-id="4d957-117">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d957-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d957-118">Return value</span></span>

<span data-ttu-id="4d957-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4d957-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4d957-120">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4d957-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4d957-121">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="4d957-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d957-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d957-122">Requirements</span></span>



| <span data-ttu-id="4d957-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d957-123">Requirement</span></span> | <span data-ttu-id="4d957-124">Value</span><span class="sxs-lookup"><span data-stu-id="4d957-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d957-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4d957-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4d957-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d957-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="4d957-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4d957-127">Library</span></span><br/> | <dl> <span data-ttu-id="4d957-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d957-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4d957-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d957-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d957-130">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="4d957-130">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
