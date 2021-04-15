---
description: Devolución de llamada para devolver un destino de representación. El formato del destino de representación devuelto es R8G8B8A8 \_ UNORM, independientemente del formato de rendertarget en el motor.
MS-HAID: vspixengine.IFrameBufferCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz IFrameBufferCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 613AD7AC-0732-49E2-8155-AE0A76597BE9
api_name:
- IFrameBufferCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 565813999cda898f693aab37b24f7979896a8497
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422932"
---
# <a name="span-idvspixengineiframebuffercallbackspaniframebuffercallback-interface"></a><span data-ttu-id="73430-104"><span id="vspixengine.iframebuffercallback"></span>Interfaz IFrameBufferCallback</span><span class="sxs-lookup"><span data-stu-id="73430-104"><span id="vspixengine.iframebuffercallback"></span>IFrameBufferCallback interface</span></span>

<span data-ttu-id="73430-105">Devolución de llamada para devolver un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="73430-105">Callback to return a render target.</span></span> <span data-ttu-id="73430-106">El formato del destino de representación devuelto es R8G8B8A8 \_ UNORM, independientemente del formato de rendertarget en el motor.</span><span class="sxs-lookup"><span data-stu-id="73430-106">The format of the returned render target is R8G8B8A8\_UNORM regardless of the format of the in-engine rendertarget.</span></span>

## <a name="members"></a><span data-ttu-id="73430-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="73430-107">Members</span></span>

<span data-ttu-id="73430-108">La interfaz **IFrameBufferCallback** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="73430-108">The **IFrameBufferCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="73430-109">**IFrameBufferCallback** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="73430-109">**IFrameBufferCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="73430-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="73430-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="73430-111"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="73430-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="73430-112">La interfaz **IFrameBufferCallback** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="73430-112">The **IFrameBufferCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="73430-113">Método</span><span class="sxs-lookup"><span data-stu-id="73430-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="73430-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="73430-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="73430-115"><a href="/windows/desktop/direct3dtools/iframebuffercallback-resultcallback-dword-dword-dword-dword-double-dword-byte-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="73430-115"><a href="/windows/desktop/direct3dtools/iframebuffercallback-resultcallback-dword-dword-dword-dword-double-dword-byte-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="73430-116">Devolución de llamada que notifica al host la información de fotogramas devuelta por la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="73430-116">A callback that notifies the host of framebuffer information returned by the associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="73430-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73430-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="73430-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73430-118">Header</span></span></p></td><td><span data-ttu-id="73430-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="73430-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
