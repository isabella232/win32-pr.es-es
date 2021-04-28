---
description: 'Método ID3DXMATRIXStack::Scale (D3DX10.h): escale la matriz actual sobre el origen de la coordenada mundial.'
ms.assetid: d0f4b341-b3b6-42e4-84df-78f203c3728e
title: Método ID3DXMATRIXStack::Scale (D3DX10.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a7b4aceb53659fc2b1a4a95f964d068e6d7d2554
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107793"
---
# <a name="id3dxmatrixstackscale-method-d3dx10h"></a><span data-ttu-id="af2c7-103">Método ID3DXMATRIXStack::Scale (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="af2c7-103">ID3DXMATRIXStack::Scale method (D3DX10.h)</span></span>

<span data-ttu-id="af2c7-104">Escale la matriz actual sobre el origen de la coordenada mundial.</span><span class="sxs-lookup"><span data-stu-id="af2c7-104">Scale the current matrix about the world coordinate origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="af2c7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="af2c7-105">Syntax</span></span>


```C++
HRESULT Scale(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="af2c7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="af2c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af2c7-107">*x* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="af2c7-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af2c7-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="af2c7-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="af2c7-109">Componente de escalado en la dirección X.</span><span class="sxs-lookup"><span data-stu-id="af2c7-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="af2c7-110">*y* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="af2c7-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af2c7-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="af2c7-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="af2c7-112">Componente de escalado en la dirección Y.</span><span class="sxs-lookup"><span data-stu-id="af2c7-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="af2c7-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af2c7-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af2c7-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="af2c7-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="af2c7-115">Componente de escalado en dirección z.</span><span class="sxs-lookup"><span data-stu-id="af2c7-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af2c7-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af2c7-116">Return value</span></span>

<span data-ttu-id="af2c7-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="af2c7-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="af2c7-118">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="af2c7-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="af2c7-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="af2c7-119">Remarks</span></span>

<span data-ttu-id="af2c7-120">Este método multiplica a la derecha la matriz actual por la matriz de escala calculada.</span><span class="sxs-lookup"><span data-stu-id="af2c7-120">This method right-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="af2c7-121">La transformación trata sobre el origen del mundo actual.</span><span class="sxs-lookup"><span data-stu-id="af2c7-121">The transformation is about the current world origin.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="af2c7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af2c7-122">Requirements</span></span>



| <span data-ttu-id="af2c7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="af2c7-123">Requirement</span></span> | <span data-ttu-id="af2c7-124">Value</span><span class="sxs-lookup"><span data-stu-id="af2c7-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af2c7-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="af2c7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="af2c7-126"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="af2c7-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="af2c7-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="af2c7-127">Library</span></span><br/> | <dl> <span data-ttu-id="af2c7-128"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="af2c7-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af2c7-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="af2c7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af2c7-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="af2c7-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="af2c7-131">D3DX Interfaces</span><span class="sxs-lookup"><span data-stu-id="af2c7-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
