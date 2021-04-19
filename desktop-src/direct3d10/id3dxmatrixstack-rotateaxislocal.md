---
description: Gira (en relación con el espacio de coordenadas local del objeto) alrededor de un eje arbitrario.
ms.assetid: 90837762-9bfe-4065-94b3-1ca61184a78e
title: 'ID3DXMATRIXStack:: RotateAxisLocal (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateAxisLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5b00e1fd5b678d89d6b5ca4680499f6fde723c12
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105689896"
---
# <a name="id3dxmatrixstackrotateaxislocal-method-d3dx10h"></a><span data-ttu-id="f69dc-103">ID3DXMATRIXStack:: RotateAxisLocal (método) (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="f69dc-103">ID3DXMATRIXStack::RotateAxisLocal method (D3DX10.h)</span></span>

<span data-ttu-id="f69dc-104">Gira (en relación con el espacio de coordenadas local del objeto) alrededor de un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="f69dc-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="f69dc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f69dc-105">Syntax</span></span>


```C++
HRESULT RotateAxisLocal(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="f69dc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f69dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f69dc-107">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f69dc-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f69dc-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f69dc-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="f69dc-109">Puntero al eje arbitrario de rotación.</span><span class="sxs-lookup"><span data-stu-id="f69dc-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="f69dc-110">Vea [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="f69dc-110">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="f69dc-111">*Ángulo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f69dc-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f69dc-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f69dc-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f69dc-113">Ángulo de giro alrededor del eje arbitrario, en radianes.</span><span class="sxs-lookup"><span data-stu-id="f69dc-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="f69dc-114">Los ángulos se miden en sentido contrario a las agujas del reloj al mirar el eje arbitrario hacia el origen.</span><span class="sxs-lookup"><span data-stu-id="f69dc-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f69dc-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f69dc-115">Return value</span></span>

<span data-ttu-id="f69dc-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f69dc-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f69dc-117">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f69dc-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f69dc-118">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f69dc-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f69dc-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f69dc-119">Remarks</span></span>

<span data-ttu-id="f69dc-120">Este método agrega la rotación a la pila de la matriz con la matriz de rotación calculada similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="f69dc-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="f69dc-121">Dado que la rotación se multiplica a la izquierda en la pila de la matriz, la rotación es relativa al espacio de coordenadas local del objeto.</span><span class="sxs-lookup"><span data-stu-id="f69dc-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="f69dc-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f69dc-122">Requirements</span></span>



| <span data-ttu-id="f69dc-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f69dc-123">Requirement</span></span> | <span data-ttu-id="f69dc-124">Value</span><span class="sxs-lookup"><span data-stu-id="f69dc-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f69dc-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f69dc-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f69dc-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f69dc-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f69dc-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f69dc-127">Library</span></span><br/> | <dl> <span data-ttu-id="f69dc-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f69dc-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f69dc-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f69dc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f69dc-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="f69dc-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="f69dc-131">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="f69dc-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
