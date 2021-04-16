---
description: Determina el producto de la matriz de traducción calculada determinada por los factores especificados (x, y y z) y la matriz actual.
ms.assetid: 96399801-dd80-4e9a-a5c3-c5d41eb9368a
title: 'ID3DXMATRIXStack:: TranslateLocal (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.TranslateLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 65a627141f552107d88c3f43988daa0d316a0bef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678851"
---
# <a name="id3dxmatrixstacktranslatelocal-method-d3dx10h"></a><span data-ttu-id="d6a61-103">ID3DXMATRIXStack:: TranslateLocal (método) (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="d6a61-103">ID3DXMATRIXStack::TranslateLocal method (D3DX10.h)</span></span>

<span data-ttu-id="d6a61-104">Determina el producto de la matriz de traducción calculada determinada por los factores especificados (x, y y z) y la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="d6a61-104">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6a61-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6a61-105">Syntax</span></span>


```C++
HRESULT TranslateLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="d6a61-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d6a61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6a61-107">*x* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="d6a61-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6a61-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6a61-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d6a61-109">Factor de traslación en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="d6a61-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="d6a61-110">*y* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="d6a61-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6a61-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6a61-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d6a61-112">Factor de traslación en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="d6a61-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="d6a61-113">*z* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="d6a61-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6a61-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6a61-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d6a61-115">Factor de traslación en la dirección z.</span><span class="sxs-lookup"><span data-stu-id="d6a61-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6a61-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d6a61-116">Return value</span></span>

<span data-ttu-id="d6a61-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d6a61-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d6a61-118">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d6a61-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6a61-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d6a61-119">Remarks</span></span>

<span data-ttu-id="d6a61-120">Este método multiplica a la izquierda la matriz actual con la matriz de conversión calculada (la transformación es sobre el origen local del objeto).</span><span class="sxs-lookup"><span data-stu-id="d6a61-120">This method left-multiplies the current matrix with the computed translation matrix (transformation is about the local origin of the object).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation(&tmp, x, y, z );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="d6a61-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6a61-121">Requirements</span></span>



| <span data-ttu-id="d6a61-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6a61-122">Requirement</span></span> | <span data-ttu-id="d6a61-123">Value</span><span class="sxs-lookup"><span data-stu-id="d6a61-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d6a61-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d6a61-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d6a61-125"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6a61-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d6a61-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d6a61-126">Library</span></span><br/> | <dl> <span data-ttu-id="d6a61-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6a61-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6a61-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6a61-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6a61-129">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="d6a61-129">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="d6a61-130">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="d6a61-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
