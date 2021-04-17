---
description: Las \_ constantes de marcador de bits LINECALLPRIVILEGE describen los tipos de derechos de acceso o los privilegios que una aplicación con un identificador de llamada puede tener en la llamada correspondiente.
ms.assetid: a58b7e9e-696e-4421-9b31-1ba8afe6e03b
title: Constantes de LINECALLPRIVILEGE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2569ec255d2da3ad384292eb87afaa285f54b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681089"
---
# <a name="linecallprivilege_-constants"></a><span data-ttu-id="69337-103">Constantes de LINECALLPRIVILEGE \_</span><span class="sxs-lookup"><span data-stu-id="69337-103">LINECALLPRIVILEGE\_ Constants</span></span>

<span data-ttu-id="69337-104">Las constantes de marcador de bits **LINECALLPRIVILEGE \_** describen los tipos de derechos de acceso o los privilegios que una aplicación con un identificador de llamada puede tener en la llamada correspondiente.</span><span class="sxs-lookup"><span data-stu-id="69337-104">The **LINECALLPRIVILEGE\_** bit-flag constants describe the kinds of access rights or privileges an application with a call handle may have to the corresponding call.</span></span>

<dl> <dt>

<span data-ttu-id="69337-105"><span id="LINECALLPRIVILEGE_MONITOR"></span><span id="linecallprivilege_monitor"></span>**MONITOR de LINECALLPRIVILEGE \_**</span><span class="sxs-lookup"><span data-stu-id="69337-105"><span id="LINECALLPRIVILEGE_MONITOR"></span><span id="linecallprivilege_monitor"></span>**LINECALLPRIVILEGE\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="69337-106">La aplicación tiene privilegios de supervisión para la llamada.</span><span class="sxs-lookup"><span data-stu-id="69337-106">The application has monitor privileges to the call.</span></span> <span data-ttu-id="69337-107">Estos privilegios permiten a la aplicación supervisar los cambios de estado y la información de consulta y el estado de la llamada.</span><span class="sxs-lookup"><span data-stu-id="69337-107">These privileges allow the application to monitor state changes and query information and status about the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69337-108"><span id="LINECALLPRIVILEGE_NONE"></span><span id="linecallprivilege_none"></span>**LINECALLPRIVILEGE \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="69337-108"><span id="LINECALLPRIVILEGE_NONE"></span><span id="linecallprivilege_none"></span>**LINECALLPRIVILEGE\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="69337-109">La aplicación no tiene privilegios para la llamada.</span><span class="sxs-lookup"><span data-stu-id="69337-109">The application has no privileges to the call.</span></span> <span data-ttu-id="69337-110">El identificador de la aplicación es nulo y no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="69337-110">The application's handle is void and should not be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69337-111"><span id="LINECALLPRIVILEGE_OWNER"></span><span id="linecallprivilege_owner"></span>**propietario de LINECALLPRIVILEGE \_**</span><span class="sxs-lookup"><span data-stu-id="69337-111"><span id="LINECALLPRIVILEGE_OWNER"></span><span id="linecallprivilege_owner"></span>**LINECALLPRIVILEGE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="69337-112">La aplicación tiene privilegios de propietario en la llamada.</span><span class="sxs-lookup"><span data-stu-id="69337-112">The application has owner privileges to the call.</span></span> <span data-ttu-id="69337-113">Estos privilegios permiten a la aplicación manipular la llamada de maneras que afectan al estado de la llamada.</span><span class="sxs-lookup"><span data-stu-id="69337-113">These privileges allow the application to manipulate the call in ways that affect the state of the call.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69337-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69337-114">Remarks</span></span>

<span data-ttu-id="69337-115">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="69337-115">No extensibility.</span></span> <span data-ttu-id="69337-116">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="69337-116">All 32 bits are reserved.</span></span>

<span data-ttu-id="69337-117">Cuando un identificador de llamada se proporciona por primera vez a una aplicación o cuando se modifican los privilegios de llamada de esa aplicación, el mensaje de [**línea \_ CALLSTATE**](line-callstate.md) se envía a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="69337-117">When a call handle is first provided to an application or whenever call privileges of that application are modified, the [**LINE\_CALLSTATE**](line-callstate.md) message is sent to the application.</span></span> <span data-ttu-id="69337-118">Cuando una aplicación hace una llamada a, y si la aplicación receptora todavía no tiene un identificador con privilegios de propietario, este mensaje informa a la aplicación sobre sus nuevos privilegios a la llamada.</span><span class="sxs-lookup"><span data-stu-id="69337-118">When an application hands off a call, and if the receiving application does not already have a handle with owner privileges, then this message informs the application about its new privileges to the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="69337-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69337-119">Requirements</span></span>



| <span data-ttu-id="69337-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="69337-120">Requirement</span></span> | <span data-ttu-id="69337-121">Value</span><span class="sxs-lookup"><span data-stu-id="69337-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="69337-122">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="69337-122">TAPI version</span></span><br/> | <span data-ttu-id="69337-123">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="69337-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="69337-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69337-124">Header</span></span><br/>       | <dl> <span data-ttu-id="69337-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="69337-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




