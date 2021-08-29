---
title: Funcionamiento de SNMP
description: Cómo una aplicación de consola de administración SNMP de terceros devuelve información del servicio SNMP.
ms.assetid: 2edbf9ff-b9e3-4103-affc-a5c0f22b80a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1feb82b50a954ef96310b887b9fc6e73694242b639a354cd29a5c328c43daf5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009473"
---
# <a name="how-snmp-works"></a>Funcionamiento de SNMP

En los pasos siguientes se describe cómo una aplicación de consola de administración SNMP de terceros devuelve información del servicio SNMP:

1.  La aplicación de consola de administración de SNMP formula un mensaje SNMP basado en la entrada del usuario. El mensaje incluye una unidad de datos de protocolo (PDU) e información de autenticación. La aplicación de consola de administración puede usar la biblioteca de API de Administración SNMP de Microsoft (MGMTAPI.DLL) o la biblioteca de [API winSNMP](winsnmp-api.md) de Microsoft (WSNMP32.DLL) para realizar este paso.
2.  La aplicación de consola de administración de SNMP envía el mensaje SNMP al servicio SNMP, mediante las bibliotecas de servicios SNMP.
3.  El servicio SNMP recibe la solicitud. Comprueba la información de autenticación y la dirección IP de origen.
4.  El servicio SNMP selecciona el agente de extensión adecuado y solicita que el agente recupere la información solicitada.
5.  El servicio SNMP envía la respuesta a la aplicación de consola de administración de SNMP.

 

 




