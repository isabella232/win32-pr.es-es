---
description: Gira (respecto al espacio de coordenadas universal) alrededor de un eje arbitrario.
ms.assetid: 25a7eff4-a575-4ddb-85eb-ef3fa2d6ae3b
title: 'ID3DXMATRIXStack:: RotateYawPitchRoll (método) (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateYawPitchRoll
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5020cb6ff3af41b9ef32ef77bb71607f6cd5ea6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717642"
---
# <a name="id3dxmatrixstackrotateyawpitchroll-method-d3dx9mathh"></a><span data-ttu-id="a792d-103">ID3DXMATRIXStack:: RotateYawPitchRoll (método) (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="a792d-103">ID3DXMATRIXStack::RotateYawPitchRoll method (D3dx9math.h)</span></span>

<span data-ttu-id="a792d-104">Gira (respecto al espacio de coordenadas universal) alrededor de un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="a792d-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="a792d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a792d-105">Syntax</span></span>


```C++
HRESULT RotateYawPitchRoll(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a><span data-ttu-id="a792d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a792d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a792d-107">*Guiñada* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a792d-107">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a792d-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a792d-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a792d-109">Guiñada alrededor del eje y en radianes.</span><span class="sxs-lookup"><span data-stu-id="a792d-109">The yaw around the y-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="a792d-110">*Paso* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a792d-110">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a792d-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a792d-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a792d-112">El paso alrededor del eje x en radianes.</span><span class="sxs-lookup"><span data-stu-id="a792d-112">The pitch around the x-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="a792d-113">Poner al *día* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a792d-113">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a792d-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a792d-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a792d-115">El rollo alrededor del eje z en radianes.</span><span class="sxs-lookup"><span data-stu-id="a792d-115">The roll around the z-axis in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a792d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a792d-116">Return value</span></span>

<span data-ttu-id="a792d-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a792d-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a792d-118">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a792d-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a792d-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a792d-119">Remarks</span></span>

<span data-ttu-id="a792d-120">Este método agrega la rotación a la pila de la matriz con la matriz de rotación calculada similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="a792d-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="a792d-121">Dado que la rotación se multiplica a la derecha en la pila de la matriz, la rotación es relativa al espacio de coordenadas universal.</span><span class="sxs-lookup"><span data-stu-id="a792d-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="a792d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a792d-122">Requirements</span></span>



| <span data-ttu-id="a792d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a792d-123">Requirement</span></span> | <span data-ttu-id="a792d-124">Value</span><span class="sxs-lookup"><span data-stu-id="a792d-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a792d-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a792d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a792d-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a792d-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a792d-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a792d-127">Library</span></span><br/> | <dl> <span data-ttu-id="a792d-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a792d-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a792d-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="a792d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a792d-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="a792d-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="a792d-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="a792d-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="a792d-132">**ID3DXMATRIXStack::RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="a792d-132">**ID3DXMATRIXStack::RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[<span data-ttu-id="a792d-133">**ID3DXMATRIXStack::RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="a792d-133">**ID3DXMATRIXStack::RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[<span data-ttu-id="a792d-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="a792d-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
