---
description: Crea una instancia de la interfaz ID3DXMATRIXStack.
ms.assetid: bb067b38-efc6-4ed8-9eef-14b3cc70660f
title: Función D3DXCreateMatrixStack (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 08e1ac23d5f6bcd874b1d5bd7f60313a232b0563
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698348"
---
# <a name="d3dxcreatematrixstack-function-d3dx9mathh"></a><span data-ttu-id="53b8a-103">Función D3DXCreateMatrixStack (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="53b8a-103">D3DXCreateMatrixStack function (D3dx9math.h)</span></span>

<span data-ttu-id="53b8a-104">Crea una instancia de la interfaz [**ID3DXMATRIXStack**](id3dxmatrixstack.md) .</span><span class="sxs-lookup"><span data-stu-id="53b8a-104">Creates an instance of the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="53b8a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53b8a-105">Syntax</span></span>


```C++
HRESULT D3DXCreateMatrixStack(
  _In_  DWORD             Flags,
  _Out_ LPD3DXMATRIXSTACK *ppStack
);
```



## <a name="parameters"></a><span data-ttu-id="53b8a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53b8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53b8a-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="53b8a-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53b8a-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53b8a-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53b8a-109">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="53b8a-109">Not implemented.</span></span> <span data-ttu-id="53b8a-110">Especifique cero.</span><span class="sxs-lookup"><span data-stu-id="53b8a-110">Specify zero.</span></span>

</dd> <dt>

<span data-ttu-id="53b8a-111">*ppStack* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="53b8a-111">*ppStack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53b8a-112">Tipo: **LPD3DXMATRIXSTACK \***</span><span class="sxs-lookup"><span data-stu-id="53b8a-112">Type: **LPD3DXMATRIXSTACK\***</span></span>

<span data-ttu-id="53b8a-113">Dirección de un puntero que rellena con un puntero de la interfaz [**ID3DXMATRIXStack**](id3dxmatrixstack.md) si la función se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="53b8a-113">Address of a pointer filled with an [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface pointer if the function succeeds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53b8a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53b8a-114">Return value</span></span>

<span data-ttu-id="53b8a-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="53b8a-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="53b8a-116">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="53b8a-116">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="53b8a-117">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="53b8a-117">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="53b8a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53b8a-118">Requirements</span></span>



| <span data-ttu-id="53b8a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="53b8a-119">Requirement</span></span> | <span data-ttu-id="53b8a-120">Value</span><span class="sxs-lookup"><span data-stu-id="53b8a-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53b8a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53b8a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="53b8a-122"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="53b8a-122"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="53b8a-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="53b8a-123">Library</span></span><br/> | <dl> <span data-ttu-id="53b8a-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53b8a-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="53b8a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="53b8a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53b8a-126">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="53b8a-126">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
