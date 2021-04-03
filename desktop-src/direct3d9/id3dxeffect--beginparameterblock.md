---
description: Iniciar captura de cambios de estado en un bloque de parámetros.
ms.assetid: cdf6f572-1a21-4c1d-a113-13b48bacd060
title: 'ID3DXEffect:: BeginParameterBlock (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.BeginParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 60a43304c8e0e3d64ac6469c1c075c57b5411e3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083736"
---
# <a name="id3dxeffectbeginparameterblock-method"></a><span data-ttu-id="a92e5-103">ID3DXEffect:: BeginParameterBlock (método)</span><span class="sxs-lookup"><span data-stu-id="a92e5-103">ID3DXEffect::BeginParameterBlock method</span></span>

<span data-ttu-id="a92e5-104">Iniciar captura de cambios de estado en un bloque de parámetros.</span><span class="sxs-lookup"><span data-stu-id="a92e5-104">Start capturing state changes in a parameter block.</span></span>

## <a name="syntax"></a><span data-ttu-id="a92e5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a92e5-105">Syntax</span></span>


```C++
HRESULT BeginParameterBlock();
```



## <a name="parameters"></a><span data-ttu-id="a92e5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a92e5-106">Parameters</span></span>

<span data-ttu-id="a92e5-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a92e5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a92e5-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a92e5-108">Return value</span></span>

<span data-ttu-id="a92e5-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a92e5-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a92e5-110">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a92e5-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a92e5-111">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="a92e5-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="a92e5-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a92e5-112">Remarks</span></span>

<span data-ttu-id="a92e5-113">Captura los cambios de estado de parámetro de efecto hasta que se llama a EndParameterBlock.</span><span class="sxs-lookup"><span data-stu-id="a92e5-113">Capture effect parameter state changes until EndParameterBlock is called.</span></span> <span data-ttu-id="a92e5-114">Los parámetros de efecto incluyen cualquier cambio de estado fuera de un paso.</span><span class="sxs-lookup"><span data-stu-id="a92e5-114">Effect parameters include any state changes outside of a pass.</span></span> <span data-ttu-id="a92e5-115">Elimine los bloques de parámetros si ya no son necesarios llamando a DeleteParameterBlock.</span><span class="sxs-lookup"><span data-stu-id="a92e5-115">Delete parameter blocks if they are no longer needed by calling DeleteParameterBlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="a92e5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a92e5-116">Requirements</span></span>



| <span data-ttu-id="a92e5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a92e5-117">Requirement</span></span> | <span data-ttu-id="a92e5-118">Value</span><span class="sxs-lookup"><span data-stu-id="a92e5-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a92e5-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a92e5-119">Header</span></span><br/>  | <dl> <span data-ttu-id="a92e5-120"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a92e5-120"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="a92e5-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a92e5-121">Library</span></span><br/> | <dl> <span data-ttu-id="a92e5-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a92e5-122"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a92e5-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="a92e5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a92e5-124">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="a92e5-124">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="a92e5-125">**ID3DXEffect::EndParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="a92e5-125">**ID3DXEffect::EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)
</dt> <dt>

[<span data-ttu-id="a92e5-126">**ID3DXEffect::ApplyParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="a92e5-126">**ID3DXEffect::ApplyParameterBlock**</span></span>](id3dxeffect--applyparameterblock.md)
</dt> <dt>

[<span data-ttu-id="a92e5-127">**ID3DXEffect::D eleteParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="a92e5-127">**ID3DXEffect::DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




