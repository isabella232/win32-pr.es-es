---
description: Obtiene una matriz de valores BOOL.
ms.assetid: 4a5e2f48-fa82-47dc-a388-02a8679585d2
title: 'ID3DXBaseEffect:: GetBoolArray (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetBoolArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f714dfa91baba14524f12b6c3b2cb85211484cf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649459"
---
# <a name="id3dxbaseeffectgetboolarray-method"></a><span data-ttu-id="5a2ef-103">ID3DXBaseEffect:: GetBoolArray (método)</span><span class="sxs-lookup"><span data-stu-id="5a2ef-103">ID3DXBaseEffect::GetBoolArray method</span></span>

<span data-ttu-id="5a2ef-104">Obtiene una matriz de valores BOOL.</span><span class="sxs-lookup"><span data-stu-id="5a2ef-104">Gets an array of BOOL values.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a2ef-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a2ef-105">Syntax</span></span>


```C++
HRESULT GetBoolArray(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pB,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="5a2ef-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5a2ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a2ef-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5a2ef-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a2ef-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5a2ef-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5a2ef-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="5a2ef-109">Unique identifier.</span></span> <span data-ttu-id="5a2ef-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="5a2ef-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a2ef-111">*PB* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5a2ef-111">*pB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a2ef-112">Tipo: **[ **bool**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a2ef-112">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5a2ef-113">Devuelve una matriz de valores booleanos.</span><span class="sxs-lookup"><span data-stu-id="5a2ef-113">Returns an array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="5a2ef-114">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5a2ef-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a2ef-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a2ef-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a2ef-116">Número de valores booleanos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5a2ef-116">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a2ef-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5a2ef-117">Return value</span></span>

<span data-ttu-id="5a2ef-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5a2ef-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5a2ef-119">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5a2ef-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5a2ef-120">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5a2ef-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a2ef-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a2ef-121">Requirements</span></span>



| <span data-ttu-id="5a2ef-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a2ef-122">Requirement</span></span> | <span data-ttu-id="5a2ef-123">Value</span><span class="sxs-lookup"><span data-stu-id="5a2ef-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a2ef-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5a2ef-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5a2ef-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a2ef-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5a2ef-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5a2ef-126">Library</span></span><br/> | <dl> <span data-ttu-id="5a2ef-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a2ef-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5a2ef-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a2ef-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a2ef-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="5a2ef-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="5a2ef-130">**SetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="5a2ef-130">**SetBoolArray**</span></span>](id3dxbaseeffect--setboolarray.md)
</dt> </dl>

 

 
