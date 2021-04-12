---
description: Utiliza un sistema de coordenadas de la mano izquierda para crear una malla que contenga un tetera.
ms.assetid: c002d6d4-1829-4293-9a86-d8560d6ec0e9
title: Función D3DXCreateTeapot (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTeapot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 13f5ed44bdc31958729209f01183eba409298fcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280329"
---
# <a name="d3dxcreateteapot-function"></a><span data-ttu-id="84dea-103">D3DXCreateTeapot función)</span><span class="sxs-lookup"><span data-stu-id="84dea-103">D3DXCreateTeapot function</span></span>

<span data-ttu-id="84dea-104">Utiliza un sistema de coordenadas de la mano izquierda para crear una malla que contenga un tetera.</span><span class="sxs-lookup"><span data-stu-id="84dea-104">Uses a left-handed coordinate system to create a mesh containing a teapot.</span></span>

## <a name="syntax"></a><span data-ttu-id="84dea-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84dea-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTeapot(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="84dea-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84dea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84dea-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84dea-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84dea-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="84dea-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="84dea-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la malla tetera creada.</span><span class="sxs-lookup"><span data-stu-id="84dea-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created teapot mesh.</span></span>

</dd> <dt>

<span data-ttu-id="84dea-110">*ppMesh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="84dea-110">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84dea-111">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="84dea-111">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="84dea-112">Dirección de un puntero a la forma de salida, una interfaz [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="84dea-112">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="84dea-113">*ppAdjacency* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="84dea-113">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84dea-114">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="84dea-114">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="84dea-115">Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="84dea-115">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="84dea-116">Cuando el método devuelve un valor, este parámetro se rellena con una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla.</span><span class="sxs-lookup"><span data-stu-id="84dea-116">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="84dea-117">Se puede especificar **null** .</span><span class="sxs-lookup"><span data-stu-id="84dea-117">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84dea-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84dea-118">Return value</span></span>

<span data-ttu-id="84dea-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="84dea-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="84dea-120">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="84dea-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="84dea-121">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="84dea-121">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="84dea-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="84dea-122">Remarks</span></span>

<span data-ttu-id="84dea-123">Esta función crea una malla con la \_ opción de creación administrada D3DXMESH y el formato de vértice flexible [normal de D3DFVF \_ XYZ \| D3DFVF \_ ](d3dfvf.md) (FVF).</span><span class="sxs-lookup"><span data-stu-id="84dea-123">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="84dea-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84dea-124">Requirements</span></span>



| <span data-ttu-id="84dea-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="84dea-125">Requirement</span></span> | <span data-ttu-id="84dea-126">Value</span><span class="sxs-lookup"><span data-stu-id="84dea-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84dea-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="84dea-127">Header</span></span><br/>  | <dl> <span data-ttu-id="84dea-128"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="84dea-128"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="84dea-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="84dea-129">Library</span></span><br/> | <dl> <span data-ttu-id="84dea-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="84dea-130"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="84dea-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="84dea-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84dea-132">Funciones de dibujo de forma</span><span class="sxs-lookup"><span data-stu-id="84dea-132">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
