---
description: Gira (respecto al espacio de coordenadas universal) alrededor de un eje arbitrario.
ms.assetid: 7c842bf6-2d13-422e-8136-0506a76ce9fe
title: 'ID3DXMATRIXStack:: RotateAxis (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateAxis
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: badd26d61fa6580b0193039e29a8fceedabe2d3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362799"
---
# <a name="id3dxmatrixstackrotateaxis-method-d3dx10h"></a><span data-ttu-id="fb005-103">ID3DXMATRIXStack:: RotateAxis (método) (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="fb005-103">ID3DXMATRIXStack::RotateAxis method (D3DX10.h)</span></span>

<span data-ttu-id="fb005-104">Gira (respecto al espacio de coordenadas universal) alrededor de un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="fb005-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb005-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb005-105">Syntax</span></span>


```C++
HRESULT RotateAxis(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="fb005-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb005-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb005-107">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb005-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb005-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="fb005-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="fb005-109">Puntero al eje arbitrario de rotación.</span><span class="sxs-lookup"><span data-stu-id="fb005-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="fb005-110">Vea [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="fb005-110">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="fb005-111">*Ángulo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb005-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb005-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb005-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb005-113">Ángulo de giro alrededor del eje arbitrario, en radianes.</span><span class="sxs-lookup"><span data-stu-id="fb005-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="fb005-114">Los ángulos se miden en sentido contrario a las agujas del reloj al mirar el eje arbitrario hacia el origen.</span><span class="sxs-lookup"><span data-stu-id="fb005-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb005-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb005-115">Return value</span></span>

<span data-ttu-id="fb005-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fb005-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fb005-117">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fb005-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fb005-118">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="fb005-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb005-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb005-119">Remarks</span></span>

<span data-ttu-id="fb005-120">Este método agrega la rotación a la pila de la matriz con la matriz de rotación calculada similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="fb005-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="fb005-121">Dado que la rotación se multiplica a la derecha en la pila de la matriz, la rotación es relativa al espacio de coordenadas universal.</span><span class="sxs-lookup"><span data-stu-id="fb005-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb005-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb005-122">Requirements</span></span>



| <span data-ttu-id="fb005-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb005-123">Requirement</span></span> | <span data-ttu-id="fb005-124">Value</span><span class="sxs-lookup"><span data-stu-id="fb005-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fb005-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb005-125">Header</span></span><br/>  | <dl> <span data-ttu-id="fb005-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb005-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="fb005-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb005-127">Library</span></span><br/> | <dl> <span data-ttu-id="fb005-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb005-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb005-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb005-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb005-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="fb005-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="fb005-131">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="fb005-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
