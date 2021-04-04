---
description: La técnica de autenticación de clave secreta no explica cómo el cliente y el servidor obtienen la clave de sesión secreta que se utiliza en las sesiones entre sí.
ms.assetid: 90ab0359-5079-49e9-809c-0c0005cc61bf
title: Distribución de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f04a2968e8b7b978bc7b325d65b4a2acf08e1f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814371"
---
# <a name="key-distribution"></a>Distribución de claves

La técnica de autenticación de clave secreta no explica cómo el cliente y el servidor obtienen la [*clave de sesión*](../secgloss/s-gly.md) secreta que se utiliza en las sesiones entre sí. Si son personas, pueden reunirse en secreto y aceptar la clave. Pero si el cliente es un programa que se ejecuta en una estación de trabajo y el servidor es un servicio que se ejecuta en un servidor de red, ese método no funcionará.

Un cliente querrá comunicarse con muchos servidores y necesitará claves diferentes para cada uno de ellos. Un servidor se comunica con muchos clientes y necesita claves diferentes para cada uno de ellos. Si cada cliente necesita una clave diferente para cada servidor y cada servidor necesita una clave diferente para cada cliente, la distribución de claves se convierte en un problema. Además, la necesidad de almacenar y proteger muchas claves en muchos equipos crea un riesgo de seguridad enorme.

El nombre del [*protocolo Kerberos*](../secgloss/k-gly.md) sugiere su solución al problema de distribución de claves. Kerberos (o Cerberus) fue una figura en la mitología griega clásica, un perro de tres puntas y un paso prolongado que mantuvo a los intrusos en el mundo. Como la protección de mitos, el protocolo Kerberos tiene tres cabezas: un cliente, un servidor y un tercero de confianza para mediar entre ellos. El intermediario de confianza de este protocolo es el Centro de distribución de claves (KDC).

El KDC es un servicio que se ejecuta en un servidor protegido físicamente. Mantiene una base de datos con información de cuenta para todas las [*entidades de seguridad*](../secgloss/s-gly.md) de su dominio Kerberos. Un dominio Kerberos es el equivalente de Kerberos de un dominio en Windows.

Junto con otra información acerca de cada entidad de seguridad, el KDC almacena una clave criptográfica conocida únicamente para el servidor principal y el KDC. Esta es la [*clave maestra*](../secgloss/m-gly.md) que se usa en los intercambios entre cada entidad de seguridad y el KDC. En la mayoría de las implementaciones del protocolo Kerberos, esta clave maestra se deriva usando una función [*hash*](../secgloss/h-gly.md) de la contraseña de una entidad de seguridad.

Cuando un cliente desea crear una conexión segura con un servidor, el cliente comienza enviando una solicitud al KDC, no al servidor al que desea tener acceso. El KDC crea y envía al cliente una clave de [*sesión*](../secgloss/s-gly.md) única para el cliente y un servidor que se utiliza para autenticarse entre sí. El KDC tiene acceso tanto a la clave maestra del cliente como a la clave maestra del servidor. El KDC cifra la copia del servidor de la clave de sesión mediante la clave maestra del servidor y la copia del cliente mediante la clave maestra del cliente.

El KDC podría cumplir su rol como intermediario de confianza enviando la clave de sesión directamente a cada una de las entidades de seguridad implicadas, pero en la práctica este procedimiento no funcionará, por una serie de motivos. En su lugar, el KDC envía al cliente ambas claves de sesión cifrada. La clave de sesión del servidor se incluye en un [vale de sesión](session-tickets.md).

 

 
