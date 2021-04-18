---
description: Obtiene una descripción del paso.
ms.assetid: 44c65a82-bcf4-49f5-9312-8320e133bb2f
title: 'ID3DXBaseEffect:: GetPassDesc (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 15a997470fddf5056b7191fcc3226ad210724041
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718512"
---
# <a name="id3dxbaseeffectgetpassdesc-method"></a><span data-ttu-id="9fb9f-103">ID3DXBaseEffect:: GetPassDesc (método)</span><span class="sxs-lookup"><span data-stu-id="9fb9f-103">ID3DXBaseEffect::GetPassDesc method</span></span>

<span data-ttu-id="9fb9f-104">Obtiene una descripción del paso.</span><span class="sxs-lookup"><span data-stu-id="9fb9f-104">Gets a pass description.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fb9f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9fb9f-105">Syntax</span></span>


```C++
HRESULT GetPassDesc(
  [in]  D3DXHANDLE    hPass,
  [out] D3DXPASS_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="9fb9f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9fb9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fb9f-107">*hPass* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9fb9f-107">*hPass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fb9f-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="9fb9f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="9fb9f-109">Identificador de paso.</span><span class="sxs-lookup"><span data-stu-id="9fb9f-109">Pass handle.</span></span> <span data-ttu-id="9fb9f-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="9fb9f-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fb9f-111">*pDesc* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9fb9f-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fb9f-112">Tipo: **[ **D3DXPASS \_ DESC**](d3dxpass-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="9fb9f-112">Type: **[**D3DXPASS\_DESC**](d3dxpass-desc.md)\***</span></span>

<span data-ttu-id="9fb9f-113">Devuelve una descripción del paso especificado.</span><span class="sxs-lookup"><span data-stu-id="9fb9f-113">Returns a description of the specified pass.</span></span> <span data-ttu-id="9fb9f-114">Vea [**D3DXPASS \_ DESC**](d3dxpass-desc.md).</span><span class="sxs-lookup"><span data-stu-id="9fb9f-114">See [**D3DXPASS\_DESC**](d3dxpass-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fb9f-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9fb9f-115">Return value</span></span>

<span data-ttu-id="9fb9f-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9fb9f-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9fb9f-117">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9fb9f-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9fb9f-118">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="9fb9f-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fb9f-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9fb9f-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9fb9f-120">Si se crea un efecto con [D3DXFX que no se pueda \_ \_ clonar](d3dxfx.md), este método devolverá punteros **null** (en [**D3DXPASS \_ DESC**](d3dxpass-desc.md)) a las funciones de sombreador.</span><span class="sxs-lookup"><span data-stu-id="9fb9f-120">If an effect is created with [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md), this method will return **NULL** pointers (in [**D3DXPASS\_DESC**](d3dxpass-desc.md)) to the shader functions.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9fb9f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fb9f-121">Requirements</span></span>



| <span data-ttu-id="9fb9f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fb9f-122">Requirement</span></span> | <span data-ttu-id="9fb9f-123">Value</span><span class="sxs-lookup"><span data-stu-id="9fb9f-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fb9f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9fb9f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9fb9f-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fb9f-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="9fb9f-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9fb9f-126">Library</span></span><br/> | <dl> <span data-ttu-id="9fb9f-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9fb9f-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9fb9f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="9fb9f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fb9f-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="9fb9f-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




