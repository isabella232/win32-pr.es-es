---
description: Los siguientes términos son útiles para comprender la tecnología de TAPI.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 23331332-38bc-41b9-84c4-281722ddf563
title: C (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c6fade540235ef6c68b42a0aba364038d674e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677619"
---
# <a name="c-telephony-api"></a><span data-ttu-id="15fc3-103">C (API de telefonía)</span><span class="sxs-lookup"><span data-stu-id="15fc3-103">C (Telephony API)</span></span>

<span data-ttu-id="15fc3-104">[A](a-tapgloss.md) [B](b-tapgloss.md) C [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N o [p](p-tapgloss.md) Q [R](r-tapgloss.md) [s](s-tapgloss.md) [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="15fc3-104">[A](a-tapgloss.md) [B](b-tapgloss.md) C [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) [S](s-tapgloss.md) [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="15fc3-105"><span id="tapi2.call_classification_tapgloss"></span><span id="TAPI2.CALL_CLASSIFICATION_TAPGLOSS"></span>**clasificación de llamadas**</span><span class="sxs-lookup"><span data-stu-id="15fc3-105"><span id="tapi2.call_classification_tapgloss"></span><span id="TAPI2.CALL_CLASSIFICATION_TAPGLOSS"></span>**call classification**</span></span>
</dt> <dd>

<span data-ttu-id="15fc3-106">Proceso TAPI que informa de los cambios en el tipo de flujo multimedia (voz, fax, módem de datos, etc.) a las aplicaciones participantes.</span><span class="sxs-lookup"><span data-stu-id="15fc3-106">TAPI process that reports changes in the type of media stream (voice, fax, data modem, and so on) to participating applications.</span></span>

</dd> <dt>

<span data-ttu-id="15fc3-107"><span id="tapi2.call_progress_monitoring_tapgloss"></span><span id="TAPI2.CALL_PROGRESS_MONITORING_TAPGLOSS"></span>**supervisión del progreso de las llamadas**</span><span class="sxs-lookup"><span data-stu-id="15fc3-107"><span id="tapi2.call_progress_monitoring_tapgloss"></span><span id="TAPI2.CALL_PROGRESS_MONITORING_TAPGLOSS"></span>**call progress monitoring**</span></span>
</dt> <dd>

<span data-ttu-id="15fc3-108">Proceso de escucha de tonos auditivos como un tono de marcado, tonos de información especiales, señales ocupadas y tonos de timbre para determinar el estado de una llamada (su progreso a través de la red).</span><span class="sxs-lookup"><span data-stu-id="15fc3-108">The process of listening for audible tones such as a dial tone, special information tones, busy signals, and ringback tones to determine the state of a call (its progress through the network).</span></span>

</dd> <dt>

<span data-ttu-id="15fc3-109"><span id="tapi2.call_redirection_tapgloss"></span><span id="TAPI2.CALL_REDIRECTION_TAPGLOSS"></span>**redirección de llamadas**</span><span class="sxs-lookup"><span data-stu-id="15fc3-109"><span id="tapi2.call_redirection_tapgloss"></span><span id="TAPI2.CALL_REDIRECTION_TAPGLOSS"></span>**call redirection**</span></span>
</dt> <dd>

<span data-ttu-id="15fc3-110">Función que permite que una aplicación desvíe una llamada de oferta a otra dirección sin responder primero a la llamada.</span><span class="sxs-lookup"><span data-stu-id="15fc3-110">A function that allows an application to deflect an offering call to another address without first answering the call.</span></span> <span data-ttu-id="15fc3-111">La redirección de llamadas difiere del reenvío de llamadas en que el reenvío de llamadas se realiza mediante el modificador sin la implicación de la aplicación; la aplicación, por ejemplo, controlada por la información del identificador de llamada, puede realizar la redirección en función de la llamada.</span><span class="sxs-lookup"><span data-stu-id="15fc3-111">Call redirection differs from call forwarding in that call forwarding is performed by the switch without the involvement of the application; redirection can be done on a call-by-call basis by the application, for example, driven by caller ID information.</span></span> <span data-ttu-id="15fc3-112">Difiere de la transferencia de llamadas en que transferir una llamada requiere que se responda primero a la llamada.</span><span class="sxs-lookup"><span data-stu-id="15fc3-112">It differs from call transfer in that transferring a call requires that the call first be answered.</span></span> <span data-ttu-id="15fc3-113">Vea *llamado:* ID., *ID. de llamador*, ID. de [*redireccionamiento*](r-tapgloss.md), ID. de [*redireccionamiento*](r-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="15fc3-113">See *called-ID*, *caller-ID*, [*redirecting ID*](r-tapgloss.md), [*redirection ID*](r-tapgloss.md).</span></span>

</dd> <dt>

<span data-ttu-id="15fc3-114"><span id="tapi2.called_id_tapgloss"></span><span id="TAPI2.CALLED_ID_TAPGLOSS"></span>**IDENTIFICADOR llamado**</span><span class="sxs-lookup"><span data-stu-id="15fc3-114"><span id="tapi2.called_id_tapgloss"></span><span id="TAPI2.CALLED_ID_TAPGLOSS"></span>**called-ID**</span></span>
</dt> <dd>

<span data-ttu-id="15fc3-115">Identifica la dirección de destino original de una llamada.</span><span class="sxs-lookup"><span data-stu-id="15fc3-115">Identifies the original destination address of a call.</span></span> <span data-ttu-id="15fc3-116">Consulte *redirección de llamadas*.</span><span class="sxs-lookup"><span data-stu-id="15fc3-116">See *call redirection*.</span></span>

</dd> <dt>

<span data-ttu-id="15fc3-117"><span id="tapi2.caller_id_tapgloss"></span><span id="TAPI2.CALLER_ID_TAPGLOSS"></span>**IDENTIFICADOR del autor de la llamada**</span><span class="sxs-lookup"><span data-stu-id="15fc3-117"><span id="tapi2.caller_id_tapgloss"></span><span id="TAPI2.CALLER_ID_TAPGLOSS"></span>**caller-ID**</span></span>
</dt> <dd>

<span data-ttu-id="15fc3-118">Identifica la dirección de origen de una llamada.</span><span class="sxs-lookup"><span data-stu-id="15fc3-118">Identifies the originating address of a call.</span></span> <span data-ttu-id="15fc3-119">Consulte *redirección de llamadas*.</span><span class="sxs-lookup"><span data-stu-id="15fc3-119">See *call redirection*.</span></span>

</dd> <dt>

<span data-ttu-id="15fc3-120"><span id="tapi2.central_office_tapgloss"></span><span id="TAPI2.CENTRAL_OFFICE_TAPGLOSS"></span>**Oficina central**</span><span class="sxs-lookup"><span data-stu-id="15fc3-120"><span id="tapi2.central_office_tapgloss"></span><span id="TAPI2.CENTRAL_OFFICE_TAPGLOSS"></span>**central office**</span></span>
</dt> <dd>

<span data-ttu-id="15fc3-121">La instalación local de la compañía telefónica que proporciona el servicio telefónico en una zona específica.</span><span class="sxs-lookup"><span data-stu-id="15fc3-121">Telephone company's local facility that provides telephone service in a specific area.</span></span> <span data-ttu-id="15fc3-122">Normalmente, las líneas de los suscriptores se unen al equipo de conmutación que conecta a otros suscriptores entre sí, de forma local y a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="15fc3-122">Typically, subscribers' lines are joined to switching equipment that connects other subscribers to each other, locally and over long distance.</span></span> <span data-ttu-id="15fc3-123">También se denomina *Co*.</span><span class="sxs-lookup"><span data-stu-id="15fc3-123">Also called *CO*.</span></span>

</dd> <dt>

<span data-ttu-id="15fc3-124"><span id="tapi2.centrex_tapgloss"></span><span id="TAPI2.CENTREX_TAPGLOSS"></span>**Centrex**</span><span class="sxs-lookup"><span data-stu-id="15fc3-124"><span id="tapi2.centrex_tapgloss"></span><span id="TAPI2.CENTREX_TAPGLOSS"></span>**Centrex**</span></span>
</dt> <dd>

<span data-ttu-id="15fc3-125">Un servicio de teléfono de la empresa ofrecido por una compañía telefónica local desde una oficina central local.</span><span class="sxs-lookup"><span data-stu-id="15fc3-125">A business telephone service offered by a local telephone company from a local, central office.</span></span>

</dd> <dt>

<span data-ttu-id="15fc3-126"><span id="tapi2.computer_centric_connection_tapgloss"></span><span id="TAPI2.COMPUTER_CENTRIC_CONNECTION_TAPGLOSS"></span>**conexión centrada en el equipo**</span><span class="sxs-lookup"><span data-stu-id="15fc3-126"><span id="tapi2.computer_centric_connection_tapgloss"></span><span id="TAPI2.COMPUTER_CENTRIC_CONNECTION_TAPGLOSS"></span>**computer-centric connection**</span></span>
</dt> <dd>

<span data-ttu-id="15fc3-127">Una conexión que usa una tarjeta de complemento de equipo o un cuadro externo que está conectado a la red telefónica y al conjunto de teléfonos.</span><span class="sxs-lookup"><span data-stu-id="15fc3-127">A connection that uses a computer add-in card or external box that is connected to both the telephone network and the phone set.</span></span> <span data-ttu-id="15fc3-128">Compare [*la conexión centrada en el teléfono*](p-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="15fc3-128">Compare [*phone-centric connection*](p-tapgloss.md).</span></span>

</dd> <dt>

<span data-ttu-id="15fc3-129"><span id="tapi2.connected_id_tapgloss"></span><span id="TAPI2.CONNECTED_ID_TAPGLOSS"></span>**Connected-ID**</span><span class="sxs-lookup"><span data-stu-id="15fc3-129"><span id="tapi2.connected_id_tapgloss"></span><span id="TAPI2.CONNECTED_ID_TAPGLOSS"></span>**connected-ID**</span></span>
</dt> <dd>

<span data-ttu-id="15fc3-130">Identificador de la entidad a la que se conectó realmente la llamada.</span><span class="sxs-lookup"><span data-stu-id="15fc3-130">Identifier for the party to which the call was actually connected.</span></span> <span data-ttu-id="15fc3-131">Puede ser diferente de la entidad a la que se llama si se desvía la llamada.</span><span class="sxs-lookup"><span data-stu-id="15fc3-131">This may be different from the called party if the call was diverted.</span></span>

</dd> </dl>

 

 



