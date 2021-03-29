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
# <a name="how-snmp-works"></a>Cómo funciona SNMP

En los pasos siguientes se describe cómo una aplicación de consola de administración SNMP de terceros devuelve información del servicio SNMP:

1.  La aplicación de consola de administración de SNMP formula un mensaje SNMP basado en la entrada del usuario. El mensaje incluye una unidad de datos de protocolo (PDU) y la información de autenticación. La aplicación de consola de administración puede usar la biblioteca de API de administración de SNMP de Microsoft (MGMTAPI.DLL) o la biblioteca de API de Microsoft [WinSNMP](winsnmp-api.md) (WSNMP32.DLL) para realizar este paso.
2.  La aplicación de consola de administración de SNMP envía el mensaje SNMP al servicio SNMP mediante las bibliotecas de servicios SNMP.
3.  El servicio SNMP recibe la solicitud. Comprueba la información de autenticación y la dirección IP de origen.
4.  El servicio SNMP selecciona el agente de extensión adecuado y solicita que el agente recupere la información solicitada.
5.  El servicio SNMP envía la respuesta a la aplicación de consola de administración de SNMP.

 

 




