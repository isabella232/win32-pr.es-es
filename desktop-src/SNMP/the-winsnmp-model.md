---
title: El modelo WinSNMP
description: El modelo compatible con WinSNMP incluye los siguientes componentes básicos.
ms.assetid: 491df017-0b91-4fcf-97c3-4e296c3324bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7ae4fa1c1ee56fc534e4aa4c9bffefb8d7f4d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075378"
---
# <a name="the-winsnmp-model"></a>El modelo WinSNMP

El modelo compatible con WinSNMP incluye los siguientes componentes básicos:

-   Una aplicación de administración de red SNMP habilitada para WinSNMP, es decir, una *aplicación* compatible con WinSNMP
-   La capa de función WinSNMP
-   Un proveedor de servicios SNMP habilitado para WinSNMP, es decir, una *implementación* compatible con WinSNMP

Las aplicaciones de administración de red que deben transmitir mensajes SNMP funcionan de manera eficaz en un entorno orientado a eventos. Esto se debe a que SNMP es un protocolo basado en datagramas o sin conexión entre entidades remotas que no establecen circuitos virtuales.

Dado que las aplicaciones de Microsoft Windows también están orientadas a eventos, WinSNMP usa un modelo de programación en el que la recepción y el procesamiento de las aplicaciones de administración de la unidad de *eventos de mensajes* asincrónicos. Un evento de mensaje asincrónico puede ser una solicitud de operación SNMP por parte de una aplicación de administrador o la respuesta a una solicitud de una aplicación de agente.

SNMP envía solicitudes y respuestas como mensajes SNMP. Un mensaje SNMP es una unidad de datos de protocolo SNMP (PDU) más elementos de encabezado de mensaje adicionales definidos por la RFC correspondiente. Para obtener más información, consulte [About SNMP messages](about-snmp-messages.md), [Working with variables Binding lists](working-with-variable-binding-lists.md) and [Working with Protocol Data Units](working-with-protocol-data-units.md).

 

 




