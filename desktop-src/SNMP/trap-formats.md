---
title: Formatos de captura
description: El formato de las PDU de captura es diferente del de otras PDU. El formato de las capturas SNMPv1 y las capturas de SNMPv2C también es diferente.
ms.assetid: 2d2b4520-28b7-4a2e-8dee-456e17d9d6f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b73e9cd2a5396bbe258fcb67c88cc207ea0243a9e8aff9f31e4866b9ee8adcc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885685"
---
# <a name="trap-formats"></a>Formatos de captura

El formato de las PDU de captura es diferente del de otras PDU. El formato de las capturas SNMPv1 y las capturas de SNMPv2C también es diferente.

En el marco SNMPv2C, el formato de captura de PDU es una lista de enlace de variables de *n* entradas de enlace de variables organizadas de la siguiente manera:

-   La primera entrada de enlace de variable contiene una marca de tiempo.
-   La segunda entrada de enlace de variable es un identificador de objeto que identifica la captura.
-   Las entradas de enlace de variables de la tercera a *n,* si están presentes, contienen información adicional asociada a la captura.

En el marco SNMPv1, el formato de captura de PDU es el siguiente.

| Campo                      | Descripción                                                      |
|----------------------------|------------------------------------------------------------------|
| empresa                 | Identifica el tipo de dispositivo que generó la captura.           |
| agent-addr                 | Identifica la dirección IP del dispositivo que generó la captura. |
| generic-trap/specific-trap | Identifica un tipo de captura predefinido.                               |
| marca de tiempo                 | Identifica cuándo se generó la captura.                          |
| enlaces de variables          | Contiene información adicional asociada a la captura.        |



 

La [**función SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) siempre devuelve un mensaje en formato SNMPv2C. Si el mensaje contiene el tipo de operación **\_ SNMP PDU \_ TRAP**, la aplicación puede leer las entradas de enlace de variables del mensaje y recuperar la información asociada a la captura.

 

 




