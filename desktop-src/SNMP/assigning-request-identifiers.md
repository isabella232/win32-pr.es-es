---
title: Asignar identificadores de solicitud
description: Una aplicación WinSNMP puede llamar a la función SnmpCreatePdu o a la función SnmpSetPduData para asignar un identificador de solicitud generado por la aplicación a una PDU. La aplicación debe pasar el valor en el \_ parámetro de ID. de solicitud.
ms.assetid: 72559054-982f-4c2b-83d2-268f130f6ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753f0ec1f5f3ca4347b6344aa111b91e735f06ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772853"
---
# <a name="assigning-request-identifiers"></a><span data-ttu-id="cf32b-104">Asignar identificadores de solicitud</span><span class="sxs-lookup"><span data-stu-id="cf32b-104">Assigning Request Identifiers</span></span>

<span data-ttu-id="cf32b-105">Una aplicación WinSNMP puede llamar a la función [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) o a la función [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) para asignar un identificador de solicitud generado por la aplicación a una PDU.</span><span class="sxs-lookup"><span data-stu-id="cf32b-105">A WinSNMP application can call the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function or the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function to assign an application-generated request identifier to a PDU.</span></span> <span data-ttu-id="cf32b-106">La aplicación debe pasar el valor en el parámetro de *\_ ID* . de solicitud.</span><span class="sxs-lookup"><span data-stu-id="cf32b-106">The application must pass the value in the *request\_id* parameter.</span></span>

<span data-ttu-id="cf32b-107">Una aplicación puede solicitar que la implementación de Microsoft WinSNMP genere y asigne un identificador de solicitud a una PDU pasando cero en el parámetro de *\_ identificador de solicitud* de la función [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) .</span><span class="sxs-lookup"><span data-stu-id="cf32b-107">An application can request that the Microsoft WinSNMP implementation generate and assign a request identifier to a PDU by passing zero in the *request\_id* parameter of the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function.</span></span> <span data-ttu-id="cf32b-108">La aplicación puede recuperar el identificador de solicitud asignado con una llamada a la función [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) .</span><span class="sxs-lookup"><span data-stu-id="cf32b-108">The application can retrieve the assigned request identifier with a call to the [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) function.</span></span>

<span data-ttu-id="cf32b-109">Para asignar un identificador de solicitud igual a un valor específico, incluido cero, la aplicación debe pasar ese valor en el parámetro de *\_ identificador de solicitud* de la función [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) .</span><span class="sxs-lookup"><span data-stu-id="cf32b-109">To assign a request identifier equal to a specific value, including zero, the application must pass that value in the *request\_id* parameter of the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function.</span></span>

<span data-ttu-id="cf32b-110">Cuando la implementación ejecuta la Directiva de retransmisión de la aplicación, incluye el **campo \_ ID. de solicitud** de la PDU original en cada mensaje SNMP retransmitido.</span><span class="sxs-lookup"><span data-stu-id="cf32b-110">When the implementation executes the application's retransmission policy, it includes the **request\_id** field of the original PDU in each retransmitted SNMP message.</span></span> <span data-ttu-id="cf32b-111">Para obtener más información, vea [acerca de la retransmisión](about-retransmission.md) y [Administración de la Directiva de retransmisión](managing-the-retransmission-policy.md).</span><span class="sxs-lookup"><span data-stu-id="cf32b-111">For more information, see [About Retransmission](about-retransmission.md) and [Managing the Retransmission Policy](managing-the-retransmission-policy.md).</span></span>

> [!Note]  
> <span data-ttu-id="cf32b-112">Cuando la implementación recibe capturas de una entidad SNMPv1, asigna un valor distinto de cero al campo **\_ ID. de solicitud** de la PDU.</span><span class="sxs-lookup"><span data-stu-id="cf32b-112">When the implementation receives traps from an SNMPv1 entity, it assigns a non-zero value to the **request\_id** field of the PDU.</span></span> <span data-ttu-id="cf32b-113">Este valor puede duplicar un identificador de solicitud usado por la aplicación en una PDU de solicitud.</span><span class="sxs-lookup"><span data-stu-id="cf32b-113">This value may duplicate a request identifier used by the application in a request PDU.</span></span> <span data-ttu-id="cf32b-114">Las aplicaciones deben comprobar la duplicación.</span><span class="sxs-lookup"><span data-stu-id="cf32b-114">Applications must check for duplication.</span></span>

 

 

 




