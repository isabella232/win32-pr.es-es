---
title: Respuesta coincidente y solicitud de PDU
description: El orden en el que la aplicación WinSNMP recibe respuestas SNMP puede no coincidir con el orden en el que la aplicación envía las solicitudes de operación SNMP.
ms.assetid: cd09cc4b-2ef6-4d2f-8f0f-b83d8df8599a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75a05f4a450ac1712d7cdd01a3c0e79dfddeb2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994405"
---
# <a name="matching-response-and-request-pdus"></a><span data-ttu-id="2c258-103">Respuesta coincidente y solicitud de PDU</span><span class="sxs-lookup"><span data-stu-id="2c258-103">Matching Response and Request PDUs</span></span>

<span data-ttu-id="2c258-104">El orden en el que la aplicación WinSNMP recibe respuestas SNMP puede no coincidir con el orden en el que la aplicación envía las solicitudes de operación SNMP.</span><span class="sxs-lookup"><span data-stu-id="2c258-104">The order in which the WinSNMP application receives SNMP responses may not match the order in which the application submits SNMP operation requests.</span></span> <span data-ttu-id="2c258-105">Para hacer coincidir la respuesta con la solicitud, la aplicación debe usar el campo Identificador de solicitud (el **\_ identificador de solicitud**) de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2c258-105">To match the response with the request, the application must use the request identifier field (the **request\_id**) of the response.</span></span>

<span data-ttu-id="2c258-106">El **campo \_ ID. de solicitud** es un valor numérico único que identifica la PDU.</span><span class="sxs-lookup"><span data-stu-id="2c258-106">The **request\_id** field is a unique numeric value that identifies the PDU.</span></span> <span data-ttu-id="2c258-107">Las aplicaciones pueden asignar identificadores de solicitud mediante una llamada a la función [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) o a la función [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) .</span><span class="sxs-lookup"><span data-stu-id="2c258-107">Applications can assign request identifiers by calling the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function or the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function.</span></span> <span data-ttu-id="2c258-108">Llame a la función [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) para recuperar el **\_ identificador de solicitud** de una PDU.</span><span class="sxs-lookup"><span data-stu-id="2c258-108">Call the [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) function to retrieve a PDU's **request\_id**.</span></span>

 

 




