---
title: Activación y desactivación de la retransmisión
description: Una aplicación puede establecer el modo de retransmisión con una llamada a la función SnmpSetRetransmitMode. El nuevo modo de retransmisión se aplica a las llamadas subsiguientes a la función SnmpSendMsg.
ms.assetid: 0e167014-2703-4942-91f0-c60a5c0d8e12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24936bcc90ed0debf66eb9040334fff3bceee2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685492"
---
# <a name="turning-retransmission-on-and-off"></a><span data-ttu-id="73d94-104">Activación y desactivación de la retransmisión</span><span class="sxs-lookup"><span data-stu-id="73d94-104">Turning Retransmission On and Off</span></span>

<span data-ttu-id="73d94-105">Una aplicación puede establecer el modo de retransmisión con una llamada a la función [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) .</span><span class="sxs-lookup"><span data-stu-id="73d94-105">An application can set the retransmission mode with a call to the [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) function.</span></span> <span data-ttu-id="73d94-106">El nuevo modo de retransmisión se aplica a las llamadas subsiguientes a la función [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) .</span><span class="sxs-lookup"><span data-stu-id="73d94-106">The new retransmission mode applies to subsequent calls to the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function.</span></span>

<span data-ttu-id="73d94-107">Cuando la aplicación llama a **SnmpSetRetransmitMode** con el valor de modo de retransmisión snmpapi \_ en, la implementación de Microsoft WinSNMP comienza a ejecutar la Directiva de retransmisión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="73d94-107">When the application calls **SnmpSetRetransmitMode** with the retransmission mode value SNMPAPI\_ON, the Microsoft WinSNMP implementation begins execution of the application's retransmission policy.</span></span> <span data-ttu-id="73d94-108">El nuevo modo de retransmisión no afecta a los mensajes SNMP pendientes.</span><span class="sxs-lookup"><span data-stu-id="73d94-108">The new retransmission mode does not affect outstanding SNMP messages.</span></span> <span data-ttu-id="73d94-109">Un mensaje pendiente es aquél que no tiene respuesta en el momento en que la aplicación cambia el modo de retransmisión.</span><span class="sxs-lookup"><span data-stu-id="73d94-109">An outstanding message is one that has no response at the time the application changes the retransmission mode.</span></span>

<span data-ttu-id="73d94-110">Cuando la aplicación WinSNMP llama a la función [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) con el valor de modo de REtransmisión snmpapi \_ desactivado, la implementación deja de ejecutar la Directiva de retransmisión.</span><span class="sxs-lookup"><span data-stu-id="73d94-110">When the WinSNMP application calls the [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) function with the retransmission mode value SNMPAPI\_OFF, the implementation stops executing the retransmission policy.</span></span> <span data-ttu-id="73d94-111">La implementación cancela los intentos de retransmisión para los mensajes SNMP pendientes.</span><span class="sxs-lookup"><span data-stu-id="73d94-111">The implementation cancels retransmission attempts for outstanding SNMP messages.</span></span> <span data-ttu-id="73d94-112">Esto se debe a que es posible que la implementación de controle todas las solicitudes y operaciones SNMP pendientes y las nuevas solicitudes, antes de que el tiempo de espera de la aplicación o el contador de reintentos señale un evento.</span><span class="sxs-lookup"><span data-stu-id="73d94-112">This is because it may not be possible for the implementation to handle all outstanding SNMP requests and operations plus new requests, before an application time-out or retry counter signals an event.</span></span>

 

 




