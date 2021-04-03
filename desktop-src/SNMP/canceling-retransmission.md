---
title: Cancelando retransmisión
description: Si no hay ninguna respuesta a una solicitud de comunicación en el período de tiempo de espera especificado para una entidad de destino, y si se especifican retransmisiones para la entidad, la implementación de Microsoft WinSNMP vuelve a transmitir la solicitud.
ms.assetid: 3fd39425-7d57-4bbb-9dcb-f43b6211228c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f7346ee6e1e336b4f8fe56df3dce602fe65a0b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075716"
---
# <a name="canceling-retransmission"></a><span data-ttu-id="1ab61-103">Cancelando retransmisión</span><span class="sxs-lookup"><span data-stu-id="1ab61-103">Canceling Retransmission</span></span>

<span data-ttu-id="1ab61-104">Si no hay ninguna respuesta a una solicitud de comunicación en el período de tiempo de espera especificado para una entidad de destino, y si se especifican retransmisiones para la entidad, la implementación de Microsoft WinSNMP vuelve a transmitir la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1ab61-104">If there is no response to a communication request within the time-out period specified for a destination entity, and if retransmissions are specified for the entity, the Microsoft WinSNMP implementation retransmits the request.</span></span> <span data-ttu-id="1ab61-105">Una llamada a la función [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) puede cancelar este ciclo de retransmisión y liberar las estructuras de datos internas asociadas a la solicitud de mensaje.</span><span class="sxs-lookup"><span data-stu-id="1ab61-105">A call to the [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) function can cancel this retransmission cycle and release internal data structures associated with the message request.</span></span>

<span data-ttu-id="1ab61-106">Tenga en cuenta que es posible que una entidad de destino reciba un mensaje SNMP cancelado por una llamada a la función [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) .</span><span class="sxs-lookup"><span data-stu-id="1ab61-106">Note that it is possible for a destination entity to receive an SNMP message that has been canceled by a call to the [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) function.</span></span> <span data-ttu-id="1ab61-107">También es posible que una entidad de destino pueda responder a un mensaje SNMP cancelado.</span><span class="sxs-lookup"><span data-stu-id="1ab61-107">It is also possible that a destination entity can respond to a canceled SNMP message.</span></span> <span data-ttu-id="1ab61-108">Esto se debe a que las colas de transacciones se producen en varios niveles.</span><span class="sxs-lookup"><span data-stu-id="1ab61-108">This is because transaction queuing occurs at multiple levels.</span></span> <span data-ttu-id="1ab61-109">Sin embargo, una vez que se ha cancelado un mensaje mediante una llamada a [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg), la implementación de Microsoft WinSNMP no volverá a transmitir el mensaje, enviará una PDU de respuesta o enviará una notificación de tiempo de espera a la aplicación para ese mensaje.</span><span class="sxs-lookup"><span data-stu-id="1ab61-109">However, once a message has been canceled by a call to [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg), the Microsoft WinSNMP implementation will not retransmit the message, submit a response PDU, or send a time-out notification to the application for that message.</span></span>

 

 




