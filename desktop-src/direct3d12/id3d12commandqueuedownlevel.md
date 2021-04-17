---
title: Interfaz ID3D12CommandQueueDownlevel
description: Proporciona un mecanismo presente específico de Windows-7.
keywords:
- Interfaz ID3D12CommandQueueDownlevel
topic_type:
- apiref
api_name:
- ID3D12CommandQueueDownlevel
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 6f2aee6fd1b0f58469162c640d92aeb187bd9641
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721434"
---
# <a name="id3d12commandqueuedownlevel-interface"></a><span data-ttu-id="a8f26-104">Interfaz ID3D12CommandQueueDownlevel</span><span class="sxs-lookup"><span data-stu-id="a8f26-104">ID3D12CommandQueueDownlevel interface</span></span>

<span data-ttu-id="a8f26-105">Se puede tener acceso a esta interfaz a través de **QueryInterface** fuera de una [cola de comandos de Direct3D 12](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) al usar [Direct3D 12 en Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/).</span><span class="sxs-lookup"><span data-stu-id="a8f26-105">This interface can be accessed via **QueryInterface** off of a [Direct3D 12 command queue](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) when using [Direct3D 12 on Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/).</span></span> <span data-ttu-id="a8f26-106">Proporciona un mecanismo presente específico de Windows-7.</span><span class="sxs-lookup"><span data-stu-id="a8f26-106">It provides a Windows-7-specific present mechanism.</span></span>

### <a name="methods"></a><span data-ttu-id="a8f26-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="a8f26-107">Methods</span></span>

<span data-ttu-id="a8f26-108">La interfaz **ID3D12CommandQueueDownlevel** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a8f26-108">The **ID3D12CommandQueueDownlevel** interface has these methods.</span></span>

| <span data-ttu-id="a8f26-109">Método</span><span class="sxs-lookup"><span data-stu-id="a8f26-109">Method</span></span> | <span data-ttu-id="a8f26-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8f26-110">Description</span></span> |
|:-------|:------------|
| [<span data-ttu-id="a8f26-111">**Presente**</span><span class="sxs-lookup"><span data-stu-id="a8f26-111">**Present**</span></span>](id3d12commandqueuedownlevel-present.md) | <span data-ttu-id="a8f26-112">Copia el contenido de un recurso de D3D12 Texture2D en una ventana.</span><span class="sxs-lookup"><span data-stu-id="a8f26-112">Copies contents from a D3D12 Texture2D resource into a window.</span></span> |

## <a name="requirements"></a><span data-ttu-id="a8f26-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8f26-113">Requirements</span></span>

| <span data-ttu-id="a8f26-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8f26-114">Requirement</span></span> | <span data-ttu-id="a8f26-115">Value</span><span class="sxs-lookup"><span data-stu-id="a8f26-115">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="a8f26-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8f26-116">Header</span></span> | <span data-ttu-id="a8f26-117">d3d12downlevel. h</span><span class="sxs-lookup"><span data-stu-id="a8f26-117">d3d12downlevel.h</span></span> |
| <span data-ttu-id="a8f26-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a8f26-118">DLL</span></span>    | <span data-ttu-id="a8f26-119">D3D12.dll (solo Windows 7)</span><span class="sxs-lookup"><span data-stu-id="a8f26-119">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="a8f26-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8f26-120">See also</span></span>
* [<span data-ttu-id="a8f26-121">Direct3D 12 en interfaces de Windows 7</span><span class="sxs-lookup"><span data-stu-id="a8f26-121">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="a8f26-122">Referencia de Direct3D 12 en Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="a8f26-122">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="a8f26-123">Direct3D 12 en Windows 7</span><span class="sxs-lookup"><span data-stu-id="a8f26-123">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
