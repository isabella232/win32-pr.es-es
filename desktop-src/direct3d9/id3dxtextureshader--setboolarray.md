---
description: Establece una matriz de valores BOOL.
ms.assetid: d168d362-86b3-4db4-bc52-748a640ebc18
title: 'ID3DXTextureShader:: SetBoolArray (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetBoolArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0799e4ef9d35a886e59fae44c37a841bcda3aed6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698365"
---
# <a name="id3dxtextureshadersetboolarray-method"></a><span data-ttu-id="a1f9f-103">ID3DXTextureShader:: SetBoolArray (método)</span><span class="sxs-lookup"><span data-stu-id="a1f9f-103">ID3DXTextureShader::SetBoolArray method</span></span>

<span data-ttu-id="a1f9f-104">Establece una matriz de valores BOOL.</span><span class="sxs-lookup"><span data-stu-id="a1f9f-104">Sets an array of BOOL values.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1f9f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1f9f-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       D3DXHANDLE hConstant,
  [in] const BOOL       *pB,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="a1f9f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1f9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1f9f-107">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a1f9f-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1f9f-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a1f9f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a1f9f-109">Identificador único de la matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="a1f9f-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="a1f9f-110">Vea [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="a1f9f-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1f9f-111">*PB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a1f9f-111">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1f9f-112">Tipo: **const [**bool**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="a1f9f-112">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a1f9f-113">Matriz de valores BOOL.</span><span class="sxs-lookup"><span data-stu-id="a1f9f-113">Array of BOOL values.</span></span>

</dd> <dt>

<span data-ttu-id="a1f9f-114">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a1f9f-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1f9f-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1f9f-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1f9f-116">Número de valores BOOLEANOs de la matriz.</span><span class="sxs-lookup"><span data-stu-id="a1f9f-116">Number of BOOL values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1f9f-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a1f9f-117">Return value</span></span>

<span data-ttu-id="a1f9f-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a1f9f-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a1f9f-119">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a1f9f-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a1f9f-120">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a1f9f-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1f9f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1f9f-121">Requirements</span></span>



| <span data-ttu-id="a1f9f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1f9f-122">Requirement</span></span> | <span data-ttu-id="a1f9f-123">Value</span><span class="sxs-lookup"><span data-stu-id="a1f9f-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1f9f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1f9f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a1f9f-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1f9f-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a1f9f-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a1f9f-126">Library</span></span><br/> | <dl> <span data-ttu-id="a1f9f-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1f9f-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a1f9f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1f9f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1f9f-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="a1f9f-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
