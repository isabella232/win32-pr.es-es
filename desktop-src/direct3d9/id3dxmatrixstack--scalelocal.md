---
description: Escala la matriz actual sobre el origen del objeto.
ms.assetid: fe71da67-c8c9-4c78-9055-9bc3cadc0780
title: 'ID3DXMATRIXStack:: ScaleLocal (método) (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 05b188e3f1b0322225584bc0ef7c194c52ef949f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280267"
---
# <a name="id3dxmatrixstackscalelocal-method-d3dx9mathh"></a><span data-ttu-id="77d55-103">ID3DXMATRIXStack:: ScaleLocal (método) (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="77d55-103">ID3DXMATRIXStack::ScaleLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="77d55-104">Escala la matriz actual sobre el origen del objeto.</span><span class="sxs-lookup"><span data-stu-id="77d55-104">Scale the current matrix about the object origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="77d55-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="77d55-105">Syntax</span></span>


```C++
HRESULT ScaleLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="77d55-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="77d55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77d55-107">*x* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="77d55-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77d55-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="77d55-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="77d55-109">Componente de escala en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="77d55-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="77d55-110">*y* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="77d55-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77d55-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="77d55-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="77d55-112">Componente de escala en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="77d55-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="77d55-113">*z* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="77d55-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77d55-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="77d55-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="77d55-115">Componente de escala en la dirección z.</span><span class="sxs-lookup"><span data-stu-id="77d55-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77d55-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77d55-116">Return value</span></span>

<span data-ttu-id="77d55-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="77d55-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="77d55-118">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="77d55-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="77d55-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77d55-119">Remarks</span></span>

<span data-ttu-id="77d55-120">Este método multiplica a la izquierda la matriz actual por la matriz de escala calculada.</span><span class="sxs-lookup"><span data-stu-id="77d55-120">This method left-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="77d55-121">La transformación es sobre el origen local del objeto.</span><span class="sxs-lookup"><span data-stu-id="77d55-121">The transformation is about the local origin of the object.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="77d55-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77d55-122">Requirements</span></span>



| <span data-ttu-id="77d55-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="77d55-123">Requirement</span></span> | <span data-ttu-id="77d55-124">Value</span><span class="sxs-lookup"><span data-stu-id="77d55-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="77d55-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="77d55-125">Header</span></span><br/>  | <dl> <span data-ttu-id="77d55-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="77d55-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="77d55-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="77d55-127">Library</span></span><br/> | <dl> <span data-ttu-id="77d55-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77d55-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="77d55-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="77d55-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77d55-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="77d55-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="77d55-131">**ID3DXMATRIXStack:: scale**</span><span class="sxs-lookup"><span data-stu-id="77d55-131">**ID3DXMATRIXStack::Scale**</span></span>](id3dxmatrixstack--scale.md)
</dt> </dl>

 

 
