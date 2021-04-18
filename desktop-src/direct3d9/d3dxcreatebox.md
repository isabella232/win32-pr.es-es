---
description: Utiliza un sistema de coordenadas de la mano izquierda para crear una malla que contenga un cuadro alineado con el eje.
ms.assetid: 396ef0f7-65d5-46f9-9b97-e6471f2fb5fe
title: Función D3DXCreateBox (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateBox
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 187c389dd2d90b4457237540026a63edc4ab4f4c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721443"
---
# <a name="d3dxcreatebox-function"></a><span data-ttu-id="20776-103">D3DXCreateBox función)</span><span class="sxs-lookup"><span data-stu-id="20776-103">D3DXCreateBox function</span></span>

<span data-ttu-id="20776-104">Utiliza un sistema de coordenadas de la mano izquierda para crear una malla que contenga un cuadro alineado con el eje.</span><span class="sxs-lookup"><span data-stu-id="20776-104">Uses a left-handed coordinate system to create a mesh containing an axis-aligned box.</span></span>

## <a name="syntax"></a><span data-ttu-id="20776-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20776-105">Syntax</span></span>


```C++
HRESULT D3DXCreateBox(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Width,
  _In_  FLOAT             Height,
  _In_  FLOAT             Depth,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="20776-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="20776-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20776-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="20776-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20776-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="20776-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="20776-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la malla de cuadro creada.</span><span class="sxs-lookup"><span data-stu-id="20776-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created box mesh.</span></span>

</dd> <dt>

<span data-ttu-id="20776-110">*Ancho* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="20776-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20776-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20776-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20776-112">Ancho del cuadro, a lo largo del eje x.</span><span class="sxs-lookup"><span data-stu-id="20776-112">Width of the box, along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="20776-113">*Alto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="20776-113">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20776-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20776-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20776-115">Alto del cuadro, a lo largo del eje y.</span><span class="sxs-lookup"><span data-stu-id="20776-115">Height of the box, along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="20776-116">*Nivel de detalle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="20776-116">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20776-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20776-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20776-118">Profundidad del cuadro, a lo largo del eje z.</span><span class="sxs-lookup"><span data-stu-id="20776-118">Depth of the box, along the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="20776-119">*ppMesh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="20776-119">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20776-120">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="20776-120">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="20776-121">Dirección de un puntero a la forma de salida, una interfaz [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="20776-121">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="20776-122">*ppAdjacency* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="20776-122">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20776-123">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="20776-123">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="20776-124">Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="20776-124">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="20776-125">Cuando el método devuelve un valor, este parámetro se rellena con una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla.</span><span class="sxs-lookup"><span data-stu-id="20776-125">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="20776-126">Se puede especificar **null** .</span><span class="sxs-lookup"><span data-stu-id="20776-126">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20776-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20776-127">Return value</span></span>

<span data-ttu-id="20776-128">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="20776-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="20776-129">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="20776-129">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="20776-130">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="20776-130">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="20776-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="20776-131">Remarks</span></span>

<span data-ttu-id="20776-132">El cuadro creado se centra en el origen.</span><span class="sxs-lookup"><span data-stu-id="20776-132">The created box is centered at the origin.</span></span>

<span data-ttu-id="20776-133">Esta función crea una malla con la \_ opción de creación administrada D3DXMESH y el formato de vértice flexible [normal de D3DFVF \_ XYZ \| D3DFVF \_ ](d3dfvf.md) (FVF).</span><span class="sxs-lookup"><span data-stu-id="20776-133">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="20776-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20776-134">Requirements</span></span>



| <span data-ttu-id="20776-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="20776-135">Requirement</span></span> | <span data-ttu-id="20776-136">Value</span><span class="sxs-lookup"><span data-stu-id="20776-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20776-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="20776-137">Header</span></span><br/>  | <dl> <span data-ttu-id="20776-138"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="20776-138"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="20776-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="20776-139">Library</span></span><br/> | <dl> <span data-ttu-id="20776-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20776-140"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="20776-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="20776-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20776-142">Funciones de dibujo de forma</span><span class="sxs-lookup"><span data-stu-id="20776-142">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
