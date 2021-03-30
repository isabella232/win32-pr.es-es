---
description: Establece una matriz de números de punto flotante.
ms.assetid: 8e64b569-a6bf-4925-9d21-4df0b6661ee2
title: 'ID3DXTextureShader:: SetFloatArray (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetFloatArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5dbd39e8a4acfa004fb623d578e5922d477884fc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280345"
---
# <a name="id3dxtextureshadersetfloatarray-method"></a><span data-ttu-id="5c135-103">ID3DXTextureShader:: SetFloatArray (método)</span><span class="sxs-lookup"><span data-stu-id="5c135-103">ID3DXTextureShader::SetFloatArray method</span></span>

<span data-ttu-id="5c135-104">Establece una matriz de números de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="5c135-104">Sets an array of floating-point numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c135-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c135-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       D3DXHANDLE hConstant,
  [in] const FLOAT      *pf,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="5c135-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c135-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c135-107">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5c135-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c135-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5c135-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5c135-109">Identificador único de la matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="5c135-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="5c135-110">Vea [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="5c135-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c135-111">*PF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5c135-111">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c135-112">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="5c135-112">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5c135-113">Matriz de números de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="5c135-113">Array of floating-point numbers.</span></span>

</dd> <dt>

<span data-ttu-id="5c135-114">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5c135-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c135-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c135-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5c135-116">Número de valores de punto flotante de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5c135-116">Number of floating-point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c135-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c135-117">Return value</span></span>

<span data-ttu-id="5c135-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5c135-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5c135-119">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5c135-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5c135-120">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5c135-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c135-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c135-121">Requirements</span></span>



| <span data-ttu-id="5c135-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c135-122">Requirement</span></span> | <span data-ttu-id="5c135-123">Value</span><span class="sxs-lookup"><span data-stu-id="5c135-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c135-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c135-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5c135-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c135-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5c135-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5c135-126">Library</span></span><br/> | <dl> <span data-ttu-id="5c135-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c135-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5c135-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c135-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c135-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="5c135-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
