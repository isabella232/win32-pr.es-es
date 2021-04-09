---
title: Trasladar capturas de SNMPv1 a SNMPv2C
description: Cuando la implementación de Microsoft WinSNMP recibe capturas de una entidad que funciona con el marco de SNMPv1, traduce las capturas al formato SNMPv2C.
ms.assetid: 472f67ba-05d5-46f7-a2f1-1cef6182574e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d36870bda9b434bcc19f42332f2751020689591
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903275"
---
# <a name="translating-traps-from-snmpv1-to-snmpv2c"></a><span data-ttu-id="d7cdb-103">Trasladar capturas de SNMPv1 a SNMPv2C</span><span class="sxs-lookup"><span data-stu-id="d7cdb-103">Translating Traps from SNMPv1 to SNMPv2C</span></span>

<span data-ttu-id="d7cdb-104">Cuando la implementación de Microsoft WinSNMP recibe capturas de una entidad que funciona con el marco de SNMPv1, traduce las capturas al formato SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="d7cdb-104">When the Microsoft WinSNMP implementation receives traps from an entity operating under the SNMPv1 framework, it translates the traps to the SNMPv2C format.</span></span> <span data-ttu-id="d7cdb-105">Por lo tanto, cuando [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) entrega una captura, siempre está en el formato SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="d7cdb-105">Therefore, when [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) delivers a trap it is always in the SNMPv2C format.</span></span> <span data-ttu-id="d7cdb-106">RFC 1908, "coexistencia entre la versión 1 y la versión 2 del marco de administración de redes estándar de Internet", especifica las reglas de conversión de SNMPv1 al formato de captura de SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="d7cdb-106">RFC 1908, "Coexistence between Version 1 and Version 2 of the Internet-standard Network Management Framework," specifies the rules for translating from the SNMPv1 to the SNMPv2C trap format.</span></span>

<span data-ttu-id="d7cdb-107">Una aplicación WinSNMP puede comprobar la entrada de enlace de la última variable en una lista de enlaces de variables para determinar si la entrada es una captura traducida desde SNMPv1 al formato SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="d7cdb-107">A WinSNMP application can check the last variable binding entry in a variable binding list to determine if the entry is a trap translated from the SNMPv1 to the SNMPv2C format.</span></span> <span data-ttu-id="d7cdb-108">Si es así, el último enlace de variables siempre será igual al valor "snmpTrapEnterpriseOID. 0".</span><span class="sxs-lookup"><span data-stu-id="d7cdb-108">If so, the last variable binding will always be equal to the value "snmpTrapEnterpriseOID.0".</span></span>

<span data-ttu-id="d7cdb-109">Para obtener más información, consulte [Administración de capturas y notificaciones](managing-traps-and-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="d7cdb-109">For more information, see [Managing Traps and Notifications](managing-traps-and-notifications.md).</span></span>

 

 




