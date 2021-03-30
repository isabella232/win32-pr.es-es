---
description: Utiliza un sistema de coordenadas de la mano izquierda para crear una malla que contenga un toro.
ms.assetid: 68df7650-8a87-4762-8b57-5704c419b0d7
title: Función D3DXCreateTorus (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTorus
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 384950ca1f00d0115135cf9ae36a2883ec5470e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280326"
---
# <a name="d3dxcreatetorus-function"></a><span data-ttu-id="e0182-103">D3DXCreateTorus función)</span><span class="sxs-lookup"><span data-stu-id="e0182-103">D3DXCreateTorus function</span></span>

<span data-ttu-id="e0182-104">Utiliza un sistema de coordenadas de la mano izquierda para crear una malla que contenga un toro.</span><span class="sxs-lookup"><span data-stu-id="e0182-104">Uses a left-handed coordinate system to create a mesh containing a torus.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0182-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0182-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTorus(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             InnerRadius,
  _In_  FLOAT             OuterRadius,
  _In_  UINT              Sides,
  _In_  UINT              Rings,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="e0182-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0182-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0182-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0182-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0182-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="e0182-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="e0182-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la malla de aro creada.</span><span class="sxs-lookup"><span data-stu-id="e0182-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created torus mesh.</span></span>

</dd> <dt>

<span data-ttu-id="e0182-110">*InnerRadius* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0182-110">*InnerRadius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0182-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0182-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0182-112">Radio interior del aro.</span><span class="sxs-lookup"><span data-stu-id="e0182-112">Inner-radius of the torus.</span></span> <span data-ttu-id="e0182-113">El valor debe ser mayor o igual que 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="e0182-113">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="e0182-114">*OuterRadius* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0182-114">*OuterRadius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0182-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0182-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0182-116">Radio exterior del aro.</span><span class="sxs-lookup"><span data-stu-id="e0182-116">Outer-radius of the torus.</span></span> <span data-ttu-id="e0182-117">El valor debe ser mayor o igual que 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="e0182-117">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="e0182-118">*Lados* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0182-118">*Sides* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0182-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0182-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0182-120">Número de lados de una sección transversal.</span><span class="sxs-lookup"><span data-stu-id="e0182-120">Number of sides in a cross-section.</span></span> <span data-ttu-id="e0182-121">El valor debe ser mayor o igual que 3.</span><span class="sxs-lookup"><span data-stu-id="e0182-121">Value must be greater than or equal to 3.</span></span>

</dd> <dt>

<span data-ttu-id="e0182-122">*Anillos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0182-122">*Rings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0182-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0182-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0182-124">Número de anillos que conforman el aro.</span><span class="sxs-lookup"><span data-stu-id="e0182-124">Number of rings making up the torus.</span></span> <span data-ttu-id="e0182-125">El valor debe ser mayor o igual que 3.</span><span class="sxs-lookup"><span data-stu-id="e0182-125">Value must be greater than or equal to 3.</span></span>

</dd> <dt>

<span data-ttu-id="e0182-126">*ppMesh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e0182-126">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0182-127">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="e0182-127">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="e0182-128">Dirección de un puntero a la forma de salida, una interfaz [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="e0182-128">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="e0182-129">*ppAdjacency* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e0182-129">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0182-130">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="e0182-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="e0182-131">Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="e0182-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="e0182-132">Cuando el método devuelve un valor, este parámetro se rellena con una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla.</span><span class="sxs-lookup"><span data-stu-id="e0182-132">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="e0182-133">Se puede especificar **null** .</span><span class="sxs-lookup"><span data-stu-id="e0182-133">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0182-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0182-134">Return value</span></span>

<span data-ttu-id="e0182-135">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e0182-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e0182-136">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e0182-136">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e0182-137">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="e0182-137">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0182-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0182-138">Remarks</span></span>

<span data-ttu-id="e0182-139">El aro creado se centra en el origen y su eje está alineado con el eje z.</span><span class="sxs-lookup"><span data-stu-id="e0182-139">The created torus is centered at the origin, and its axis is aligned with the z-axis.</span></span> <span data-ttu-id="e0182-140">El radio interior del aro es el radio de la sección transversal (el radio menor) y el radio exterior del aro es el radio del orificio central.</span><span class="sxs-lookup"><span data-stu-id="e0182-140">The inner radius of the torus is the radius of the cross-section (the minor radius), and the outer radius of the torus is the radius of the central hole.</span></span>

<span data-ttu-id="e0182-141">Esta función devuelve una malla que la aplicación puede usar posteriormente para dibujar o manipular.</span><span class="sxs-lookup"><span data-stu-id="e0182-141">This function returns a mesh that can be used later for drawing or manipulation by the application.</span></span>

<span data-ttu-id="e0182-142">Esta función crea una malla con la \_ opción de creación administrada D3DXMESH y el formato de vértice flexible [normal de D3DFVF \_ XYZ \| D3DFVF \_ ](d3dfvf.md) (FVF).</span><span class="sxs-lookup"><span data-stu-id="e0182-142">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0182-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0182-143">Requirements</span></span>



| <span data-ttu-id="e0182-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0182-144">Requirement</span></span> | <span data-ttu-id="e0182-145">Value</span><span class="sxs-lookup"><span data-stu-id="e0182-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0182-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0182-146">Header</span></span><br/>  | <dl> <span data-ttu-id="e0182-147"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0182-147"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="e0182-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0182-148">Library</span></span><br/> | <dl> <span data-ttu-id="e0182-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0182-149"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e0182-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0182-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0182-151">Funciones de dibujo de forma</span><span class="sxs-lookup"><span data-stu-id="e0182-151">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
