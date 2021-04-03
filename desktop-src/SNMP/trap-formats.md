---
title: Formatos de captura
description: El formato de las PDU de captura es diferente del de otras PDU. El formato de las capturas de SNMPv1 y las capturas de SNMPv2C también es diferente.
ms.assetid: 2d2b4520-28b7-4a2e-8dee-456e17d9d6f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87adc3222808fcc7e81904ade07c09afa13bc6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075377"
---
# <a name="trap-formats"></a>Formatos de captura

El formato de las PDU de captura es diferente del de otras PDU. El formato de las capturas de SNMPv1 y las capturas de SNMPv2C también es diferente.

En el marco de SNMPv2C, el formato de reventado de PDU es una lista de enlaces variables de *n* entradas de enlace variable organizadas de la siguiente manera:

-   La primera entrada de enlace de variable contiene una marca de tiempo.
-   La segunda entrada de enlace de variables es un identificador de objeto que identifica la captura.
-   Las demás entradas de enlace de variables, si están presentes, contienen información adicional *asociada a la* captura.

En la plataforma SNMPv1, el formato de la captura PDU es el siguiente.

| Campo                      | Descripción                                                      |
|----------------------------|------------------------------------------------------------------|
| empresa                 | Identifica el tipo de dispositivo que generó la captura.           |
| Agent-addr                 | Identifica la dirección IP del dispositivo que generó la captura. |
| captura de tipos genéricos y de captura específica | Identifica un tipo de captura predefinido.                               |
| marca de tiempo                 | Identifica Cuándo se generó la captura.                          |
| enlaces de variables          | Contiene información adicional asociada a la captura.        |



 

La función [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) siempre devuelve un mensaje en el formato SNMPv2c. Si el mensaje contiene el tipo de **operación \_ \_ captura de PDU de SNMP**, la aplicación puede leer las entradas de enlace de variables del mensaje y recuperar la información asociada a la captura.

 

 




