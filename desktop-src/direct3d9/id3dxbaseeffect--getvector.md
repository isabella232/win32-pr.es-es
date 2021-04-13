---
description: Obtiene un vector.
ms.assetid: 55f5512f-42f2-4588-abd4-1cdea530b9bf
title: 'ID3DXBaseEffect:: GetVector (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetVector
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ea50cb6bf8c3f5b08d408539eba6c9f7cb09efc1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362425"
---
# <a name="id3dxbaseeffectgetvector-method"></a><span data-ttu-id="6c0b1-103">ID3DXBaseEffect:: GetVector (método)</span><span class="sxs-lookup"><span data-stu-id="6c0b1-103">ID3DXBaseEffect::GetVector method</span></span>

<span data-ttu-id="6c0b1-104">Obtiene un vector.</span><span class="sxs-lookup"><span data-stu-id="6c0b1-104">Gets a vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c0b1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c0b1-105">Syntax</span></span>


```C++
HRESULT GetVector(
  [in]  D3DXHANDLE  hParameter,
  [out] D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="6c0b1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c0b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c0b1-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6c0b1-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c0b1-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6c0b1-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6c0b1-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="6c0b1-109">Unique identifier.</span></span> <span data-ttu-id="6c0b1-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="6c0b1-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c0b1-111">*pVector* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6c0b1-111">*pVector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c0b1-112">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c0b1-112">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="6c0b1-113">Devuelve un vector 4D.</span><span class="sxs-lookup"><span data-stu-id="6c0b1-113">Returns a 4D vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c0b1-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c0b1-114">Return value</span></span>

<span data-ttu-id="6c0b1-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6c0b1-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6c0b1-116">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6c0b1-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6c0b1-117">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6c0b1-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c0b1-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c0b1-118">Remarks</span></span>

<span data-ttu-id="6c0b1-119">Si el vector de destino es mayor que el vector de origen, solo se rellenarán los componentes iniciales del vector de destino y los demás componentes se establecerán en cero.</span><span class="sxs-lookup"><span data-stu-id="6c0b1-119">If the destination vector is larger than the source vector, only the initial components of the destination vector will be filled, and the remaining components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c0b1-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c0b1-120">Requirements</span></span>



| <span data-ttu-id="6c0b1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c0b1-121">Requirement</span></span> | <span data-ttu-id="6c0b1-122">Value</span><span class="sxs-lookup"><span data-stu-id="6c0b1-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c0b1-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c0b1-123">Header</span></span><br/>  | <dl> <span data-ttu-id="6c0b1-124"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c0b1-124"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="6c0b1-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6c0b1-125">Library</span></span><br/> | <dl> <span data-ttu-id="6c0b1-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c0b1-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6c0b1-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c0b1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c0b1-128">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="6c0b1-128">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="6c0b1-129">**SetVector**</span><span class="sxs-lookup"><span data-stu-id="6c0b1-129">**SetVector**</span></span>](id3dxbaseeffect--setvector.md)
</dt> </dl>

 

 




