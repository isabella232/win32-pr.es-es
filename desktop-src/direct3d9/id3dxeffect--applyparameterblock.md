---
description: Aplique los valores de un bloque de estado al estado del sistema de efecto actual.
ms.assetid: f228e2a2-64fa-4354-9f49-42d1d3b12d50
title: 'ID3DXEffect:: ApplyParameterBlock (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.ApplyParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 12af672b929822180c4dba681ca333692a9174ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718244"
---
# <a name="id3dxeffectapplyparameterblock-method"></a><span data-ttu-id="f992d-103">ID3DXEffect:: ApplyParameterBlock (método)</span><span class="sxs-lookup"><span data-stu-id="f992d-103">ID3DXEffect::ApplyParameterBlock method</span></span>

<span data-ttu-id="f992d-104">Aplique los valores de un bloque de estado al estado del sistema de efecto actual.</span><span class="sxs-lookup"><span data-stu-id="f992d-104">Apply the values in a state block to the current effect system state.</span></span>

## <a name="syntax"></a><span data-ttu-id="f992d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f992d-105">Syntax</span></span>


```C++
HRESULT ApplyParameterBlock(
  [in] D3DXHANDLE  hParameterBlock
);
```



## <a name="parameters"></a><span data-ttu-id="f992d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f992d-106">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="f992d-107">*hParameterBlock* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f992d-107">*hParameterBlock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f992d-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f992d-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f992d-109">Identificador del bloque de parámetros.</span><span class="sxs-lookup"><span data-stu-id="f992d-109">A handle to the parameter block.</span></span> <span data-ttu-id="f992d-110">Este es el identificador devuelto por [**ID3DXEffect:: EndParameterBlock**](id3dxeffect--endparameterblock.md).</span><span class="sxs-lookup"><span data-stu-id="f992d-110">This is the handle returned by [**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f992d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f992d-111">Return value</span></span>

<span data-ttu-id="f992d-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f992d-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f992d-113">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f992d-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f992d-114">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="f992d-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="f992d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f992d-115">Remarks</span></span>

<span data-ttu-id="f992d-116">Captura los cambios de estado de parámetro de efecto en un bloque de parámetros mediante una llamada a BeginParameterBlock; Detenga la captura de los cambios de estado llamando a EndParameterBlock.</span><span class="sxs-lookup"><span data-stu-id="f992d-116">Capture effect parameter state changes in a parameter block by calling BeginParameterBlock; stop capturing state changes by calling EndParameterBlock.</span></span> <span data-ttu-id="f992d-117">Estos cambios de estado incluyen cualquier cambio de parámetro de efecto que se produce dentro de una técnica (incluidos los que se encuentran fuera de un paso).</span><span class="sxs-lookup"><span data-stu-id="f992d-117">These state changes include any effect parameter changes that occur inside of a technique (including those outside of a pass).</span></span> <span data-ttu-id="f992d-118">Una vez que haya terminado con el bloque de parámetros, llame a DeleteParameterBlock para recuperar memoria.</span><span class="sxs-lookup"><span data-stu-id="f992d-118">Once you are done with the parameter block, call DeleteParameterBlock to recover memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="f992d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f992d-119">Requirements</span></span>



| <span data-ttu-id="f992d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f992d-120">Requirement</span></span> | <span data-ttu-id="f992d-121">Value</span><span class="sxs-lookup"><span data-stu-id="f992d-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f992d-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f992d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f992d-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f992d-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="f992d-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f992d-124">Library</span></span><br/> | <dl> <span data-ttu-id="f992d-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f992d-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f992d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f992d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f992d-127">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="f992d-127">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="f992d-128">**ID3DXEffect::BeginParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="f992d-128">**ID3DXEffect::BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[<span data-ttu-id="f992d-129">**ID3DXEffect::EndParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="f992d-129">**ID3DXEffect::EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)
</dt> <dt>

[<span data-ttu-id="f992d-130">**ID3DXEffect::D eleteParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="f992d-130">**ID3DXEffect::DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




