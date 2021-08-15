---
title: Acerca de los mensajes SNMP
description: El Protocolo simple de administración de redes usa mensajes para comunicar e intercambiar información entre entidades SNMP remotas.
ms.assetid: 9ba4b854-fc02-40c1-a92f-7c102c900e95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90c8e6aba33384ddaf16fbe847f20488f0be4d584c70563a34d052a37e80a23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009953"
---
# <a name="about-snmp-messages"></a>Acerca de los mensajes SNMP

El Protocolo simple de administración de redes usa mensajes para comunicar e intercambiar información entre entidades SNMP remotas. Los mensajes SNMP contienen unidades de datos de protocolo (PDU) más elementos de encabezado de mensaje adicionales definidos por la RFC pertinente. Una PDU es un paquete de datos que contiene componentes de datos SNMP (o campos).

El formato de un mensaje SNMP es el mismo para SNMPv1 y SNMPv2C. Sin embargo, SNMPv2C admite tipos PDU adicionales. Por ejemplo, admite el tipo de solicitud [ \_ \_ GETBULK PDU](snmp-variable-types-and-request-pdu-types.md) de SNMP, que permite a una aplicación recuperar eficazmente grandes bloques de datos de entidades de destino.

 

 




