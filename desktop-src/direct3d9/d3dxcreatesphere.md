---
description: Utiliza un sistema de coordenadas de la mano izquierda para crear una malla que contenga una esfera.
ms.assetid: d3198805-9435-4849-892d-ec98dc2221d2
title: Función D3DXCreateSphere (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e56ac6b8e8cc2195e2176e505cf430ea33b6b6ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280330"
---
# <a name="d3dxcreatesphere-function"></a><span data-ttu-id="41e10-103">D3DXCreateSphere función)</span><span class="sxs-lookup"><span data-stu-id="41e10-103">D3DXCreateSphere function</span></span>

<span data-ttu-id="41e10-104">Utiliza un sistema de coordenadas de la mano izquierda para crear una malla que contenga una esfera.</span><span class="sxs-lookup"><span data-stu-id="41e10-104">Uses a left-handed coordinate system to create a mesh containing a sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="41e10-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="41e10-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSphere(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Radius,
  _In_  UINT              Slices,
  _In_  UINT              Stacks,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="41e10-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="41e10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41e10-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="41e10-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41e10-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="41e10-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="41e10-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la malla de esfera creada.</span><span class="sxs-lookup"><span data-stu-id="41e10-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created sphere mesh.</span></span>

</dd> <dt>

<span data-ttu-id="41e10-110">*RADIUS* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="41e10-110">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41e10-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41e10-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41e10-112">Radio de la esfera.</span><span class="sxs-lookup"><span data-stu-id="41e10-112">Radius of the sphere.</span></span> <span data-ttu-id="41e10-113">Este valor debe ser mayor o igual que 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="41e10-113">This value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="41e10-114">*Segmentos* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="41e10-114">*Slices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41e10-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41e10-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41e10-116">Número de segmentos sobre el eje principal.</span><span class="sxs-lookup"><span data-stu-id="41e10-116">Number of slices about the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="41e10-117">*Pilas de* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="41e10-117">*Stacks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41e10-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41e10-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41e10-119">Número de pilas a lo largo del eje principal.</span><span class="sxs-lookup"><span data-stu-id="41e10-119">Number of stacks along the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="41e10-120">*ppMesh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="41e10-120">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41e10-121">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="41e10-121">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="41e10-122">Dirección de un puntero a la forma de salida, una interfaz [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="41e10-122">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="41e10-123">*ppAdjacency* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="41e10-123">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41e10-124">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="41e10-124">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="41e10-125">Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="41e10-125">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="41e10-126">Cuando el método devuelve un valor, este parámetro se rellena con una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla.</span><span class="sxs-lookup"><span data-stu-id="41e10-126">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="41e10-127">Se puede especificar **null** .</span><span class="sxs-lookup"><span data-stu-id="41e10-127">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41e10-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="41e10-128">Return value</span></span>

<span data-ttu-id="41e10-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="41e10-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="41e10-130">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="41e10-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="41e10-131">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="41e10-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="41e10-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="41e10-132">Remarks</span></span>

<span data-ttu-id="41e10-133">La esfera creada se centra en el origen y su eje se alinea con el eje z.</span><span class="sxs-lookup"><span data-stu-id="41e10-133">The created sphere is centered at the origin, and its axis is aligned with the z-axis.</span></span>

<span data-ttu-id="41e10-134">Esta función crea una malla con la \_ opción de creación administrada D3DXMESH y el formato de vértice flexible [normal de D3DFVF \_ XYZ \| D3DFVF \_ ](d3dfvf.md) (FVF).</span><span class="sxs-lookup"><span data-stu-id="41e10-134">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="41e10-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41e10-135">Requirements</span></span>



| <span data-ttu-id="41e10-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="41e10-136">Requirement</span></span> | <span data-ttu-id="41e10-137">Value</span><span class="sxs-lookup"><span data-stu-id="41e10-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41e10-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41e10-138">Header</span></span><br/>  | <dl> <span data-ttu-id="41e10-139"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="41e10-139"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="41e10-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="41e10-140">Library</span></span><br/> | <dl> <span data-ttu-id="41e10-141"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41e10-141"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="41e10-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="41e10-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41e10-143">Funciones de dibujo de forma</span><span class="sxs-lookup"><span data-stu-id="41e10-143">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
