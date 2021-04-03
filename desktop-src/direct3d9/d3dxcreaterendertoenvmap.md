---
description: Crea un mapa de entorno de representación.
ms.assetid: 5ca10602-5ab1-4766-a350-706c46c55df2
title: Función D3DXCreateRenderToEnvMap (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateRenderToEnvMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6829d53f53bd6a4783f5873eeed614e48bbe1088
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083726"
---
# <a name="d3dxcreaterendertoenvmap-function"></a><span data-ttu-id="0c77d-103">D3DXCreateRenderToEnvMap función)</span><span class="sxs-lookup"><span data-stu-id="0c77d-103">D3DXCreateRenderToEnvMap function</span></span>

<span data-ttu-id="0c77d-104">Crea un mapa de entorno de representación.</span><span class="sxs-lookup"><span data-stu-id="0c77d-104">Creates a render environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c77d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c77d-105">Syntax</span></span>


```C++
HRESULT D3DXCreateRenderToEnvMap(
  _In_  LPDIRECT3DDEVICE9    pDevice,
  _In_  UINT                 Size,
  _In_  UINT                 MipLevels,
  _In_  D3DFORMAT            Format,
  _In_  BOOL                 DepthStencil,
  _In_  D3DFORMAT            DepthStencilFormat,
  _Out_ LPD3DXRENDERTOENVMAP *ppRenderToEnvMap
);
```



## <a name="parameters"></a><span data-ttu-id="0c77d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0c77d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c77d-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0c77d-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c77d-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0c77d-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0c77d-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , que es el dispositivo que se va a asociar a la superficie de representación.</span><span class="sxs-lookup"><span data-stu-id="0c77d-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, which is the device to associate with the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="0c77d-110">*Tamaño* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0c77d-110">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c77d-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0c77d-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0c77d-112">Tamaño de la superficie de representación.</span><span class="sxs-lookup"><span data-stu-id="0c77d-112">Size of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="0c77d-113">*MipLevels* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0c77d-113">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c77d-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0c77d-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0c77d-115">Número de niveles de mipmap.</span><span class="sxs-lookup"><span data-stu-id="0c77d-115">The number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="0c77d-116">*Formato* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0c77d-116">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c77d-117">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="0c77d-117">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="0c77d-118">Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) que describe el formato de píxel del mapa de entorno.</span><span class="sxs-lookup"><span data-stu-id="0c77d-118">Member of the [D3DFORMAT](d3dformat.md) enumerated type that describes the pixel format of the environment map.</span></span>

</dd> <dt>

<span data-ttu-id="0c77d-119">*DepthStencil* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0c77d-119">*DepthStencil* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c77d-120">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0c77d-120">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0c77d-121">Si **es true**, la superficie de representación admite una superficie de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="0c77d-121">If **TRUE**, the render surface supports a depth-stencil surface.</span></span> <span data-ttu-id="0c77d-122">De lo contrario, este miembro se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="0c77d-122">Otherwise, this member is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="0c77d-123">*DepthStencilFormat* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0c77d-123">*DepthStencilFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c77d-124">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="0c77d-124">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="0c77d-125">Si DepthStencil se establece en **true**, este parámetro es un miembro del tipo enumerado [D3DFORMAT](d3dformat.md) que describe el formato de la galería de símbolos de profundidad del mapa de entorno.</span><span class="sxs-lookup"><span data-stu-id="0c77d-125">If DepthStencil is set to **TRUE**, this parameter is a member of the [D3DFORMAT](d3dformat.md) enumerated type that describes the depth-stencil format of the environment map.</span></span>

</dd> <dt>

<span data-ttu-id="0c77d-126">*ppRenderToEnvMap* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0c77d-126">*ppRenderToEnvMap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c77d-127">Tipo: **[ **LPD3DXRENDERTOENVMAP**](id3dxrendertoenvmap.md)\***</span><span class="sxs-lookup"><span data-stu-id="0c77d-127">Type: **[**LPD3DXRENDERTOENVMAP**](id3dxrendertoenvmap.md)\***</span></span>

<span data-ttu-id="0c77d-128">Dirección de un puntero a una interfaz [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) que representa la asignación de entorno de representación creada.</span><span class="sxs-lookup"><span data-stu-id="0c77d-128">Address of a pointer to an [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) interface that represents the created render environment map.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c77d-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0c77d-129">Return value</span></span>

<span data-ttu-id="0c77d-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0c77d-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0c77d-131">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0c77d-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0c77d-132">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0c77d-132">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c77d-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c77d-133">Requirements</span></span>



| <span data-ttu-id="0c77d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c77d-134">Requirement</span></span> | <span data-ttu-id="0c77d-135">Value</span><span class="sxs-lookup"><span data-stu-id="0c77d-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c77d-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0c77d-136">Header</span></span><br/>  | <dl> <span data-ttu-id="0c77d-137"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c77d-137"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="0c77d-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0c77d-138">Library</span></span><br/> | <dl> <span data-ttu-id="0c77d-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c77d-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0c77d-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c77d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c77d-141">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="0c77d-141">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
