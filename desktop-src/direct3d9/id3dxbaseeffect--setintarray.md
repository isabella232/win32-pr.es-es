---
description: 'Método ID3DXBaseEffect::SetIntArray: establece una matriz de enteros.'
ms.assetid: 4491bffd-ce5e-4f84-ac11-0314a1b16d63
title: Método ID3DXBaseEffect::SetIntArray (D3DX9Shader.h)
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
ms.openlocfilehash: a14e837a0903290c3197bbb17ec4b2da3f68b419
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093763"
---
# <a name="id3dxbaseeffectsetintarray-method"></a><span data-ttu-id="b6047-103">Método ID3DXBaseEffect::SetIntArray</span><span class="sxs-lookup"><span data-stu-id="b6047-103">ID3DXBaseEffect::SetIntArray method</span></span>

<span data-ttu-id="b6047-104">Establece una matriz de enteros.</span><span class="sxs-lookup"><span data-stu-id="b6047-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6047-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6047-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       D3DXHANDLE hParameter,
  [in] const INT        *pn,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="b6047-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b6047-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6047-107">*hParameter* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b6047-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6047-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b6047-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b6047-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="b6047-109">Unique identifier.</span></span> <span data-ttu-id="b6047-110">Vea [Identificadores (Direct3D 9).](handles.md)</span><span class="sxs-lookup"><span data-stu-id="b6047-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6047-111">*pn* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b6047-111">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6047-112">Tipo: **const [**INT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b6047-112">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b6047-113">Matriz de enteros.</span><span class="sxs-lookup"><span data-stu-id="b6047-113">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="b6047-114">*Recuento* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b6047-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6047-115">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b6047-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b6047-116">Número de enteros de la matriz.</span><span class="sxs-lookup"><span data-stu-id="b6047-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6047-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b6047-117">Return value</span></span>

<span data-ttu-id="b6047-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b6047-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b6047-119">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b6047-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b6047-120">Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b6047-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6047-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6047-121">Requirements</span></span>



| <span data-ttu-id="b6047-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6047-122">Requirement</span></span> | <span data-ttu-id="b6047-123">Value</span><span class="sxs-lookup"><span data-stu-id="b6047-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6047-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6047-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b6047-125"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="b6047-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b6047-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b6047-126">Library</span></span><br/> | <dl> <span data-ttu-id="b6047-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6047-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b6047-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b6047-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6047-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="b6047-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="b6047-130">**GetIntArray**</span><span class="sxs-lookup"><span data-stu-id="b6047-130">**GetIntArray**</span></span>](id3dxbaseeffect--getintarray.md)
</dt> </dl>

 

 
