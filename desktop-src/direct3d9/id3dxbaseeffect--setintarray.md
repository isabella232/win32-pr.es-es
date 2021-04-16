---
description: Establece una matriz de enteros.
ms.assetid: 4491bffd-ce5e-4f84-ac11-0314a1b16d63
title: 'ID3DXBaseEffect:: SetIntArray (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetIntArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f76ff0d7f4bcc68d7cce85f3d02f2bc207a5f4b1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649371"
---
# <a name="id3dxbaseeffectsetintarray-method"></a><span data-ttu-id="05c00-103">ID3DXBaseEffect:: SetIntArray (método)</span><span class="sxs-lookup"><span data-stu-id="05c00-103">ID3DXBaseEffect::SetIntArray method</span></span>

<span data-ttu-id="05c00-104">Establece una matriz de enteros.</span><span class="sxs-lookup"><span data-stu-id="05c00-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="05c00-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05c00-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       D3DXHANDLE hParameter,
  [in] const INT        *pn,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="05c00-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05c00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05c00-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="05c00-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05c00-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="05c00-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="05c00-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="05c00-109">Unique identifier.</span></span> <span data-ttu-id="05c00-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="05c00-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="05c00-111">*PN* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="05c00-111">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05c00-112">Tipo: **const [**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="05c00-112">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="05c00-113">Matriz de enteros.</span><span class="sxs-lookup"><span data-stu-id="05c00-113">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="05c00-114">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="05c00-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05c00-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="05c00-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="05c00-116">Número de enteros de la matriz.</span><span class="sxs-lookup"><span data-stu-id="05c00-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05c00-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05c00-117">Return value</span></span>

<span data-ttu-id="05c00-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="05c00-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="05c00-119">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="05c00-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="05c00-120">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="05c00-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="05c00-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05c00-121">Requirements</span></span>



| <span data-ttu-id="05c00-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="05c00-122">Requirement</span></span> | <span data-ttu-id="05c00-123">Value</span><span class="sxs-lookup"><span data-stu-id="05c00-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="05c00-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="05c00-124">Header</span></span><br/>  | <dl> <span data-ttu-id="05c00-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="05c00-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="05c00-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="05c00-126">Library</span></span><br/> | <dl> <span data-ttu-id="05c00-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05c00-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="05c00-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="05c00-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05c00-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="05c00-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="05c00-130">**GetIntArray**</span><span class="sxs-lookup"><span data-stu-id="05c00-130">**GetIntArray**</span></span>](id3dxbaseeffect--getintarray.md)
</dt> </dl>

 

 
