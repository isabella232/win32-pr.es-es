---
description: 'Método ID3DXMATRIXStack::ScaleLocal (D3dx9math.h): escala la matriz actual sobre el origen del objeto.'
ms.assetid: fe71da67-c8c9-4c78-9055-9bc3cadc0780
title: Método ID3DXMATRIXStack::ScaleLocal (D3dx9math.h)
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
ms.openlocfilehash: 5bd9f47b6c38b5ec72bcd25ecb5981859a87038b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093333"
---
# <a name="id3dxmatrixstackscalelocal-method-d3dx9mathh"></a><span data-ttu-id="2bdce-103">Método ID3DXMATRIXStack::ScaleLocal (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="2bdce-103">ID3DXMATRIXStack::ScaleLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="2bdce-104">Escale la matriz actual sobre el origen del objeto.</span><span class="sxs-lookup"><span data-stu-id="2bdce-104">Scale the current matrix about the object origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bdce-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2bdce-105">Syntax</span></span>


```C++
HRESULT ScaleLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="2bdce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2bdce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bdce-107">*x* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="2bdce-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bdce-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2bdce-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2bdce-109">Componente de escalado en la dirección X.</span><span class="sxs-lookup"><span data-stu-id="2bdce-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="2bdce-110">*y* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="2bdce-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bdce-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2bdce-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2bdce-112">Componente de escalado en la dirección Y.</span><span class="sxs-lookup"><span data-stu-id="2bdce-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="2bdce-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2bdce-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bdce-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2bdce-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2bdce-115">Componente de escalado en dirección z.</span><span class="sxs-lookup"><span data-stu-id="2bdce-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bdce-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2bdce-116">Return value</span></span>

<span data-ttu-id="2bdce-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2bdce-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2bdce-118">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2bdce-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bdce-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2bdce-119">Remarks</span></span>

<span data-ttu-id="2bdce-120">Este método multiplica a la izquierda la matriz actual con la matriz de escala calculada.</span><span class="sxs-lookup"><span data-stu-id="2bdce-120">This method left-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="2bdce-121">La transformación trata sobre el origen local del objeto.</span><span class="sxs-lookup"><span data-stu-id="2bdce-121">The transformation is about the local origin of the object.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="2bdce-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bdce-122">Requirements</span></span>



| <span data-ttu-id="2bdce-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bdce-123">Requirement</span></span> | <span data-ttu-id="2bdce-124">Value</span><span class="sxs-lookup"><span data-stu-id="2bdce-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2bdce-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2bdce-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2bdce-126"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="2bdce-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2bdce-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2bdce-127">Library</span></span><br/> | <dl> <span data-ttu-id="2bdce-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2bdce-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2bdce-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2bdce-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bdce-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="2bdce-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="2bdce-131">**ID3DXMATRIXStack::Scale**</span><span class="sxs-lookup"><span data-stu-id="2bdce-131">**ID3DXMATRIXStack::Scale**</span></span>](id3dxmatrixstack--scale.md)
</dt> </dl>

 

 
