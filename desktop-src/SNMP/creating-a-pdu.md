---
title: Creación de una PDU
description: Para crear e inicializar una PDU, una aplicación WinSNMP llama a la función SnmpCreatePdu.
ms.assetid: 7f02a2c6-19bc-456f-bf04-3297d19000f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aba7a4ca42e2a5d63169d2521410773ca018c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903495"
---
# <a name="creating-a-pdu"></a><span data-ttu-id="f33ee-103">Creación de una PDU</span><span class="sxs-lookup"><span data-stu-id="f33ee-103">Creating a PDU</span></span>

<span data-ttu-id="f33ee-104">Para crear e inicializar una PDU, una aplicación WinSNMP llama a la función [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) .</span><span class="sxs-lookup"><span data-stu-id="f33ee-104">To create and initialize a PDU a WinSNMP application calls the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function.</span></span> <span data-ttu-id="f33ee-105">La aplicación debe llamar a **SnmpCreatePdu** antes de llamar a la función [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) para solicitar que la implementación de Microsoft WINSNMP transmita una PDU.</span><span class="sxs-lookup"><span data-stu-id="f33ee-105">The application must call **SnmpCreatePdu** before it calls the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function to request that the Microsoft WinSNMP implementation transmit a PDU.</span></span> <span data-ttu-id="f33ee-106">La aplicación también debe llamar a [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) antes de llamar a la función [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) para solicitar la codificación de un mensaje SNMP.</span><span class="sxs-lookup"><span data-stu-id="f33ee-106">The application must also call [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) before it calls the [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) function to request encoding of an SNMP message.</span></span>

<span data-ttu-id="f33ee-107">La aplicación debe llamar a la función [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) para liberar los recursos que la función [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) asigna para las PDU nuevas.</span><span class="sxs-lookup"><span data-stu-id="f33ee-107">The application must call the [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) function to release the resources that the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function allocates for new PDUs.</span></span>

 

 




