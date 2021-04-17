---
title: Función MemcpySubresource (D3dx12. h)
description: Copia un subrecurso fila por fila.
ms.assetid: 33A9F99D-FD85-4FD6-AFD6-7A10F16C3D9B
keywords:
- MemcpySubresource función)
topic_type:
- apiref
api_name:
- MemcpySubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b955211a490927033186442480b3449773b4ebcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698324"
---
# <a name="memcpysubresource-function"></a><span data-ttu-id="d65a8-104">MemcpySubresource función)</span><span class="sxs-lookup"><span data-stu-id="d65a8-104">MemcpySubresource function</span></span>

<span data-ttu-id="d65a8-105">Copia un subrecurso fila por fila.</span><span class="sxs-lookup"><span data-stu-id="d65a8-105">Copies a subresource row by row.</span></span>

## <a name="syntax"></a><span data-ttu-id="d65a8-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d65a8-106">Syntax</span></span>


```C++
void inline MemcpySubresource(
  _In_ const D3D12_MEMCPY_DEST      *pDest,
  _In_ const D3D12_SUBRESOURCE_DATA *pSrc,
             SIZE_T                 RowSizeInBytes,
             UINT                   NumRows,
             UINT                   NumSlices
);
```



## <a name="parameters"></a><span data-ttu-id="d65a8-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d65a8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d65a8-108">*pDest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d65a8-108">*pDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d65a8-109">Tipo: **const [**D3D12 \_ MEMCPY \_ dest**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) \***</span><span class="sxs-lookup"><span data-stu-id="d65a8-109">Type: **const [**D3D12\_MEMCPY\_DEST**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest)\***</span></span>

<span data-ttu-id="d65a8-110">Puntero a una estructura [**de \_ \_ destino de D3D12 MEMCPY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) que describe el destino de la operación de copia de memoria.</span><span class="sxs-lookup"><span data-stu-id="d65a8-110">A pointer to a [**D3D12\_MEMCPY\_DEST**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) structure that describes the destination of the memory copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="d65a8-111">*pSrc* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d65a8-111">*pSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d65a8-112">Tipo: **\* [**datos de \_ subrecurso \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) const**</span><span class="sxs-lookup"><span data-stu-id="d65a8-112">Type: **const [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="d65a8-113">Puntero a una estructura [**de \_ \_ datos de Subrecursos D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) que describe el origen de la operación de copia de la memoria.</span><span class="sxs-lookup"><span data-stu-id="d65a8-113">A pointer to a [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structure that describes the source of the memory copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="d65a8-114">*RowSizeInBytes*</span><span class="sxs-lookup"><span data-stu-id="d65a8-114">*RowSizeInBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="d65a8-115">Tipo: **[ **tamaño \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d65a8-115">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d65a8-116">Tamaño, en bytes, de cada fila.</span><span class="sxs-lookup"><span data-stu-id="d65a8-116">The size, in bytes, of each row.</span></span>

</dd> <dt>

<span data-ttu-id="d65a8-117">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="d65a8-117">*NumRows*</span></span> 
</dt> <dd>

<span data-ttu-id="d65a8-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d65a8-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d65a8-119">Número de filas.</span><span class="sxs-lookup"><span data-stu-id="d65a8-119">The number of rows.</span></span>

</dd> <dt>

<span data-ttu-id="d65a8-120">*NumSlices*</span><span class="sxs-lookup"><span data-stu-id="d65a8-120">*NumSlices*</span></span> 
</dt> <dd>

<span data-ttu-id="d65a8-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d65a8-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d65a8-122">Número de segmentos.</span><span class="sxs-lookup"><span data-stu-id="d65a8-122">The number of slices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d65a8-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d65a8-123">Return value</span></span>

<span data-ttu-id="d65a8-124">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d65a8-124">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d65a8-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d65a8-125">Remarks</span></span>

<span data-ttu-id="d65a8-126">Considere también los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="d65a8-126">Also consider the following methods:</span></span>

-   [<span data-ttu-id="d65a8-127">**ID3D12Resource::WriteToSubresource**</span><span class="sxs-lookup"><span data-stu-id="d65a8-127">**ID3D12Resource::WriteToSubresource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource)
-   [<span data-ttu-id="d65a8-128">**ID3D12Resource::ReadFromSubresource**</span><span class="sxs-lookup"><span data-stu-id="d65a8-128">**ID3D12Resource::ReadFromSubresource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource)
-   [<span data-ttu-id="d65a8-129">**ID3D12GraphicsCommandList::CopyResource**</span><span class="sxs-lookup"><span data-stu-id="d65a8-129">**ID3D12GraphicsCommandList::CopyResource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)

## <a name="requirements"></a><span data-ttu-id="d65a8-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d65a8-130">Requirements</span></span>



| <span data-ttu-id="d65a8-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d65a8-131">Requirement</span></span> | <span data-ttu-id="d65a8-132">Value</span><span class="sxs-lookup"><span data-stu-id="d65a8-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d65a8-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d65a8-133">Header</span></span><br/>  | <dl> <span data-ttu-id="d65a8-134"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="d65a8-134"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="d65a8-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d65a8-135">Library</span></span><br/> | <dl> <span data-ttu-id="d65a8-136"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d65a8-136"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="d65a8-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d65a8-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="d65a8-138"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d65a8-138"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d65a8-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="d65a8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d65a8-140">Funciones auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="d65a8-140">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="d65a8-141">Subrecursos</span><span class="sxs-lookup"><span data-stu-id="d65a8-141">Subresources</span></span>](subresources.md)
</dt> </dl>

 

