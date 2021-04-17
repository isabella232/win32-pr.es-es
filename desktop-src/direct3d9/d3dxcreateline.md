---
description: Utiliza un sistema de coordenadas de la mano izquierda para crear una línea.
ms.assetid: 0d2ef331-9edf-4b0a-ace4-ecb8bb2f7352
title: Función D3DXCreateLine (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateLine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5cf7d75ca63d64be39733b36a1b7d7a1b464238e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698218"
---
# <a name="d3dxcreateline-function"></a><span data-ttu-id="b9771-103">D3DXCreateLine función)</span><span class="sxs-lookup"><span data-stu-id="b9771-103">D3DXCreateLine function</span></span>

<span data-ttu-id="b9771-104">Utiliza un sistema de coordenadas de la mano izquierda para crear una línea.</span><span class="sxs-lookup"><span data-stu-id="b9771-104">Uses a left-handed coordinate system to create a line.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9771-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9771-105">Syntax</span></span>


```C++
HRESULT D3DXCreateLine(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXLINE        *ppLine
);
```



## <a name="parameters"></a><span data-ttu-id="b9771-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b9771-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9771-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b9771-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9771-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="b9771-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="b9771-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la malla de cuadro creada.</span><span class="sxs-lookup"><span data-stu-id="b9771-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created box mesh.</span></span>

</dd> <dt>

<span data-ttu-id="b9771-110">*ppLine* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b9771-110">*ppLine* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9771-111">Tipo: **[ **LPD3DXLINE**](id3dxline.md)\***</span><span class="sxs-lookup"><span data-stu-id="b9771-111">Type: **[**LPD3DXLINE**](id3dxline.md)\***</span></span>

<span data-ttu-id="b9771-112">Puntero a una interfaz [**ID3DXLine**](id3dxline.md) .</span><span class="sxs-lookup"><span data-stu-id="b9771-112">Pointer to an [**ID3DXLine**](id3dxline.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9771-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9771-113">Return value</span></span>

<span data-ttu-id="b9771-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b9771-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b9771-115">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b9771-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b9771-116">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="b9771-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9771-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b9771-117">Remarks</span></span>

<span data-ttu-id="b9771-118">Esta función crea una malla con la \_ opción de creación administrada D3DXMESH y el formato de vértice flexible [normal de D3DFVF \_ XYZ \| D3DFVF \_ ](d3dfvf.md) (FVF).</span><span class="sxs-lookup"><span data-stu-id="b9771-118">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) Flexible Vertex Format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="b9771-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9771-119">Requirements</span></span>



| <span data-ttu-id="b9771-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9771-120">Requirement</span></span> | <span data-ttu-id="b9771-121">Value</span><span class="sxs-lookup"><span data-stu-id="b9771-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9771-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b9771-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b9771-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9771-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="b9771-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b9771-124">Library</span></span><br/> | <dl> <span data-ttu-id="b9771-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9771-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b9771-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9771-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9771-127">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="b9771-127">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
