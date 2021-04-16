---
description: Establece una matriz de valores booleanos.
ms.assetid: 920b3482-cc30-4ab2-bfce-59f03afe11da
title: 'ID3DXBaseEffect:: SetBoolArray (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetBoolArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 813259fc9fcca954c4d7a992c7542387be33bb6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649372"
---
# <a name="id3dxbaseeffectsetboolarray-method"></a><span data-ttu-id="3fe0d-103">ID3DXBaseEffect:: SetBoolArray (método)</span><span class="sxs-lookup"><span data-stu-id="3fe0d-103">ID3DXBaseEffect::SetBoolArray method</span></span>

<span data-ttu-id="3fe0d-104">Establece una matriz de valores booleanos.</span><span class="sxs-lookup"><span data-stu-id="3fe0d-104">Sets an array of Boolean values.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fe0d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3fe0d-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       D3DXHANDLE hParameter,
  [in] const BOOL       *pB,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="3fe0d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3fe0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fe0d-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3fe0d-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fe0d-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="3fe0d-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="3fe0d-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="3fe0d-109">Unique identifier.</span></span> <span data-ttu-id="3fe0d-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="3fe0d-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="3fe0d-111">*PB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3fe0d-111">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fe0d-112">Tipo: **const [**bool**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="3fe0d-112">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3fe0d-113">Matriz de valores booleanos.</span><span class="sxs-lookup"><span data-stu-id="3fe0d-113">Array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="3fe0d-114">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3fe0d-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fe0d-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3fe0d-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3fe0d-116">Número de valores booleanos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="3fe0d-116">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fe0d-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3fe0d-117">Return value</span></span>

<span data-ttu-id="3fe0d-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3fe0d-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3fe0d-119">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3fe0d-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3fe0d-120">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="3fe0d-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fe0d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fe0d-121">Requirements</span></span>



| <span data-ttu-id="3fe0d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fe0d-122">Requirement</span></span> | <span data-ttu-id="3fe0d-123">Value</span><span class="sxs-lookup"><span data-stu-id="3fe0d-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fe0d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3fe0d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3fe0d-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fe0d-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="3fe0d-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3fe0d-126">Library</span></span><br/> | <dl> <span data-ttu-id="3fe0d-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3fe0d-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3fe0d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="3fe0d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fe0d-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="3fe0d-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="3fe0d-130">**GetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="3fe0d-130">**GetBoolArray**</span></span>](id3dxbaseeffect--getboolarray.md)
</dt> </dl>

 

 
