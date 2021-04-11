---
description: Solicitud de datos de pila de llamadas.
MS-HAID: vspixengine.ICallStackRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz ICallStackRequest
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 08976720-C403-4609-BDB4-6250CA6EBC9C
api_name:
- ICallStackRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bbbcd1a7874cbab5c9914eee36a37b991c7f6b06
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152380"
---
# <a name="span-idvspixengineicallstackrequestspanicallstackrequest-interface"></a><span data-ttu-id="cd2b8-103"><span id="vspixengine.icallstackrequest"></span>Interfaz ICallStackRequest</span><span class="sxs-lookup"><span data-stu-id="cd2b8-103"><span id="vspixengine.icallstackrequest"></span>ICallStackRequest interface</span></span>

<span data-ttu-id="cd2b8-104">Solicitud de datos de pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="cd2b8-104">Request for callstack data.</span></span>

## <a name="members"></a><span data-ttu-id="cd2b8-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="cd2b8-105">Members</span></span>

<span data-ttu-id="cd2b8-106">La interfaz **ICallStackRequest** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="cd2b8-106">The **ICallStackRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cd2b8-107">**ICallStackRequest** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cd2b8-107">**ICallStackRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="cd2b8-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="cd2b8-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="cd2b8-109"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="cd2b8-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="cd2b8-110">La interfaz **ICallStackRequest** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="cd2b8-110">The **ICallStackRequest** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="cd2b8-111">Método</span><span class="sxs-lookup"><span data-stu-id="cd2b8-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="cd2b8-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd2b8-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="cd2b8-113"><a href="/windows/desktop/direct3dtools/icallstackrequest-requestasync-eventid-icallstackcallback-ptr-dword-dword"><strong>RequestAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="cd2b8-113"><a href="/windows/desktop/direct3dtools/icallstackrequest-requestasync-eventid-icallstackcallback-ptr-dword-dword"><strong>RequestAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="cd2b8-114">Una solicitud asincrónica para obtener las RVA de la pila de llamadas (direcciones virtuales relativas) del evento especificado.</span><span class="sxs-lookup"><span data-stu-id="cd2b8-114">An asynchronous request to get the call stack RVAs (relative virtual addresses) of the specified event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="cd2b8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd2b8-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="cd2b8-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd2b8-116">Header</span></span></p></td><td><span data-ttu-id="cd2b8-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="cd2b8-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
