---
description: Obtiene una matriz de vectores.
ms.assetid: 75fe454c-75f7-4f03-acd2-dd9cbf94fb96
title: 'ID3DXBaseEffect:: GetVectorArray (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetVectorArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fa57553b993d5746b54e9a03c6b4e52f71937f0d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362424"
---
# <a name="id3dxbaseeffectgetvectorarray-method"></a><span data-ttu-id="ee73a-103">ID3DXBaseEffect:: GetVectorArray (método)</span><span class="sxs-lookup"><span data-stu-id="ee73a-103">ID3DXBaseEffect::GetVectorArray method</span></span>

<span data-ttu-id="ee73a-104">Obtiene una matriz de vectores.</span><span class="sxs-lookup"><span data-stu-id="ee73a-104">Gets an array of vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee73a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee73a-105">Syntax</span></span>


```C++
HRESULT GetVectorArray(
  [in]  D3DXHANDLE  hParameter,
  [out] D3DXVECTOR4 *pVector,
  [in]  UINT        Count
);
```



## <a name="parameters"></a><span data-ttu-id="ee73a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee73a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee73a-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ee73a-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee73a-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ee73a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ee73a-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="ee73a-109">Unique identifier.</span></span> <span data-ttu-id="ee73a-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="ee73a-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee73a-111">*pVector* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ee73a-111">*pVector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee73a-112">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="ee73a-112">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="ee73a-113">Devuelve una matriz de los vectores de punto flotante 4D.</span><span class="sxs-lookup"><span data-stu-id="ee73a-113">Returns an array of 4D floating point vectors.</span></span>

</dd> <dt>

<span data-ttu-id="ee73a-114">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ee73a-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee73a-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee73a-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee73a-116">Número de vectores de la matriz.</span><span class="sxs-lookup"><span data-stu-id="ee73a-116">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee73a-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee73a-117">Return value</span></span>

<span data-ttu-id="ee73a-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ee73a-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ee73a-119">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ee73a-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ee73a-120">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ee73a-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee73a-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee73a-121">Remarks</span></span>

<span data-ttu-id="ee73a-122">Si los vectores de destino son mayores que los vectores de origen, solo se rellenarán los componentes iniciales de cada vector de destino y los demás componentes de vector de destino se establecerán en cero.</span><span class="sxs-lookup"><span data-stu-id="ee73a-122">If the destination vectors are larger than the source vectors, only the initial components of each destination vector will be filled, and the remaining destination vector components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee73a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee73a-123">Requirements</span></span>



| <span data-ttu-id="ee73a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee73a-124">Requirement</span></span> | <span data-ttu-id="ee73a-125">Value</span><span class="sxs-lookup"><span data-stu-id="ee73a-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee73a-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee73a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ee73a-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee73a-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ee73a-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ee73a-128">Library</span></span><br/> | <dl> <span data-ttu-id="ee73a-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee73a-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ee73a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee73a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee73a-131">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="ee73a-131">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="ee73a-132">**SetVectorArray**</span><span class="sxs-lookup"><span data-stu-id="ee73a-132">**SetVectorArray**</span></span>](id3dxbaseeffect--setvectorarray.md)
</dt> </dl>

 

 
