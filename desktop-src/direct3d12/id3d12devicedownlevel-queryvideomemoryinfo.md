---
title: 'ID3D12DeviceDownlevel:: QueryVideoMemoryInfo (método)'
description: 'Copia el contenido de un recurso de Texture2D de Direct3D 12 en una ventana. | ID3D12DeviceDownlevel:: QueryVideoMemoryInfo (método)'
keywords:
- Método QueryVideoMemoryInfo
- Método QueryVideoMemoryInfo, interfaz ID3D12DeviceDownlevel
- Interfaz ID3D12DeviceDownlevel, método QueryVideoMemoryInfo
topic_type:
- apiref
api_name:
- ID3D12DeviceDownlevel.QueryVideoMemoryInfo
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 32b93fcbbe44aaae0916e6d8f3f403eb960e26eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721487"
---
# <a name="id3d12devicedownlevelqueryvideomemoryinfo-method"></a><span data-ttu-id="e48f2-107">ID3D12DeviceDownlevel:: QueryVideoMemoryInfo (método)</span><span class="sxs-lookup"><span data-stu-id="e48f2-107">ID3D12DeviceDownlevel::QueryVideoMemoryInfo method</span></span>

<span data-ttu-id="e48f2-108">Proporciona estadísticas de memoria en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e48f2-108">Provides memory statistics on Windows 7.</span></span> <span data-ttu-id="e48f2-109">Este método es equivalente a [IDXGIAdapter3:: QueryVideoMemoryInfo](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo), que no está disponible en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e48f2-109">This method is equivalent to [IDXGIAdapter3::QueryVideoMemoryInfo](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo), which is not available on Windows 7.</span></span>

## <a name="syntax"></a><span data-ttu-id="e48f2-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e48f2-110">Syntax</span></span>

```cpp
HRESULT QueryVideoMemoryInfo( 
    UINT NodeIndex,
    DXGI_MEMORY_SEGMENT_GROUP MemorySegmentGroup,
    DXGI_QUERY_VIDEO_MEMORY_INFO *pVideoMemoryInfo
);
```

## <a name="parameters"></a><span data-ttu-id="e48f2-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e48f2-111">Parameters</span></span>

`NodeIndex`

<span data-ttu-id="e48f2-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="e48f2-112">Type: **UINT**</span></span>

<span data-ttu-id="e48f2-113">Especifica el adaptador físico del dispositivo para el que se consulta la información de memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e48f2-113">Specifies the device's physical adapter for which the video memory information is queried.</span></span> <span data-ttu-id="e48f2-114">Para la operación de una sola GPU, establezca este valor en cero.</span><span class="sxs-lookup"><span data-stu-id="e48f2-114">For single-GPU operation, set this to zero.</span></span> <span data-ttu-id="e48f2-115">Si hay varios nodos de GPU, establézcalo en el índice del nodo (el adaptador físico del dispositivo) para el que se consulta la información de la memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e48f2-115">If there are multiple GPU nodes, set this to the index of the node (the device's physical adapter) for which the video memory information is queried.</span></span> <span data-ttu-id="e48f2-116">Consulte [sistemas de varios adaptadores](multi-engine.md).</span><span class="sxs-lookup"><span data-stu-id="e48f2-116">See [Multi-adapter systems](multi-engine.md).</span></span>

`MemorySegmentGroup`

<span data-ttu-id="e48f2-117">Tipo: **[DXGI_MEMORY_SEGMENT_GROUP](/windows/win32/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)**</span><span class="sxs-lookup"><span data-stu-id="e48f2-117">Type: **[DXGI_MEMORY_SEGMENT_GROUP](/windows/win32/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)**</span></span>

<span data-ttu-id="e48f2-118">Especifica un **DXGI_MEMORY_SEGMENT_GROUP** que identifica el grupo como local o no local.</span><span class="sxs-lookup"><span data-stu-id="e48f2-118">Specifies a **DXGI_MEMORY_SEGMENT_GROUP** that identifies the group as local or non-local.</span></span>

`pVideoMemoryInfo`

<span data-ttu-id="e48f2-119">Tipo: **[DXGI_QUERY_VIDEO_MEMORY_INFO](/windows/win32/api/dxgi1_4/ns-dxgi1_4-dxgi_query_video_memory_info)\***</span><span class="sxs-lookup"><span data-stu-id="e48f2-119">Type: **[DXGI_QUERY_VIDEO_MEMORY_INFO](/windows/win32/api/dxgi1_4/ns-dxgi1_4-dxgi_query_video_memory_info)\***</span></span>

<span data-ttu-id="e48f2-120">Rellena una estructura de **DXGI_QUERY_VIDEO_MEMORY_INFO** con los valores actuales.</span><span class="sxs-lookup"><span data-stu-id="e48f2-120">Fills in a **DXGI_QUERY_VIDEO_MEMORY_INFO** structure with the current values.</span></span>

## <a name="return-value"></a><span data-ttu-id="e48f2-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e48f2-121">Return value</span></span>

<span data-ttu-id="e48f2-122">Devuelve **S_OK** si se ejecuta correctamente o, de lo contrario, un HRESULT con error.</span><span class="sxs-lookup"><span data-stu-id="e48f2-122">Returns **S_OK** on success, or else a failing HRESULT.</span></span>

## <a name="requirements"></a><span data-ttu-id="e48f2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e48f2-123">Requirements</span></span>

| <span data-ttu-id="e48f2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e48f2-124">Requirement</span></span> | <span data-ttu-id="e48f2-125">Value</span><span class="sxs-lookup"><span data-stu-id="e48f2-125">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="e48f2-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e48f2-126">Header</span></span> | <span data-ttu-id="e48f2-127">d3d12downlevel. h y dxgi1_4. h</span><span class="sxs-lookup"><span data-stu-id="e48f2-127">d3d12downlevel.h and dxgi1_4.h</span></span> |
| <span data-ttu-id="e48f2-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e48f2-128">DLL</span></span>    | <span data-ttu-id="e48f2-129">D3D12.dll (solo Windows 7)</span><span class="sxs-lookup"><span data-stu-id="e48f2-129">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="e48f2-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="e48f2-130">See also</span></span>
* [<span data-ttu-id="e48f2-131">ID3D12DeviceDownlevel</span><span class="sxs-lookup"><span data-stu-id="e48f2-131">ID3D12DeviceDownlevel</span></span>](id3d12devicedownlevel.md)
* [<span data-ttu-id="e48f2-132">Direct3D 12 en interfaces de Windows 7</span><span class="sxs-lookup"><span data-stu-id="e48f2-132">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="e48f2-133">Referencia de Direct3D 12 en Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="e48f2-133">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="e48f2-134">Direct3D 12 en Windows 7</span><span class="sxs-lookup"><span data-stu-id="e48f2-134">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
