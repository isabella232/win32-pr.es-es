---
description: Filtra los niveles de mipmap de una textura.
ms.assetid: bfeae9b0-9480-4a26-a225-4a34780546ce
title: Función D3DXFilterTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFilterTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e8a0d1c211b50379451c8b04830e9c97fe988137
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718211"
---
# <a name="d3dxfiltertexture-function"></a><span data-ttu-id="9695e-103">D3DXFilterTexture función)</span><span class="sxs-lookup"><span data-stu-id="9695e-103">D3DXFilterTexture function</span></span>

<span data-ttu-id="9695e-104">Filtra los niveles de mipmap de una textura.</span><span class="sxs-lookup"><span data-stu-id="9695e-104">Filters mipmap levels of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="9695e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9695e-105">Syntax</span></span>


```C++
HRESULT D3DXFilterTexture(
  _In_        LPDIRECT3DBASETEXTURE9 pBaseTexture,
  _Out_ const PALETTEENTRY           *pPalette,
  _In_        UINT                   SrcLevel,
  _In_        DWORD                  MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="9695e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9695e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9695e-107">*pBaseTexture* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9695e-107">*pBaseTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9695e-108">Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="9695e-108">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="9695e-109">Puntero a una interfaz [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) que representa el objeto de textura que se va a filtrar.</span><span class="sxs-lookup"><span data-stu-id="9695e-109">Pointer to an [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface that represents the texture object to filter.</span></span>

</dd> <dt>

<span data-ttu-id="9695e-110">*pPalette* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9695e-110">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9695e-111">Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="9695e-111">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="9695e-112">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que representa una paleta de 256 colores que se va a rellenar o **null** para los formatos nonpalettized.</span><span class="sxs-lookup"><span data-stu-id="9695e-112">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure that represents a 256-color palette to fill in, or **NULL** for nonpalettized formats.</span></span> <span data-ttu-id="9695e-113">Si no se especifica una paleta, se proporciona la paleta de Direct3D predeterminada (una paleta blanca opaca).</span><span class="sxs-lookup"><span data-stu-id="9695e-113">If a palette is not specified, the default Direct3D palette (an all opaque white palette) is provided.</span></span> <span data-ttu-id="9695e-114">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="9695e-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="9695e-115">*SrcLevel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9695e-115">*SrcLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9695e-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9695e-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9695e-117">Nivel cuya imagen se usa para generar los niveles posteriores.</span><span class="sxs-lookup"><span data-stu-id="9695e-117">Level whose image is used to generate the subsequent levels.</span></span> <span data-ttu-id="9695e-118">Especificar \_ el valor predeterminado de D3DX para este parámetro equivale a especificar 0.</span><span class="sxs-lookup"><span data-stu-id="9695e-118">Specifying D3DX\_DEFAULT for this parameter is equivalent to specifying 0.</span></span>

</dd> <dt>

<span data-ttu-id="9695e-119">*MipFilter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9695e-119">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9695e-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9695e-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9695e-121">Combinación de uno o más [ \_ filtros de D3DX](d3dx-filter.md) que controlan cómo se filtra el mipmap.</span><span class="sxs-lookup"><span data-stu-id="9695e-121">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the mipmap is filtered.</span></span> <span data-ttu-id="9695e-122">Especificar \_ el valor predeterminado de d3dx para este parámetro es el equivalente a especificar el cuadro de filtro de d3dx \_ \_ si el tamaño de la textura es una potencia de dos y la interpolación de filtros de d3dx del \_ cuadro de filtro de \_ \| d3dx \_ \_ en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9695e-122">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX if the texture size is a power of two, and D3DX\_FILTER\_BOX \| D3DX\_FILTER\_DITHER otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9695e-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9695e-123">Return value</span></span>

<span data-ttu-id="9695e-124">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9695e-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9695e-125">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9695e-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9695e-126">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="9695e-126">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="9695e-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9695e-127">Remarks</span></span>

<span data-ttu-id="9695e-128">Un filtro se aplica de forma recursiva a cada nivel de textura para generar el siguiente nivel de textura.</span><span class="sxs-lookup"><span data-stu-id="9695e-128">A filter is recursively applied to each texture level to generate the next texture level.</span></span>

<span data-ttu-id="9695e-129">La escritura en una superficie sin nivel cero de la textura no hará que se actualice el rectángulo sucio.</span><span class="sxs-lookup"><span data-stu-id="9695e-129">Writing to a non-level-zero surface of the texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="9695e-130">Si se llama a **D3DXFilterTexture** y no se ha modificado la superficie (esto no es probable en escenarios de uso normal), la aplicación debe llamar explícitamente a [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) en la textura.</span><span class="sxs-lookup"><span data-stu-id="9695e-130">If **D3DXFilterTexture** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the texture.</span></span>

<span data-ttu-id="9695e-131">Las texturas creadas en el grupo predeterminado ( \_ valor predeterminado de D3DPOOL) no se pueden usar con **D3DXFilterTexture** (a menos que se cree con D3DUSAGE \_ Dynamic) porque se necesita una operación de bloqueo en el objeto.</span><span class="sxs-lookup"><span data-stu-id="9695e-131">Textures created in the default pool (D3DPOOL\_DEFAULT) cannot be used with **D3DXFilterTexture** (unless created with D3DUSAGE\_DYNAMIC) because a lock operation is needed on the object.</span></span> <span data-ttu-id="9695e-132">Tenga en cuenta que los bloqueos están prohibidos en las texturas en el grupo predeterminado (a menos que sean dinámicos).</span><span class="sxs-lookup"><span data-stu-id="9695e-132">Note that locks are prohibited on textures in the default pool (unless they are dynamic).</span></span>

<span data-ttu-id="9695e-133">Para obtener más información sobre [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), vea el SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="9695e-133">For details on [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), see the Platform SDK.</span></span> <span data-ttu-id="9695e-134">Tenga en cuenta que, a partir de DirectX 8,0, el miembro peFlags de la estructura **PALETTEENTRY** no funciona como se documenta en el SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="9695e-134">Note that as of DirectX 8.0, the peFlags member of the **PALETTEENTRY** structure does not function as documented in the Platform SDK.</span></span> <span data-ttu-id="9695e-135">El miembro peFlags es ahora el canal alfa para formatos de paleta de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="9695e-135">The peFlags member is now the alpha channel for 8-bit palettized formats.</span></span>

<span data-ttu-id="9695e-136">Solo hay una función de filtrado de texturas, pero dos macros que llaman a este método.</span><span class="sxs-lookup"><span data-stu-id="9695e-136">There is only one texture filtering function, but two macros that call this method.</span></span>


```
#define D3DXFilterCubeTexture D3DXFilterTexture
#define D3DXFilterVolumeTexture D3DXFilterTexture
```



## <a name="requirements"></a><span data-ttu-id="9695e-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9695e-137">Requirements</span></span>



| <span data-ttu-id="9695e-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="9695e-138">Requirement</span></span> | <span data-ttu-id="9695e-139">Value</span><span class="sxs-lookup"><span data-stu-id="9695e-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9695e-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9695e-140">Header</span></span><br/>  | <dl> <span data-ttu-id="9695e-141"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="9695e-141"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="9695e-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9695e-142">Library</span></span><br/> | <dl> <span data-ttu-id="9695e-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9695e-143"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="9695e-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="9695e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9695e-145">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="9695e-145">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
