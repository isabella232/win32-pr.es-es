---
title: Función UpdateSubresources (asignación de la pila) (D3dx12. h)
description: Actualiza Subrecursos con una implementación de asignación de pila.
ms.assetid: 2F30FDF1-4450-473E-AEA8-C5FF54260BCE
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
ms.openlocfilehash: 237e7df26b35b4cb5b1dba7b2a80c1baaac64e8c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707805"
---
# <a name="updatesubresources-stack-allocating-function"></a><span data-ttu-id="8408b-104">Función UpdateSubresources (asignación de pila)</span><span class="sxs-lookup"><span data-stu-id="8408b-104">UpdateSubresources (stack-allocating) function</span></span>

<span data-ttu-id="8408b-105">Actualiza Subrecursos con una implementación de asignación de pila.</span><span class="sxs-lookup"><span data-stu-id="8408b-105">Updates subresources with a stack-allocating implementation.</span></span>

## <a name="syntax"></a><span data-ttu-id="8408b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8408b-106">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="8408b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8408b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8408b-108">*pCmdList* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8408b-108">*pCmdList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8408b-109">Tipo: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="8408b-109">Type: **[**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="8408b-110">La lista de comandos, como un puntero a un [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span><span class="sxs-lookup"><span data-stu-id="8408b-110">The command list, as a pointer to an [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span></span>

</dd> <dt>

<span data-ttu-id="8408b-111">*pDestinationResource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8408b-111">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8408b-112">Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="8408b-112">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="8408b-113">El recurso de destino, como un puntero a un [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="8408b-113">The destination resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="8408b-114">*pIntermediate* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8408b-114">*pIntermediate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8408b-115">Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="8408b-115">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="8408b-116">El recurso intermedio, como un puntero a un [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="8408b-116">The intermediate resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="8408b-117">*IntermediateOffset*</span><span class="sxs-lookup"><span data-stu-id="8408b-117">*IntermediateOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="8408b-118">Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8408b-118">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8408b-119">Desplazamiento, en bytes, al recurso intermedio.</span><span class="sxs-lookup"><span data-stu-id="8408b-119">The offset, in bytes, to the intermediate resource.</span></span>

</dd> <dt>

<span data-ttu-id="8408b-120">*FirstSubresource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8408b-120">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8408b-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8408b-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8408b-122">Índice del primer subrecurso del recurso.</span><span class="sxs-lookup"><span data-stu-id="8408b-122">The index of the first subresource in the resource.</span></span> <span data-ttu-id="8408b-123">Los valores válidos oscilan entre 0 y *MaxSubresources*.</span><span class="sxs-lookup"><span data-stu-id="8408b-123">Valid values range from 0 to *MaxSubresources*.</span></span>

</dd> <dt>

<span data-ttu-id="8408b-124">*NumSubresources* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8408b-124">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8408b-125">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8408b-125">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8408b-126">El número de Subrecursos del recurso.</span><span class="sxs-lookup"><span data-stu-id="8408b-126">The number of subresources in the resource.</span></span> <span data-ttu-id="8408b-127">Los valores válidos van de 1 a (*MaxSubresources*  -  *FirstSubresource*).</span><span class="sxs-lookup"><span data-stu-id="8408b-127">Valid values range from 1 to (*MaxSubresources* - *FirstSubresource*).</span></span>

</dd> <dt>

<span data-ttu-id="8408b-128">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8408b-128">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8408b-129">Tipo: **[ **D3D12 \_ subresource \_ Data**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span><span class="sxs-lookup"><span data-stu-id="8408b-129">Type: **[**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="8408b-130">Puntero a una matriz (de longitud *NumSubresources*) de punteros a estructuras de [**\_ \_ datos de Subrecursos de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) que contienen descripciones de los datos de los Subrecursos utilizados para la actualización.</span><span class="sxs-lookup"><span data-stu-id="8408b-130">Pointer to an array (of length *NumSubresources*) of pointers to [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structures containing descriptions of the subresource data used for the update.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8408b-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8408b-131">Return value</span></span>

<span data-ttu-id="8408b-132">Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8408b-132">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8408b-133">Tamaño del búfer en bytes.</span><span class="sxs-lookup"><span data-stu-id="8408b-133">The size, in bytes, of the buffer.</span></span>

## <a name="remarks"></a><span data-ttu-id="8408b-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8408b-134">Remarks</span></span>

<span data-ttu-id="8408b-135">La declaración de esta función comienza por: `template <UINT MaxSubresources>`</span><span class="sxs-lookup"><span data-stu-id="8408b-135">The declaration of this function begins with: `template <UINT MaxSubresources>`</span></span>

## <a name="requirements"></a><span data-ttu-id="8408b-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8408b-136">Requirements</span></span>



| <span data-ttu-id="8408b-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="8408b-137">Requirement</span></span> | <span data-ttu-id="8408b-138">Value</span><span class="sxs-lookup"><span data-stu-id="8408b-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8408b-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8408b-139">Header</span></span><br/>  | <dl> <span data-ttu-id="8408b-140"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8408b-140"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="8408b-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8408b-141">Library</span></span><br/> | <dl> <span data-ttu-id="8408b-142"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8408b-142"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="8408b-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8408b-143">DLL</span></span><br/>     | <dl> <span data-ttu-id="8408b-144"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8408b-144"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8408b-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="8408b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8408b-146">Funciones auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="8408b-146">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="8408b-147">Subrecursos</span><span class="sxs-lookup"><span data-stu-id="8408b-147">Subresources</span></span>](subresources.md)
</dt> </dl>

 

