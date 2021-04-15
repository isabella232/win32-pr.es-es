---
description: Establece un entero.
ms.assetid: 1090d4a6-b4f5-4e15-a49f-e2724f1c3f95
title: 'ID3DXBaseEffect:: SetInt (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetInt
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3c27d66544d4064c8d6c682db168b57b88d213cd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362421"
---
# <a name="id3dxbaseeffectsetint-method"></a><span data-ttu-id="fde2c-103">ID3DXBaseEffect:: SetInt (método)</span><span class="sxs-lookup"><span data-stu-id="fde2c-103">ID3DXBaseEffect::SetInt method</span></span>

<span data-ttu-id="fde2c-104">Establece un entero.</span><span class="sxs-lookup"><span data-stu-id="fde2c-104">Sets an integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="fde2c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fde2c-105">Syntax</span></span>


```C++
HRESULT SetInt(
  [in] D3DXHANDLE hParameter,
  [in] INT        n
);
```



## <a name="parameters"></a><span data-ttu-id="fde2c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fde2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fde2c-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fde2c-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fde2c-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fde2c-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fde2c-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="fde2c-109">Unique identifier.</span></span> <span data-ttu-id="fde2c-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="fde2c-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="fde2c-111">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fde2c-111">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fde2c-112">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fde2c-112">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fde2c-113">Valor entero.</span><span class="sxs-lookup"><span data-stu-id="fde2c-113">Integer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fde2c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fde2c-114">Return value</span></span>

<span data-ttu-id="fde2c-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fde2c-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fde2c-116">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fde2c-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fde2c-117">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="fde2c-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="fde2c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fde2c-118">Requirements</span></span>



| <span data-ttu-id="fde2c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fde2c-119">Requirement</span></span> | <span data-ttu-id="fde2c-120">Value</span><span class="sxs-lookup"><span data-stu-id="fde2c-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fde2c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fde2c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fde2c-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="fde2c-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="fde2c-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fde2c-123">Library</span></span><br/> | <dl> <span data-ttu-id="fde2c-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fde2c-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fde2c-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="fde2c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fde2c-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="fde2c-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="fde2c-127">**GetInt**</span><span class="sxs-lookup"><span data-stu-id="fde2c-127">**GetInt**</span></span>](id3dxbaseeffect--getint.md)
</dt> </dl>

 

 
