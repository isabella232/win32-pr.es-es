---
description: Crea una superficie de representación.
ms.assetid: 35e0007e-c405-46e1-a52b-625adc84732b
title: Función D3DXCreateRenderToSurface (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateRenderToSurface
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6fc64cbc65d30838db2105e0458d3553247f1ab1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718217"
---
# <a name="d3dxcreaterendertosurface-function"></a><span data-ttu-id="0756d-103">D3DXCreateRenderToSurface función)</span><span class="sxs-lookup"><span data-stu-id="0756d-103">D3DXCreateRenderToSurface function</span></span>

<span data-ttu-id="0756d-104">Crea una superficie de representación.</span><span class="sxs-lookup"><span data-stu-id="0756d-104">Creates a render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0756d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0756d-105">Syntax</span></span>


```C++
HRESULT D3DXCreateRenderToSurface(
  _In_  LPDIRECT3DDEVICE9     pDevice,
  _In_  UINT                  Width,
  _In_  UINT                  Height,
  _In_  D3DFORMAT             Format,
  _In_  BOOL                  DepthStencil,
  _In_  D3DFORMAT             DepthStencilFormat,
  _Out_ LPD3DXRENDERTOSURFACE *ppRenderToSurface
);
```



## <a name="parameters"></a><span data-ttu-id="0756d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0756d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0756d-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0756d-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0756d-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0756d-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0756d-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , el dispositivo que se va a asociar a la superficie de representación.</span><span class="sxs-lookup"><span data-stu-id="0756d-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="0756d-110">*Ancho* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0756d-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0756d-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0756d-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0756d-112">Ancho de la superficie de representación, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="0756d-112">Width of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="0756d-113">*Alto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0756d-113">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0756d-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0756d-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0756d-115">Alto de la superficie de representación, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="0756d-115">Height of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="0756d-116">*Formato* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0756d-116">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0756d-117">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="0756d-117">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="0756d-118">Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de píxel de la superficie de representación.</span><span class="sxs-lookup"><span data-stu-id="0756d-118">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the pixel format of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="0756d-119">*DepthStencil* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0756d-119">*DepthStencil* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0756d-120">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0756d-120">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0756d-121">Si **es true**, la superficie de representación admite una superficie de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="0756d-121">If **TRUE**, the render surface supports a depth-stencil surface.</span></span> <span data-ttu-id="0756d-122">De lo contrario, este miembro se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="0756d-122">Otherwise, this member is set to **FALSE**.</span></span> <span data-ttu-id="0756d-123">Esta función creará un nuevo búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="0756d-123">This function will create a new depth buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0756d-124">*DepthStencilFormat* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0756d-124">*DepthStencilFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0756d-125">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="0756d-125">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="0756d-126">Si *DepthStencil* se establece en **true**, este parámetro es un miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de la galería de símbolos de profundidad de la superficie de representación.</span><span class="sxs-lookup"><span data-stu-id="0756d-126">If *DepthStencil* is set to **TRUE**, this parameter is a member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the depth-stencil format of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="0756d-127">*ppRenderToSurface* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0756d-127">*ppRenderToSurface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0756d-128">Tipo: **[ **LPD3DXRENDERTOSURFACE**](id3dxrendertosurface.md)\***</span><span class="sxs-lookup"><span data-stu-id="0756d-128">Type: **[**LPD3DXRENDERTOSURFACE**](id3dxrendertosurface.md)\***</span></span>

<span data-ttu-id="0756d-129">Dirección de un puntero a una interfaz [**ID3DXRenderToSurface**](id3dxrendertosurface.md) que representa la superficie de representación creada.</span><span class="sxs-lookup"><span data-stu-id="0756d-129">Address of a pointer to an [**ID3DXRenderToSurface**](id3dxrendertosurface.md) interface, representing the created render surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0756d-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0756d-130">Return value</span></span>

<span data-ttu-id="0756d-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0756d-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0756d-132">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0756d-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0756d-133">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0756d-133">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="0756d-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0756d-134">Requirements</span></span>



| <span data-ttu-id="0756d-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="0756d-135">Requirement</span></span> | <span data-ttu-id="0756d-136">Value</span><span class="sxs-lookup"><span data-stu-id="0756d-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0756d-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0756d-137">Header</span></span><br/>  | <dl> <span data-ttu-id="0756d-138"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="0756d-138"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="0756d-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0756d-139">Library</span></span><br/> | <dl> <span data-ttu-id="0756d-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0756d-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0756d-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="0756d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0756d-142">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="0756d-142">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
