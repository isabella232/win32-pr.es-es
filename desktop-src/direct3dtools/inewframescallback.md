---
description: Devolución de llamada desde el motor que indica que se ha terminado de analizar los nuevos marcos agregados al registro.
MS-HAID: vspixengine.INewFramesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz INewFramesCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A73E1EA4-F9D5-43F1-B363-20B3F7B3D8B0
api_name:
- INewFramesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 134de14d95ceb625f1c5d4461c0b379b7f9e8a0a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423135"
---
# <a name="span-idvspixengineinewframescallbackspaninewframescallback-interface"></a><span data-ttu-id="35873-103"><span id="vspixengine.inewframescallback"></span>Interfaz INewFramesCallback</span><span class="sxs-lookup"><span data-stu-id="35873-103"><span id="vspixengine.inewframescallback"></span>INewFramesCallback interface</span></span>

<span data-ttu-id="35873-104">Devolución de llamada desde el motor que indica que se ha terminado de analizar los nuevos marcos agregados al registro.</span><span class="sxs-lookup"><span data-stu-id="35873-104">Callback from engine indicating that it is done parsing any new frames added to the log.</span></span>

## <a name="members"></a><span data-ttu-id="35873-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="35873-105">Members</span></span>

<span data-ttu-id="35873-106">La interfaz **INewFramesCallback** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="35873-106">The **INewFramesCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="35873-107">**INewFramesCallback** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="35873-107">**INewFramesCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="35873-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="35873-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="35873-109"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="35873-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="35873-110">La interfaz **INewFramesCallback** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="35873-110">The **INewFramesCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="35873-111">Método</span><span class="sxs-lookup"><span data-stu-id="35873-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="35873-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="35873-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="35873-113"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelall"><strong>CancelAll</strong></a></span><span class="sxs-lookup"><span data-stu-id="35873-113"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelall"><strong>CancelAll</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="35873-114">Devolución de llamada que notifica al host que se han cancelado todas las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="35873-114">A callback that notifies the host that all requests have been cancelled.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="35873-115"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcallback-iunknown-ptr"><strong>CancelUsingCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="35873-115"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcallback-iunknown-ptr"><strong>CancelUsingCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="35873-116">Devolución de llamada que notifica al host de una solicitud cancelada.</span><span class="sxs-lookup"><span data-stu-id="35873-116">A callback that notifies the host of a canceled request.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="35873-117"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcookie-dword"><strong>CancelUsingCookie</strong></a></span><span class="sxs-lookup"><span data-stu-id="35873-117"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcookie-dword"><strong>CancelUsingCookie</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="35873-118">Devolución de llamada que notifica al host de una solicitud cancelada mediante una cookie que identifica de forma única la solicitud.</span><span class="sxs-lookup"><span data-stu-id="35873-118">A callback that notifies the host of a canceled request by using a cookie that uniquely identifies the request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="35873-119"><a href="/windows/desktop/direct3dtools/inewframescallback-newframesavailable"><strong>NewFramesAvailable</strong></a></span><span class="sxs-lookup"><span data-stu-id="35873-119"><a href="/windows/desktop/direct3dtools/inewframescallback-newframesavailable"><strong>NewFramesAvailable</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="35873-120">Devolución de llamada que notifica al host que hay nuevos marcos disponibles para su procesamiento.</span><span class="sxs-lookup"><span data-stu-id="35873-120">A callback that notifies the host that new frames are available to be processed.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="35873-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35873-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="35873-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35873-122">Header</span></span></p></td><td><span data-ttu-id="35873-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="35873-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
