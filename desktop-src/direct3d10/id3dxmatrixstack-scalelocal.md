---
description: 'Método ID3DXMATRIXStack::ScaleLocal (D3DX10.h): escale la matriz actual sobre el origen del objeto.'
ms.assetid: 748fce3a-a33c-4975-bbf0-dd3167a036f1
title: Método ID3DXMATRIXStack::ScaleLocal (D3DX10.h)
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
ms.openlocfilehash: 3961db0794703e3974dbd92d8eae8293173c2354
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107783"
---
# <a name="id3dxmatrixstackscalelocal-method-d3dx10h"></a><span data-ttu-id="08a4f-103">Método ID3DXMATRIXStack::ScaleLocal (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="08a4f-103">ID3DXMATRIXStack::ScaleLocal method (D3DX10.h)</span></span>

<span data-ttu-id="08a4f-104">Escale la matriz actual sobre el origen del objeto.</span><span class="sxs-lookup"><span data-stu-id="08a4f-104">Scale the current matrix about the object origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="08a4f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08a4f-105">Syntax</span></span>


```C++
HRESULT ScaleLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="08a4f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08a4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08a4f-107">*x* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="08a4f-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08a4f-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="08a4f-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="08a4f-109">Componente de escalado en la dirección X.</span><span class="sxs-lookup"><span data-stu-id="08a4f-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="08a4f-110">*y* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="08a4f-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08a4f-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="08a4f-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="08a4f-112">Componente de escalado en la dirección Y.</span><span class="sxs-lookup"><span data-stu-id="08a4f-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="08a4f-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08a4f-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08a4f-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="08a4f-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="08a4f-115">Componente de escalado en dirección z.</span><span class="sxs-lookup"><span data-stu-id="08a4f-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08a4f-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08a4f-116">Return value</span></span>

<span data-ttu-id="08a4f-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="08a4f-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="08a4f-118">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="08a4f-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="08a4f-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="08a4f-119">Remarks</span></span>

<span data-ttu-id="08a4f-120">Este método multiplica a la izquierda la matriz actual con la matriz de escala calculada.</span><span class="sxs-lookup"><span data-stu-id="08a4f-120">This method left-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="08a4f-121">La transformación trata sobre el origen local del objeto.</span><span class="sxs-lookup"><span data-stu-id="08a4f-121">The transformation is about the local origin of the object.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="08a4f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08a4f-122">Requirements</span></span>



| <span data-ttu-id="08a4f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="08a4f-123">Requirement</span></span> | <span data-ttu-id="08a4f-124">Value</span><span class="sxs-lookup"><span data-stu-id="08a4f-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="08a4f-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="08a4f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="08a4f-126"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="08a4f-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="08a4f-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="08a4f-127">Library</span></span><br/> | <dl> <span data-ttu-id="08a4f-128"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="08a4f-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08a4f-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="08a4f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08a4f-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="08a4f-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="08a4f-131">D3DX Interfaces</span><span class="sxs-lookup"><span data-stu-id="08a4f-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
