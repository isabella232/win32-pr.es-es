---
title: Trabajar con unidades de datos de protocolo
description: El Protocolo simple de administración de redes (SNMP) envía solicitudes y respuestas de operaciones como mensajes SNMP.
ms.assetid: 0928981c-4d60-4583-9eef-8127e05b1ba8
keywords:
- Trabajar con SNMP de unidades de datos de protocolo
- Unidades de datos de protocolo SNMP, trabajar con
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b61fff4aed06d548718df130801c5c64674ff0b10feaf52b8bfad208d441d4fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142768"
---
# <a name="working-with-protocol-data-units"></a>Trabajar con unidades de datos de protocolo

El Protocolo simple de administración de redes (SNMP) envía solicitudes y respuestas de operaciones como mensajes SNMP. Un mensaje SNMP es una unidad de datos del protocolo SNMP (PDU) más elementos de encabezado de mensaje adicionales definidos por la RFC correspondiente. Una PDU incluye una lista de enlaces de variables.

La estructura de una PDU está restringida a la implementación de Microsoft WinSNMP. Una aplicación WinSNMP puede acceder a una PDU con un identificador del tipo **HSNMP \_ PDU**. La aplicación WinSNMP debe crear una PDU antes de llamar a la [**función SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) o a [**la función SnmpEncodeMsg.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg)

La aplicación puede extraer y actualizar los elementos de datos de una PDU y liberar recursos asignados para PDU. Para realizar estas operaciones, la aplicación usa las funciones [PDU de](winsnmp-functions.md)WinSNMP . En la tabla siguiente se enumeran los temas en los que se describe cómo trabajar con PDU en el entorno de programación WinSNMP.



| Tema                                                                        | Descripción                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Creación de una PDU](creating-a-pdu.md)                                         | Describe cómo crear una PDU.                                     |
| [Actualización de una PDU](updating-a-pdu.md)                                         | Describe cómo recuperar y actualizar campos PDU.                   |
| [Duplicación de una PDU](duplicating-a-pdu.md)                                   | Describe cómo duplicar una PDU.                                  |
| [Validación de una PDU](validating-a-pdu.md)                                     | Describe la validación de una PDU.                                 |
| [Respuesta de coincidencia y PDU de solicitud](matching-response-and-request-pdus.md) | Describe el proceso de hacer coincidir una PDU de respuesta con una PDU de solicitud. |



 

Para obtener más información, vea [Trabajar con listas de enlaces de variables y](working-with-variable-binding-lists.md) Objetos de identificador de [recursos.](resource-handle-objects.md)

 

 




