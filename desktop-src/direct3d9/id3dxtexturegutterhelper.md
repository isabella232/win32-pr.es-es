---
description: La interfaz ID3DXTextureGutterHelper se usa para crear y administrar regiones de medianil en una textura. Las regiones de medianil separan las texturas y permiten la interpolación bilineal para evitar la representación de artefactos en los límites de textura.
ms.assetid: 097e27bf-a1a6-4e7e-bdad-33015b50f91f
title: Interfaz ID3DXTextureGutterHelper (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ece03e14da490bd6d6f5aef69f9457939bc8bab7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362722"
---
# <a name="id3dxtexturegutterhelper-interface"></a><span data-ttu-id="dc976-104">Interfaz ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="dc976-104">ID3DXTextureGutterHelper interface</span></span>

<span data-ttu-id="dc976-105">La interfaz ID3DXTextureGutterHelper se usa para crear y administrar regiones de medianil en una textura.</span><span class="sxs-lookup"><span data-stu-id="dc976-105">The ID3DXTextureGutterHelper interface is used to build and manage gutter regions in a texture.</span></span> <span data-ttu-id="dc976-106">Las regiones de medianil separan las texturas y permiten la interpolación bilineal para evitar la representación de artefactos en los límites de textura.</span><span class="sxs-lookup"><span data-stu-id="dc976-106">Gutter regions separate textures and allow for bilinear interpolation to avoid rendering artifacts at texture boundaries.</span></span>

<span data-ttu-id="dc976-107">La... los métodos proporcionan acceso a las estructuras de datos que usa el método Apply... modalidades.</span><span class="sxs-lookup"><span data-stu-id="dc976-107">The Get... methods provide access to the data structures used by the Apply... methods.</span></span>

## <a name="members"></a><span data-ttu-id="dc976-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="dc976-108">Members</span></span>

<span data-ttu-id="dc976-109">La interfaz **ID3DXTextureGutterHelper** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dc976-109">The **ID3DXTextureGutterHelper** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dc976-110">**ID3DXTextureGutterHelper** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dc976-110">**ID3DXTextureGutterHelper** also has these types of members:</span></span>

-   [<span data-ttu-id="dc976-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="dc976-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dc976-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="dc976-112">Methods</span></span>

<span data-ttu-id="dc976-113">La interfaz **ID3DXTextureGutterHelper** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="dc976-113">The **ID3DXTextureGutterHelper** interface has these methods.</span></span>



| <span data-ttu-id="dc976-114">Método</span><span class="sxs-lookup"><span data-stu-id="dc976-114">Method</span></span>                                                                   | <span data-ttu-id="dc976-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc976-115">Description</span></span>                                                                                            |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc976-116">**ApplyGuttersFloat**</span><span class="sxs-lookup"><span data-stu-id="dc976-116">**ApplyGuttersFloat**</span></span>](id3dxtexturegutterhelper--applyguttersfloat.md) | <span data-ttu-id="dc976-117">Aplica medianils a un búfer de textura flotante.</span><span class="sxs-lookup"><span data-stu-id="dc976-117">Applies gutters to a FLOAT texture buffer.</span></span><br/>                                                  |
| [<span data-ttu-id="dc976-118">**ApplyGuttersPRT**</span><span class="sxs-lookup"><span data-stu-id="dc976-118">**ApplyGuttersPRT**</span></span>](id3dxtexturegutterhelper--applyguttersprt.md)     | <span data-ttu-id="dc976-119">Aplica medianils a un objeto de búfer de [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="dc976-119">Applies gutters to an [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer object.</span></span><br/>               |
| [<span data-ttu-id="dc976-120">**ApplyGuttersTex**</span><span class="sxs-lookup"><span data-stu-id="dc976-120">**ApplyGuttersTex**</span></span>](id3dxtexturegutterhelper--applygutterstex.md)     | <span data-ttu-id="dc976-121">Aplica medianils a un objeto de textura [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="dc976-121">Applies gutters to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) texture object.</span></span><br/>        |
| [<span data-ttu-id="dc976-122">**GetBaryMap**</span><span class="sxs-lookup"><span data-stu-id="dc976-122">**GetBaryMap**</span></span>](id3dxtexturegutterhelper--getbarymap.md)               | <span data-ttu-id="dc976-123">Recupera las coordenadas de Barycentric de textura.</span><span class="sxs-lookup"><span data-stu-id="dc976-123">Retrieves texel barycentric coordinates.</span></span><br/>                                                    |
| [<span data-ttu-id="dc976-124">**GetFaceMap**</span><span class="sxs-lookup"><span data-stu-id="dc976-124">**GetFaceMap**</span></span>](id3dxtexturegutterhelper--getfacemap.md)               | <span data-ttu-id="dc976-125">Recupera el índice de la superficie de la malla a la que pertenece cada textura.</span><span class="sxs-lookup"><span data-stu-id="dc976-125">Retrieves the index of the mesh face to which each texel belongs.</span></span><br/>                           |
| [<span data-ttu-id="dc976-126">**GetGutterMap**</span><span class="sxs-lookup"><span data-stu-id="dc976-126">**GetGutterMap**</span></span>](id3dxtexturegutterhelper--getguttermap.md)           | <span data-ttu-id="dc976-127">Recibe un valor de la clase textura que indica la clase textura según la ubicación de cada textura.</span><span class="sxs-lookup"><span data-stu-id="dc976-127">Receives a texel class value that indicates texel class according to each texel's location.</span></span><br/> |
| [<span data-ttu-id="dc976-128">**GetHeight**</span><span class="sxs-lookup"><span data-stu-id="dc976-128">**GetHeight**</span></span>](id3dxtexturegutterhelper--getheight.md)                 | <span data-ttu-id="dc976-129">Recupera el alto de la textura, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="dc976-129">Retrieves the height of the texture, in pixels.</span></span><br/>                                             |
| [<span data-ttu-id="dc976-130">**GetTexelMap**</span><span class="sxs-lookup"><span data-stu-id="dc976-130">**GetTexelMap**</span></span>](id3dxtexturegutterhelper--gettexelmap.md)             | <span data-ttu-id="dc976-131">Recupera las coordenadas de textura (u, v) de cada textura.</span><span class="sxs-lookup"><span data-stu-id="dc976-131">Retrieves the (u, v) texture coordinates of each texel.</span></span><br/>                                     |
| [<span data-ttu-id="dc976-132">**GetWidth**</span><span class="sxs-lookup"><span data-stu-id="dc976-132">**GetWidth**</span></span>](id3dxtexturegutterhelper--getwidth.md)                   | <span data-ttu-id="dc976-133">Recupera el ancho de la textura, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="dc976-133">Retrieves the width of the texture, in pixels.</span></span><br/>                                              |
| [<span data-ttu-id="dc976-134">**ResampleTex**</span><span class="sxs-lookup"><span data-stu-id="dc976-134">**ResampleTex**</span></span>](id3dxtexturegutterhelper--resampletex.md)             | <span data-ttu-id="dc976-135">Remuestrea una textura en la parametrización de esta gutterhelper.</span><span class="sxs-lookup"><span data-stu-id="dc976-135">Resamples a texture into this gutterhelper's parameterization.</span></span><br/>                              |
| [<span data-ttu-id="dc976-136">**SetBaryMap**</span><span class="sxs-lookup"><span data-stu-id="dc976-136">**SetBaryMap**</span></span>](id3dxtexturegutterhelper--setbarymap.md)               | <span data-ttu-id="dc976-137">Establece las coordenadas de Barycentric de textura.</span><span class="sxs-lookup"><span data-stu-id="dc976-137">Sets texel barycentric coordinates.</span></span><br/>                                                         |
| [<span data-ttu-id="dc976-138">**SetFaceMap**</span><span class="sxs-lookup"><span data-stu-id="dc976-138">**SetFaceMap**</span></span>](id3dxtexturegutterhelper--setfacemap.md)               | <span data-ttu-id="dc976-139">Establece el índice de la superficie de la malla a la que pertenece cada textura.</span><span class="sxs-lookup"><span data-stu-id="dc976-139">Sets the index of the mesh face to which each texel belongs.</span></span><br/>                                |
| [<span data-ttu-id="dc976-140">**SetGutterMap**</span><span class="sxs-lookup"><span data-stu-id="dc976-140">**SetGutterMap**</span></span>](id3dxtexturegutterhelper--setguttermap.md)           | <span data-ttu-id="dc976-141">Establece un valor de la clase textura que indica la clase textura según la ubicación de cada textura.</span><span class="sxs-lookup"><span data-stu-id="dc976-141">Sets a texel class value that indicates texel class according to each texel's location.</span></span><br/>     |
| [<span data-ttu-id="dc976-142">**SetTexelMap**</span><span class="sxs-lookup"><span data-stu-id="dc976-142">**SetTexelMap**</span></span>](id3dxtexturegutterhelper--settexelmap.md)             | <span data-ttu-id="dc976-143">Establece las coordenadas de textura (u, v) de cada textura.</span><span class="sxs-lookup"><span data-stu-id="dc976-143">Sets the (u, v) texture coordinates of each texel.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="dc976-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc976-144">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="dc976-145">Cuando se usa con radiance Transfer (PRT) precalculado, esta interfaz requiere una parametrización única del modelo.</span><span class="sxs-lookup"><span data-stu-id="dc976-145">When used with precomputed radiance transfer (PRT), this interface requires a unique parameterization of the model.</span></span> <span data-ttu-id="dc976-146">Cada textura debe corresponder a un solo punto en la superficie del modelo y viceversa.</span><span class="sxs-lookup"><span data-stu-id="dc976-146">Every texel must correspond to a single point on the surface of the model and vice-versa.</span></span> <span data-ttu-id="dc976-147">Si el modelo incluye varias texturas, debe dividirse en partes independientes, cada una de las cuales contenga un objeto auxiliar de medianil por textura.</span><span class="sxs-lookup"><span data-stu-id="dc976-147">If the model includes multiple textures, it must be split into separate pieces that each contain one gutter helper object per texture.</span></span>

 

<span data-ttu-id="dc976-148">Esta interfaz se puede usar para generar un mapa en el espacio de textura en el que cada textura se encuentra en una de las cuatro clases.</span><span class="sxs-lookup"><span data-stu-id="dc976-148">This interface can be used to generate a map in texture space in which each texel is in one of four classes.</span></span>



| <span data-ttu-id="dc976-149">Clase textura</span><span class="sxs-lookup"><span data-stu-id="dc976-149">Texel Class</span></span> | <span data-ttu-id="dc976-150">Ubicación de textura</span><span class="sxs-lookup"><span data-stu-id="dc976-150">Texel Location</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc976-151">0</span><span class="sxs-lookup"><span data-stu-id="dc976-151">0</span></span>           | <span data-ttu-id="dc976-152">Punto no válido; no se usará textura.</span><span class="sxs-lookup"><span data-stu-id="dc976-152">Invalid point; texel will not be used.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="dc976-153">1</span><span class="sxs-lookup"><span data-stu-id="dc976-153">1</span></span>           | <span data-ttu-id="dc976-154">Triángulo interior.</span><span class="sxs-lookup"><span data-stu-id="dc976-154">Inside triangle.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="dc976-155">2</span><span class="sxs-lookup"><span data-stu-id="dc976-155">2</span></span>           | <span data-ttu-id="dc976-156">Encuadernación interior.</span><span class="sxs-lookup"><span data-stu-id="dc976-156">Inside gutter.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="dc976-157">4</span><span class="sxs-lookup"><span data-stu-id="dc976-157">4</span></span>           | <span data-ttu-id="dc976-158">Encuadernación interior; textura se evaluará como un ejemplo completo en los métodos [**ID3DXTextureGutterHelper:: ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper:: ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)o [**ID3DXTextureGutterHelper:: ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) .</span><span class="sxs-lookup"><span data-stu-id="dc976-158">Inside gutter; texel will be evaluated as a full sample in the [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md), or [**ID3DXTextureGutterHelper::ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) methods.</span></span> |



 

<span data-ttu-id="dc976-159">En el caso de las clases 1 y 2, un textura se almacena con la superficie a la que pertenece, junto con las coordenadas Barycentric de los dos primeros vértices de esa superficie.</span><span class="sxs-lookup"><span data-stu-id="dc976-159">For classes 1 and 2, a texel is stored with the face it belongs to, along with barycentric coordinates of the first two vertices of that face.</span></span> <span data-ttu-id="dc976-160">Los vértices de medianil se asignan al borde más cercano en el espacio de textura.</span><span class="sxs-lookup"><span data-stu-id="dc976-160">Gutter vertices are assigned to the closest edge in texture space.</span></span>

<span data-ttu-id="dc976-161">No hay ninguna clase textura 3.</span><span class="sxs-lookup"><span data-stu-id="dc976-161">There is no texel class 3.</span></span>

<span data-ttu-id="dc976-162">La interfaz **ID3DXTextureGutterHelper** se obtiene mediante una llamada a la función [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) .</span><span class="sxs-lookup"><span data-stu-id="dc976-162">The **ID3DXTextureGutterHelper** interface is obtained by calling the [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) function.</span></span>

<span data-ttu-id="dc976-163">El tipo LPD3DXTEXTUREGUTTERHELPER se define como un puntero a la interfaz **ID3DXTextureGutterHelper** .</span><span class="sxs-lookup"><span data-stu-id="dc976-163">The LPD3DXTEXTUREGUTTERHELPER type is defined as a pointer to the **ID3DXTextureGutterHelper** interface.</span></span>


```
typedef interface ID3DXTextureGutterHelper ID3DXTextureGutterHelper;
typedef interface ID3DXTextureGutterHelper *LPD3DXTEXTUREGUTTERHELPER;
```



## <a name="requirements"></a><span data-ttu-id="dc976-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc976-164">Requirements</span></span>



| <span data-ttu-id="dc976-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc976-165">Requirement</span></span> | <span data-ttu-id="dc976-166">Value</span><span class="sxs-lookup"><span data-stu-id="dc976-166">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc976-167">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dc976-167">Header</span></span><br/>  | <dl> <span data-ttu-id="dc976-168"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc976-168"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="dc976-169">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dc976-169">Library</span></span><br/> | <dl> <span data-ttu-id="dc976-170"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc976-170"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dc976-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc976-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc976-172">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="dc976-172">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
