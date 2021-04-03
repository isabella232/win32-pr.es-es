---
description: Establece un valor de punto flotante.
ms.assetid: f49fb4d2-6e3d-4452-8102-76200c55cf1f
title: 'ID3DXBaseEffect:: SetFloat (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetFloat
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: af955748fff66e67e0e2f5650b869a746168de54
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914697"
---
# <a name="id3dxbaseeffectsetfloat-method"></a><span data-ttu-id="0a45c-103">ID3DXBaseEffect:: SetFloat (método)</span><span class="sxs-lookup"><span data-stu-id="0a45c-103">ID3DXBaseEffect::SetFloat method</span></span>

<span data-ttu-id="0a45c-104">Establece un valor de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="0a45c-104">Sets a floating point value.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a45c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a45c-105">Syntax</span></span>


```C++
HRESULT SetFloat(
  [in] D3DXHANDLE hParameter,
  [in] FLOAT      f
);
```



## <a name="parameters"></a><span data-ttu-id="0a45c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a45c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a45c-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0a45c-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a45c-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0a45c-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0a45c-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="0a45c-109">Unique identifier.</span></span> <span data-ttu-id="0a45c-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="0a45c-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a45c-111">*f* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="0a45c-111">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a45c-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a45c-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a45c-113">Valor de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="0a45c-113">Floating point value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a45c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a45c-114">Return value</span></span>

<span data-ttu-id="0a45c-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0a45c-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0a45c-116">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0a45c-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0a45c-117">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0a45c-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a45c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a45c-118">Requirements</span></span>



| <span data-ttu-id="0a45c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a45c-119">Requirement</span></span> | <span data-ttu-id="0a45c-120">Value</span><span class="sxs-lookup"><span data-stu-id="0a45c-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a45c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0a45c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0a45c-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a45c-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0a45c-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0a45c-123">Library</span></span><br/> | <dl> <span data-ttu-id="0a45c-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a45c-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0a45c-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a45c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a45c-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="0a45c-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="0a45c-127">**GetFloat**</span><span class="sxs-lookup"><span data-stu-id="0a45c-127">**GetFloat**</span></span>](id3dxbaseeffect--getfloat.md)
</dt> </dl>

 

 
