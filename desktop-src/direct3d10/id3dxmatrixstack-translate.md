---
description: Determina el producto de la matriz actual y la matriz de traslación calculada determinada por los factores especificados (x, y y z).
ms.assetid: d6e347a5-bb66-451d-b66e-49ea8eff70b3
title: 'ID3DXMATRIXStack:: translate (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Translate
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 159e1dc6b3dabeb92b32798cbe318f6c72c01d70
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708101"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx10h"></a><span data-ttu-id="36abc-103">ID3DXMATRIXStack:: translate (método) (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="36abc-103">ID3DXMATRIXStack::Translate method (D3DX10.h)</span></span>

<span data-ttu-id="36abc-104">Determina el producto de la matriz actual y la matriz de traslación calculada determinada por los factores especificados (x, y y z).</span><span class="sxs-lookup"><span data-stu-id="36abc-104">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span>

## <a name="syntax"></a><span data-ttu-id="36abc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36abc-105">Syntax</span></span>


```C++
HRESULT Translate(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="36abc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="36abc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36abc-107">*x* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="36abc-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36abc-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36abc-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36abc-109">Factor de traslación en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="36abc-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="36abc-110">*y* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="36abc-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36abc-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36abc-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36abc-112">Factor de traslación en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="36abc-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="36abc-113">*z* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="36abc-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36abc-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36abc-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36abc-115">Factor de traslación en la dirección z.</span><span class="sxs-lookup"><span data-stu-id="36abc-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36abc-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="36abc-116">Return value</span></span>

<span data-ttu-id="36abc-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="36abc-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="36abc-118">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="36abc-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="36abc-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="36abc-119">Remarks</span></span>

<span data-ttu-id="36abc-120">Este método multiplica la matriz actual con la matriz de traslación calculada (la transformación es sobre el origen mundial actual).</span><span class="sxs-lookup"><span data-stu-id="36abc-120">This method right-multiplies the current matrix with the computed translation matrix (transformation is about the current world origin).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="36abc-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36abc-121">Requirements</span></span>



| <span data-ttu-id="36abc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="36abc-122">Requirement</span></span> | <span data-ttu-id="36abc-123">Value</span><span class="sxs-lookup"><span data-stu-id="36abc-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="36abc-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="36abc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="36abc-125"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="36abc-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="36abc-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="36abc-126">Library</span></span><br/> | <dl> <span data-ttu-id="36abc-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="36abc-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36abc-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="36abc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36abc-129">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="36abc-129">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="36abc-130">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="36abc-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
