---
description: Establece una matriz de valores de punto flotante.
ms.assetid: 4b9c27b4-0255-4bbf-9168-491936d64fb9
title: 'ID3DXBaseEffect:: SetFloatArray (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetFloatArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9927f3cd79d7950a94e62881089fb06c67395bac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280237"
---
# <a name="id3dxbaseeffectsetfloatarray-method"></a><span data-ttu-id="39392-103">ID3DXBaseEffect:: SetFloatArray (método)</span><span class="sxs-lookup"><span data-stu-id="39392-103">ID3DXBaseEffect::SetFloatArray method</span></span>

<span data-ttu-id="39392-104">Establece una matriz de valores de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="39392-104">Sets an array of floating point values.</span></span>

## <a name="syntax"></a><span data-ttu-id="39392-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39392-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       D3DXHANDLE hParameter,
  [in] const FLOAT      *pf,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="39392-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39392-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39392-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="39392-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39392-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="39392-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="39392-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="39392-109">Unique identifier.</span></span> <span data-ttu-id="39392-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="39392-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="39392-111">*PF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="39392-111">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39392-112">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="39392-112">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="39392-113">Matriz de valores de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="39392-113">Array of floating point values.</span></span>

</dd> <dt>

<span data-ttu-id="39392-114">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="39392-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39392-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="39392-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="39392-116">Número de valores de punto flotante en la matriz.</span><span class="sxs-lookup"><span data-stu-id="39392-116">Number of floating point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39392-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39392-117">Return value</span></span>

<span data-ttu-id="39392-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="39392-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="39392-119">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="39392-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="39392-120">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="39392-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="39392-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39392-121">Requirements</span></span>



| <span data-ttu-id="39392-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="39392-122">Requirement</span></span> | <span data-ttu-id="39392-123">Value</span><span class="sxs-lookup"><span data-stu-id="39392-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="39392-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39392-124">Header</span></span><br/>  | <dl> <span data-ttu-id="39392-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="39392-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="39392-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="39392-126">Library</span></span><br/> | <dl> <span data-ttu-id="39392-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39392-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="39392-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="39392-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39392-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="39392-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="39392-130">**GetFloatArray**</span><span class="sxs-lookup"><span data-stu-id="39392-130">**GetFloatArray**</span></span>](id3dxbaseeffect--getfloatarray.md)
</dt> </dl>

 

 
