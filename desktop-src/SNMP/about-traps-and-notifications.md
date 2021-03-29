---
title: Acerca de las capturas y notificaciones
description: Un tipo de mensaje que una aplicación de agente SNMP puede enviar a una aplicación WinSNMP es un mensaje asincrónico que informa a la aplicación de un evento significativo.
ms.assetid: 5249c5a5-9260-4a67-b00f-a12214012bb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bacc6a92de2cb5a12aaf09f5caa629f28338f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903498"
---
# <a name="about-traps-and-notifications"></a><span data-ttu-id="15252-103">Acerca de las capturas y notificaciones</span><span class="sxs-lookup"><span data-stu-id="15252-103">About Traps and Notifications</span></span>

<span data-ttu-id="15252-104">Un tipo de mensaje que una aplicación de agente SNMP puede enviar a una aplicación WinSNMP es un mensaje asincrónico que informa a la aplicación de un evento significativo.</span><span class="sxs-lookup"><span data-stu-id="15252-104">One type of message an SNMP agent application can send to a WinSNMP application is an asynchronous message that informs the application of a significant event.</span></span> <span data-ttu-id="15252-105">Un ejemplo de un evento significativo es cuando un vínculo de red se cierra o cuando se produce un error de autenticación.</span><span class="sxs-lookup"><span data-stu-id="15252-105">An example of a significant event is when a network link shuts down or when an authentication failure occurs.</span></span>

<span data-ttu-id="15252-106">Estos tipos de mensajes se denominan capturas en SNMPv1 y notificaciones en SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="15252-106">These types of messages are called traps under SNMPv1 and notifications under SNMPv2C.</span></span> <span data-ttu-id="15252-107">La implementación de Microsoft WinSNMP siempre traduce las capturas de SNMPv1 al formato SNMPv2C, tal como se define en RFC 1908.</span><span class="sxs-lookup"><span data-stu-id="15252-107">The Microsoft WinSNMP implementation always translates SNMPv1 traps to the SNMPv2C format, as defined by RFC 1908.</span></span>

<span data-ttu-id="15252-108">Cuando se llama a la función [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) para crear una PDU de captura, solo se puede crear una PDU de captura de SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="15252-108">When you call the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function to create a trap PDU, you can create only an SNMPv2C trap PDU.</span></span> <span data-ttu-id="15252-109">El único tipo de PDU de captura que se puede actualizar con una llamada a la función [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) es una PDU de captura de SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="15252-109">The only type of trap PDU you can update with a call to the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function is an SNMPv2C trap PDU.</span></span>

<span data-ttu-id="15252-110">Para obtener más información, vea los siguientes temas.</span><span class="sxs-lookup"><span data-stu-id="15252-110">For more information, see the following topics.</span></span>



| <span data-ttu-id="15252-111">Tema</span><span class="sxs-lookup"><span data-stu-id="15252-111">Topic</span></span>                                                                                    | <span data-ttu-id="15252-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="15252-112">Description</span></span> |
|------------------------------------------------------------------------------------------|-------------|
| [<span data-ttu-id="15252-113">Trasladar capturas de SNMPv1 a SNMPv2C</span><span class="sxs-lookup"><span data-stu-id="15252-113">Translating Traps from SNMPv1 to SNMPv2C</span></span>](translating-traps-from-snmpv1-to-snmpv2c.md) |             |
| [<span data-ttu-id="15252-114">Formatos de captura</span><span class="sxs-lookup"><span data-stu-id="15252-114">Trap Formats</span></span>](trap-formats.md)                                                         |             |



 

 

 




