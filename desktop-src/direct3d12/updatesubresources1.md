---
title: Función UpdateSubresources (D3dx12. h)
description: Actualiza los Subrecursos, se deben rellenar todas las matrices de Subrecursos, normalmente llamando a ID3D12Device GetCopyableFootprints.
ms.assetid: D6885165-095E-452D-8D93-A2C43A215F48
keywords:
- UpdateSubresources función)
topic_type:
- apiref
api_name:
- UpdateSubresources
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 885ee058aacbfca238448830f2b7b1b54a298f89
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708083"
---
# <a name="updatesubresources-function"></a><span data-ttu-id="21dc3-104">UpdateSubresources función)</span><span class="sxs-lookup"><span data-stu-id="21dc3-104">UpdateSubresources function</span></span>

<span data-ttu-id="21dc3-105">Actualiza los Subrecursos, se deben rellenar todas las matrices de Subrecursos, normalmente mediante una llamada a [**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span><span class="sxs-lookup"><span data-stu-id="21dc3-105">Updates subresources, all the subresource arrays should be populated, typically by calling [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span></span>

## <a name="syntax"></a><span data-ttu-id="21dc3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21dc3-106">Syntax</span></span>


```C++
UINT64 inline UpdateSubresources(
  _In_       ID3D12GraphicsCommandList          *pCmdList,
  _In_       ID3D12Resource                     *pDestinationResource,
  _In_       ID3D12Resource                     *pIntermediate,
  _In_       UINT                               FirstSubresource,
  _In_       UINT                               NumSubresources,
             UINT64                             RequiredSize,
  _In_ const D3D12_PLACED_SUBRESOURCE_FOOTPRINT *pLayouts,
  _In_ const UINT                               *pNumRows,
  _In_ const UINT64                             *pRowSizesInBytes,
  _In_ const D3D12_SUBRESOURCE_DATA             *pSrcData
);
```



## <a name="parameters"></a><span data-ttu-id="21dc3-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21dc3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21dc3-108">*pCmdList* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21dc3-108">*pCmdList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21dc3-109">Tipo: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="21dc3-109">Type: **[**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="21dc3-110">La lista de comandos, como un puntero a un [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span><span class="sxs-lookup"><span data-stu-id="21dc3-110">The command list, as a pointer to an [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span></span>

</dd> <dt>

<span data-ttu-id="21dc3-111">*pDestinationResource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21dc3-111">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21dc3-112">Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="21dc3-112">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="21dc3-113">El recurso de destino, como un puntero a un [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="21dc3-113">The destination resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="21dc3-114">*pIntermediate* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21dc3-114">*pIntermediate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21dc3-115">Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="21dc3-115">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="21dc3-116">El recurso intermedio, como un puntero a un [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="21dc3-116">The intermediate resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="21dc3-117">*FirstSubresource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21dc3-117">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21dc3-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="21dc3-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="21dc3-119">Índice del primer subrecurso del recurso.</span><span class="sxs-lookup"><span data-stu-id="21dc3-119">The index of the first subresource in the resource.</span></span> <span data-ttu-id="21dc3-120">El intervalo de valores válidos es de 0 a D3D12 \_ req \_ subsources.</span><span class="sxs-lookup"><span data-stu-id="21dc3-120">The range of valid values is 0 to D3D12\_REQ\_SUBRESOURCES.</span></span>

</dd> <dt>

<span data-ttu-id="21dc3-121">*NumSubresources* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21dc3-121">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21dc3-122">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="21dc3-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="21dc3-123">El número de Subrecursos del recurso.</span><span class="sxs-lookup"><span data-stu-id="21dc3-123">The number of subresources in the resource.</span></span> <span data-ttu-id="21dc3-124">El intervalo de valores válidos es de 0 a (D3D12 \_ req \_ subsources- *FirstSubresource*).</span><span class="sxs-lookup"><span data-stu-id="21dc3-124">The range of valid values is 0 to (D3D12\_REQ\_SUBRESOURCES - *FirstSubresource*).</span></span>

</dd> <dt>

<span data-ttu-id="21dc3-125">*RequiredSize*</span><span class="sxs-lookup"><span data-stu-id="21dc3-125">*RequiredSize*</span></span> 
</dt> <dd>

<span data-ttu-id="21dc3-126">Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="21dc3-126">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="21dc3-127">Tamaño necesario, en bytes, para la actualización.</span><span class="sxs-lookup"><span data-stu-id="21dc3-127">The required size, in bytes, for the update.</span></span>

</dd> <dt>

<span data-ttu-id="21dc3-128">*emisiones* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21dc3-128">*pLayouts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21dc3-129">Tipo: **\* const [**D3D12 \_ colocada \_ \_ superficie de Subrecursos**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)**</span><span class="sxs-lookup"><span data-stu-id="21dc3-129">Type: **const [**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)\***</span></span>

<span data-ttu-id="21dc3-130">Puntero a una matriz (de longitud *NumSubresources*) de punteros a las estructuras que contiene la descripción y la ubicación de los Subrecursos del recurso.</span><span class="sxs-lookup"><span data-stu-id="21dc3-130">Pointer to an array (of length *NumSubresources*) of pointers to the structures that contains the description and placement of the resource's subresources.</span></span>

</dd> <dt>

<span data-ttu-id="21dc3-131">*pNumRows* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21dc3-131">*pNumRows* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21dc3-132">Tipo: **const [**uint**](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="21dc3-132">Type: **const [**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="21dc3-133">Puntero a una matriz (de longitud *NumSubresources*) de los uint que contienen el número de filas de cada subrecurso.</span><span class="sxs-lookup"><span data-stu-id="21dc3-133">Pointer to an array (of length *NumSubresources*) of UINTS containing the number of rows for each subresource.</span></span>

</dd> <dt>

<span data-ttu-id="21dc3-134">*pRowSizesInBytes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21dc3-134">*pRowSizesInBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21dc3-135">Tipo: **const [**UINT64**](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="21dc3-135">Type: **const [**UINT64**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="21dc3-136">Puntero a una matriz (de longitud *NumSubresources*) de los uint que contiene el tamaño, en bytes, de cada fila.</span><span class="sxs-lookup"><span data-stu-id="21dc3-136">Pointer to an array (of length *NumSubresources*) of UINTS containing the size, in bytes, of each row.</span></span>

</dd> <dt>

<span data-ttu-id="21dc3-137">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21dc3-137">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21dc3-138">Tipo: **\* [**datos de \_ subrecurso \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) const**</span><span class="sxs-lookup"><span data-stu-id="21dc3-138">Type: **const [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="21dc3-139">Puntero a una matriz (de longitud *NumSubresources*) de punteros a estructuras de [**\_ \_ datos de Subrecursos de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) que contienen descripciones de los datos de los Subrecursos utilizados para la actualización.</span><span class="sxs-lookup"><span data-stu-id="21dc3-139">Pointer to an array (of length *NumSubresources*) of pointers to [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structures containing descriptions of the subresource data used for the update.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21dc3-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21dc3-140">Return value</span></span>

<span data-ttu-id="21dc3-141">Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="21dc3-141">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="21dc3-142">Tamaño del búfer en bytes.</span><span class="sxs-lookup"><span data-stu-id="21dc3-142">The size, in bytes, of the buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="21dc3-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21dc3-143">Requirements</span></span>



| <span data-ttu-id="21dc3-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="21dc3-144">Requirement</span></span> | <span data-ttu-id="21dc3-145">Value</span><span class="sxs-lookup"><span data-stu-id="21dc3-145">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="21dc3-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21dc3-146">Header</span></span><br/>  | <dl> <span data-ttu-id="21dc3-147"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="21dc3-147"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="21dc3-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="21dc3-148">Library</span></span><br/> | <dl> <span data-ttu-id="21dc3-149"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21dc3-149"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="21dc3-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="21dc3-150">DLL</span></span><br/>     | <dl> <span data-ttu-id="21dc3-151"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21dc3-151"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21dc3-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="21dc3-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21dc3-153">Funciones auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="21dc3-153">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="21dc3-154">Subrecursos</span><span class="sxs-lookup"><span data-stu-id="21dc3-154">Subresources</span></span>](subresources.md)
</dt> </dl>

 

