---
description: Establece un vector 4D.
ms.assetid: befed2a8-7695-4f06-a6ee-aff466d1940a
title: 'ID3DXTextureShader:: SetVector (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetVector
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b7bc7e3b7f4920c21c52111410c626090e452fa7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670228"
---
# <a name="id3dxtextureshadersetvector-method"></a><span data-ttu-id="9f4aa-103">ID3DXTextureShader:: SetVector (método)</span><span class="sxs-lookup"><span data-stu-id="9f4aa-103">ID3DXTextureShader::SetVector method</span></span>

<span data-ttu-id="9f4aa-104">Establece un vector 4D.</span><span class="sxs-lookup"><span data-stu-id="9f4aa-104">Sets a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f4aa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f4aa-105">Syntax</span></span>


```C++
HRESULT SetVector(
  [in]       D3DXHANDLE  hConstant,
  [in] const D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="9f4aa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f4aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f4aa-107">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9f4aa-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f4aa-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="9f4aa-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="9f4aa-109">Identificador único de la constante de vector.</span><span class="sxs-lookup"><span data-stu-id="9f4aa-109">Unique identifier to the vector constant.</span></span> <span data-ttu-id="9f4aa-110">Vea [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="9f4aa-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f4aa-111">*pVector* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9f4aa-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f4aa-112">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="9f4aa-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="9f4aa-113">Puntero a un vector 4D.</span><span class="sxs-lookup"><span data-stu-id="9f4aa-113">Pointer to a 4D vector.</span></span> <span data-ttu-id="9f4aa-114">Vea [**D3DXVECTOR4**](d3dxvector4.md).</span><span class="sxs-lookup"><span data-stu-id="9f4aa-114">See [**D3DXVECTOR4**](d3dxvector4.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f4aa-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9f4aa-115">Return value</span></span>

<span data-ttu-id="9f4aa-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9f4aa-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9f4aa-117">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9f4aa-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9f4aa-118">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="9f4aa-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f4aa-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f4aa-119">Requirements</span></span>



| <span data-ttu-id="9f4aa-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f4aa-120">Requirement</span></span> | <span data-ttu-id="9f4aa-121">Value</span><span class="sxs-lookup"><span data-stu-id="9f4aa-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f4aa-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f4aa-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9f4aa-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f4aa-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="9f4aa-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9f4aa-124">Library</span></span><br/> | <dl> <span data-ttu-id="9f4aa-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f4aa-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9f4aa-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f4aa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f4aa-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="9f4aa-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




