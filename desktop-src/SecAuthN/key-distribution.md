---
description: La técnica de autenticación de clave secreta no explica cómo el cliente y el servidor obtienen la clave de sesión secreta para usarla en sesiones entre sí.
ms.assetid: 90ab0359-5079-49e9-809c-0c0005cc61bf
title: Distribución de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd39f9cd5e219ac1e6339c0a6c3e7b9a19dc2680c21e948bdb979af791719a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013335"
---
# <a name="key-distribution"></a>Distribución de claves

La técnica de autenticación de clave secreta no explica cómo el cliente y el servidor obtienen la clave de [*sesión*](../secgloss/s-gly.md) secreta para usarla en sesiones entre sí. Si son personas, podrían reunirse en secreto y acordar la clave. Pero si el cliente es un programa que se ejecuta en una estación de trabajo y el servidor es un servicio que se ejecuta en un servidor de red, ese método no funcionará.

Un cliente querrá comunicarse con muchos servidores y necesitará claves diferentes para cada uno de ellos. Un servidor se comunica con muchos clientes y también necesita claves diferentes para cada uno de ellos. Si cada cliente necesita una clave diferente para cada servidor y cada servidor necesita una clave diferente para cada cliente, la distribución de claves se convierte en un problema. Además, la necesidad de almacenar y proteger muchas claves en muchos equipos crea un riesgo de seguridad enorme.

El nombre del protocolo [*Kerberos sugiere*](../secgloss/k-gly.md) su solución al problema de distribución de claves. Kerberos (o Cerberus) era una figura en el clásico griego, un perro de tres cabezas e infieres que no dejaban de entrar en el subgobernador. Al igual que la mítica protección, el protocolo Kerberos tiene tres caras: un cliente, un servidor y un tercero de confianza para mediar entre ellos. El intermediario de confianza en este protocolo es el Centro de distribución de claves (KDC).

El KDC es un servicio que se ejecuta en un servidor físicamente seguro. Mantiene una base de datos con información de cuenta para todas las [*entidades de seguridad*](../secgloss/s-gly.md) de su dominio. Un dominio kerberos es el equivalente de Kerberos de un dominio en Windows.

Junto con otra información sobre cada entidad de seguridad, el KDC almacena una clave criptográfica conocida solo para la entidad de seguridad y el KDC. Esta es la [*clave maestra que se*](../secgloss/m-gly.md) usa en los intercambios entre cada entidad de seguridad y el KDC. En la mayoría de las implementaciones del protocolo Kerberos, esta clave maestra se deriva mediante una [*función hash*](../secgloss/h-gly.md) de la contraseña de una entidad de seguridad.

Cuando un cliente quiere crear una conexión segura con un servidor, el cliente comienza enviando una solicitud al KDC, no al servidor al que quiere llegar. El KDC crea y envía al cliente una clave de sesión [*única*](../secgloss/s-gly.md) para que el cliente y un servidor lo usen para autenticarse entre sí. El KDC tiene acceso a la clave maestra del cliente y a la clave maestra del servidor. El KDC cifra la copia del servidor de la clave de sesión mediante la clave maestra del servidor y la copia del cliente mediante la clave maestra del cliente.

El KDC podría cumplir su rol como intermediario de confianza mediante el envío de la clave de sesión directamente a cada una de las entidades de seguridad implicadas, pero en la práctica este procedimiento no funcionará, por diversos motivos. En su lugar, el KDC envía ambas claves de sesión cifradas al cliente. La clave de sesión para el servidor se incluye en un vale [de sesión](session-tickets.md).

 

 
