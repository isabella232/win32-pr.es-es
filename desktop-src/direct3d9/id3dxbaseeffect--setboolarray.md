---
description: 'Método ID3DXBaseEffect::SetBoolArray: establece una matriz de valores booleanos.'
ms.assetid: 920b3482-cc30-4ab2-bfce-59f03afe11da
title: Método ID3DXBaseEffect::SetBoolArray (D3DX9Shader.h)
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
ms.openlocfilehash: cad6846914d348dd49d6362d70271c5af078e35d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093833"
---
# <a name="id3dxbaseeffectsetboolarray-method"></a><span data-ttu-id="d21b2-103">Método ID3DXBaseEffect::SetBoolArray</span><span class="sxs-lookup"><span data-stu-id="d21b2-103">ID3DXBaseEffect::SetBoolArray method</span></span>

<span data-ttu-id="d21b2-104">Establece una matriz de valores booleanos.</span><span class="sxs-lookup"><span data-stu-id="d21b2-104">Sets an array of Boolean values.</span></span>

## <a name="syntax"></a><span data-ttu-id="d21b2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d21b2-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       D3DXHANDLE hParameter,
  [in] const BOOL       *pB,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="d21b2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d21b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d21b2-107">*hParameter* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d21b2-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d21b2-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d21b2-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d21b2-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="d21b2-109">Unique identifier.</span></span> <span data-ttu-id="d21b2-110">Vea [Identificadores (Direct3D 9).](handles.md)</span><span class="sxs-lookup"><span data-stu-id="d21b2-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="d21b2-111">*pB* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d21b2-111">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d21b2-112">Tipo: **const [**BOOL**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d21b2-112">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d21b2-113">Matriz de valores booleanos.</span><span class="sxs-lookup"><span data-stu-id="d21b2-113">Array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="d21b2-114">*Recuento* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d21b2-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d21b2-115">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d21b2-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d21b2-116">Número de valores booleanos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="d21b2-116">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d21b2-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d21b2-117">Return value</span></span>

<span data-ttu-id="d21b2-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d21b2-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d21b2-119">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d21b2-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d21b2-120">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d21b2-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d21b2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d21b2-121">Requirements</span></span>



| <span data-ttu-id="d21b2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d21b2-122">Requirement</span></span> | <span data-ttu-id="d21b2-123">Value</span><span class="sxs-lookup"><span data-stu-id="d21b2-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d21b2-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d21b2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d21b2-125"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="d21b2-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d21b2-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d21b2-126">Library</span></span><br/> | <dl> <span data-ttu-id="d21b2-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d21b2-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d21b2-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d21b2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d21b2-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="d21b2-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="d21b2-130">**GetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="d21b2-130">**GetBoolArray**</span></span>](id3dxbaseeffect--getboolarray.md)
</dt> </dl>

 

 
