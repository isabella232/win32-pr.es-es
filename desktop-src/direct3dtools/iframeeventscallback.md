---
description: Devolución de llamada para devolver la lista de eventos de un marco.
MS-HAID: vspixengine.IFrameEventsCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz IFrameEventsCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F40DD5DC-E78E-41F3-9D25-4D7CAE27DE45
api_name:
- IFrameEventsCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 98815681db182c99a86c05c1ea22eaad41526438
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714710"
---
# <a name="span-idvspixengineiframeeventscallbackspaniframeeventscallback-interface"></a><span data-ttu-id="f9c57-103"><span id="vspixengine.iframeeventscallback"></span>Interfaz IFrameEventsCallback</span><span class="sxs-lookup"><span data-stu-id="f9c57-103"><span id="vspixengine.iframeeventscallback"></span>IFrameEventsCallback interface</span></span>

<span data-ttu-id="f9c57-104">Devolución de llamada para devolver la lista de eventos de un marco.</span><span class="sxs-lookup"><span data-stu-id="f9c57-104">Callback to return the list of events in a frame.</span></span>

## <a name="members"></a><span data-ttu-id="f9c57-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="f9c57-105">Members</span></span>

<span data-ttu-id="f9c57-106">La interfaz **IFrameEventsCallback** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f9c57-106">The **IFrameEventsCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f9c57-107">**IFrameEventsCallback** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f9c57-107">**IFrameEventsCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="f9c57-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="f9c57-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="f9c57-109"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="f9c57-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="f9c57-110">La interfaz **IFrameEventsCallback** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="f9c57-110">The **IFrameEventsCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="f9c57-111">Método</span><span class="sxs-lookup"><span data-stu-id="f9c57-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="f9c57-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9c57-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="f9c57-113"><a href="/windows/desktop/direct3dtools/iframeeventscallback-getsupportedeventcolumns-dword-eventcolumnid-arr-bstr-arr"><strong>GetSupportedEventColumns</strong></a></span><span class="sxs-lookup"><span data-stu-id="f9c57-113"><a href="/windows/desktop/direct3dtools/iframeeventscallback-getsupportedeventcolumns-dword-eventcolumnid-arr-bstr-arr"><strong>GetSupportedEventColumns</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f9c57-114">Obtiene información sobre qué columnas (tipos de datos de eventos) se admiten en la lista de eventos.</span><span class="sxs-lookup"><span data-stu-id="f9c57-114">Gets information about which columns (types of event data) are supported by the event list.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="f9c57-115"><a href="/windows/desktop/direct3dtools/iframeeventscallback-resultcallback-dword-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="f9c57-115"><a href="/windows/desktop/direct3dtools/iframeeventscallback-resultcallback-dword-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f9c57-116">Función de devolución de llamada que se usa para notificar al host de información sobre eventos en la lista de eventos.</span><span class="sxs-lookup"><span data-stu-id="f9c57-116">A callback function used to notify the host of information about events in the event list.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="f9c57-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9c57-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f9c57-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9c57-118">Header</span></span></p></td><td><span data-ttu-id="f9c57-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f9c57-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
