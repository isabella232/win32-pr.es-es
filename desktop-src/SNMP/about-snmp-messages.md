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
# <a name="about-snmp-messages"></a>Acerca de los mensajes SNMP

El Protocolo simple de administración de redes usa mensajes para comunicarse e intercambiar información entre entidades SNMP remotas. Los mensajes SNMP contienen unidades de datos de protocolo (PDU) más elementos de encabezado de mensaje adicionales definidos por la RFC correspondiente. Una PDU es un paquete de datos que contiene componentes de datos SNMP (o campos).

El formato de un mensaje SNMP es el mismo para SNMPv1 y SNMPv2C. Sin embargo, SNMPv2C admite otros tipos de PDU. Por ejemplo, admite el tipo de solicitud [ \_ \_ GetBulk e inform PDU de SNMP](snmp-variable-types-and-request-pdu-types.md) , que permite que una aplicación recupere de forma eficaz bloques grandes de datos de las entidades de destino.

 

 




