---
title: Envío de mensajes SNMP
description: Una aplicación WinSNMP inicia una solicitud de transmisión mediante el envío de un mensaje SNMP. Los mensajes SNMP incluyen una unidad de datos de protocolo SNMP. Para obtener más información, vea trabajar con unidades de datos de protocolo.
ms.assetid: a7439cd2-af13-4e2b-a0a6-5cc271a011e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613ac7079f7dc206280b8d8077d2d5ea8db7151c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357440"
---
# <a name="sending-snmp-messages"></a><span data-ttu-id="26b83-105">Envío de mensajes SNMP</span><span class="sxs-lookup"><span data-stu-id="26b83-105">Sending SNMP Messages</span></span>

<span data-ttu-id="26b83-106">Una aplicación WinSNMP inicia una solicitud de transmisión mediante el envío de un mensaje SNMP.</span><span class="sxs-lookup"><span data-stu-id="26b83-106">A WinSNMP application initiates a transmission request by sending an SNMP message.</span></span> <span data-ttu-id="26b83-107">Los mensajes SNMP incluyen una unidad de datos de protocolo SNMP.</span><span class="sxs-lookup"><span data-stu-id="26b83-107">SNMP messages include an SNMP protocol data unit.</span></span> <span data-ttu-id="26b83-108">Para obtener más información, vea [trabajar con unidades de datos de protocolo](working-with-protocol-data-units.md).</span><span class="sxs-lookup"><span data-stu-id="26b83-108">For more information, see [Working with Protocol Data Units](working-with-protocol-data-units.md).</span></span>

<span data-ttu-id="26b83-109">Una aplicación WinSNMP debe llamar a la función [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) para solicitar que la implementación de Microsoft WinSNMP transmita la PDU, con los otros elementos de mensaje necesarios definidos por la RFC correspondiente.</span><span class="sxs-lookup"><span data-stu-id="26b83-109">A WinSNMP application must call the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function to request that the Microsoft WinSNMP implementation transmit the PDU, with the other required message elements defined by the relevant RFC.</span></span> <span data-ttu-id="26b83-110">Además de la entidad de destino, la aplicación debe especificar la entidad de origen y un contexto para la solicitud.</span><span class="sxs-lookup"><span data-stu-id="26b83-110">In addition to the destination entity, the application must specify the source entity and a context for the request.</span></span> <span data-ttu-id="26b83-111">La función [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) se ejecuta de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="26b83-111">The [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function executes asynchronously.</span></span>

<span data-ttu-id="26b83-112">La aplicación WinSNMP debe llamar a la función [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) para recuperar la respuesta a una solicitud **SnmpSendMsg** .</span><span class="sxs-lookup"><span data-stu-id="26b83-112">The WinSNMP application must call the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function to retrieve the response to an **SnmpSendMsg** request.</span></span>

<span data-ttu-id="26b83-113">La implementación de comprueba la validez de la PDU y los otros elementos del mensaje cuando una aplicación llama a [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg).</span><span class="sxs-lookup"><span data-stu-id="26b83-113">The implementation verifies the validity of the PDU and the other message elements when an application calls [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg).</span></span>

 

 




