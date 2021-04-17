---
description: Recupera las opciones de malla habilitadas para esta malla en el momento de la creación.
ms.assetid: 4be990d7-77ab-4273-b852-e6283a89ac6c
title: 'ID3DXBaseMesh:: GetOptions (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetOptions
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a751230b4ccfc537f651846ed455b62d7c7f8262
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718383"
---
# <a name="id3dxbasemeshgetoptions-method"></a><span data-ttu-id="07be0-103">ID3DXBaseMesh:: GetOptions (método)</span><span class="sxs-lookup"><span data-stu-id="07be0-103">ID3DXBaseMesh::GetOptions method</span></span>

<span data-ttu-id="07be0-104">Recupera las opciones de malla habilitadas para esta malla en el momento de la creación.</span><span class="sxs-lookup"><span data-stu-id="07be0-104">Retrieves the mesh options enabled for this mesh at creation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="07be0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07be0-105">Syntax</span></span>


```C++
DWORD GetOptions();
```



## <a name="parameters"></a><span data-ttu-id="07be0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="07be0-106">Parameters</span></span>

<span data-ttu-id="07be0-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="07be0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="07be0-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="07be0-108">Return value</span></span>

<span data-ttu-id="07be0-109">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07be0-109">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="07be0-110">Devuelve una combinación de una o varias de las marcas siguientes, que indican las opciones habilitadas para esta malla en el momento de su creación.</span><span class="sxs-lookup"><span data-stu-id="07be0-110">Returns a combination of one or more of the following flags, indicating the options enabled for this mesh at creation time.</span></span>



| <span data-ttu-id="07be0-111">Value</span><span class="sxs-lookup"><span data-stu-id="07be0-111">Value</span></span>                   | <span data-ttu-id="07be0-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="07be0-112">Description</span></span>                                                                                                                                                                                      |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07be0-113">D3DXMESH \_ 32 bits</span><span class="sxs-lookup"><span data-stu-id="07be0-113">D3DXMESH\_32BIT</span></span>         | <span data-ttu-id="07be0-114">Usar índices de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="07be0-114">Use 32-bit indices.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="07be0-115">D3DXMESH \_ DONOTCLIP</span><span class="sxs-lookup"><span data-stu-id="07be0-115">D3DXMESH\_DONOTCLIP</span></span>     | <span data-ttu-id="07be0-116">Use la \_ marca de uso de D3DUSAGE DONOTCLIP para los búferes de vértices y de índices.</span><span class="sxs-lookup"><span data-stu-id="07be0-116">Use the D3DUSAGE\_DONOTCLIP usage flag for vertex and index buffers.</span></span>                                                                                                                             |
| <span data-ttu-id="07be0-117">D3DXMESH \_ dinámico</span><span class="sxs-lookup"><span data-stu-id="07be0-117">D3DXMESH\_DYNAMIC</span></span>       | <span data-ttu-id="07be0-118">Equivale a especificar D3DXMESH \_ VB \_ Dynamic y D3DXMESH \_ IB \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="07be0-118">Equivalent to specifying both D3DXMESH\_VB\_DYNAMIC and D3DXMESH\_IB\_DYNAMIC.</span></span>                                                                                                                   |
| <span data-ttu-id="07be0-119">D3DXMESH \_ RTPATCHES</span><span class="sxs-lookup"><span data-stu-id="07be0-119">D3DXMESH\_RTPATCHES</span></span>     | <span data-ttu-id="07be0-120">Use la \_ marca de uso de D3DUSAGE RTPATCHES para los búferes de vértices y de índices.</span><span class="sxs-lookup"><span data-stu-id="07be0-120">Use the D3DUSAGE\_RTPATCHES usage flag for vertex and index buffers.</span></span>                                                                                                                             |
| <span data-ttu-id="07be0-121">D3DXMESH \_ NPATCHES</span><span class="sxs-lookup"><span data-stu-id="07be0-121">D3DXMESH\_NPATCHES</span></span>      | <span data-ttu-id="07be0-122">Si se especifica esta marca, el vértice y el búfer de índice de la malla se crearán con la \_ marca D3DUSAGE NPATCHES.</span><span class="sxs-lookup"><span data-stu-id="07be0-122">Specifying this flag causes the vertex and index buffer of the mesh to be created with D3DUSAGE\_NPATCHES flag.</span></span> <span data-ttu-id="07be0-123">Esto es necesario si el objeto de malla se va a representar mediante la mejora de N-patch.</span><span class="sxs-lookup"><span data-stu-id="07be0-123">This is required if the mesh object is to be rendered using N-Patch enhancement.</span></span> |
| <span data-ttu-id="07be0-124">Administrado por D3DXMESH \_</span><span class="sxs-lookup"><span data-stu-id="07be0-124">D3DXMESH\_MANAGED</span></span>       | <span data-ttu-id="07be0-125">Equivale a especificar D3DXMESH \_ VB \_ administrado y D3DXMESH \_ IB \_ administrado.</span><span class="sxs-lookup"><span data-stu-id="07be0-125">Equivalent to specifying both D3DXMESH\_VB\_MANAGED and D3DXMESH\_IB\_MANAGED.</span></span>                                                                                                                   |
| <span data-ttu-id="07be0-126">\_Puntos D3DXMESH</span><span class="sxs-lookup"><span data-stu-id="07be0-126">D3DXMESH\_POINTS</span></span>        | <span data-ttu-id="07be0-127">Use la \_ marca de uso de puntos D3DUSAGE para los búferes de vértices y de índices.</span><span class="sxs-lookup"><span data-stu-id="07be0-127">Use the D3DUSAGE\_POINTS usage flag for vertex and index buffers.</span></span>                                                                                                                                |
| <span data-ttu-id="07be0-128">D3DXMESH \_ IB \_ Dynamic</span><span class="sxs-lookup"><span data-stu-id="07be0-128">D3DXMESH\_IB\_DYNAMIC</span></span>   | <span data-ttu-id="07be0-129">Use la \_ marca de uso dinámico D3DUSAGE para los búferes de índice.</span><span class="sxs-lookup"><span data-stu-id="07be0-129">Use the D3DUSAGE\_DYNAMIC usage flag for index buffers.</span></span>                                                                                                                                          |
| <span data-ttu-id="07be0-130">Administrado por D3DXMESH \_ IB \_</span><span class="sxs-lookup"><span data-stu-id="07be0-130">D3DXMESH\_IB\_MANAGED</span></span>   | <span data-ttu-id="07be0-131">Use la \_ clase de memoria administrada D3DPOOL para los búferes de índice.</span><span class="sxs-lookup"><span data-stu-id="07be0-131">Use the D3DPOOL\_MANAGED memory class for index buffers.</span></span>                                                                                                                                         |
| <span data-ttu-id="07be0-132">D3DXMESH \_ IB \_ SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="07be0-132">D3DXMESH\_IB\_SYSTEMMEM</span></span> | <span data-ttu-id="07be0-133">Use la \_ clase de memoria D3DPOOL SYSTEMMEM para los búferes de índice.</span><span class="sxs-lookup"><span data-stu-id="07be0-133">Use the D3DPOOL\_SYSTEMMEM memory class for index buffers.</span></span>                                                                                                                                       |
| <span data-ttu-id="07be0-134">D3DXMESH \_ IB \_ WRITEONLY</span><span class="sxs-lookup"><span data-stu-id="07be0-134">D3DXMESH\_IB\_WRITEONLY</span></span> | <span data-ttu-id="07be0-135">Use la \_ marca de uso WRITEONLY de D3DUSAGE para los búferes de índice.</span><span class="sxs-lookup"><span data-stu-id="07be0-135">Use the D3DUSAGE\_WRITEONLY usage flag for index buffers.</span></span>                                                                                                                                        |
| <span data-ttu-id="07be0-136">D3DXMESH \_ SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="07be0-136">D3DXMESH\_SYSTEMMEM</span></span>     | <span data-ttu-id="07be0-137">Equivale a especificar D3DXMESH \_ VB \_ SYSTEMMEM y D3DXMESH \_ IB \_ SYSTEMMEM.</span><span class="sxs-lookup"><span data-stu-id="07be0-137">Equivalent to specifying both D3DXMESH\_VB\_SYSTEMMEM and D3DXMESH\_IB\_SYSTEMMEM.</span></span>                                                                                                               |
| <span data-ttu-id="07be0-138">D3DXMESH \_ VB \_ dinámico</span><span class="sxs-lookup"><span data-stu-id="07be0-138">D3DXMESH\_VB\_DYNAMIC</span></span>   | <span data-ttu-id="07be0-139">Use la \_ marca de uso dinámico D3DUSAGE para los búferes de vértices.</span><span class="sxs-lookup"><span data-stu-id="07be0-139">Use the D3DUSAGE\_DYNAMIC usage flag for vertex buffers.</span></span>                                                                                                                                         |
| <span data-ttu-id="07be0-140">D3DXMESH \_ VB \_ administrado</span><span class="sxs-lookup"><span data-stu-id="07be0-140">D3DXMESH\_VB\_MANAGED</span></span>   | <span data-ttu-id="07be0-141">Use la \_ clase de memoria administrada D3DPOOL para los búferes de vértices.</span><span class="sxs-lookup"><span data-stu-id="07be0-141">Use the D3DPOOL\_MANAGED memory class for vertex buffers.</span></span>                                                                                                                                        |
| <span data-ttu-id="07be0-142">D3DXMESH \_ VB \_ SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="07be0-142">D3DXMESH\_VB\_SYSTEMMEM</span></span> | <span data-ttu-id="07be0-143">Use la \_ clase de memoria D3DPOOL SYSTEMMEM para los búferes de vértices.</span><span class="sxs-lookup"><span data-stu-id="07be0-143">Use the D3DPOOL\_SYSTEMMEM memory class for vertex buffers.</span></span>                                                                                                                                      |
| <span data-ttu-id="07be0-144">D3DXMESH \_ VB \_ WRITEONLY</span><span class="sxs-lookup"><span data-stu-id="07be0-144">D3DXMESH\_VB\_WRITEONLY</span></span> | <span data-ttu-id="07be0-145">Use la \_ marca de uso WRITEONLY de D3DUSAGE para los búferes de vértices.</span><span class="sxs-lookup"><span data-stu-id="07be0-145">Use the D3DUSAGE\_WRITEONLY usage flag for vertex buffers.</span></span>                                                                                                                                       |
| <span data-ttu-id="07be0-146">D3DXMESH \_ WRITEONLY</span><span class="sxs-lookup"><span data-stu-id="07be0-146">D3DXMESH\_WRITEONLY</span></span>     | <span data-ttu-id="07be0-147">Equivalente a especificar tanto D3DXMESH \_ VB \_ WRITEONLY como D3DXMESH \_ IB \_ WriteOnly.</span><span class="sxs-lookup"><span data-stu-id="07be0-147">Equivalent to specifying both D3DXMESH\_VB\_WRITEONLY and D3DXMESH\_IB\_WRITEONLY.</span></span>                                                                                                               |



 

## <a name="requirements"></a><span data-ttu-id="07be0-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07be0-148">Requirements</span></span>



| <span data-ttu-id="07be0-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="07be0-149">Requirement</span></span> | <span data-ttu-id="07be0-150">Value</span><span class="sxs-lookup"><span data-stu-id="07be0-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07be0-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07be0-151">Header</span></span><br/>  | <dl> <span data-ttu-id="07be0-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="07be0-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="07be0-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="07be0-153">Library</span></span><br/> | <dl> <span data-ttu-id="07be0-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07be0-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="07be0-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="07be0-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07be0-156">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="07be0-156">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
