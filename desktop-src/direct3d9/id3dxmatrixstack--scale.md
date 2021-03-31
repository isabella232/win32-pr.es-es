---
description: Escalar la matriz actual sobre el origen de la coordenada mundial.
ms.assetid: 6c4ef625-736e-41a0-8a79-4d71e8685754
title: 'ID3DXMATRIXStack:: Scale (método) (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Scale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5ed926a55c0dba6f74e819cd89a7fa75f6d087c4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157144"
---
# <a name="id3dxmatrixstackscale-method-d3dx9mathh"></a><span data-ttu-id="e1d86-103">ID3DXMATRIXStack:: Scale (método) (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="e1d86-103">ID3DXMATRIXStack::Scale method (D3dx9math.h)</span></span>

<span data-ttu-id="e1d86-104">Escalar la matriz actual sobre el origen de la coordenada mundial.</span><span class="sxs-lookup"><span data-stu-id="e1d86-104">Scale the current matrix about the world coordinate origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1d86-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1d86-105">Syntax</span></span>


```C++
HRESULT Scale(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="e1d86-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1d86-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1d86-107">*x* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="e1d86-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1d86-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1d86-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e1d86-109">Componente de escala en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="e1d86-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="e1d86-110">*y* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="e1d86-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1d86-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1d86-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e1d86-112">Componente de escala en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="e1d86-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="e1d86-113">*z* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="e1d86-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1d86-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1d86-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e1d86-115">Componente de escala en la dirección z.</span><span class="sxs-lookup"><span data-stu-id="e1d86-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1d86-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1d86-116">Return value</span></span>

<span data-ttu-id="e1d86-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e1d86-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e1d86-118">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e1d86-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1d86-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1d86-119">Remarks</span></span>

<span data-ttu-id="e1d86-120">Este método multiplica a la derecha la matriz actual con la matriz de escala calculada.</span><span class="sxs-lookup"><span data-stu-id="e1d86-120">This method right-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="e1d86-121">La transformación es sobre el origen mundial actual.</span><span class="sxs-lookup"><span data-stu-id="e1d86-121">The transformation is about the current world origin.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="e1d86-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1d86-122">Requirements</span></span>



| <span data-ttu-id="e1d86-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1d86-123">Requirement</span></span> | <span data-ttu-id="e1d86-124">Value</span><span class="sxs-lookup"><span data-stu-id="e1d86-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1d86-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e1d86-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e1d86-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1d86-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e1d86-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e1d86-127">Library</span></span><br/> | <dl> <span data-ttu-id="e1d86-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1d86-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e1d86-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1d86-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1d86-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="e1d86-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="e1d86-131">**ID3DXMATRIXStack::ScaleLocal**</span><span class="sxs-lookup"><span data-stu-id="e1d86-131">**ID3DXMATRIXStack::ScaleLocal**</span></span>](id3dxmatrixstack--scalelocal.md)
</dt> </dl>

 

 
