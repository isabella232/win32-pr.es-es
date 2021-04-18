---
description: Obtiene los parámetros de desplazamiento de geometría de la malla.
ms.assetid: 155724ba-71be-4e9f-8c84-bb04f8eec578
title: 'ID3DXPatchMesh:: GetDisplaceParam (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDisplaceParam
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3ce6891af8a15aa8f4af5c85312f124db6c05321
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718556"
---
# <a name="id3dxpatchmeshgetdisplaceparam-method"></a><span data-ttu-id="99c84-103">ID3DXPatchMesh:: GetDisplaceParam (método)</span><span class="sxs-lookup"><span data-stu-id="99c84-103">ID3DXPatchMesh::GetDisplaceParam method</span></span>

<span data-ttu-id="99c84-104">Obtiene los parámetros de desplazamiento de geometría de la malla.</span><span class="sxs-lookup"><span data-stu-id="99c84-104">Gets mesh geometry displacement parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="99c84-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99c84-105">Syntax</span></span>


```C++
HRESULT GetDisplaceParam(
  [in] LPDIRECT3DBASETEXTURE9 *Texture,
  [in] D3DTEXTUREFILTERTYPE   *MinFilter,
  [in] D3DTEXTUREFILTERTYPE   *MagFilter,
  [in] D3DTEXTUREFILTERTYPE   *MipFilter,
  [in] D3DTEXTUREADDRESS      *Wrap,
  [in] DWORD                  *dwLODBias
);
```



## <a name="parameters"></a><span data-ttu-id="99c84-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="99c84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99c84-107">*Textura* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="99c84-107">*Texture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99c84-108">Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="99c84-108">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***</span></span>

<span data-ttu-id="99c84-109">Textura que contiene los datos de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="99c84-109">Texture containing the displacement data.</span></span>

</dd> <dt>

<span data-ttu-id="99c84-110">*MinFilter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="99c84-110">*MinFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99c84-111">Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span><span class="sxs-lookup"><span data-stu-id="99c84-111">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span></span>

<span data-ttu-id="99c84-112">Nivel de minificación.</span><span class="sxs-lookup"><span data-stu-id="99c84-112">Minification level.</span></span> <span data-ttu-id="99c84-113">Para obtener más información, vea [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="99c84-113">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="99c84-114">*MagFilter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="99c84-114">*MagFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99c84-115">Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span><span class="sxs-lookup"><span data-stu-id="99c84-115">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span></span>

<span data-ttu-id="99c84-116">Nivel de ampliación.</span><span class="sxs-lookup"><span data-stu-id="99c84-116">Magnification level.</span></span> <span data-ttu-id="99c84-117">Para obtener más información, vea [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="99c84-117">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="99c84-118">*MipFilter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="99c84-118">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99c84-119">Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span><span class="sxs-lookup"><span data-stu-id="99c84-119">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span></span>

<span data-ttu-id="99c84-120">Nivel de filtro MIP.</span><span class="sxs-lookup"><span data-stu-id="99c84-120">Mip filter level.</span></span> <span data-ttu-id="99c84-121">Para obtener más información, vea [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="99c84-121">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="99c84-122">*Ajustar* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="99c84-122">*Wrap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99c84-123">Tipo: **[ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)\***</span><span class="sxs-lookup"><span data-stu-id="99c84-123">Type: **[**D3DTEXTUREADDRESS**](./d3dtextureaddress.md)\***</span></span>

<span data-ttu-id="99c84-124">Modo de ajuste de dirección de textura.</span><span class="sxs-lookup"><span data-stu-id="99c84-124">Texture address wrap mode.</span></span> <span data-ttu-id="99c84-125">Para obtener más información, vea [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span><span class="sxs-lookup"><span data-stu-id="99c84-125">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="99c84-126">*dwLODBias* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="99c84-126">*dwLODBias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99c84-127">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="99c84-127">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="99c84-128">Nivel de valor de diferencia de detalle.</span><span class="sxs-lookup"><span data-stu-id="99c84-128">Level of detail bias value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99c84-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99c84-129">Return value</span></span>

<span data-ttu-id="99c84-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="99c84-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="99c84-131">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="99c84-131">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="99c84-132">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="99c84-132">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="99c84-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99c84-133">Remarks</span></span>

<span data-ttu-id="99c84-134">Los mapas de desplazamiento solo pueden ser texturas 2D.</span><span class="sxs-lookup"><span data-stu-id="99c84-134">Displacement maps can only be 2D textures.</span></span> <span data-ttu-id="99c84-135">Mipmapping se omite para la teselación no adaptable.</span><span class="sxs-lookup"><span data-stu-id="99c84-135">Mipmapping is ignored for nonadaptive tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="99c84-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99c84-136">Requirements</span></span>



| <span data-ttu-id="99c84-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="99c84-137">Requirement</span></span> | <span data-ttu-id="99c84-138">Value</span><span class="sxs-lookup"><span data-stu-id="99c84-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99c84-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="99c84-139">Header</span></span><br/>  | <dl> <span data-ttu-id="99c84-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="99c84-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="99c84-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="99c84-141">Library</span></span><br/> | <dl> <span data-ttu-id="99c84-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99c84-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="99c84-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="99c84-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99c84-144">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="99c84-144">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
