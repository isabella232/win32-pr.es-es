---
description: La interfaz ID3DXPRTBuffer se usa como un búfer de datos para almacenar datos de vértices y píxeles para su uso con los métodos y funciones de transferencia Radiance precalculada (PRT).
ms.assetid: 36c1fd13-0949-4991-93cb-41ace458802d
title: Interfaz ID3DXPRTBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: daadb5b0ad8155062e75ea4eca566a0afbf3631b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708115"
---
# <a name="id3dxprtbuffer-interface"></a><span data-ttu-id="56c51-103">Interfaz ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="56c51-103">ID3DXPRTBuffer interface</span></span>

<span data-ttu-id="56c51-104">La interfaz ID3DXPRTBuffer se usa como un búfer de datos para almacenar datos de vértices y píxeles para su uso con los métodos y funciones de transferencia Radiance precalculada (PRT).</span><span class="sxs-lookup"><span data-stu-id="56c51-104">The ID3DXPRTBuffer interface is used as a data buffer to store vertex and pixel data for use with precomputed radiance transfer (PRT) methods and functions.</span></span>

## <a name="members"></a><span data-ttu-id="56c51-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="56c51-105">Members</span></span>

<span data-ttu-id="56c51-106">La interfaz **ID3DXPRTBuffer** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="56c51-106">The **ID3DXPRTBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="56c51-107">**ID3DXPRTBuffer** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="56c51-107">**ID3DXPRTBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="56c51-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="56c51-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="56c51-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="56c51-109">Methods</span></span>

<span data-ttu-id="56c51-110">La interfaz **ID3DXPRTBuffer** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="56c51-110">The **ID3DXPRTBuffer** interface has these methods.</span></span>



| <span data-ttu-id="56c51-111">Método</span><span class="sxs-lookup"><span data-stu-id="56c51-111">Method</span></span>                                                   | <span data-ttu-id="56c51-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="56c51-112">Description</span></span>                                                                                                                                                                                   |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="56c51-113">**AddBuffer**</span><span class="sxs-lookup"><span data-stu-id="56c51-113">**AddBuffer**</span></span>](id3dxprtbuffer--addbuffer.md)           | <span data-ttu-id="56c51-114">Agrega otro búfer a **ID3DXPRTBuffer** y almacena los resultados en **ID3DXPRTBuffer**.</span><span class="sxs-lookup"><span data-stu-id="56c51-114">Adds another buffer to the **ID3DXPRTBuffer** and stores the results in **ID3DXPRTBuffer**.</span></span><br/>                                                                                        |
| [<span data-ttu-id="56c51-115">**AttachGH**</span><span class="sxs-lookup"><span data-stu-id="56c51-115">**AttachGH**</span></span>](id3dxprtbuffer--attachgh.md)             | <span data-ttu-id="56c51-116">Asocia un objeto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) al objeto **ID3DXPRTBuffer** .</span><span class="sxs-lookup"><span data-stu-id="56c51-116">Associates an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the **ID3DXPRTBuffer** object.</span></span><br/>                                                              |
| [<span data-ttu-id="56c51-117">**EvalGH**</span><span class="sxs-lookup"><span data-stu-id="56c51-117">**EvalGH**</span></span>](id3dxprtbuffer--evalgh.md)                 | <span data-ttu-id="56c51-118">Aplica los datos de medianil de textura almacenados a un búfer de textura de **ID3DXPRTBuffer** .</span><span class="sxs-lookup"><span data-stu-id="56c51-118">Applies stored texture gutter data to an **ID3DXPRTBuffer** texture buffer.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="56c51-119">**ExtractTexture**</span><span class="sxs-lookup"><span data-stu-id="56c51-119">**ExtractTexture**</span></span>](id3dxprtbuffer--extracttexture.md) | <span data-ttu-id="56c51-120">Extrae los datos coeficientes de un canal de color del búfer para un intervalo de coeficientes especificado y agrega los datos a un objeto [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="56c51-120">Extracts coefficient data from a color channel of the buffer for a specified range of coefficients, and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span><br/> |
| [<span data-ttu-id="56c51-121">**ExtractToMesh**</span><span class="sxs-lookup"><span data-stu-id="56c51-121">**ExtractToMesh**</span></span>](id3dxprtbuffer--extracttomesh.md)   | <span data-ttu-id="56c51-122">Extrae los datos coeficientes de un búfer de un solo canal y agrega los datos a un objeto [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="56c51-122">Extracts coefficient data from a single-channel buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span><br/>                                                              |
| [<span data-ttu-id="56c51-123">**GetHeight**</span><span class="sxs-lookup"><span data-stu-id="56c51-123">**GetHeight**</span></span>](id3dxprtbuffer--getheight.md)           | <span data-ttu-id="56c51-124">Recupera el alto de la textura, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="56c51-124">Retrieves the height of the texture, in pixels.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="56c51-125">**GetNumChannels**</span><span class="sxs-lookup"><span data-stu-id="56c51-125">**GetNumChannels**</span></span>](id3dxprtbuffer--getnumchannels.md) | <span data-ttu-id="56c51-126">Recupera el número de canales de color utilizados en la memoria para almacenar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="56c51-126">Retrieves the number of color channels used in memory to store samples.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="56c51-127">**GetNumCoeffs**</span><span class="sxs-lookup"><span data-stu-id="56c51-127">**GetNumCoeffs**</span></span>](id3dxprtbuffer--getnumcoeffs.md)     | <span data-ttu-id="56c51-128">Recupera el número de escalares por canal de color usado en la memoria para almacenar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="56c51-128">Retrieves the number of scalars per color channel used in memory to store samples.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="56c51-129">**GetNumSamples**</span><span class="sxs-lookup"><span data-stu-id="56c51-129">**GetNumSamples**</span></span>](id3dxprtbuffer--getnumsamples.md)   | <span data-ttu-id="56c51-130">Recupera el número de vértices (o textura) muestreados.</span><span class="sxs-lookup"><span data-stu-id="56c51-130">Retrieves the number of vertices (or texels) sampled.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="56c51-131">**GetWidth**</span><span class="sxs-lookup"><span data-stu-id="56c51-131">**GetWidth**</span></span>](id3dxprtbuffer--getwidth.md)             | <span data-ttu-id="56c51-132">Recupera el ancho de la textura, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="56c51-132">Retrieves the width of the texture, in pixels.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="56c51-133">**IsTexture**</span><span class="sxs-lookup"><span data-stu-id="56c51-133">**IsTexture**</span></span>](id3dxprtbuffer--istexture.md)           | <span data-ttu-id="56c51-134">Indica si el búfer contiene una textura.</span><span class="sxs-lookup"><span data-stu-id="56c51-134">Indicates whether the buffer contains a texture.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="56c51-135">**LockBuffer**</span><span class="sxs-lookup"><span data-stu-id="56c51-135">**LockBuffer**</span></span>](id3dxprtbuffer--lockbuffer.md)         | <span data-ttu-id="56c51-136">Bloquea un intervalo de datos de ejemplo de vértice o textura y obtiene un puntero a la ubicación en la memoria de búfer.</span><span class="sxs-lookup"><span data-stu-id="56c51-136">Locks a range of vertex or texel sample data and obtains a pointer to the location in buffer memory.</span></span><br/>                                                                               |
| [<span data-ttu-id="56c51-137">**ReleaseGH**</span><span class="sxs-lookup"><span data-stu-id="56c51-137">**ReleaseGH**</span></span>](id3dxprtbuffer--releasegh.md)           | <span data-ttu-id="56c51-138">Desasocia un objeto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) asociado con el objeto **ID3DXPRTBuffer** .</span><span class="sxs-lookup"><span data-stu-id="56c51-138">Unassociates an attached [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the **ID3DXPRTBuffer** object.</span></span><br/>                                                   |
| [<span data-ttu-id="56c51-139">**Cambiar de tamaño**</span><span class="sxs-lookup"><span data-stu-id="56c51-139">**Resize**</span></span>](id3dxprtbuffer--resize.md)                 | <span data-ttu-id="56c51-140">Cambia el número de ejemplos contenidos en el búfer.</span><span class="sxs-lookup"><span data-stu-id="56c51-140">Changes the number of samples contained in the buffer.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="56c51-141">**ScaleBuffer**</span><span class="sxs-lookup"><span data-stu-id="56c51-141">**ScaleBuffer**</span></span>](id3dxprtbuffer--scalebuffer.md)       | <span data-ttu-id="56c51-142">Multiplica cada valor del búfer por un valor constante.</span><span class="sxs-lookup"><span data-stu-id="56c51-142">Multiplies every value in the buffer by a constant value.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="56c51-143">**UnlockBuffer**</span><span class="sxs-lookup"><span data-stu-id="56c51-143">**UnlockBuffer**</span></span>](id3dxprtbuffer--unlockbuffer.md)     | <span data-ttu-id="56c51-144">Finaliza la duración del puntero ppData devuelto por [**ID3DXPRTBuffer:: LockBuffer**](id3dxprtbuffer--lockbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="56c51-144">Ends the lifespan of the ppData pointer returned by [**ID3DXPRTBuffer::LockBuffer**](id3dxprtbuffer--lockbuffer.md).</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="56c51-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56c51-145">Remarks</span></span>

<span data-ttu-id="56c51-146">La interfaz **ID3DXPRTBuffer** se obtiene llamando a las funciones [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) o [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) .</span><span class="sxs-lookup"><span data-stu-id="56c51-146">The **ID3DXPRTBuffer** interface is obtained by calling the [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) or [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) functions.</span></span>

<span data-ttu-id="56c51-147">El tipo LPD3DXPRTBUFFER se define como un puntero a la interfaz **ID3DXPRTBuffer** .</span><span class="sxs-lookup"><span data-stu-id="56c51-147">The LPD3DXPRTBUFFER type is defined as a pointer to the **ID3DXPRTBuffer** interface.</span></span>


```
typedef interface ID3DXPRTBuffer ID3DXPRTBuffer;
typedef interface ID3DXPRTBuffer *LPD3DXPRTBUFFER;
```



## <a name="requirements"></a><span data-ttu-id="56c51-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56c51-148">Requirements</span></span>



| <span data-ttu-id="56c51-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="56c51-149">Requirement</span></span> | <span data-ttu-id="56c51-150">Value</span><span class="sxs-lookup"><span data-stu-id="56c51-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56c51-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56c51-151">Header</span></span><br/>  | <dl> <span data-ttu-id="56c51-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="56c51-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="56c51-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="56c51-153">Library</span></span><br/> | <dl> <span data-ttu-id="56c51-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56c51-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="56c51-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="56c51-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56c51-156">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="56c51-156">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="56c51-157">**D3DXCreatePRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="56c51-157">**D3DXCreatePRTBuffer**</span></span>](d3dxcreateprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="56c51-158">**D3DXCreatePRTBufferTex**</span><span class="sxs-lookup"><span data-stu-id="56c51-158">**D3DXCreatePRTBufferTex**</span></span>](d3dxcreateprtbuffertex.md)
</dt> <dt>

[<span data-ttu-id="56c51-159">**ID3DXPRTCompBuffer**</span><span class="sxs-lookup"><span data-stu-id="56c51-159">**ID3DXPRTCompBuffer**</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
