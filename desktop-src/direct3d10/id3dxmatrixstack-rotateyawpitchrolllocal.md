---
description: 'Método ID3DXMATRIXStack::RotateYawPitchRollLocal (D3DX10.h): gira (en relación con el espacio de coordenadas local del objeto) alrededor de un eje arbitrario.'
ms.assetid: da023816-5176-460d-ab6b-909b89cc46cd
title: Método ID3DXMATRIXStack::RotateYawPitchRollLocal (D3DX10.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 726a6d7092b95f53d17625f68884b92d347de3a6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107843"
---
# <a name="id3dxmatrixstackrotateyawpitchrolllocal-method-d3dx10h"></a><span data-ttu-id="b1098-103">Método ID3DXMATRIXStack::RotateYawPitchRollLocal (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="b1098-103">ID3DXMATRIXStack::RotateYawPitchRollLocal method (D3DX10.h)</span></span>

<span data-ttu-id="b1098-104">Gira (en relación con el espacio de coordenadas local del objeto) alrededor de un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="b1098-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1098-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1098-105">Syntax</span></span>


```C++
HRESULT RotateYawPitchRollLocal(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a><span data-ttu-id="b1098-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b1098-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1098-107">*Yaw* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b1098-107">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1098-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1098-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1098-109">La yaw alrededor del eje Y en radianes.</span><span class="sxs-lookup"><span data-stu-id="b1098-109">The yaw around the y-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="b1098-110">*Pitch* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b1098-110">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1098-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1098-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1098-112">El tono alrededor del eje X en radianes.</span><span class="sxs-lookup"><span data-stu-id="b1098-112">The pitch around the x-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="b1098-113">*Roll* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b1098-113">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1098-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1098-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1098-115">La rotación alrededor del eje Z en radianes.</span><span class="sxs-lookup"><span data-stu-id="b1098-115">The roll around the z-axis in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1098-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b1098-116">Return value</span></span>

<span data-ttu-id="b1098-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b1098-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b1098-118">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b1098-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1098-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b1098-119">Remarks</span></span>

<span data-ttu-id="b1098-120">Este método agrega la rotación a la pila de matriz con la matriz de rotación calculada similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="b1098-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="b1098-121">Dado que la rotación se multiplica a la izquierda en la pila de matriz, la rotación es relativa al espacio de coordenadas local del objeto.</span><span class="sxs-lookup"><span data-stu-id="b1098-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1098-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1098-122">Requirements</span></span>



| <span data-ttu-id="b1098-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1098-123">Requirement</span></span> | <span data-ttu-id="b1098-124">Value</span><span class="sxs-lookup"><span data-stu-id="b1098-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1098-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b1098-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b1098-126"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="b1098-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b1098-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b1098-127">Library</span></span><br/> | <dl> <span data-ttu-id="b1098-128"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1098-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1098-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b1098-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1098-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="b1098-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="b1098-131">D3DX Interfaces</span><span class="sxs-lookup"><span data-stu-id="b1098-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
