---
description: 'Método ID3DXMATRIXStack::RotateYawPitchRollLocal (D3dx9math.h): gira (en relación con el espacio de coordenadas local del objeto) alrededor de un eje arbitrario.'
ms.assetid: c69f5ea7-5d14-4187-9405-1ceff8230185
title: Método ID3DXMATRIXStack::RotateYawPtrixRollLocal (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateYawPitchRollLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1d104676b6d346afd527552dbfba4bac23ed09cd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093453"
---
# <a name="id3dxmatrixstackrotateyawpitchrolllocal-method-d3dx9mathh"></a><span data-ttu-id="57ca4-103">Método ID3DXMATRIXStack::RotateYawPtrixRollLocal (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="57ca4-103">ID3DXMATRIXStack::RotateYawPitchRollLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="57ca4-104">Gira (en relación con el espacio de coordenadas local del objeto) alrededor de un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="57ca4-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="57ca4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57ca4-105">Syntax</span></span>


```C++
HRESULT RotateYawPitchRollLocal(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a><span data-ttu-id="57ca4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="57ca4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57ca4-107">*Yaw* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="57ca4-107">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57ca4-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="57ca4-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="57ca4-109">La yaw alrededor del eje Y en radianes.</span><span class="sxs-lookup"><span data-stu-id="57ca4-109">The yaw around the y-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="57ca4-110">*Pitch* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="57ca4-110">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57ca4-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="57ca4-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="57ca4-112">Paso alrededor del eje X en radianes.</span><span class="sxs-lookup"><span data-stu-id="57ca4-112">The pitch around the x-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="57ca4-113">*Roll* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="57ca4-113">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57ca4-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="57ca4-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="57ca4-115">La rotación alrededor del eje Z en radianes.</span><span class="sxs-lookup"><span data-stu-id="57ca4-115">The roll around the z-axis in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57ca4-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57ca4-116">Return value</span></span>

<span data-ttu-id="57ca4-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="57ca4-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="57ca4-118">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="57ca4-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="57ca4-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="57ca4-119">Remarks</span></span>

<span data-ttu-id="57ca4-120">Este método agrega la rotación a la pila de matriz con la matriz de rotación calculada similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="57ca4-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="57ca4-121">Dado que la rotación se multiplica a la izquierda en la pila de matriz, la rotación es relativa al espacio de coordenadas local del objeto.</span><span class="sxs-lookup"><span data-stu-id="57ca4-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="57ca4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57ca4-122">Requirements</span></span>



| <span data-ttu-id="57ca4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="57ca4-123">Requirement</span></span> | <span data-ttu-id="57ca4-124">Value</span><span class="sxs-lookup"><span data-stu-id="57ca4-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="57ca4-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="57ca4-125">Header</span></span><br/>  | <dl> <span data-ttu-id="57ca4-126"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="57ca4-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="57ca4-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="57ca4-127">Library</span></span><br/> | <dl> <span data-ttu-id="57ca4-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="57ca4-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="57ca4-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="57ca4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57ca4-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="57ca4-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="57ca4-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="57ca4-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="57ca4-132">**ID3DXMATRIXStack::RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="57ca4-132">**ID3DXMATRIXStack::RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[<span data-ttu-id="57ca4-133">**ID3DXMATRIXStack::RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="57ca4-133">**ID3DXMATRIXStack::RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[<span data-ttu-id="57ca4-134">**ID3DXMATRIXStack::RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="57ca4-134">**ID3DXMATRIXStack::RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> </dl>

 

 
