---
description: 'Método ID3DXMATRIXStack::Scale (D3dx9math.h): escale la matriz actual sobre el origen de coordenadas del mundo.'
ms.assetid: 6c4ef625-736e-41a0-8a79-4d71e8685754
title: Método ID3DXMATRIXStack::Scale (D3dx9math.h)
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
ms.openlocfilehash: 6d877fccf5bfebfdc1f9cf3943c4334e5b8c7fff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093373"
---
# <a name="id3dxmatrixstackscale-method-d3dx9mathh"></a><span data-ttu-id="a1404-103">Método ID3DXMATRIXStack::Scale (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="a1404-103">ID3DXMATRIXStack::Scale method (D3dx9math.h)</span></span>

<span data-ttu-id="a1404-104">Escale la matriz actual sobre el origen de coordenadas del mundo.</span><span class="sxs-lookup"><span data-stu-id="a1404-104">Scale the current matrix about the world coordinate origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1404-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1404-105">Syntax</span></span>


```C++
HRESULT Scale(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="a1404-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1404-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1404-107">*x* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="a1404-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1404-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1404-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1404-109">Componente de escalado en la dirección X.</span><span class="sxs-lookup"><span data-stu-id="a1404-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="a1404-110">*y* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="a1404-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1404-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1404-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1404-112">Componente de escalado en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="a1404-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="a1404-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1404-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1404-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1404-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1404-115">Componente de escalado en la dirección Z.</span><span class="sxs-lookup"><span data-stu-id="a1404-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1404-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a1404-116">Return value</span></span>

<span data-ttu-id="a1404-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a1404-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a1404-118">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a1404-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1404-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a1404-119">Remarks</span></span>

<span data-ttu-id="a1404-120">Este método multiplica a la derecha la matriz actual con la matriz de escala calculada.</span><span class="sxs-lookup"><span data-stu-id="a1404-120">This method right-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="a1404-121">La transformación trata sobre el origen del mundo actual.</span><span class="sxs-lookup"><span data-stu-id="a1404-121">The transformation is about the current world origin.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="a1404-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1404-122">Requirements</span></span>



| <span data-ttu-id="a1404-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1404-123">Requirement</span></span> | <span data-ttu-id="a1404-124">Value</span><span class="sxs-lookup"><span data-stu-id="a1404-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1404-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1404-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a1404-126"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="a1404-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a1404-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a1404-127">Library</span></span><br/> | <dl> <span data-ttu-id="a1404-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1404-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a1404-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a1404-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1404-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="a1404-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="a1404-131">**ID3DXMATRIXStack::ScaleLocal**</span><span class="sxs-lookup"><span data-stu-id="a1404-131">**ID3DXMATRIXStack::ScaleLocal**</span></span>](id3dxmatrixstack--scalelocal.md)
</dt> </dl>

 

 
