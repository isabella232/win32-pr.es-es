---
description: Devolución de llamada para devolver la lista de fotogramas con el identificador de evento y el número de marco.
MS-HAID: vspixengine.IFrameListCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz IFrameListCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 16318DBE-4126-4331-B726-DCF929F712DA
api_name:
- IFrameListCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a4fe281584a9ca51d18eee22f7e9fd4a92e48f88
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423140"
---
# <a name="span-idvspixengineiframelistcallbackspaniframelistcallback-interface"></a><span data-ttu-id="e6406-103"><span id="vspixengine.iframelistcallback"></span>Interfaz IFrameListCallback</span><span class="sxs-lookup"><span data-stu-id="e6406-103"><span id="vspixengine.iframelistcallback"></span>IFrameListCallback interface</span></span>

<span data-ttu-id="e6406-104">Devolución de llamada para devolver la lista de fotogramas con el identificador de evento y el número de marco.</span><span class="sxs-lookup"><span data-stu-id="e6406-104">Callback to return the list of frames with their event id and frame number.</span></span>

## <a name="members"></a><span data-ttu-id="e6406-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="e6406-105">Members</span></span>

<span data-ttu-id="e6406-106">La interfaz **IFrameListCallback** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e6406-106">The **IFrameListCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e6406-107">**IFrameListCallback** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e6406-107">**IFrameListCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="e6406-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="e6406-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="e6406-109"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="e6406-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="e6406-110">La interfaz **IFrameListCallback** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="e6406-110">The **IFrameListCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="e6406-111">Método</span><span class="sxs-lookup"><span data-stu-id="e6406-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="e6406-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6406-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="e6406-113"><a href="/windows/desktop/direct3dtools/iframelistcallback-resultcallback-dword-dword-arr-dword-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6406-113"><a href="/windows/desktop/direct3dtools/iframelistcallback-resultcallback-dword-dword-arr-dword-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="e6406-114">Función de devolución de llamada que se usa para notificar al host qué fotogramas se han capturado.</span><span class="sxs-lookup"><span data-stu-id="e6406-114">A callback function used to notify the host of which frames were captured.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="e6406-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6406-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e6406-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6406-116">Header</span></span></p></td><td><span data-ttu-id="e6406-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e6406-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
