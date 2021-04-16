---
description: Cree una pila de matriz.
ms.assetid: df0f3564-0226-44b8-b22b-4dd27905c44c
title: Función D3DXCreateMatrixStack (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMatrixStack
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b5799632f171d1b80f95f0f684bb22d24f741f6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424472"
---
# <a name="d3dxcreatematrixstack-function-d3dx10mathh"></a><span data-ttu-id="b1456-103">Función D3DXCreateMatrixStack (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="b1456-103">D3DXCreateMatrixStack function (D3DX10Math.h)</span></span>

<span data-ttu-id="b1456-104">Cree una pila de matriz.</span><span class="sxs-lookup"><span data-stu-id="b1456-104">Create a matrix stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1456-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1456-105">Syntax</span></span>


```C++
HRESULT D3DXCreateMatrixStack(
  _In_  UINT              Flags,
  _Out_ LPD3DXMATRIXSTACK *ppStack
);
```



## <a name="parameters"></a><span data-ttu-id="b1456-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b1456-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1456-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="b1456-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1456-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1456-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1456-109">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="b1456-109">Not implemented.</span></span> <span data-ttu-id="b1456-110">Especifique cero.</span><span class="sxs-lookup"><span data-stu-id="b1456-110">Specify zero.</span></span>

</dd> <dt>

<span data-ttu-id="b1456-111">*ppStack* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b1456-111">*ppStack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1456-112">Tipo: **LPD3DXMATRIXSTACK \***</span><span class="sxs-lookup"><span data-stu-id="b1456-112">Type: **LPD3DXMATRIXSTACK\***</span></span>

<span data-ttu-id="b1456-113">Dirección de un puntero a una pila de matrices (vea la [**interfaz ID3DXMatrixStack**](d3d10-id3dxmatrixstack.md)).</span><span class="sxs-lookup"><span data-stu-id="b1456-113">The address of a pointer to a matrix stack (see [**ID3DXMatrixStack Interface**](d3d10-id3dxmatrixstack.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1456-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b1456-114">Return value</span></span>

<span data-ttu-id="b1456-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b1456-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b1456-116">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b1456-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1456-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1456-117">Requirements</span></span>



| <span data-ttu-id="b1456-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1456-118">Requirement</span></span> | <span data-ttu-id="b1456-119">Value</span><span class="sxs-lookup"><span data-stu-id="b1456-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1456-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b1456-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b1456-121"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1456-121"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="b1456-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b1456-122">Library</span></span><br/> | <dl> <span data-ttu-id="b1456-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1456-123"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b1456-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1456-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1456-125">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="b1456-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
