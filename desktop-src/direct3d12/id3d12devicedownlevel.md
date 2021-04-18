---
title: Interfaz ID3D12DeviceDownlevel
description: Proporciona una consulta de estadísticas de memoria específica de Windows-7.
keywords:
- Interfaz ID3D12DeviceDownlevel
topic_type:
- apiref
api_name:
- ID3D12DeviceDownlevel
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 401cbd0045211ef51e3ef6b06042262964ae2ec5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721433"
---
# <a name="id3d12devicedownlevel-interface"></a><span data-ttu-id="6da9d-104">Interfaz ID3D12DeviceDownlevel</span><span class="sxs-lookup"><span data-stu-id="6da9d-104">ID3D12DeviceDownlevel interface</span></span>

<span data-ttu-id="6da9d-105">Se puede tener acceso a esta interfaz a través de **QueryInterface** fuera de un [dispositivo de Direct3D 12](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) cuando se usa [Direct3D 12 en Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/).</span><span class="sxs-lookup"><span data-stu-id="6da9d-105">This interface can be accessed via **QueryInterface** off of a [Direct3D 12 device](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) when using [Direct3D 12 on Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/).</span></span> <span data-ttu-id="6da9d-106">Proporciona una consulta de estadísticas de memoria específica de Windows-7.</span><span class="sxs-lookup"><span data-stu-id="6da9d-106">It provides a Windows-7-specific memory statistics query.</span></span>

### <a name="methods"></a><span data-ttu-id="6da9d-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="6da9d-107">Methods</span></span>

<span data-ttu-id="6da9d-108">La interfaz **ID3D12DeviceDownlevel** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6da9d-108">The **ID3D12DeviceDownlevel** interface has these methods.</span></span>

| <span data-ttu-id="6da9d-109">Método</span><span class="sxs-lookup"><span data-stu-id="6da9d-109">Method</span></span> | <span data-ttu-id="6da9d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6da9d-110">Description</span></span> |
|:-------|:------------|
| [<span data-ttu-id="6da9d-111">**QueryVideoMemoryInfo**</span><span class="sxs-lookup"><span data-stu-id="6da9d-111">**QueryVideoMemoryInfo**</span></span>](id3d12devicedownlevel-queryvideomemoryinfo.md) | <span data-ttu-id="6da9d-112">Proporciona estadísticas de memoria en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6da9d-112">Provides memory statistics on Windows 7.</span></span> |

## <a name="requirements"></a><span data-ttu-id="6da9d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6da9d-113">Requirements</span></span>

| <span data-ttu-id="6da9d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6da9d-114">Requirement</span></span> | <span data-ttu-id="6da9d-115">Value</span><span class="sxs-lookup"><span data-stu-id="6da9d-115">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="6da9d-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6da9d-116">Header</span></span> | <span data-ttu-id="6da9d-117">d3d12downlevel. h</span><span class="sxs-lookup"><span data-stu-id="6da9d-117">d3d12downlevel.h</span></span> |
| <span data-ttu-id="6da9d-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6da9d-118">DLL</span></span>    | <span data-ttu-id="6da9d-119">D3D12.dll (solo Windows 7)</span><span class="sxs-lookup"><span data-stu-id="6da9d-119">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="6da9d-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="6da9d-120">See also</span></span>
* [<span data-ttu-id="6da9d-121">Direct3D 12 en interfaces de Windows 7</span><span class="sxs-lookup"><span data-stu-id="6da9d-121">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="6da9d-122">Referencia de Direct3D 12 en Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="6da9d-122">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="6da9d-123">Direct3D 12 en Windows 7</span><span class="sxs-lookup"><span data-stu-id="6da9d-123">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
