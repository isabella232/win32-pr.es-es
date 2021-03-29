---
title: Duplicación de una PDU
description: La función SnmpDuplicatePdu duplica una PDU, asignando cualquier memoria necesaria. Para liberar los recursos asignados por SnmpDuplicatePdu para una nueva PDU, una aplicación WinSNMP debe llamar a la función SnmpFreePdu.
ms.assetid: 371e566b-0577-4089-b081-17085c9587fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd860d84ac102f2c2cdd1132476b3279e640f9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777274"
---
# <a name="duplicating-a-pdu"></a><span data-ttu-id="638fa-104">Duplicación de una PDU</span><span class="sxs-lookup"><span data-stu-id="638fa-104">Duplicating a PDU</span></span>

<span data-ttu-id="638fa-105">La función [**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) duplica una PDU, asignando cualquier memoria necesaria.</span><span class="sxs-lookup"><span data-stu-id="638fa-105">The [**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) function duplicates a PDU, allocating any necessary memory.</span></span> <span data-ttu-id="638fa-106">Para liberar los recursos asignados por **SnmpDuplicatePdu** para una nueva PDU, una aplicación WinSNMP debe llamar a la función [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) .</span><span class="sxs-lookup"><span data-stu-id="638fa-106">To release resources allocated by **SnmpDuplicatePdu** for a new PDU, a WinSNMP application must call the [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) function.</span></span>

 

 




