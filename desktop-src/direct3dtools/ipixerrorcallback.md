---
description: Devolución de llamada del motor para controlar errores.
MS-HAID: vspixengine.IPixErrorCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz IPixErrorCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2FEAB4CF-80C8-4A3F-9D62-DFBAB34DE8C8
api_name:
- IPixErrorCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: df9e34f83f3cdd4c8c36024cf0d4ed042da0070f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422823"
---
# <a name="span-idvspixengineipixerrorcallbackspanipixerrorcallback-interface"></a><span data-ttu-id="86c99-103"><span id="vspixengine.ipixerrorcallback"></span>Interfaz IPixErrorCallback</span><span class="sxs-lookup"><span data-stu-id="86c99-103"><span id="vspixengine.ipixerrorcallback"></span>IPixErrorCallback interface</span></span>

<span data-ttu-id="86c99-104">Devolución de llamada del motor para controlar errores.</span><span class="sxs-lookup"><span data-stu-id="86c99-104">Callback from engine to handle errors.</span></span>

## <a name="members"></a><span data-ttu-id="86c99-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="86c99-105">Members</span></span>

<span data-ttu-id="86c99-106">La interfaz **IPixErrorCallback** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="86c99-106">The **IPixErrorCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="86c99-107">**IPixErrorCallback** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="86c99-107">**IPixErrorCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="86c99-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="86c99-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="86c99-109"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="86c99-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="86c99-110">La interfaz **IPixErrorCallback** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="86c99-110">The **IPixErrorCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="86c99-111">Método</span><span class="sxs-lookup"><span data-stu-id="86c99-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="86c99-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="86c99-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="86c99-113"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-errorlistcallback-dword-issue-arr-dword-issue-arr"><strong>ErrorListCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="86c99-113"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-errorlistcallback-dword-issue-arr-dword-issue-arr"><strong>ErrorListCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="86c99-114">Devolución de llamada que notifica al host de errores devueltos por la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="86c99-114">A callback that notifies the host of errors returned by the associated request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="86c99-115"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-messagescallback-dword-issue-arr"><strong>MessagesCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="86c99-115"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-messagescallback-dword-issue-arr"><strong>MessagesCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="86c99-116">Devolución de llamada que notifica al host de los mensajes devueltos por la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="86c99-116">A callback that notifies the host of messages returned by the associated request.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="86c99-117"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-warninglistcallback"><strong>WarningListCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="86c99-117"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-warninglistcallback"><strong>WarningListCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="86c99-118">Devolución de llamada que notifica al host de las advertencias devueltas por la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="86c99-118">A callback that notifies the host of warnings returned by the associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="86c99-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86c99-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="86c99-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86c99-120">Header</span></span></p></td><td><span data-ttu-id="86c99-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="86c99-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
