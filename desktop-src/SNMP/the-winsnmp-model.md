---
title: El modelo WinSNMP
description: El modelo compatible con WinSNMP incluye los siguientes componentes básicos.
ms.assetid: 491df017-0b91-4fcf-97c3-4e296c3324bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8814786b6ae44527460930daf5a9e8164645ca0ecfce52824831b2dbc7e61e80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127585"
---
# <a name="the-winsnmp-model"></a>El modelo WinSNMP

El modelo compatible con WinSNMP incluye los siguientes componentes básicos:

-   Una aplicación de administración de red SNMP habilitada para WinSNMP, es decir, una aplicación compatible con *WinSNMP*
-   Capa de función WinSNMP
-   Un proveedor de servicios SNMP habilitado para WinSNMP, es  decir, una implementación compatible con WinSNMP

Las aplicaciones de administración de redes que deben transmitir mensajes SNMP funcionan de forma eficaz en un entorno controlado por eventos. Esto se debe a que SNMP es un protocolo sin conexión o basado en datagramas entre entidades remotas que no establecen circuitos virtuales.

Puesto que Windows aplicaciones de Microsoft también están controladas por eventos, WinSNMP usa un modelo de programación en el que la recepción y el procesamiento de eventos *de* mensajes asincrónicos impulsan las aplicaciones de administración. Un evento de mensaje asincrónico puede ser una solicitud de operación SNMP por parte de una aplicación de administrador o la respuesta a una solicitud de una aplicación de agente.

SNMP envía solicitudes y respuestas como mensajes SNMP. Un mensaje SNMP es una unidad de datos de protocolo SNMP (PDU) más elementos de encabezado de mensaje adicionales definidos por la RFC pertinente. Para obtener más información, vea [Acerca de los mensajes SNMP,](about-snmp-messages.md)Trabajar con listas de enlaces de [variables](working-with-variable-binding-lists.md) y Trabajar [con unidades de datos de protocolo.](working-with-protocol-data-units.md)

 

 




