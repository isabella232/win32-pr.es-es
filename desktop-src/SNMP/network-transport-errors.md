---
title: Errores de transporte de red
description: La implementación de Microsoft WinSNMP puede detectar un error de transporte de red después de transmitir un mensaje SNMP.
ms.assetid: 2ff535b1-76cb-42aa-baeb-14c1a1bc41ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cf6b7610fbfe8d19a375bd3e3146263b9e9f0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904761"
---
# <a name="network-transport-errors"></a><span data-ttu-id="fda46-103">Errores de transporte de red</span><span class="sxs-lookup"><span data-stu-id="fda46-103">Network Transport Errors</span></span>

<span data-ttu-id="fda46-104">\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="fda46-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fda46-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="fda46-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="fda46-106">En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]</span><span class="sxs-lookup"><span data-stu-id="fda46-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="fda46-107">La implementación de Microsoft WinSNMP puede detectar un error de transporte de red después de transmitir un mensaje SNMP.</span><span class="sxs-lookup"><span data-stu-id="fda46-107">The Microsoft WinSNMP implementation can detect a network transport error after it transmits an SNMP message.</span></span> <span data-ttu-id="fda46-108">Cuando esto ocurre, la implementación envía una notificación de recepción de datos a la sesión WinSNMP que inició la solicitud de comunicación.</span><span class="sxs-lookup"><span data-stu-id="fda46-108">When this occurs, the implementation sends a data receipt notification to the WinSNMP session that initiated the communication request.</span></span> <span data-ttu-id="fda46-109">La implementación también devuelve \_ un error snmpapi en la siguiente llamada a la función [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) para la sesión.</span><span class="sxs-lookup"><span data-stu-id="fda46-109">The implementation also returns SNMPAPI\_FAILURE on the next call to the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function for the session.</span></span> <span data-ttu-id="fda46-110">Se produce un error en la función **SnmpRecvMsg** con un código de error extendido que indica un error de capa de transporte de red.</span><span class="sxs-lookup"><span data-stu-id="fda46-110">The **SnmpRecvMsg** function fails with an extended error code that indicates a network transport layer error.</span></span>

<span data-ttu-id="fda46-111">Para obtener una lista de errores de capa de transporte específicos, vea las páginas de referencia de las funciones [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)y [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) .</span><span class="sxs-lookup"><span data-stu-id="fda46-111">For a list of specific transport layer errors, see the reference pages for the [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg), and [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) functions.</span></span>

 

 