---
title: Interfaces de la capa de depuración
description: Las siguientes interfaces se declaran en d3d12sdklayers. h.
ms.assetid: 9BD5910A-8FF2-4540-BB8E-8EA5C10528CE
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e37dbe2e3348a500a8898d1e1076d2fafde66768
ms.sourcegitcommit: 0aa1dd7577961438a1b3172f3a92fb11cbf359f1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2020
ms.locfileid: "105651344"
---
# <a name="debug-layer-interfaces"></a><span data-ttu-id="2040c-103">Depurar interfaces de capa</span><span class="sxs-lookup"><span data-stu-id="2040c-103">Debug Layer interfaces</span></span>

<span data-ttu-id="2040c-104">Las siguientes interfaces se definen en `d3d12sdklayers.h` .</span><span class="sxs-lookup"><span data-stu-id="2040c-104">The following interfaces are defined in `d3d12sdklayers.h`.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2040c-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="2040c-105">In this section</span></span>

| <span data-ttu-id="2040c-106">Tema</span><span class="sxs-lookup"><span data-stu-id="2040c-106">Topic</span></span> | <span data-ttu-id="2040c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="2040c-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="2040c-108">**ID3D12Debug**</span><span class="sxs-lookup"><span data-stu-id="2040c-108">**ID3D12Debug**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug) | <span data-ttu-id="2040c-109">Una interfaz de depuración controla la configuración de depuración y valida el estado de la canalización.</span><span class="sxs-lookup"><span data-stu-id="2040c-109">A debug interface controls debug settings and validates pipeline state.</span></span> <span data-ttu-id="2040c-110">Solo se puede usar si la capa de depuración está activada.</span><span class="sxs-lookup"><span data-stu-id="2040c-110">It can only be used if the debug layer is turned on.</span></span> |
| [<span data-ttu-id="2040c-111">**ID3D12Debug1**</span><span class="sxs-lookup"><span data-stu-id="2040c-111">**ID3D12Debug1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1) | <span data-ttu-id="2040c-112">Agrega la validación basada en GPU y la sincronización de colas de comandos dependientes a la capa de depuración.</span><span class="sxs-lookup"><span data-stu-id="2040c-112">Adds GPU-based validation and Dependent Command Queue Synchronization to the debug layer.</span></span> |
| [<span data-ttu-id="2040c-113">**ID3D12Debug2**</span><span class="sxs-lookup"><span data-stu-id="2040c-113">**ID3D12Debug2**</span></span>](/windows/desktop/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2) | <span data-ttu-id="2040c-114">Agrega niveles configurables de la validación de GPU-Based.</span><span class="sxs-lookup"><span data-stu-id="2040c-114">Adds configurable levels of GPU-Based Validation.</span></span> |
| [<span data-ttu-id="2040c-115">**ID3D12Debug3**</span><span class="sxs-lookup"><span data-stu-id="2040c-115">**ID3D12Debug3**</span></span>](/windows/desktop/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug3) | <span data-ttu-id="2040c-116">Agrega a la validación basada en GPU de la capa de depuración, la sincronización de la cola de comandos dependiente y los niveles configurables de la validación basada en GPU.</span><span class="sxs-lookup"><span data-stu-id="2040c-116">Adds to the debug layer GPU-based validation, Dependent Command Queue Synchronization, and configurable levels of GPU-based validation.</span></span> |
| [<span data-ttu-id="2040c-117">**ID3D12DebugCommandList**</span><span class="sxs-lookup"><span data-stu-id="2040c-117">**ID3D12DebugCommandList**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist) | <span data-ttu-id="2040c-118">Proporciona métodos para supervisar y depurar una lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="2040c-118">Provides methods to monitor and debug a command list.</span></span> |
| [<span data-ttu-id="2040c-119">**ID3D12DebugCommandList1**</span><span class="sxs-lookup"><span data-stu-id="2040c-119">**ID3D12DebugCommandList1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1) | <span data-ttu-id="2040c-120">Esta interfaz permite modificar la configuración de la capa de depuración de la lista de comandos adicional.</span><span class="sxs-lookup"><span data-stu-id="2040c-120">This interface enables modification of additional command list debug layer settings.</span></span> |
| [<span data-ttu-id="2040c-121">**ID3D12DebugCommandQueue**</span><span class="sxs-lookup"><span data-stu-id="2040c-121">**ID3D12DebugCommandQueue**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandqueue) | <span data-ttu-id="2040c-122">Proporciona métodos para supervisar y depurar una cola de comandos.</span><span class="sxs-lookup"><span data-stu-id="2040c-122">Provides methods to monitor and debug a command queue.</span></span> |
| [<span data-ttu-id="2040c-123">**ID3D12DebugDevice**</span><span class="sxs-lookup"><span data-stu-id="2040c-123">**ID3D12DebugDevice**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice) | <span data-ttu-id="2040c-124">Esta interfaz representa un dispositivo de gráficos para la depuración.</span><span class="sxs-lookup"><span data-stu-id="2040c-124">This interface represents a graphics device for debugging.</span></span> |
| [<span data-ttu-id="2040c-125">**ID3D12DebugDevice1**</span><span class="sxs-lookup"><span data-stu-id="2040c-125">**ID3D12DebugDevice1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1) | <span data-ttu-id="2040c-126">Especifica la configuración del nivel de depuración para todo el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2040c-126">Specifies device-wide debug layer settings.</span></span> |
| [<span data-ttu-id="2040c-127">**ID3D12InfoQueue**</span><span class="sxs-lookup"><span data-stu-id="2040c-127">**ID3D12InfoQueue**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue) | <span data-ttu-id="2040c-128">Una interfaz de cola de información almacena, recupera y filtra los mensajes de depuración.</span><span class="sxs-lookup"><span data-stu-id="2040c-128">An information-queue interface stores, retrieves, and filters debug messages.</span></span> <span data-ttu-id="2040c-129">La cola está formada por una cola de mensajes, una pila de filtros de almacenamiento opcional y una pila de filtros de recuperación opcional.</span><span class="sxs-lookup"><span data-stu-id="2040c-129">The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.</span></span> |
| [<span data-ttu-id="2040c-130">**ID3D12SharingContract**</span><span class="sxs-lookup"><span data-stu-id="2040c-130">**ID3D12SharingContract**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12sharingcontract) | <span data-ttu-id="2040c-131">Parte de un contrato entre las capas de diagnóstico de D3D11On12 y las herramientas de diagnóstico de gráficos.</span><span class="sxs-lookup"><span data-stu-id="2040c-131">Part of a contract between D3D11On12 diagnostic layers and graphics diagnostics tools.</span></span> |

## <a name="related-topics"></a><span data-ttu-id="2040c-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2040c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2040c-133">Configuración del entorno de programación de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="2040c-133">Direct3D 12 Programming Environment Setup</span></span>](directx-12-programming-environment-set-up.md)
</dt> <dt>

[<span data-ttu-id="2040c-134">Referencia de la capa de depuración</span><span class="sxs-lookup"><span data-stu-id="2040c-134">Debug Layer Reference</span></span>](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[<span data-ttu-id="2040c-135">Referencia de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="2040c-135">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>