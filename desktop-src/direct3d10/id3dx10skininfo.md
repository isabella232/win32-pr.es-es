---
description: ID3DX10SkinInfo permite optimizar, procesar y establecer manualmente la relación entre los huesos y los vértices de las mallas (consulte la animación del esqueleto en Wikipedia).
ms.assetid: bea0fe71-c201-45c6-8036-d0d76d5851fd
title: Interfaz ID3DX10SkinInfo (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3216765ab9ef2ba9f2b0883c31a878a7eae6861f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362585"
---
# <a name="id3dx10skininfo-interface"></a><span data-ttu-id="6f0d5-103">Interfaz ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="6f0d5-103">ID3DX10SkinInfo interface</span></span>

<span data-ttu-id="6f0d5-104">ID3DX10SkinInfo permite optimizar, procesar y establecer manualmente la relación entre los huesos y los vértices de las mallas (consulte la [animación del esqueleto en Wikipedia](https://en.wikipedia.org/wiki/Skeletal_animation)).</span><span class="sxs-lookup"><span data-stu-id="6f0d5-104">ID3DX10SkinInfo allows you to optimize, process, and manually set the relationship between bones and vertices in your meshes (see [Skeletal Animation on Wikipedia](https://en.wikipedia.org/wiki/Skeletal_animation)).</span></span> <span data-ttu-id="6f0d5-105">Es más útil para hacer que los archivos. x exportados por las aplicaciones de DCC (por ejemplo, 3DS Max y Maya) sean más fáciles de utilizar para el hardware y para mejorar la velocidad de representación de las mallas estratificadas en el modo de representación de software.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-105">It is most useful for making .x files exported by DCC Apps (such as 3DS Max and Maya) more hardware-friendly, and for improving the render speed of your skinned meshes in software render mode.</span></span>

## <a name="members"></a><span data-ttu-id="6f0d5-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="6f0d5-106">Members</span></span>

<span data-ttu-id="6f0d5-107">La interfaz **ID3DX10SkinInfo** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6f0d5-107">The **ID3DX10SkinInfo** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6f0d5-108">**ID3DX10SkinInfo** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6f0d5-108">**ID3DX10SkinInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="6f0d5-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="6f0d5-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6f0d5-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="6f0d5-110">Methods</span></span>

<span data-ttu-id="6f0d5-111">La interfaz **ID3DX10SkinInfo** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-111">The **ID3DX10SkinInfo** interface has these methods.</span></span>



| <span data-ttu-id="6f0d5-112">Método</span><span class="sxs-lookup"><span data-stu-id="6f0d5-112">Method</span></span>                                                                   | <span data-ttu-id="6f0d5-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f0d5-113">Description</span></span>                                                                                                                        |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f0d5-114">**AddBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="6f0d5-114">**AddBoneInfluences**</span></span>](id3dx10skininfo-addboneinfluences.md)           | <span data-ttu-id="6f0d5-115">Permite que un hueso existente afecte a un grupo de vértices y defina la influencia que tenga el hueso en cada vértice.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-115">Enable an existing bone to influence a group of vertices and define how much influence the bone has on each vertex.</span></span><br/>     |
| [<span data-ttu-id="6f0d5-116">**AddBones**</span><span class="sxs-lookup"><span data-stu-id="6f0d5-116">**AddBones**</span></span>](id3dx10skininfo-addbones.md)                             | <span data-ttu-id="6f0d5-117">Asigne espacio para más huesos.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-117">Allocate space for more bones.</span></span><br/>                                                                                          |
| [<span data-ttu-id="6f0d5-118">**AddVertices**</span><span class="sxs-lookup"><span data-stu-id="6f0d5-118">**AddVertices**</span></span>](id3dx10skininfo-addvertices.md)                       | <span data-ttu-id="6f0d5-119">Asigne espacio para los vértices adicionales.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-119">Allocate space for additional vertices.</span></span><br/>                                                                                 |
| [<span data-ttu-id="6f0d5-120">**ClearBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="6f0d5-120">**ClearBoneInfluences**</span></span>](id3dx10skininfo-clearboneinfluences.md)       | <span data-ttu-id="6f0d5-121">Borre la lista de vértices de un hueso a los que influye.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-121">Clear a bone's list of vertices that it influences.</span></span><br/>                                                                     |
| [<span data-ttu-id="6f0d5-122">**Compacto**</span><span class="sxs-lookup"><span data-stu-id="6f0d5-122">**Compact**</span></span>](id3dx10skininfo-compact.md)                               | <span data-ttu-id="6f0d5-123">Limite el número de huesos que pueden influir en un vértice o limite la cantidad de influencia que puede tener un hueso en un vértice.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-123">Limit the number of bones that can influence a vertex and/or limit the amount of influence a bone can have on a vertex.</span></span><br/> |
| [<span data-ttu-id="6f0d5-124">**DoSoftwareSkinning**</span><span class="sxs-lookup"><span data-stu-id="6f0d5-124">**DoSoftwareSkinning**</span></span>](id3dx10skininfo-dosoftwareskinning.md)         | <span data-ttu-id="6f0d5-125">Realice la piel de software en una matriz de vértices.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-125">Do software skinning on an array of vertices.</span></span><br/>                                                                           |
| [<span data-ttu-id="6f0d5-126">**FindBoneInfluenceIndex**</span><span class="sxs-lookup"><span data-stu-id="6f0d5-126">**FindBoneInfluenceIndex**</span></span>](id3dx10skininfo-findboneinfluenceindex.md) | <span data-ttu-id="6f0d5-127">Busque el índice que indica dónde se encuentra un vértice determinado en la lista de vértices influida de un hueso determinado.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-127">Find the index that indicates where a given vertex is in a given bone's list of influenced vertices.</span></span><br/>                    |
| [<span data-ttu-id="6f0d5-128">**GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="6f0d5-128">**GetBoneInfluence**</span></span>](id3dx10skininfo-getboneinfluence.md)             | <span data-ttu-id="6f0d5-129">Obtiene la cantidad de influencia que un hueso determinado tiene sobre un vértice determinado.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-129">Get the amount of influence a given bone has over a given vertex.</span></span><br/>                                                       |
| [<span data-ttu-id="6f0d5-130">**GetBoneInfluenceCount**</span><span class="sxs-lookup"><span data-stu-id="6f0d5-130">**GetBoneInfluenceCount**</span></span>](id3dx10skininfo-getboneinfluencecount.md)   | <span data-ttu-id="6f0d5-131">Obtiene el número de vértices a los que afecta un hueso determinado.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-131">Get the number of vertices that a given bone influences.</span></span><br/>                                                                |
| [<span data-ttu-id="6f0d5-132">**GetBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="6f0d5-132">**GetBoneInfluences**</span></span>](id3dx10skininfo-getboneinfluences.md)           | <span data-ttu-id="6f0d5-133">Obtiene una lista de vértices a los que afecta un hueso determinado y una lista de la cantidad de influencia que tiene el hueso en cada vértice.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-133">Get a list of vertices that a given bone influences and a list of the amount of influence that bone has on each vertex.</span></span><br/> |
| [<span data-ttu-id="6f0d5-134">**GetMaxBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="6f0d5-134">**GetMaxBoneInfluences**</span></span>](id3dx10skininfo-getmaxboneinfluences.md)     | <span data-ttu-id="6f0d5-135">Obtiene el número de vértices a los que puede afectar máximamente el hueso.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-135">Get the number of vertices a bone can maximally influence.</span></span><br/>                                                              |
| [<span data-ttu-id="6f0d5-136">**GetNumBones**</span><span class="sxs-lookup"><span data-stu-id="6f0d5-136">**GetNumBones**</span></span>](id3dx10skininfo-getnumbones.md)                       | <span data-ttu-id="6f0d5-137">Obtiene el número de huesos en ID3DX10SkinInfo.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-137">Get the number of bones in ID3DX10SkinInfo.</span></span><br/>                                                                             |
| [<span data-ttu-id="6f0d5-138">**GetNumVertices**</span><span class="sxs-lookup"><span data-stu-id="6f0d5-138">**GetNumVertices**</span></span>](id3dx10skininfo-getnumvertices.md)                 | <span data-ttu-id="6f0d5-139">Obtiene el número de vértices en ID3DX10SkinInfo.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-139">Get the number of vertices in ID3DX10SkinInfo.</span></span><br/>                                                                          |
| [<span data-ttu-id="6f0d5-140">**RemapBones**</span><span class="sxs-lookup"><span data-stu-id="6f0d5-140">**RemapBones**</span></span>](id3dx10skininfo-remapbones.md)                         | <span data-ttu-id="6f0d5-141">Cambiar los huesos influyen en los vértices.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-141">Change which bones influence which vertices.</span></span><br/>                                                                            |
| [<span data-ttu-id="6f0d5-142">**RemapVertices**</span><span class="sxs-lookup"><span data-stu-id="6f0d5-142">**RemapVertices**</span></span>](id3dx10skininfo-remapvertices.md)                   | <span data-ttu-id="6f0d5-143">Cambiar los vértices afectados por los huesos.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-143">Change which vertices are influenced by which bones.</span></span><br/>                                                                    |
| [<span data-ttu-id="6f0d5-144">**RemoveBone**</span><span class="sxs-lookup"><span data-stu-id="6f0d5-144">**RemoveBone**</span></span>](id3dx10skininfo-removebone.md)                         | <span data-ttu-id="6f0d5-145">Quitar un hueso.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-145">Remove a bone.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="6f0d5-146">**SetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="6f0d5-146">**SetBoneInfluence**</span></span>](id3dx10skininfo-setboneinfluence.md)             | <span data-ttu-id="6f0d5-147">Establece la cantidad de influencia que un hueso determinado tiene sobre un vértice determinado.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-147">Set the amount of influence a given bone has over a given vertex.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="6f0d5-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f0d5-148">Remarks</span></span>

<span data-ttu-id="6f0d5-149">Cree una interfaz ID3DX10SkinInfo con [**D3DX10CreateSkinInfo**](d3d10-d3dx10createskininfo.md), **D3DX10CreateSkinInfoFromBlendedMesh** o **D3DX10CreateSkinInfoFVF**.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-149">Create a ID3DX10SkinInfo interface with [**D3DX10CreateSkinInfo**](d3d10-d3dx10createskininfo.md), **D3DX10CreateSkinInfoFromBlendedMesh**, or **D3DX10CreateSkinInfoFVF**.</span></span>

<span data-ttu-id="6f0d5-150">El tipo LPD3DX10SKININFO se define como un puntero a la interfaz **ID3DX10SkinInfo** .</span><span class="sxs-lookup"><span data-stu-id="6f0d5-150">The LPD3DX10SKININFO type is defined as a pointer to the **ID3DX10SkinInfo** interface.</span></span>


```
typedef struct ID3DX10SkinInfo *LPD3DX10SKININFO;
```



## <a name="requirements"></a><span data-ttu-id="6f0d5-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f0d5-151">Requirements</span></span>



| <span data-ttu-id="6f0d5-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f0d5-152">Requirement</span></span> | <span data-ttu-id="6f0d5-153">Value</span><span class="sxs-lookup"><span data-stu-id="6f0d5-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f0d5-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f0d5-154">Header</span></span><br/>  | <dl> <span data-ttu-id="6f0d5-155"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f0d5-155"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="6f0d5-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6f0d5-156">Library</span></span><br/> | <dl> <span data-ttu-id="6f0d5-157"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f0d5-157"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f0d5-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f0d5-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f0d5-159">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="6f0d5-159">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
