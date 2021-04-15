---
title: Función UpdateSubresources (asignación del montón) (D3dx12. h)
description: Actualiza Subrecursos con una implementación de asignación de montón.
ms.assetid: 328D8755-D328-471D-AAF4-9771CBFF7539
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
ms.openlocfilehash: c97abe59bdd0334fe4b7badf03e44ddc03b85495
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707921"
---
# <a name="updatesubresources-heap-allocating-function"></a><span data-ttu-id="22e6f-104">Función UpdateSubresources (asignación de montones)</span><span class="sxs-lookup"><span data-stu-id="22e6f-104">UpdateSubresources (heap-allocating) function</span></span>

<span data-ttu-id="22e6f-105">Actualiza Subrecursos con una implementación de asignación de montón.</span><span class="sxs-lookup"><span data-stu-id="22e6f-105">Updates subresources with a heap-allocating implementation.</span></span>

## <a name="syntax"></a><span data-ttu-id="22e6f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22e6f-106">Syntax</span></span>


```C++
UINT64 inline UpdateSubresources(
  _In_ ID3D12GraphicsCommandList *pCmdList,
  _In_ ID3D12Resource            *pDestinationResource,
  _In_ ID3D12Resource            *pIntermediate,
       UINT64                    IntermediateOffset,
  _In_ UINT                      FirstSubresource,
  _In_ UINT                      NumSubresources,
  _In_ D3D12_SUBRESOURCE_DATA    *pSrcData
);
```



## <a name="parameters"></a><span data-ttu-id="22e6f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22e6f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22e6f-108">*pCmdList* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="22e6f-108">*pCmdList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22e6f-109">Tipo: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="22e6f-109">Type: **[**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="22e6f-110">Un puntero a la interfaz [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) para la lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="22e6f-110">A pointer to the [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface for the command list.</span></span>

</dd> <dt>

<span data-ttu-id="22e6f-111">*pDestinationResource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="22e6f-111">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22e6f-112">Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="22e6f-112">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="22e6f-113">Puntero a la interfaz [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) que representa el recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="22e6f-113">A pointer to the [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) interface that represents the destination resource.</span></span>

</dd> <dt>

<span data-ttu-id="22e6f-114">*pIntermediate* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="22e6f-114">*pIntermediate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22e6f-115">Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="22e6f-115">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="22e6f-116">Puntero a la interfaz [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) que representa el recurso intermedio.</span><span class="sxs-lookup"><span data-stu-id="22e6f-116">A pointer to the [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) interface that represents the intermediate resource.</span></span>

</dd> <dt>

<span data-ttu-id="22e6f-117">*IntermediateOffset*</span><span class="sxs-lookup"><span data-stu-id="22e6f-117">*IntermediateOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="22e6f-118">Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="22e6f-118">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="22e6f-119">Desplazamiento, en bytes, al recurso intermedio.</span><span class="sxs-lookup"><span data-stu-id="22e6f-119">The offset, in bytes, to the intermediate resource.</span></span>

</dd> <dt>

<span data-ttu-id="22e6f-120">*FirstSubresource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="22e6f-120">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22e6f-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="22e6f-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="22e6f-122">Índice del primer subrecurso del recurso.</span><span class="sxs-lookup"><span data-stu-id="22e6f-122">The index of the first subresource in the resource.</span></span> <span data-ttu-id="22e6f-123">El intervalo de valores válidos es de 0 a D3D12 \_ req \_ subsources.</span><span class="sxs-lookup"><span data-stu-id="22e6f-123">The range of valid values is 0 to D3D12\_REQ\_SUBRESOURCES.</span></span>

</dd> <dt>

<span data-ttu-id="22e6f-124">*NumSubresources* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="22e6f-124">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22e6f-125">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="22e6f-125">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="22e6f-126">El número de Subrecursos del recurso.</span><span class="sxs-lookup"><span data-stu-id="22e6f-126">The number of subresources in the resource.</span></span> <span data-ttu-id="22e6f-127">El intervalo de valores válidos es de 0 a (D3D12 \_ req \_ subsources- *FirstSubresource*).</span><span class="sxs-lookup"><span data-stu-id="22e6f-127">The range of valid values is 0 to (D3D12\_REQ\_SUBRESOURCES - *FirstSubresource*).</span></span>

</dd> <dt>

<span data-ttu-id="22e6f-128">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="22e6f-128">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22e6f-129">Tipo: **[ **D3D12 \_ subresource \_ Data**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span><span class="sxs-lookup"><span data-stu-id="22e6f-129">Type: **[**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="22e6f-130">Puntero a una matriz (de longitud *NumSubresources*) de punteros a estructuras de [**\_ \_ datos de Subrecursos de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) que contienen descripciones de los datos de los Subrecursos utilizados para la actualización.</span><span class="sxs-lookup"><span data-stu-id="22e6f-130">Pointer to an array (of length *NumSubresources*) of pointers to [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structures containing descriptions of the subresource data used for the update.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22e6f-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22e6f-131">Return value</span></span>

<span data-ttu-id="22e6f-132">Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="22e6f-132">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="22e6f-133">Tamaño del búfer en bytes.</span><span class="sxs-lookup"><span data-stu-id="22e6f-133">The size, in bytes, of the buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="22e6f-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22e6f-134">Requirements</span></span>



| <span data-ttu-id="22e6f-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="22e6f-135">Requirement</span></span> | <span data-ttu-id="22e6f-136">Value</span><span class="sxs-lookup"><span data-stu-id="22e6f-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="22e6f-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22e6f-137">Header</span></span><br/>  | <dl> <span data-ttu-id="22e6f-138"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="22e6f-138"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="22e6f-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="22e6f-139">Library</span></span><br/> | <dl> <span data-ttu-id="22e6f-140"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22e6f-140"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="22e6f-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="22e6f-141">DLL</span></span><br/>     | <dl> <span data-ttu-id="22e6f-142"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22e6f-142"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22e6f-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="22e6f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22e6f-144">Funciones auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="22e6f-144">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="22e6f-145">Subrecursos</span><span class="sxs-lookup"><span data-stu-id="22e6f-145">Subresources</span></span>](subresources.md)
</dt> </dl>

 

