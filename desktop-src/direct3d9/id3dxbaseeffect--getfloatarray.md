---
description: Obtiene una matriz de valores de punto flotante.
ms.assetid: ba839129-c332-4ce8-b7c1-ea0ef4697ade
title: 'ID3DXBaseEffect:: GetFloatArray (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFloatArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 2ea71daa3b207a8f7716bf0a0db3608554c0b9f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362783"
---
# <a name="id3dxbaseeffectgetfloatarray-method"></a><span data-ttu-id="dcc40-103">ID3DXBaseEffect:: GetFloatArray (método)</span><span class="sxs-lookup"><span data-stu-id="dcc40-103">ID3DXBaseEffect::GetFloatArray method</span></span>

<span data-ttu-id="dcc40-104">Obtiene una matriz de valores de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="dcc40-104">Gets an array of floating point values.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcc40-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dcc40-105">Syntax</span></span>


```C++
HRESULT GetFloatArray(
  [in]  D3DXHANDLE hParameter,
  [out] FLOAT      *pf,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="dcc40-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dcc40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcc40-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dcc40-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcc40-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="dcc40-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="dcc40-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="dcc40-109">Unique identifier.</span></span> <span data-ttu-id="dcc40-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="dcc40-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="dcc40-111">*PF* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="dcc40-111">*pf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcc40-112">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="dcc40-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="dcc40-113">Devuelve una matriz de valores de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="dcc40-113">Returns an array of floating point values.</span></span>

</dd> <dt>

<span data-ttu-id="dcc40-114">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dcc40-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcc40-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dcc40-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dcc40-116">Número de valores de punto flotante en la matriz.</span><span class="sxs-lookup"><span data-stu-id="dcc40-116">Number of floating point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcc40-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dcc40-117">Return value</span></span>

<span data-ttu-id="dcc40-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dcc40-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dcc40-119">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dcc40-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="dcc40-120">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="dcc40-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcc40-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcc40-121">Requirements</span></span>



| <span data-ttu-id="dcc40-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcc40-122">Requirement</span></span> | <span data-ttu-id="dcc40-123">Value</span><span class="sxs-lookup"><span data-stu-id="dcc40-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcc40-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dcc40-124">Header</span></span><br/>  | <dl> <span data-ttu-id="dcc40-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcc40-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="dcc40-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dcc40-126">Library</span></span><br/> | <dl> <span data-ttu-id="dcc40-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcc40-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="dcc40-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="dcc40-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcc40-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="dcc40-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="dcc40-130">**SetFloatArray**</span><span class="sxs-lookup"><span data-stu-id="dcc40-130">**SetFloatArray**</span></span>](id3dxbaseeffect--setfloatarray.md)
</dt> </dl>

 

 
