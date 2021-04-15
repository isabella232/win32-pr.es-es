---
title: Estructuras de las capas de depuración
description: Las siguientes estructuras se declaran en d3d12sdklayers. h.
ms.assetid: FE8796A7-98D1-4333-8755-2A47567560B3
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 573d49d34c4432796ebac68ce004f265259b9eb2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714241"
---
# <a name="debug-layer-structures"></a><span data-ttu-id="8162e-103">Estructuras de las capas de depuración</span><span class="sxs-lookup"><span data-stu-id="8162e-103">Debug Layer Structures</span></span>

<span data-ttu-id="8162e-104">Las siguientes estructuras se declaran en d3d12sdklayers. h.</span><span class="sxs-lookup"><span data-stu-id="8162e-104">The following structures are declared in d3d12sdklayers.h.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8162e-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="8162e-105">In this section</span></span>



| <span data-ttu-id="8162e-106">Tema</span><span class="sxs-lookup"><span data-stu-id="8162e-106">Topic</span></span>                                                                                                                                      | <span data-ttu-id="8162e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="8162e-107">Description</span></span>                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8162e-108">**D3D12 \_ depurar \_ \_ \_ configuración de \_ validación basada en GPU \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8162e-108">**D3D12\_DEBUG\_COMMAND\_LIST\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_command_list_gpu_based_validation_settings)<br/> | <span data-ttu-id="8162e-109">Describe la configuración por lista de comandos utilizada por la validación de GPU-Based.</span><span class="sxs-lookup"><span data-stu-id="8162e-109">Describes per-command-list settings used by GPU-Based Validation.</span></span> <br/>                                                        |
| [<span data-ttu-id="8162e-110">**D3D12 \_ depurar \_ \_ \_ configuración de validación basada en GPU \_ del dispositivo \_**</span><span class="sxs-lookup"><span data-stu-id="8162e-110">**D3D12\_DEBUG\_DEVICE\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings)<br/>              | <span data-ttu-id="8162e-111">Describe la configuración usada por la validación de GPU-Based.</span><span class="sxs-lookup"><span data-stu-id="8162e-111">Describes settings used by GPU-Based Validation.</span></span> <br/>                                                                         |
| [<span data-ttu-id="8162e-112">**FACTOR de rendimiento de degradación del \_ dispositivo de depuración D3D12 \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8162e-112">**D3D12\_DEBUG\_DEVICE\_GPU\_SLOWDOWN\_PERFORMANCE\_FACTOR**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_slowdown_performance_factor)<br/>          | <span data-ttu-id="8162e-113">Describe la cantidad de ralentización artificial insertada por el dispositivo de depuración para simular adaptadores de gráficos de menor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="8162e-113">Describes the amount of artificial slowdown inserted by the debug device to simulate lower-performance graphics adapters.</span></span><br/> |
| [<span data-ttu-id="8162e-114">**\_Filtro de \_ cola de información de D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="8162e-114">**D3D12\_INFO\_QUEUE\_FILTER**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter)<br/>                                                                   | <span data-ttu-id="8162e-115">Filtro de mensajes de depuración; contiene una lista de tipos de mensaje que se va a permitir o denegar.</span><span class="sxs-lookup"><span data-stu-id="8162e-115">Debug message filter; contains a lists of message types to allow or deny.</span></span><br/>                                                 |
| [<span data-ttu-id="8162e-116">**D3D12 \_ info \_ cola \_ filtro \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="8162e-116">**D3D12\_INFO\_QUEUE\_FILTER\_DESC**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter_desc)<br/>                                                        | <span data-ttu-id="8162e-117">Permite o deniega determinados tipos de mensajes para pasar a través de un filtro.</span><span class="sxs-lookup"><span data-stu-id="8162e-117">Allow or deny certain types of messages to pass through a filter.</span></span><br/>                                                         |
| [<span data-ttu-id="8162e-118">**\_Mensaje D3D12**</span><span class="sxs-lookup"><span data-stu-id="8162e-118">**D3D12\_MESSAGE**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_message)<br/>                                                                                         | <span data-ttu-id="8162e-119">Un mensaje de depuración en la cola de información.</span><span class="sxs-lookup"><span data-stu-id="8162e-119">A debug message in the Information Queue.</span></span><br/>                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="8162e-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8162e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8162e-121">Configuración del entorno de programación de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="8162e-121">Direct3D 12 Programming Environment Setup</span></span>](directx-12-programming-environment-set-up.md)
</dt> <dt>

[<span data-ttu-id="8162e-122">Referencia de la capa de depuración</span><span class="sxs-lookup"><span data-stu-id="8162e-122">Debug Layer Reference</span></span>](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[<span data-ttu-id="8162e-123">Referencia de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="8162e-123">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





