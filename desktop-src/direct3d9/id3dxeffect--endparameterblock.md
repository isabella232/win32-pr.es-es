---
description: Detiene la captura de cambios de estado de parámetro de efecto.
ms.assetid: b6ca2917-2df0-4f3a-9ee3-23e9d2501ff4
title: 'ID3DXEffect:: EndParameterBlock (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.EndParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3359e3b923d05e003ffbda18791e497d18ba627e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003836"
---
# <a name="id3dxeffectendparameterblock-method"></a><span data-ttu-id="8bf3d-103">ID3DXEffect:: EndParameterBlock (método)</span><span class="sxs-lookup"><span data-stu-id="8bf3d-103">ID3DXEffect::EndParameterBlock method</span></span>

<span data-ttu-id="8bf3d-104">Detiene la captura de cambios de estado de parámetro de efecto.</span><span class="sxs-lookup"><span data-stu-id="8bf3d-104">Stop capturing effect parameter state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bf3d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8bf3d-105">Syntax</span></span>


```C++
D3DXHANDLE EndParameterBlock();
```



## <a name="parameters"></a><span data-ttu-id="8bf3d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8bf3d-106">Parameters</span></span>

<span data-ttu-id="8bf3d-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8bf3d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8bf3d-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8bf3d-108">Return value</span></span>

<span data-ttu-id="8bf3d-109">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8bf3d-109">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8bf3d-110">Devuelve un identificador para el bloque de estado del parámetro.</span><span class="sxs-lookup"><span data-stu-id="8bf3d-110">Returns a handle to the parameter state block.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bf3d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8bf3d-111">Remarks</span></span>

<span data-ttu-id="8bf3d-112">Todos los parámetros de efecto que cambian el estado (después de llamar a BeginParameterBlock y antes de llamar a EndParameterBlock) se guardarán en un bloque de estado de parámetro de efecto.</span><span class="sxs-lookup"><span data-stu-id="8bf3d-112">All effect parameters that change state (after calling BeginParameterBlock and before calling EndParameterBlock) will be saved in an effect parameter state block.</span></span> <span data-ttu-id="8bf3d-113">Use ApplyParameterBlock para aplicar este bloque de cambios de estado en el sistema de efectos.</span><span class="sxs-lookup"><span data-stu-id="8bf3d-113">Use ApplyParameterBlock to apply this block of state changes to the effect system.</span></span> <span data-ttu-id="8bf3d-114">Una vez que haya terminado con un bloque de estado, use DeleteParameterBlock para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="8bf3d-114">Once you are finished with a state block use DeleteParameterBlock to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bf3d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bf3d-115">Requirements</span></span>



| <span data-ttu-id="8bf3d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bf3d-116">Requirement</span></span> | <span data-ttu-id="8bf3d-117">Value</span><span class="sxs-lookup"><span data-stu-id="8bf3d-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bf3d-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8bf3d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8bf3d-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bf3d-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="8bf3d-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8bf3d-120">Library</span></span><br/> | <dl> <span data-ttu-id="8bf3d-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8bf3d-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8bf3d-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="8bf3d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bf3d-123">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="8bf3d-123">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="8bf3d-124">**ID3DXEffect::BeginParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="8bf3d-124">**ID3DXEffect::BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[<span data-ttu-id="8bf3d-125">**ID3DXEffect::ApplyParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="8bf3d-125">**ID3DXEffect::ApplyParameterBlock**</span></span>](id3dxeffect--applyparameterblock.md)
</dt> <dt>

[<span data-ttu-id="8bf3d-126">**ID3DXEffect::D eleteParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="8bf3d-126">**ID3DXEffect::DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




