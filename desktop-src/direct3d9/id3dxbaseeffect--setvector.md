---
description: Establece un vector.
ms.assetid: 7dae88fc-d5d3-4751-859a-fa1bde4d0ce8
title: 'ID3DXBaseEffect:: SetVector (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetVector
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5d6fccc24410e06dd9bb4e6b0b1f1c36b03dd355
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718529"
---
# <a name="id3dxbaseeffectsetvector-method"></a><span data-ttu-id="0834f-103">ID3DXBaseEffect:: SetVector (método)</span><span class="sxs-lookup"><span data-stu-id="0834f-103">ID3DXBaseEffect::SetVector method</span></span>

<span data-ttu-id="0834f-104">Establece un vector.</span><span class="sxs-lookup"><span data-stu-id="0834f-104">Sets a vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="0834f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0834f-105">Syntax</span></span>


```C++
HRESULT SetVector(
  [in]       D3DXHANDLE  hParameter,
  [in] const D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="0834f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0834f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0834f-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0834f-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0834f-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0834f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0834f-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="0834f-109">Unique identifier.</span></span> <span data-ttu-id="0834f-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="0834f-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="0834f-111">*pVector* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0834f-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0834f-112">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="0834f-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="0834f-113">Puntero a un vector 4D.</span><span class="sxs-lookup"><span data-stu-id="0834f-113">Pointer to a 4D vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0834f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0834f-114">Return value</span></span>

<span data-ttu-id="0834f-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0834f-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0834f-116">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0834f-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0834f-117">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0834f-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0834f-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0834f-118">Remarks</span></span>

<span data-ttu-id="0834f-119">Si el vector de destino es menor que el vector de origen, se omitirán los componentes adicionales del vector de origen.</span><span class="sxs-lookup"><span data-stu-id="0834f-119">If the destination vector is smaller than the source vector, the additional components of the source vector will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="0834f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0834f-120">Requirements</span></span>



| <span data-ttu-id="0834f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0834f-121">Requirement</span></span> | <span data-ttu-id="0834f-122">Value</span><span class="sxs-lookup"><span data-stu-id="0834f-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0834f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0834f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0834f-124"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0834f-124"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0834f-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0834f-125">Library</span></span><br/> | <dl> <span data-ttu-id="0834f-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0834f-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0834f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="0834f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0834f-128">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="0834f-128">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="0834f-129">**GetVector**</span><span class="sxs-lookup"><span data-stu-id="0834f-129">**GetVector**</span></span>](id3dxbaseeffect--getvector.md)
</dt> </dl>

 

 




