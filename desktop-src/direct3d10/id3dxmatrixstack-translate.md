---
description: 'Método ID3DXMATRIXStack::Translate (D3DX10.h): determina el producto de la matriz actual y la matriz de traducción calculada determinada por los factores especificados (x, y y z).'
ms.assetid: d6e347a5-bb66-451d-b66e-49ea8eff70b3
title: Método ID3DXMATRIXStack::Translate (D3DX10.h)
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
ms.openlocfilehash: 41e84b62c077da03806a5e781498c05ee3c8ee67
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107773"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx10h"></a><span data-ttu-id="64b21-103">Método ID3DXMATRIXStack::Translate (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="64b21-103">ID3DXMATRIXStack::Translate method (D3DX10.h)</span></span>

<span data-ttu-id="64b21-104">Determina el producto de la matriz actual y la matriz de traducción calculada determinada por los factores especificados (x, y y z).</span><span class="sxs-lookup"><span data-stu-id="64b21-104">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span>

## <a name="syntax"></a><span data-ttu-id="64b21-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="64b21-105">Syntax</span></span>


```C++
HRESULT Translate(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="64b21-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="64b21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64b21-107">*x* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="64b21-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64b21-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64b21-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64b21-109">Factor de traducción en la dirección X.</span><span class="sxs-lookup"><span data-stu-id="64b21-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="64b21-110">*y* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="64b21-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64b21-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64b21-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64b21-112">Factor de traducción en la dirección Y.</span><span class="sxs-lookup"><span data-stu-id="64b21-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="64b21-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64b21-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64b21-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64b21-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64b21-115">Factor de traducción en la dirección Z.</span><span class="sxs-lookup"><span data-stu-id="64b21-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64b21-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="64b21-116">Return value</span></span>

<span data-ttu-id="64b21-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="64b21-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="64b21-118">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="64b21-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="64b21-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="64b21-119">Remarks</span></span>

<span data-ttu-id="64b21-120">Este método multiplica a la derecha la matriz actual por la matriz de traducción calculada (la transformación trata sobre el origen del mundo actual).</span><span class="sxs-lookup"><span data-stu-id="64b21-120">This method right-multiplies the current matrix with the computed translation matrix (transformation is about the current world origin).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="64b21-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64b21-121">Requirements</span></span>



| <span data-ttu-id="64b21-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="64b21-122">Requirement</span></span> | <span data-ttu-id="64b21-123">Value</span><span class="sxs-lookup"><span data-stu-id="64b21-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="64b21-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="64b21-124">Header</span></span><br/>  | <dl> <span data-ttu-id="64b21-125"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="64b21-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="64b21-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="64b21-126">Library</span></span><br/> | <dl> <span data-ttu-id="64b21-127"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="64b21-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64b21-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="64b21-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64b21-129">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="64b21-129">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="64b21-130">D3DX Interfaces</span><span class="sxs-lookup"><span data-stu-id="64b21-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
