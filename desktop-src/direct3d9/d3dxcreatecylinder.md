---
description: Utiliza un sistema de coordenadas de la mano izquierda para crear una malla que contenga un cilindro.
ms.assetid: 54b8a59e-d13f-44cb-84c0-f63c7b1ffb1b
title: Función D3DXCreateCylinder (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCylinder
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ec97755d45b21a85e1a73bbcd2214ee4c1e2358f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821143"
---
# <a name="d3dxcreatecylinder-function"></a><span data-ttu-id="31dab-103">D3DXCreateCylinder función)</span><span class="sxs-lookup"><span data-stu-id="31dab-103">D3DXCreateCylinder function</span></span>

<span data-ttu-id="31dab-104">Utiliza un sistema de coordenadas de la mano izquierda para crear una malla que contenga un cilindro.</span><span class="sxs-lookup"><span data-stu-id="31dab-104">Uses a left-handed coordinate system to create a mesh containing a cylinder.</span></span>

## <a name="syntax"></a><span data-ttu-id="31dab-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31dab-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCylinder(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Radius1,
  _In_  FLOAT             Radius2,
  _In_  FLOAT             Length,
  _In_  UINT              Slices,
  _In_  UINT              Stacks,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="31dab-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="31dab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31dab-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="31dab-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31dab-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="31dab-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="31dab-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la malla cilíndrica creada.</span><span class="sxs-lookup"><span data-stu-id="31dab-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created cylinder mesh.</span></span>

</dd> <dt>

<span data-ttu-id="31dab-110">*Radius1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="31dab-110">*Radius1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31dab-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31dab-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31dab-112">RADIUS en el extremo negativo Z.</span><span class="sxs-lookup"><span data-stu-id="31dab-112">Radius at the negative Z end.</span></span> <span data-ttu-id="31dab-113">El valor debe ser mayor o igual que 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="31dab-113">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="31dab-114">*Radius2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="31dab-114">*Radius2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31dab-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31dab-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31dab-116">Radio en el extremo positivo.</span><span class="sxs-lookup"><span data-stu-id="31dab-116">Radius at the positive Z end.</span></span> <span data-ttu-id="31dab-117">El valor debe ser mayor o igual que 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="31dab-117">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="31dab-118">*Longitud* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="31dab-118">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31dab-119">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31dab-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31dab-120">Longitud del cilindro a lo largo del eje z.</span><span class="sxs-lookup"><span data-stu-id="31dab-120">Length of the cylinder along the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="31dab-121">*Segmentos* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="31dab-121">*Slices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31dab-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31dab-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31dab-123">Número de segmentos sobre el eje principal.</span><span class="sxs-lookup"><span data-stu-id="31dab-123">Number of slices about the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="31dab-124">*Pilas de* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="31dab-124">*Stacks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31dab-125">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31dab-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31dab-126">Número de pilas a lo largo del eje principal.</span><span class="sxs-lookup"><span data-stu-id="31dab-126">Number of stacks along the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="31dab-127">*ppMesh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="31dab-127">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31dab-128">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="31dab-128">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="31dab-129">Dirección de un puntero a la forma de salida, una interfaz [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="31dab-129">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="31dab-130">*ppAdjacency* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="31dab-130">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31dab-131">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="31dab-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="31dab-132">Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="31dab-132">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="31dab-133">Cuando el método devuelve un valor, este parámetro se rellena con una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla.</span><span class="sxs-lookup"><span data-stu-id="31dab-133">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="31dab-134">Se puede especificar **null** .</span><span class="sxs-lookup"><span data-stu-id="31dab-134">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31dab-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31dab-135">Return value</span></span>

<span data-ttu-id="31dab-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="31dab-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="31dab-137">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="31dab-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="31dab-138">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="31dab-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="31dab-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31dab-139">Remarks</span></span>

<span data-ttu-id="31dab-140">El cilindro creado se centra en el origen y su eje está alineado con el eje z.</span><span class="sxs-lookup"><span data-stu-id="31dab-140">The created cylinder is centered at the origin, and its axis is aligned with the z-axis.</span></span>

<span data-ttu-id="31dab-141">Esta función crea una malla con la \_ opción de creación administrada D3DXMESH y el formato de vértice flexible [normal de D3DFVF \_ XYZ \| D3DFVF \_ ](d3dfvf.md) (FVF).</span><span class="sxs-lookup"><span data-stu-id="31dab-141">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="31dab-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31dab-142">Requirements</span></span>



| <span data-ttu-id="31dab-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="31dab-143">Requirement</span></span> | <span data-ttu-id="31dab-144">Value</span><span class="sxs-lookup"><span data-stu-id="31dab-144">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31dab-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31dab-145">Header</span></span><br/>  | <dl> <span data-ttu-id="31dab-146"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="31dab-146"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="31dab-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="31dab-147">Library</span></span><br/> | <dl> <span data-ttu-id="31dab-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31dab-148"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="31dab-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="31dab-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31dab-150">Funciones de dibujo de forma</span><span class="sxs-lookup"><span data-stu-id="31dab-150">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
