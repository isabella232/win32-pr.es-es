---
title: Enumeraciones de capas
description: Esta sección contiene información sobre las enumeraciones de capas.
ms.assetid: 0fd0456b-2638-4b4c-8a34-a3e104a1a034
keywords:
- enumeraciones, capa de Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e1cca3fa500a529930c8d0c39005697045d18b
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104984119"
---
# <a name="layer-enumerations"></a><span data-ttu-id="b3d90-104">Enumeraciones de capas</span><span class="sxs-lookup"><span data-stu-id="b3d90-104">Layer Enumerations</span></span>

<span data-ttu-id="b3d90-105">Esta sección contiene información sobre las enumeraciones de capas.</span><span class="sxs-lookup"><span data-stu-id="b3d90-105">This section contains information about the layer enumerations.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="b3d90-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b3d90-106">In this section</span></span>



| <span data-ttu-id="b3d90-107">Tema</span><span class="sxs-lookup"><span data-stu-id="b3d90-107">Topic</span></span>                                                                                             | <span data-ttu-id="b3d90-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3d90-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b3d90-109">**\_Categoría de mensaje D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="b3d90-109">**D3D11\_MESSAGE\_CATEGORY**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_category)<br/>                             | <span data-ttu-id="b3d90-110">Categorías de mensajes de depuración.</span><span class="sxs-lookup"><span data-stu-id="b3d90-110">Categories of debug messages.</span></span> <span data-ttu-id="b3d90-111">Esto identificará la categoría de un mensaje cuando se recupere un mensaje con [**ID3D11InfoQueue:: GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) y al agregar un mensaje con [**ID3D11InfoQueue:: AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage).</span><span class="sxs-lookup"><span data-stu-id="b3d90-111">This will identify the category of a message when retrieving a message with [**ID3D11InfoQueue::GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) and when adding a message with [**ID3D11InfoQueue::AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage).</span></span> <span data-ttu-id="b3d90-112">Al crear un [**filtro de cola de información**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter), estos valores se pueden usar para permitir o denegar que las categorías de mensajes pasen por los filtros de almacenamiento y recuperación.</span><span class="sxs-lookup"><span data-stu-id="b3d90-112">When creating an [**info queue filter**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter), these values can be used to allow or deny any categories of messages to pass through the storage and retrieval filters.</span></span><br/> |
| [<span data-ttu-id="b3d90-113">**\_Identificador de mensaje de D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="b3d90-113">**D3D11\_MESSAGE\_ID**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_id)<br/>                                         | <span data-ttu-id="b3d90-114">Depuración de mensajes para configurar un filtro de info-Queue (consulte [**D3D11 \_ info \_ Queue \_ Filter**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)); Utilice estos mensajes para permitir o denegar que las categorías de mensajes pasan a través de los filtros de almacenamiento y recuperación.</span><span class="sxs-lookup"><span data-stu-id="b3d90-114">Debug messages for setting up an info-queue filter (see [**D3D11\_INFO\_QUEUE\_FILTER**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)); use these messages to allow or deny message categories to pass through the storage and retrieval filters.</span></span> <span data-ttu-id="b3d90-115">Estos identificadores son usados por métodos como [**ID3D11InfoQueue:: GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) o [**ID3D11InfoQueue:: AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage).</span><span class="sxs-lookup"><span data-stu-id="b3d90-115">These IDs are used by methods such as [**ID3D11InfoQueue::GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) or [**ID3D11InfoQueue::AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage).</span></span> <br/>                                                             |
| [<span data-ttu-id="b3d90-116">**\_Gravedad del mensaje de D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="b3d90-116">**D3D11\_MESSAGE\_SEVERITY**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_severity)<br/>                             | <span data-ttu-id="b3d90-117">Depurar los niveles de gravedad del mensaje para una cola de información.</span><span class="sxs-lookup"><span data-stu-id="b3d90-117">Debug message severity levels for an information queue.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="b3d90-118">**D3D11 \_ marcas de RLDO \_**</span><span class="sxs-lookup"><span data-stu-id="b3d90-118">**D3D11\_RLDO\_FLAGS**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_rldo_flags)<br/>                                         | <span data-ttu-id="b3d90-119">Opciones para la cantidad de información que se va a notificar sobre la duración de un objeto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b3d90-119">Options for the amount of information to report about a device object's lifetime.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="b3d90-120">**\_Opciones de seguimiento del sombreador de D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b3d90-120">**D3D11\_SHADER\_TRACKING\_OPTIONS**</span></span>](/windows/win32/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_shader_tracking_options)<br/>              | <span data-ttu-id="b3d90-121">Opciones que especifican cómo realizar el seguimiento de depuración del sombreador.</span><span class="sxs-lookup"><span data-stu-id="b3d90-121">Options that specify how to perform shader debug tracking.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="b3d90-122">**\_Tipo de recurso de seguimiento del sombreador de D3D11 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b3d90-122">**D3D11\_SHADER\_TRACKING\_RESOURCE\_TYPE**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_shader_tracking_resource_type)<br/> | <span data-ttu-id="b3d90-123">Indica los tipos de recursos de los que se va a realizar un seguimiento.</span><span class="sxs-lookup"><span data-stu-id="b3d90-123">Indicates which resource types to track.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="b3d90-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b3d90-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3d90-125">Referencia de capas</span><span class="sxs-lookup"><span data-stu-id="b3d90-125">Layer Reference</span></span>](d3d11-graphics-reference-d3d11-layer.md)
</dt> </dl>

 

 





