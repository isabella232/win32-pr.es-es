---
description: La interfaz ID3DXPRTCompBuffer almacena una versión comprimida de un búfer de ID3DXPRTBuffer para su uso con el análisis de componentes principales (PCA).
ms.assetid: 97f8576c-24d5-4f60-923b-4d8d94382fe9
title: Interfaz ID3DXPRTCompBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 323ed6f2bbe9ce4caf495a00330c1b1e0e83e158
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708066"
---
# <a name="id3dxprtcompbuffer-interface"></a><span data-ttu-id="226a8-103">Interfaz ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="226a8-103">ID3DXPRTCompBuffer interface</span></span>

<span data-ttu-id="226a8-104">La interfaz **ID3DXPRTCompBuffer** almacena una versión comprimida de un búfer de [**ID3DXPRTBuffer**](id3dxprtbuffer.md) para su uso con el análisis de componentes principales (PCA).</span><span class="sxs-lookup"><span data-stu-id="226a8-104">The **ID3DXPRTCompBuffer** interface stores a compressed version of a [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer, for use with principal component analysis (PCA).</span></span>

## <a name="members"></a><span data-ttu-id="226a8-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="226a8-105">Members</span></span>

<span data-ttu-id="226a8-106">La interfaz **ID3DXPRTCompBuffer** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="226a8-106">The **ID3DXPRTCompBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="226a8-107">**ID3DXPRTCompBuffer** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="226a8-107">**ID3DXPRTCompBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="226a8-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="226a8-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="226a8-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="226a8-109">Methods</span></span>

<span data-ttu-id="226a8-110">La interfaz **ID3DXPRTCompBuffer** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="226a8-110">The **ID3DXPRTCompBuffer** interface has these methods.</span></span>



| <span data-ttu-id="226a8-111">Método</span><span class="sxs-lookup"><span data-stu-id="226a8-111">Method</span></span>                                                             | <span data-ttu-id="226a8-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="226a8-112">Description</span></span>                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="226a8-113">**ExtractBasis**</span><span class="sxs-lookup"><span data-stu-id="226a8-113">**ExtractBasis**</span></span>](id3dxprtcompbuffer--extractbasis.md)           | <span data-ttu-id="226a8-114">Extrae los vectores de referencia media y de análisis de componentes principales (PCA) para un clúster determinado a partir de un búfer de datos comprimidos **ID3DXPRTCompBuffer** .</span><span class="sxs-lookup"><span data-stu-id="226a8-114">Extracts the mean and principal component analysis (PCA) basis vectors for a given cluster from an **ID3DXPRTCompBuffer** compressed data buffer.</span></span><br/>                                                                       |
| [<span data-ttu-id="226a8-115">**ExtractClusterIDs**</span><span class="sxs-lookup"><span data-stu-id="226a8-115">**ExtractClusterIDs**</span></span>](id3dxprtcompbuffer--extractclusterids.md) | <span data-ttu-id="226a8-116">Extrae los identificadores de clúster por ejemplo de un búfer de datos comprimidos de **ID3DXPRTCompBuffer** .</span><span class="sxs-lookup"><span data-stu-id="226a8-116">Extracts the per-sample cluster IDs from an **ID3DXPRTCompBuffer** compressed data buffer.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="226a8-117">**ExtractPCA**</span><span class="sxs-lookup"><span data-stu-id="226a8-117">**ExtractPCA**</span></span>](id3dxprtcompbuffer--extractpca.md)               | <span data-ttu-id="226a8-118">Extrae los coeficientes de proyección de análisis de componentes principales por ejemplo (PCA) de un búfer de datos comprimidos **ID3DXPRTCompBuffer** .</span><span class="sxs-lookup"><span data-stu-id="226a8-118">Extracts the per-sample principal component analysis (PCA) projection coefficients from an **ID3DXPRTCompBuffer** compressed data buffer.</span></span><br/>                                                                               |
| [<span data-ttu-id="226a8-119">**ExtractTexture**</span><span class="sxs-lookup"><span data-stu-id="226a8-119">**ExtractTexture**</span></span>](id3dxprtcompbuffer--extracttexture.md)       | <span data-ttu-id="226a8-120">Extrae los coeficientes de proyección de análisis de componentes principales por ejemplo (PCA) de un búfer de datos comprimidos **ID3DXPRTCompBuffer** y agrega los datos a un objeto [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="226a8-120">Extracts the per-sample principal component analysis (PCA) projection coefficients from an **ID3DXPRTCompBuffer** compressed data buffer and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span><br/> |
| [<span data-ttu-id="226a8-121">**ExtractToMesh**</span><span class="sxs-lookup"><span data-stu-id="226a8-121">**ExtractToMesh**</span></span>](id3dxprtcompbuffer--extracttomesh.md)         | <span data-ttu-id="226a8-122">Extrae los coeficientes de proyección de análisis de componentes principales por ejemplo (PCA) de un búfer de datos comprimidos **ID3DXPRTCompBuffer** y agrega los datos a un objeto [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="226a8-122">Extracts the per-sample principal component analysis (PCA) projection coefficients from an **ID3DXPRTCompBuffer** compressed data buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span><br/>                 |
| [<span data-ttu-id="226a8-123">**GetHeight**</span><span class="sxs-lookup"><span data-stu-id="226a8-123">**GetHeight**</span></span>](id3dxprtcompbuffer--getheight.md)                 | <span data-ttu-id="226a8-124">Recupera el alto de la textura, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="226a8-124">Retrieves the height of the texture, in pixels.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="226a8-125">**GetNumChannels**</span><span class="sxs-lookup"><span data-stu-id="226a8-125">**GetNumChannels**</span></span>](id3dxprtcompbuffer--getnumchannels.md)       | <span data-ttu-id="226a8-126">Recupera el número de canales de color utilizados en la memoria para almacenar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="226a8-126">Retrieves the number of color channels used in memory to store samples.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="226a8-127">**GetNumClusters**</span><span class="sxs-lookup"><span data-stu-id="226a8-127">**GetNumClusters**</span></span>](id3dxprtcompbuffer--getnumclusters.md)       | <span data-ttu-id="226a8-128">Recupera el número de clústeres que se usarán para la compresión.</span><span class="sxs-lookup"><span data-stu-id="226a8-128">Retrieves the number of clusters to use for compression.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="226a8-129">**GetNumCoeffs**</span><span class="sxs-lookup"><span data-stu-id="226a8-129">**GetNumCoeffs**</span></span>](id3dxprtcompbuffer--getnumcoeffs.md)           | <span data-ttu-id="226a8-130">Recupera el número de escalares por canal de color usado en la memoria para almacenar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="226a8-130">Retrieves the number of scalars per color channel used in memory to store samples.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="226a8-131">**GetNumPCA**</span><span class="sxs-lookup"><span data-stu-id="226a8-131">**GetNumPCA**</span></span>](id3dxprtcompbuffer--getnumpca.md)                 | <span data-ttu-id="226a8-132">Recupera el número de vectores de base del análisis de componentes principales (PCA) que se van a usar en cada clúster.</span><span class="sxs-lookup"><span data-stu-id="226a8-132">Retrieves the number of principal component analysis (PCA) basis vectors to use in each cluster.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="226a8-133">**GetNumSamples**</span><span class="sxs-lookup"><span data-stu-id="226a8-133">**GetNumSamples**</span></span>](id3dxprtcompbuffer--getnumsamples.md)         | <span data-ttu-id="226a8-134">Recupera el número de vértices (o textura) muestreados.</span><span class="sxs-lookup"><span data-stu-id="226a8-134">Retrieves the number of vertices (or texels) sampled.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="226a8-135">**GetWidth**</span><span class="sxs-lookup"><span data-stu-id="226a8-135">**GetWidth**</span></span>](id3dxprtcompbuffer--getwidth.md)                   | <span data-ttu-id="226a8-136">Recupera el ancho de la textura, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="226a8-136">Retrieves the width of the texture, in pixels.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="226a8-137">**IsTexture**</span><span class="sxs-lookup"><span data-stu-id="226a8-137">**IsTexture**</span></span>](id3dxprtcompbuffer--istexture.md)                 | <span data-ttu-id="226a8-138">Indica si el búfer contiene una textura.</span><span class="sxs-lookup"><span data-stu-id="226a8-138">Indicates whether the buffer contains a texture.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="226a8-139">**NormalizeData**</span><span class="sxs-lookup"><span data-stu-id="226a8-139">**NormalizeData**</span></span>](id3dxprtcompbuffer--normalizedata.md)         | <span data-ttu-id="226a8-140">Normaliza todos los pesos del análisis de componentes principales (PCA) para que estén entre-1 y 1.</span><span class="sxs-lookup"><span data-stu-id="226a8-140">Normalizes all principal component analysis (PCA) weights so that they are between -1 and 1.</span></span> <span data-ttu-id="226a8-141">Los vectores de base se modifican para reflejar esta normalización.</span><span class="sxs-lookup"><span data-stu-id="226a8-141">Basis vectors are modified to reflect this normalization.</span></span><br/>                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="226a8-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="226a8-142">Remarks</span></span>

<span data-ttu-id="226a8-143">La interfaz **ID3DXPRTCompBuffer** se obtiene mediante una llamada a la función [**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="226a8-143">The **ID3DXPRTCompBuffer** interface is obtained by calling the [**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md) function.</span></span>

<span data-ttu-id="226a8-144">El tipo LPD3DXPRTCOMPBUFFER se define como un puntero a la interfaz **ID3DXPRTCompBuffer** .</span><span class="sxs-lookup"><span data-stu-id="226a8-144">The LPD3DXPRTCOMPBUFFER type is defined as a pointer to the **ID3DXPRTCompBuffer** interface.</span></span>


```
typedef interface ID3DXPRTCompBuffer ID3DXPRTCompBuffer;
typedef interface ID3DXPRTCompBuffer *LPD3DXPRTCOMPBUFFER;
```



## <a name="requirements"></a><span data-ttu-id="226a8-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="226a8-145">Requirements</span></span>



| <span data-ttu-id="226a8-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="226a8-146">Requirement</span></span> | <span data-ttu-id="226a8-147">Value</span><span class="sxs-lookup"><span data-stu-id="226a8-147">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="226a8-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="226a8-148">Header</span></span><br/>  | <dl> <span data-ttu-id="226a8-149"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="226a8-149"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="226a8-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="226a8-150">Library</span></span><br/> | <dl> <span data-ttu-id="226a8-151"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="226a8-151"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="226a8-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="226a8-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="226a8-153">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="226a8-153">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="226a8-154">**D3DXCreatePRTCompBuffer**</span><span class="sxs-lookup"><span data-stu-id="226a8-154">**D3DXCreatePRTCompBuffer**</span></span>](d3dxcreateprtcompbuffer.md)
</dt> <dt>

[<span data-ttu-id="226a8-155">**ID3DXPRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="226a8-155">**ID3DXPRTBuffer**</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
