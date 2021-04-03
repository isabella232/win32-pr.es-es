---
description: Utiliza un sistema de coordenadas de la mano izquierda para crear una malla que contenga un polígono de una cara.
ms.assetid: f3313f55-3e60-4440-8bea-d2886b636c9a
title: Función D3DXCreatePolygon (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePolygon
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 94a7e48f512d25ca53d1f3ff80889a013e2ecdcb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083728"
---
# <a name="d3dxcreatepolygon-function"></a><span data-ttu-id="f0e24-103">D3DXCreatePolygon función)</span><span class="sxs-lookup"><span data-stu-id="f0e24-103">D3DXCreatePolygon function</span></span>

<span data-ttu-id="f0e24-104">Utiliza un sistema de coordenadas de la mano izquierda para crear una malla que contenga un polígono de una cara.</span><span class="sxs-lookup"><span data-stu-id="f0e24-104">Uses a left-handed coordinate system to create a mesh containing an n-sided polygon.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0e24-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0e24-105">Syntax</span></span>


```C++
HRESULT D3DXCreatePolygon(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Length,
  _In_  UINT              Sides,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="f0e24-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f0e24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0e24-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f0e24-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0e24-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="f0e24-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="f0e24-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la malla de polígono creada.</span><span class="sxs-lookup"><span data-stu-id="f0e24-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created polygon mesh.</span></span>

</dd> <dt>

<span data-ttu-id="f0e24-110">*Longitud* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f0e24-110">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0e24-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0e24-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f0e24-112">Longitud de cada lado.</span><span class="sxs-lookup"><span data-stu-id="f0e24-112">Length of each side.</span></span>

</dd> <dt>

<span data-ttu-id="f0e24-113">*Lados* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f0e24-113">*Sides* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0e24-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0e24-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f0e24-115">Número de lados del polígono.</span><span class="sxs-lookup"><span data-stu-id="f0e24-115">Number of sides for the polygon.</span></span> <span data-ttu-id="f0e24-116">El valor debe ser mayor o igual que 3.</span><span class="sxs-lookup"><span data-stu-id="f0e24-116">Value must be greater than or equal to 3.</span></span>

</dd> <dt>

<span data-ttu-id="f0e24-117">*ppMesh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f0e24-117">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0e24-118">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0e24-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="f0e24-119">Dirección de un puntero a la forma de salida, una interfaz [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="f0e24-119">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="f0e24-120">*ppAdjacency* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f0e24-120">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0e24-121">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0e24-121">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="f0e24-122">Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="f0e24-122">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="f0e24-123">Cuando el método devuelve un valor, este parámetro se rellena con una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla.</span><span class="sxs-lookup"><span data-stu-id="f0e24-123">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="f0e24-124">Se puede especificar **null** .</span><span class="sxs-lookup"><span data-stu-id="f0e24-124">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0e24-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f0e24-125">Return value</span></span>

<span data-ttu-id="f0e24-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f0e24-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f0e24-127">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f0e24-127">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f0e24-128">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f0e24-128">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0e24-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0e24-129">Remarks</span></span>

<span data-ttu-id="f0e24-130">El polígono creado se centra en el origen.</span><span class="sxs-lookup"><span data-stu-id="f0e24-130">The created polygon is centered at the origin.</span></span>

<span data-ttu-id="f0e24-131">Esta función crea una malla con la \_ opción de creación administrada D3DXMESH y el formato de vértice flexible [normal de D3DFVF \_ XYZ \| D3DFVF \_ ](d3dfvf.md) (FVF).</span><span class="sxs-lookup"><span data-stu-id="f0e24-131">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0e24-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0e24-132">Requirements</span></span>



| <span data-ttu-id="f0e24-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0e24-133">Requirement</span></span> | <span data-ttu-id="f0e24-134">Value</span><span class="sxs-lookup"><span data-stu-id="f0e24-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0e24-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0e24-135">Header</span></span><br/>  | <dl> <span data-ttu-id="f0e24-136"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0e24-136"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="f0e24-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f0e24-137">Library</span></span><br/> | <dl> <span data-ttu-id="f0e24-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0e24-138"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="f0e24-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0e24-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0e24-140">Funciones de dibujo de forma</span><span class="sxs-lookup"><span data-stu-id="f0e24-140">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
