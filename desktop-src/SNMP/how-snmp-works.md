---
title: Cómo funciona SNMP
description: Cómo una aplicación de consola de administración SNMP de terceros devuelve información del servicio SNMP.
ms.assetid: 2edbf9ff-b9e3-4103-affc-a5c0f22b80a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d58943f0765b60f9c235094642d3fa759402db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994087"
---
# <a name="how-snmp-works"></a><span data-ttu-id="d9af3-103">Cómo funciona SNMP</span><span class="sxs-lookup"><span data-stu-id="d9af3-103">How SNMP Works</span></span>

<span data-ttu-id="d9af3-104">En los pasos siguientes se describe cómo una aplicación de consola de administración SNMP de terceros devuelve información del servicio SNMP:</span><span class="sxs-lookup"><span data-stu-id="d9af3-104">The following steps outline how a third-party SNMP management console application returns information from the SNMP service:</span></span>

1.  <span data-ttu-id="d9af3-105">La aplicación de consola de administración de SNMP formula un mensaje SNMP basado en la entrada del usuario.</span><span class="sxs-lookup"><span data-stu-id="d9af3-105">The SNMP management console application formulates an SNMP message based on input from the user.</span></span> <span data-ttu-id="d9af3-106">El mensaje incluye una unidad de datos de protocolo (PDU) y la información de autenticación.</span><span class="sxs-lookup"><span data-stu-id="d9af3-106">The message includes a protocol data unit (PDU) and authentication information.</span></span> <span data-ttu-id="d9af3-107">La aplicación de consola de administración puede usar la biblioteca de API de administración de SNMP de Microsoft (MGMTAPI.DLL) o la biblioteca de API de Microsoft [WinSNMP](winsnmp-api.md) (WSNMP32.DLL) para realizar este paso.</span><span class="sxs-lookup"><span data-stu-id="d9af3-107">The management console application can use the Microsoft SNMP Management API library (MGMTAPI.DLL) or the Microsoft [WinSNMP API](winsnmp-api.md) library (WSNMP32.DLL) to perform this step.</span></span>
2.  <span data-ttu-id="d9af3-108">La aplicación de consola de administración de SNMP envía el mensaje SNMP al servicio SNMP mediante las bibliotecas de servicios SNMP.</span><span class="sxs-lookup"><span data-stu-id="d9af3-108">The SNMP management console application sends the SNMP message to the SNMP service, using the SNMP service libraries.</span></span>
3.  <span data-ttu-id="d9af3-109">El servicio SNMP recibe la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d9af3-109">The SNMP service receives the request.</span></span> <span data-ttu-id="d9af3-110">Comprueba la información de autenticación y la dirección IP de origen.</span><span class="sxs-lookup"><span data-stu-id="d9af3-110">It verifies the authentication information and the source IP address.</span></span>
4.  <span data-ttu-id="d9af3-111">El servicio SNMP selecciona el agente de extensión adecuado y solicita que el agente recupere la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="d9af3-111">The SNMP service selects the appropriate extension agent and requests that the agent retrieve the requested information.</span></span>
5.  <span data-ttu-id="d9af3-112">El servicio SNMP envía la respuesta a la aplicación de consola de administración de SNMP.</span><span class="sxs-lookup"><span data-stu-id="d9af3-112">The SNMP service sends the response to the SNMP management console application.</span></span>

 

 




