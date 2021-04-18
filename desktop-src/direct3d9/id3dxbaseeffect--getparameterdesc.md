---
description: Obtiene un parámetro o una descripción de la anotación.
ms.assetid: fd54eb08-a7e4-4106-b0ed-49a4da7fcadc
title: 'ID3DXBaseEffect:: GetParameterDesc (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8c3a52c06ebed764b3ab1718488c2dbc55ceda41
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698412"
---
# <a name="id3dxbaseeffectgetparameterdesc-method"></a><span data-ttu-id="782de-103">ID3DXBaseEffect:: GetParameterDesc (método)</span><span class="sxs-lookup"><span data-stu-id="782de-103">ID3DXBaseEffect::GetParameterDesc method</span></span>

<span data-ttu-id="782de-104">Obtiene un parámetro o una descripción de la anotación.</span><span class="sxs-lookup"><span data-stu-id="782de-104">Gets a parameter or annotation description.</span></span>

## <a name="syntax"></a><span data-ttu-id="782de-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="782de-105">Syntax</span></span>


```C++
HRESULT GetParameterDesc(
  [in]  D3DXHANDLE         hParameter,
  [out] D3DXPARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="782de-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="782de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="782de-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="782de-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="782de-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="782de-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="782de-109">Identificador de parámetro o anotación.</span><span class="sxs-lookup"><span data-stu-id="782de-109">Parameter or annotation handle.</span></span> <span data-ttu-id="782de-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="782de-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="782de-111">*pDesc* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="782de-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="782de-112">Tipo: **[ **D3DXPARAMETER \_ DESC**](d3dxparameter-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="782de-112">Type: **[**D3DXPARAMETER\_DESC**](d3dxparameter-desc.md)\***</span></span>

<span data-ttu-id="782de-113">Devuelve una descripción del parámetro o anotación especificados.</span><span class="sxs-lookup"><span data-stu-id="782de-113">Returns a description of the specified parameter or annotation.</span></span> <span data-ttu-id="782de-114">Vea [**D3DXPARAMETER \_ DESC**](d3dxparameter-desc.md).</span><span class="sxs-lookup"><span data-stu-id="782de-114">See [**D3DXPARAMETER\_DESC**](d3dxparameter-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="782de-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="782de-115">Return value</span></span>

<span data-ttu-id="782de-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="782de-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="782de-117">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="782de-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="782de-118">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="782de-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="782de-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="782de-119">Requirements</span></span>



| <span data-ttu-id="782de-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="782de-120">Requirement</span></span> | <span data-ttu-id="782de-121">Value</span><span class="sxs-lookup"><span data-stu-id="782de-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="782de-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="782de-122">Header</span></span><br/>  | <dl> <span data-ttu-id="782de-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="782de-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="782de-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="782de-124">Library</span></span><br/> | <dl> <span data-ttu-id="782de-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="782de-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="782de-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="782de-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="782de-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="782de-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




