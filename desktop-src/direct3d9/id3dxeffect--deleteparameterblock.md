---
description: Elimine un bloque de parámetros.
ms.assetid: 5502dabc-1703-481b-a69d-f6bd8fd01d20
title: ID3DXEffect::D método eleteParameterBlock (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.DeleteParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 483b09ebf308b8cdfa14d714bc74786e5fcb1f83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718239"
---
# <a name="id3dxeffectdeleteparameterblock-method"></a><span data-ttu-id="e6a4d-103">ID3DXEffect::D método eleteParameterBlock</span><span class="sxs-lookup"><span data-stu-id="e6a4d-103">ID3DXEffect::DeleteParameterBlock method</span></span>

<span data-ttu-id="e6a4d-104">Elimine un bloque de parámetros.</span><span class="sxs-lookup"><span data-stu-id="e6a4d-104">Delete a parameter block.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6a4d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6a4d-105">Syntax</span></span>


```C++
HRESULT DeleteParameterBlock(
  [in] D3DXHANDLE  hParameterBlock
);
```



## <a name="parameters"></a><span data-ttu-id="e6a4d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6a4d-106">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="e6a4d-107">*hParameterBlock* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e6a4d-107">*hParameterBlock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6a4d-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e6a4d-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e6a4d-109">Identificador del bloque de parámetros.</span><span class="sxs-lookup"><span data-stu-id="e6a4d-109">A handle to the parameter block.</span></span> <span data-ttu-id="e6a4d-110">Este es el identificador devuelto por [**ID3DXEffect:: EndParameterBlock**](id3dxeffect--endparameterblock.md).</span><span class="sxs-lookup"><span data-stu-id="e6a4d-110">This is the handle returned by [**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6a4d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6a4d-111">Return value</span></span>

<span data-ttu-id="e6a4d-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e6a4d-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e6a4d-113">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e6a4d-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e6a4d-114">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="e6a4d-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6a4d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6a4d-115">Remarks</span></span>

<span data-ttu-id="e6a4d-116">Los bloques de parámetros son bloques de Estados de efecto.</span><span class="sxs-lookup"><span data-stu-id="e6a4d-116">Parameter blocks are blocks of effect states.</span></span> <span data-ttu-id="e6a4d-117">Use un bloque de parámetros para registrar los cambios de estado de forma que se puedan aplicar más adelante con una única llamada API.</span><span class="sxs-lookup"><span data-stu-id="e6a4d-117">Use a parameter block to record state changes so that they can be applied later on with a single API call.</span></span> <span data-ttu-id="e6a4d-118">Cuando ya no lo necesite, elimine el bloque de parámetros para reducir el uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="e6a4d-118">When no longer needed, delete the parameter block to reduce memory usage.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6a4d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6a4d-119">Requirements</span></span>



| <span data-ttu-id="e6a4d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6a4d-120">Requirement</span></span> | <span data-ttu-id="e6a4d-121">Value</span><span class="sxs-lookup"><span data-stu-id="e6a4d-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6a4d-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6a4d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e6a4d-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6a4d-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="e6a4d-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6a4d-124">Library</span></span><br/> | <dl> <span data-ttu-id="e6a4d-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6a4d-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e6a4d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6a4d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6a4d-127">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="e6a4d-127">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="e6a4d-128">**ID3DXEffect::BeginParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="e6a4d-128">**ID3DXEffect::BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[<span data-ttu-id="e6a4d-129">**ID3DXEffect::EndParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="e6a4d-129">**ID3DXEffect::EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)
</dt> </dl>

 

 




