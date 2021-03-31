---
title: Acerca de los mensajes SNMP
description: El Protocolo simple de administración de redes usa mensajes para comunicarse e intercambiar información entre entidades SNMP remotas.
ms.assetid: 9ba4b854-fc02-40c1-a92f-7c102c900e95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a0426bf44d976ddf9e2eafe2093dcea94956cb4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418508"
---
# <a name="about-snmp-messages"></a><span data-ttu-id="cf36c-103">Acerca de los mensajes SNMP</span><span class="sxs-lookup"><span data-stu-id="cf36c-103">About SNMP Messages</span></span>

<span data-ttu-id="cf36c-104">El Protocolo simple de administración de redes usa mensajes para comunicarse e intercambiar información entre entidades SNMP remotas.</span><span class="sxs-lookup"><span data-stu-id="cf36c-104">The Simple Network Management Protocol uses messages to communicate and exchange information between remote SNMP entities.</span></span> <span data-ttu-id="cf36c-105">Los mensajes SNMP contienen unidades de datos de protocolo (PDU) más elementos de encabezado de mensaje adicionales definidos por la RFC correspondiente.</span><span class="sxs-lookup"><span data-stu-id="cf36c-105">SNMP messages contain protocol data units (PDUs) plus additional message header elements defined by the relevant RFC.</span></span> <span data-ttu-id="cf36c-106">Una PDU es un paquete de datos que contiene componentes de datos SNMP (o campos).</span><span class="sxs-lookup"><span data-stu-id="cf36c-106">A PDU is a data packet that contains SNMP data components (or fields).</span></span>

<span data-ttu-id="cf36c-107">El formato de un mensaje SNMP es el mismo para SNMPv1 y SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="cf36c-107">The format of an SNMP message is the same for both SNMPv1 and SNMPv2C.</span></span> <span data-ttu-id="cf36c-108">Sin embargo, SNMPv2C admite otros tipos de PDU.</span><span class="sxs-lookup"><span data-stu-id="cf36c-108">However, SNMPv2C supports additional PDU types.</span></span> <span data-ttu-id="cf36c-109">Por ejemplo, admite el tipo de solicitud [ \_ \_ GetBulk e inform PDU de SNMP](snmp-variable-types-and-request-pdu-types.md) , que permite que una aplicación recupere de forma eficaz bloques grandes de datos de las entidades de destino.</span><span class="sxs-lookup"><span data-stu-id="cf36c-109">For example, it supports the [SNMP\_PDU\_GETBULK](snmp-variable-types-and-request-pdu-types.md) request type, which enables an application to efficiently retrieve large blocks of data from target entities.</span></span>

 

 




