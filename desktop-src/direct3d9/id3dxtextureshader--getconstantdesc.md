---
description: Obtiene un puntero a la matriz de constantes de la tabla de constantes.
ms.assetid: 2476344b-8433-46bb-9242-dff84e3168e7
title: 'ID3DXTextureShader:: GetConstantDesc (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 22898880e5cef5669defae89cda4f7d9818f9f1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708030"
---
# <a name="id3dxtextureshadergetconstantdesc-method"></a><span data-ttu-id="d1552-103">ID3DXTextureShader:: GetConstantDesc (método)</span><span class="sxs-lookup"><span data-stu-id="d1552-103">ID3DXTextureShader::GetConstantDesc method</span></span>

<span data-ttu-id="d1552-104">Obtiene un puntero a la matriz de constantes de la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="d1552-104">Gets a pointer to the array of constants in the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1552-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1552-105">Syntax</span></span>


```C++
HRESULT GetConstantDesc(
  [in]      D3DXHANDLE        hConstant,
  [in, out] D3DXCONSTANT_DESC *pDesc,
  [in, out] UINT              *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="d1552-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1552-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1552-107">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d1552-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1552-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d1552-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d1552-109">Identificador único de una constante.</span><span class="sxs-lookup"><span data-stu-id="d1552-109">Unique identifier to a constant.</span></span> <span data-ttu-id="d1552-110">Vea [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="d1552-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1552-111">*pDesc* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d1552-111">*pDesc* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1552-112">Tipo: **[ **D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="d1552-112">Type: **[**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md)\***</span></span>

<span data-ttu-id="d1552-113">Devuelve un puntero a una matriz de descripciones.</span><span class="sxs-lookup"><span data-stu-id="d1552-113">Returns a pointer to an array of descriptions.</span></span> <span data-ttu-id="d1552-114">Vea [**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md).</span><span class="sxs-lookup"><span data-stu-id="d1552-114">See [**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1552-115">*pCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d1552-115">*pCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1552-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d1552-116">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d1552-117">La entrada proporcionada debe ser el tamaño máximo de la matriz.</span><span class="sxs-lookup"><span data-stu-id="d1552-117">The input supplied must be the maximum size of the array.</span></span> <span data-ttu-id="d1552-118">El resultado es el número de elementos que se rellenan en la matriz cuando la función devuelve.</span><span class="sxs-lookup"><span data-stu-id="d1552-118">The output is the number of elements that are filled in the array when the function returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1552-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1552-119">Return value</span></span>

<span data-ttu-id="d1552-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d1552-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d1552-121">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d1552-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d1552-122">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="d1552-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1552-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1552-123">Remarks</span></span>

<span data-ttu-id="d1552-124">Los muestreadores pueden aparecer más de una vez en una tabla de constantes; por lo tanto, este método puede devolver una matriz de descripciones con un índice de registro diferente.</span><span class="sxs-lookup"><span data-stu-id="d1552-124">Samplers can appear more than once in a constant table, therefore, this method can return an array of descriptions each with a different register index.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1552-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1552-125">Requirements</span></span>



| <span data-ttu-id="d1552-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1552-126">Requirement</span></span> | <span data-ttu-id="d1552-127">Value</span><span class="sxs-lookup"><span data-stu-id="d1552-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1552-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1552-128">Header</span></span><br/>  | <dl> <span data-ttu-id="d1552-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1552-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d1552-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d1552-130">Library</span></span><br/> | <dl> <span data-ttu-id="d1552-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1552-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d1552-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1552-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1552-133">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="d1552-133">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> <dt>

[<span data-ttu-id="d1552-134">**ID3DXTextureShader::GetDesc**</span><span class="sxs-lookup"><span data-stu-id="d1552-134">**ID3DXTextureShader::GetDesc**</span></span>](id3dxtextureshader--getdesc.md)
</dt> </dl>

 

 
