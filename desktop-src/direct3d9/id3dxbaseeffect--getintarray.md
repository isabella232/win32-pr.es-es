---
description: Obtiene una matriz de enteros.
ms.assetid: c02b5343-db4f-4e8c-989c-6aba8c19c234
title: 'ID3DXBaseEffect:: GetIntArray (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetIntArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f13c6b8717c2108920d7b914da20b99f0451f5d9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362779"
---
# <a name="id3dxbaseeffectgetintarray-method"></a><span data-ttu-id="d0845-103">ID3DXBaseEffect:: GetIntArray (método)</span><span class="sxs-lookup"><span data-stu-id="d0845-103">ID3DXBaseEffect::GetIntArray method</span></span>

<span data-ttu-id="d0845-104">Obtiene una matriz de enteros.</span><span class="sxs-lookup"><span data-stu-id="d0845-104">Gets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0845-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0845-105">Syntax</span></span>


```C++
HRESULT GetIntArray(
  [in]  D3DXHANDLE hParameter,
  [out] INT        *pn,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="d0845-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0845-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0845-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d0845-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0845-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d0845-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d0845-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="d0845-109">Unique identifier.</span></span> <span data-ttu-id="d0845-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="d0845-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0845-111">*PN* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d0845-111">*pn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0845-112">Tipo: **[ **int**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d0845-112">Type: **[**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d0845-113">Devuelve una matriz de enteros.</span><span class="sxs-lookup"><span data-stu-id="d0845-113">Returns an array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="d0845-114">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d0845-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0845-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0845-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d0845-116">Número de enteros de la matriz.</span><span class="sxs-lookup"><span data-stu-id="d0845-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0845-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0845-117">Return value</span></span>

<span data-ttu-id="d0845-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d0845-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d0845-119">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d0845-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d0845-120">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d0845-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0845-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0845-121">Requirements</span></span>



| <span data-ttu-id="d0845-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0845-122">Requirement</span></span> | <span data-ttu-id="d0845-123">Value</span><span class="sxs-lookup"><span data-stu-id="d0845-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0845-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0845-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d0845-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0845-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d0845-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d0845-126">Library</span></span><br/> | <dl> <span data-ttu-id="d0845-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0845-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d0845-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0845-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0845-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="d0845-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="d0845-130">**SetIntArray**</span><span class="sxs-lookup"><span data-stu-id="d0845-130">**SetIntArray**</span></span>](id3dxbaseeffect--setintarray.md)
</dt> </dl>

 

 
