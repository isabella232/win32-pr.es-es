---
description: Interfaz para la comunicación remota de datos sobre un vsglog.
MS-HAID: vspixengine.IPeerToPeerEngine
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz IPeerToPeerEngine
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C6C4783F-ED46-47C2-98BB-C618897F8FF8
api_name:
- IPeerToPeerEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 899e5eea28ffb769e082b2e0bd7bc165889b2d37
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705224"
---
# <a name="span-idvspixengineipeertopeerenginespanipeertopeerengine-interface"></a><span data-ttu-id="229be-103"><span id="vspixengine.ipeertopeerengine"></span>Interfaz IPeerToPeerEngine</span><span class="sxs-lookup"><span data-stu-id="229be-103"><span id="vspixengine.ipeertopeerengine"></span>IPeerToPeerEngine interface</span></span>

<span data-ttu-id="229be-104">Interfaz para la comunicación remota de datos sobre un vsglog.</span><span class="sxs-lookup"><span data-stu-id="229be-104">Interface for remote communicating data about a vsglog.</span></span>

## <a name="members"></a><span data-ttu-id="229be-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="229be-105">Members</span></span>

<span data-ttu-id="229be-106">La interfaz **IPeerToPeerEngine** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="229be-106">The **IPeerToPeerEngine** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="229be-107">**IPeerToPeerEngine** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="229be-107">**IPeerToPeerEngine** also has these types of members:</span></span>

-   [<span data-ttu-id="229be-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="229be-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="229be-109"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="229be-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="229be-110">La interfaz **IPeerToPeerEngine** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="229be-110">The **IPeerToPeerEngine** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="229be-111">Método</span><span class="sxs-lookup"><span data-stu-id="229be-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="229be-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="229be-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="229be-113"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-cancelsetplaybackendpoint"><strong>CancelSetPlaybackEndpoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="229be-113"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-cancelsetplaybackendpoint"><strong>CancelSetPlaybackEndpoint</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="229be-114">Cancela una solicitud anterior para configurar una conexión remota.</span><span class="sxs-lookup"><span data-stu-id="229be-114">Cancels a previous request to set up a remote connection.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="229be-115"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-getplaybackendpoint-bool-bstr-ptr-bstr-ptr-remotingversion-ptr"><strong>GetPlaybackEndpoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="229be-115"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-getplaybackendpoint-bool-bstr-ptr-bstr-ptr-remotingversion-ptr"><strong>GetPlaybackEndpoint</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="229be-116">Obtiene la dirección del extremo de un motor remoto.</span><span class="sxs-lookup"><span data-stu-id="229be-116">Gets the endpoint address of a remote engine.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="229be-117"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-setplaybackendpoint-bool-bstr-bstr-remotingversion"><strong>SetPlaybackEndpoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="229be-117"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-setplaybackendpoint-bool-bstr-bstr-remotingversion"><strong>SetPlaybackEndpoint</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="229be-118">Establece la dirección del extremo utilizada para conectarse a un motor remoto.</span><span class="sxs-lookup"><span data-stu-id="229be-118">Sets the endpoint address used to connect to a remote engine.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="229be-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="229be-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="229be-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="229be-120">Header</span></span></p></td><td><span data-ttu-id="229be-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="229be-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
