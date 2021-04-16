---
description: Las \_ constantes de marcador de bits LINECALLCOMPLMODE describen diferentes maneras en las que se puede completar una llamada.
ms.assetid: 68f755a1-586b-4c5b-b8e8-c8b40eb71685
title: Constantes de LINECALLCOMPLMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 373a66b6ce13b7bfba00303bea824f542bf0016a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690306"
---
# <a name="linecallcomplmode_-constants"></a><span data-ttu-id="5b9ee-103">Constantes de LINECALLCOMPLMODE \_</span><span class="sxs-lookup"><span data-stu-id="5b9ee-103">LINECALLCOMPLMODE\_ Constants</span></span>

<span data-ttu-id="5b9ee-104">Las constantes de marcador de bits **LINECALLCOMPLMODE \_** describen diferentes maneras en las que se puede completar una llamada.</span><span class="sxs-lookup"><span data-stu-id="5b9ee-104">The **LINECALLCOMPLMODE\_** bit-flag constants describe different ways in which a call can be completed.</span></span>

<dl> <dt>

<span data-ttu-id="5b9ee-105"><span id="LINECALLCOMPLMODE_CALLBACK"></span><span id="linecallcomplmode_callback"></span>**\_devolución de llamada LINECALLCOMPLMODE**</span><span class="sxs-lookup"><span data-stu-id="5b9ee-105"><span id="LINECALLCOMPLMODE_CALLBACK"></span><span id="linecallcomplmode_callback"></span>**LINECALLCOMPLMODE\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5b9ee-106">Solicita a la estación llamada que devuelva la llamada cuando vuelva a estar inactiva.</span><span class="sxs-lookup"><span data-stu-id="5b9ee-106">Requests the called station to return the call when it returns to idle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b9ee-107"><span id="LINECALLCOMPLMODE_CAMPON"></span><span id="linecallcomplmode_campon"></span>**LINECALLCOMPLMODE \_ campoN**</span><span class="sxs-lookup"><span data-stu-id="5b9ee-107"><span id="LINECALLCOMPLMODE_CAMPON"></span><span id="linecallcomplmode_campon"></span>**LINECALLCOMPLMODE\_CAMPON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5b9ee-108">Pone en cola la llamada hasta que se puede completar la llamada.</span><span class="sxs-lookup"><span data-stu-id="5b9ee-108">Queues the call until the call can be completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b9ee-109"><span id="LINECALLCOMPLMODE_INTRUDE"></span><span id="linecallcomplmode_intrude"></span>**LINECALLCOMPLMODE \_ intrusión**</span><span class="sxs-lookup"><span data-stu-id="5b9ee-109"><span id="LINECALLCOMPLMODE_INTRUDE"></span><span id="linecallcomplmode_intrude"></span>**LINECALLCOMPLMODE\_INTRUDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5b9ee-110">Agrega la aplicación a la llamada existente en la estación llamada (Barge en).</span><span class="sxs-lookup"><span data-stu-id="5b9ee-110">Adds the application to the existing call at the called station (barge in).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b9ee-111"><span id="LINECALLCOMPLMODE_MESSAGE"></span><span id="linecallcomplmode_message"></span>**\_mensaje LINECALLCOMPLMODE**</span><span class="sxs-lookup"><span data-stu-id="5b9ee-111"><span id="LINECALLCOMPLMODE_MESSAGE"></span><span id="linecallcomplmode_message"></span>**LINECALLCOMPLMODE\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5b9ee-112">Deja un breve mensaje predefinido para la estación llamada (deje la llamada de Word).</span><span class="sxs-lookup"><span data-stu-id="5b9ee-112">Leaves a short predefined message for the called station (Leave Word Calling).</span></span> <span data-ttu-id="5b9ee-113">El mensaje que se va a enviar se especifica por separado.</span><span class="sxs-lookup"><span data-stu-id="5b9ee-113">The message to be sent is specified separately.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b9ee-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b9ee-114">Remarks</span></span>

<span data-ttu-id="5b9ee-115">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="5b9ee-115">No extensibility.</span></span> <span data-ttu-id="5b9ee-116">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="5b9ee-116">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b9ee-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b9ee-117">Requirements</span></span>



| <span data-ttu-id="5b9ee-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b9ee-118">Requirement</span></span> | <span data-ttu-id="5b9ee-119">Value</span><span class="sxs-lookup"><span data-stu-id="5b9ee-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5b9ee-120">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="5b9ee-120">TAPI version</span></span><br/> | <span data-ttu-id="5b9ee-121">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="5b9ee-121">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="5b9ee-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b9ee-122">Header</span></span><br/>       | <dl> <span data-ttu-id="5b9ee-123"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b9ee-123"><dt>Tapi.h</dt></span></span> </dl> |



 

 




