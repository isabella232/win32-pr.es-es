---
description: Escala la matriz actual sobre el origen del objeto.
ms.assetid: 748fce3a-a33c-4975-bbf0-dd3167a036f1
title: 'ID3DXMATRIXStack:: ScaleLocal (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.ScaleLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 868aae418ebedbc54cb8f15ba4fa4e11d47c7f50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914810"
---
# <a name="id3dxmatrixstackscalelocal-method-d3dx10h"></a><span data-ttu-id="7b0a9-103">ID3DXMATRIXStack:: ScaleLocal (método) (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="7b0a9-103">ID3DXMATRIXStack::ScaleLocal method (D3DX10.h)</span></span>

<span data-ttu-id="7b0a9-104">Escala la matriz actual sobre el origen del objeto.</span><span class="sxs-lookup"><span data-stu-id="7b0a9-104">Scale the current matrix about the object origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b0a9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b0a9-105">Syntax</span></span>


```C++
HRESULT ScaleLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="7b0a9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7b0a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b0a9-107">*x* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="7b0a9-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b0a9-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7b0a9-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7b0a9-109">Componente de escala en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="7b0a9-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="7b0a9-110">*y* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="7b0a9-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b0a9-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7b0a9-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7b0a9-112">Componente de escala en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="7b0a9-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="7b0a9-113">*z* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="7b0a9-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b0a9-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7b0a9-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7b0a9-115">Componente de escala en la dirección z.</span><span class="sxs-lookup"><span data-stu-id="7b0a9-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b0a9-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b0a9-116">Return value</span></span>

<span data-ttu-id="7b0a9-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7b0a9-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7b0a9-118">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7b0a9-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b0a9-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7b0a9-119">Remarks</span></span>

<span data-ttu-id="7b0a9-120">Este método multiplica a la izquierda la matriz actual por la matriz de escala calculada.</span><span class="sxs-lookup"><span data-stu-id="7b0a9-120">This method left-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="7b0a9-121">La transformación es sobre el origen local del objeto.</span><span class="sxs-lookup"><span data-stu-id="7b0a9-121">The transformation is about the local origin of the object.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="7b0a9-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b0a9-122">Requirements</span></span>



| <span data-ttu-id="7b0a9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b0a9-123">Requirement</span></span> | <span data-ttu-id="7b0a9-124">Value</span><span class="sxs-lookup"><span data-stu-id="7b0a9-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7b0a9-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7b0a9-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7b0a9-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b0a9-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="7b0a9-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7b0a9-127">Library</span></span><br/> | <dl> <span data-ttu-id="7b0a9-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b0a9-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b0a9-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b0a9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b0a9-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="7b0a9-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="7b0a9-131">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="7b0a9-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
