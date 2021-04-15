---
description: Obtiene una descripción de la función.
ms.assetid: a1a0ccf4-2428-4e60-9af0-07dc2132a367
title: 'ID3DXBaseEffect:: GetFunctionDesc (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunctionDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 718960da7ff73f24f865fdacc09dfe55ff09a466
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708088"
---
# <a name="id3dxbaseeffectgetfunctiondesc-method"></a><span data-ttu-id="108f5-103">ID3DXBaseEffect:: GetFunctionDesc (método)</span><span class="sxs-lookup"><span data-stu-id="108f5-103">ID3DXBaseEffect::GetFunctionDesc method</span></span>

<span data-ttu-id="108f5-104">Obtiene una descripción de la función.</span><span class="sxs-lookup"><span data-stu-id="108f5-104">Gets a function description.</span></span>

## <a name="syntax"></a><span data-ttu-id="108f5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="108f5-105">Syntax</span></span>


```C++
HRESULT GetFunctionDesc(
  [in]  D3DXHANDLE        hFunction,
  [out] D3DXFUNCTION_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="108f5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="108f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="108f5-107">*hFunction* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="108f5-107">*hFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="108f5-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="108f5-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="108f5-109">Identificador de función.</span><span class="sxs-lookup"><span data-stu-id="108f5-109">Function handle.</span></span> <span data-ttu-id="108f5-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="108f5-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="108f5-111">*pDesc* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="108f5-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="108f5-112">Tipo: **[ **D3DXFUNCTION \_ DESC**](d3dxfunction-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="108f5-112">Type: **[**D3DXFUNCTION\_DESC**](d3dxfunction-desc.md)\***</span></span>

<span data-ttu-id="108f5-113">Devuelve una descripción de la función.</span><span class="sxs-lookup"><span data-stu-id="108f5-113">Returns a description of the function.</span></span> <span data-ttu-id="108f5-114">Vea [**D3DXFUNCTION \_ DESC**](d3dxfunction-desc.md).</span><span class="sxs-lookup"><span data-stu-id="108f5-114">See [**D3DXFUNCTION\_DESC**](d3dxfunction-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="108f5-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="108f5-115">Return value</span></span>

<span data-ttu-id="108f5-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="108f5-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="108f5-117">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="108f5-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="108f5-118">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="108f5-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="108f5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="108f5-119">Requirements</span></span>



| <span data-ttu-id="108f5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="108f5-120">Requirement</span></span> | <span data-ttu-id="108f5-121">Value</span><span class="sxs-lookup"><span data-stu-id="108f5-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="108f5-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="108f5-122">Header</span></span><br/>  | <dl> <span data-ttu-id="108f5-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="108f5-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="108f5-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="108f5-124">Library</span></span><br/> | <dl> <span data-ttu-id="108f5-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="108f5-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="108f5-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="108f5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="108f5-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="108f5-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




