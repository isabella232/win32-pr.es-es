---
description: Establece los parámetros de desplazamiento de la geometría de malla.
ms.assetid: 4c78e5b3-fb63-4341-a811-5531cf9564e7
title: 'ID3DXPatchMesh:: SetDisplaceParam (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.SetDisplaceParam
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d1d59791859e0330415512db1551709729455d0d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670246"
---
# <a name="id3dxpatchmeshsetdisplaceparam-method"></a><span data-ttu-id="dd0d2-103">ID3DXPatchMesh:: SetDisplaceParam (método)</span><span class="sxs-lookup"><span data-stu-id="dd0d2-103">ID3DXPatchMesh::SetDisplaceParam method</span></span>

<span data-ttu-id="dd0d2-104">Establece los parámetros de desplazamiento de la geometría de malla.</span><span class="sxs-lookup"><span data-stu-id="dd0d2-104">Sets mesh geometry displacement parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd0d2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd0d2-105">Syntax</span></span>


```C++
HRESULT SetDisplaceParam(
  [in] LPDIRECT3DBASETEXTURE9 Texture,
  [in] D3DTEXTUREFILTERTYPE   MinFilter,
  [in] D3DTEXTUREFILTERTYPE   MagFilter,
  [in] D3DTEXTUREFILTERTYPE   MipFilter,
  [in] D3DTEXTUREADDRESS      Wrap,
  [in] DWORD                  dwLODBias
);
```



## <a name="parameters"></a><span data-ttu-id="dd0d2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd0d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd0d2-107">*Textura* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dd0d2-107">*Texture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd0d2-108">Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="dd0d2-108">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="dd0d2-109">Textura que contiene los datos de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="dd0d2-109">Texture containing the displacement data.</span></span>

</dd> <dt>

<span data-ttu-id="dd0d2-110">*MinFilter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dd0d2-110">*MinFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd0d2-111">Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**</span><span class="sxs-lookup"><span data-stu-id="dd0d2-111">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**</span></span>

<span data-ttu-id="dd0d2-112">Nivel de minificación.</span><span class="sxs-lookup"><span data-stu-id="dd0d2-112">Minification level.</span></span> <span data-ttu-id="dd0d2-113">Para obtener más información, vea [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="dd0d2-113">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd0d2-114">*MagFilter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dd0d2-114">*MagFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd0d2-115">Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**</span><span class="sxs-lookup"><span data-stu-id="dd0d2-115">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**</span></span>

<span data-ttu-id="dd0d2-116">Nivel de ampliación.</span><span class="sxs-lookup"><span data-stu-id="dd0d2-116">Magnification level.</span></span> <span data-ttu-id="dd0d2-117">Para obtener más información, vea [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="dd0d2-117">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd0d2-118">*MipFilter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dd0d2-118">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd0d2-119">Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**</span><span class="sxs-lookup"><span data-stu-id="dd0d2-119">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**</span></span>

<span data-ttu-id="dd0d2-120">Nivel de filtro MIP.</span><span class="sxs-lookup"><span data-stu-id="dd0d2-120">Mip filter level.</span></span> <span data-ttu-id="dd0d2-121">Para obtener más información, vea [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="dd0d2-121">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd0d2-122">*Ajustar* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dd0d2-122">*Wrap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd0d2-123">Tipo: **[ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)**</span><span class="sxs-lookup"><span data-stu-id="dd0d2-123">Type: **[**D3DTEXTUREADDRESS**](./d3dtextureaddress.md)**</span></span>

<span data-ttu-id="dd0d2-124">Modo de ajuste de dirección de textura.</span><span class="sxs-lookup"><span data-stu-id="dd0d2-124">Texture address wrap mode.</span></span> <span data-ttu-id="dd0d2-125">Para obtener más información, consulte [ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)</span><span class="sxs-lookup"><span data-stu-id="dd0d2-125">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md)</span></span>

</dd> <dt>

<span data-ttu-id="dd0d2-126">*dwLODBias* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dd0d2-126">*dwLODBias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd0d2-127">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dd0d2-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dd0d2-128">Nivel de valor de diferencia de detalle.</span><span class="sxs-lookup"><span data-stu-id="dd0d2-128">Level of detail bias value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd0d2-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd0d2-129">Return value</span></span>

<span data-ttu-id="dd0d2-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dd0d2-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dd0d2-131">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dd0d2-131">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="dd0d2-132">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="dd0d2-132">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd0d2-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd0d2-133">Remarks</span></span>

<span data-ttu-id="dd0d2-134">Los mapas de desplazamiento solo pueden ser texturas 2D.</span><span class="sxs-lookup"><span data-stu-id="dd0d2-134">Displacement maps can only be 2D textures.</span></span> <span data-ttu-id="dd0d2-135">Mipmapping se omite para la teselación no adaptable.</span><span class="sxs-lookup"><span data-stu-id="dd0d2-135">Mipmapping is ignored for nonadaptive tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd0d2-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd0d2-136">Requirements</span></span>



| <span data-ttu-id="dd0d2-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd0d2-137">Requirement</span></span> | <span data-ttu-id="dd0d2-138">Value</span><span class="sxs-lookup"><span data-stu-id="dd0d2-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd0d2-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd0d2-139">Header</span></span><br/>  | <dl> <span data-ttu-id="dd0d2-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd0d2-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="dd0d2-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dd0d2-141">Library</span></span><br/> | <dl> <span data-ttu-id="dd0d2-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd0d2-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dd0d2-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd0d2-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd0d2-144">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="dd0d2-144">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
