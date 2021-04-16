---
description: Obtiene un entero.
ms.assetid: 8074758a-f650-4698-8a75-aa0ffb14cb21
title: 'ID3DXBaseEffect:: GetInt (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetInt
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c0fe1fa01260be936b9d7f8be394d0c43a781680
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708087"
---
# <a name="id3dxbaseeffectgetint-method"></a><span data-ttu-id="b7e1f-103">ID3DXBaseEffect:: GetInt (método)</span><span class="sxs-lookup"><span data-stu-id="b7e1f-103">ID3DXBaseEffect::GetInt method</span></span>

<span data-ttu-id="b7e1f-104">Obtiene un entero.</span><span class="sxs-lookup"><span data-stu-id="b7e1f-104">Gets an integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7e1f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7e1f-105">Syntax</span></span>


```C++
HRESULT GetInt(
  [in]  D3DXHANDLE hParameter,
  [out] INT        *pn
);
```



## <a name="parameters"></a><span data-ttu-id="b7e1f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7e1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7e1f-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b7e1f-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7e1f-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b7e1f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b7e1f-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="b7e1f-109">Unique identifier.</span></span> <span data-ttu-id="b7e1f-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="b7e1f-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7e1f-111">*PN* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b7e1f-111">*pn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7e1f-112">Tipo: **[ **int**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b7e1f-112">Type: **[**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b7e1f-113">Devuelve un entero.</span><span class="sxs-lookup"><span data-stu-id="b7e1f-113">Returns an integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7e1f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b7e1f-114">Return value</span></span>

<span data-ttu-id="b7e1f-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b7e1f-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b7e1f-116">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b7e1f-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b7e1f-117">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b7e1f-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7e1f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7e1f-118">Requirements</span></span>



| <span data-ttu-id="b7e1f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7e1f-119">Requirement</span></span> | <span data-ttu-id="b7e1f-120">Value</span><span class="sxs-lookup"><span data-stu-id="b7e1f-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7e1f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b7e1f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b7e1f-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7e1f-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b7e1f-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b7e1f-123">Library</span></span><br/> | <dl> <span data-ttu-id="b7e1f-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7e1f-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b7e1f-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7e1f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7e1f-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="b7e1f-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="b7e1f-127">**SetInt**</span><span class="sxs-lookup"><span data-stu-id="b7e1f-127">**SetInt**</span></span>](id3dxbaseeffect--setint.md)
</dt> </dl>

 

 
