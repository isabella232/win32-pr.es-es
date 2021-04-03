---
title: Trabajar con unidades de datos de protocolo
description: El Protocolo simple de administración de redes (SNMP) envía solicitudes de operación y respuestas como mensajes SNMP.
ms.assetid: 0928981c-4d60-4583-9eef-8127e05b1ba8
keywords:
- Trabajar con unidades de datos de protocolo SNMP
- Unidades de datos de protocolo SNMP, trabajar con
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e40f36fa28f7ff17974d79f4f8ac29b8b6130b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076041"
---
# <a name="working-with-protocol-data-units"></a>Trabajar con unidades de datos de protocolo

El Protocolo simple de administración de redes (SNMP) envía solicitudes de operación y respuestas como mensajes SNMP. Un mensaje SNMP es una unidad de datos de protocolo SNMP (PDU) más elementos de encabezado de mensaje adicionales definidos por la RFC correspondiente. Una PDU incluye una lista de enlaces de variables.

La estructura de una PDU está restringida a la implementación de Microsoft WinSNMP. Una aplicación WinSNMP puede tener acceso a una PDU con un identificador del **tipo \_ PDU HSNMP**. La aplicación WinSNMP debe crear una PDU antes de llamar a la función [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) o a la función [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) .

La aplicación puede extraer y actualizar los elementos de datos de una PDU y liberar los recursos asignados para las PDU. Para realizar estas operaciones, la aplicación usa las [funciones de PDU](winsnmp-functions.md)WinSNMP. En la tabla siguiente se enumeran los temas en los que se explica cómo trabajar con PDU en el entorno de programación WinSNMP.



| Tema                                                                        | Descripción                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Creación de una PDU](creating-a-pdu.md)                                         | Describe cómo crear una PDU.                                     |
| [Actualización de una PDU](updating-a-pdu.md)                                         | Describe cómo recuperar y actualizar los campos de PDU.                   |
| [Duplicación de una PDU](duplicating-a-pdu.md)                                   | Describe cómo duplicar una PDU.                                  |
| [Validación de una PDU](validating-a-pdu.md)                                     | Describe la validación de una PDU.                                 |
| [Respuesta coincidente y solicitud de PDU](matching-response-and-request-pdus.md) | Describe el proceso de coincidencia de una PDU de respuesta con una PDU de solicitud. |



 

Para obtener más información, vea [trabajar con listas de enlaces de variables](working-with-variable-binding-lists.md) y objetos de identificador de [recursos](resource-handle-objects.md).

 

 




