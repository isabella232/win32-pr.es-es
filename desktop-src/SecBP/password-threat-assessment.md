---
description: Antes de implementar el código que protege las contraseñas, es mejor analizar su entorno concreto para conocer las maneras en las que un atacante podría intentar penetrar las defensas de software.
ms.assetid: 4ebf7185-0179-4754-80da-63b0002c883f
title: Evaluación de amenazas de contraseñas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48a79d44bda9714083c5dd1085e9d09497e7341
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669831"
---
# <a name="password-threat-assessment"></a>Evaluación de amenazas de contraseñas

Antes de implementar el código que protege las contraseñas, es mejor analizar su entorno concreto para conocer las maneras en las que un atacante podría intentar penetrar las defensas de software.

Empiece por analizar la arquitectura de red o del sistema. Estos son algunos ejemplos:

-   El número de contraseñas que se deben proteger. ¿Es necesaria una contraseña para iniciar sesión en el equipo local? ¿Se usa la misma contraseña para iniciar sesión en la red? ¿Se propagan las contraseñas a más de un servidor de la red? ¿Cuántas contraseñas se deben acomodar?
-   El tipo de red (si existe) que se va a usar. ¿Se implementa la red mediante un sistema de directorio corporativo (como LDAP) y se usa su arquitectura de contraseña? ¿Los objetos almacenan contraseñas sin cifrar?
-   Red abierta frente a cerrada. ¿La red es independiente o está abierta al exterior? Si es así, ¿está protegido por un firewall?
-   Acceso remoto. ¿Los usuarios deberán tener acceso a la red desde una ubicación remota?

Después de haber analizado el sistema o la arquitectura de red, puede empezar a analizar cómo un atacante podría intentar atacarlo. Estas son algunas posibilidades:

-   Leer una contraseña no cifrada del registro de un equipo.
-   Lea una contraseña no cifrada que esté codificada de forma rígida en el software.
-   Lea una contraseña no cifrada de la página de códigos de intercambio de un equipo.
-   Leer una contraseña del registro de eventos de un programa.
-   Lea una contraseña de un esquema de servicio de directorio extendido de Microsoft Active Directory que tenga objetos que contengan una contraseña de texto sin formato.
-   Ejecutar un depurador en un programa que requiera una contraseña.
-   Adivinar una contraseña. Puede usarse cualquiera de las diversas técnicas. Por ejemplo, el atacante podría conocer información personal sobre un usuario e intentar adivinar una contraseña de esa información (por ejemplo, el nombre de un cónyuge o socio o hijo). O bien, se puede probar un método de fuerza bruta, donde se intentan todas las combinaciones de letras, números y signos de puntuación (solo es factible donde se usan contraseñas cortas).

Comparar las posibles metodologías de ataque con la arquitectura de red o del sistema probablemente revelará riesgos de seguridad. En ese momento, se puede establecer un factor de riesgo para cada riesgo y los factores de riesgo se pueden usar para evaluar las correcciones.

 

 



