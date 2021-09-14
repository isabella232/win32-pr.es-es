---
description: Antes de implementar código que protege las contraseñas, es mejor analizar el entorno en particular para ver las formas en que un atacante podría intentar penetrar las defensas de software.
ms.assetid: 4ebf7185-0179-4754-80da-63b0002c883f
title: Evaluación de amenazas de contraseña
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48a79d44bda9714083c5dd1085e9d09497e7341
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253629"
---
# <a name="password-threat-assessment"></a>Evaluación de amenazas de contraseña

Antes de implementar código que protege las contraseñas, es mejor analizar el entorno en particular para ver las formas en que un atacante podría intentar penetrar las defensas de software.

Empiece por analizar la arquitectura de red o del sistema. Estos son algunos ejemplos:

-   Número de contraseñas que se deben proteger. ¿Se requiere una contraseña para iniciar sesión en el equipo local? ¿Se usa la misma contraseña para iniciar sesión en la red? ¿Las contraseñas se propagan a más de un servidor de la red? ¿Cuántas contraseñas se deben alojar?
-   Tipo de red (si hay alguna) que se usará. ¿La red se implementa mediante un sistema de directorios corporativos (como LDAP) y se usa su arquitectura de contraseña? ¿Hay algún objeto que almacene contraseñas sin cifrar?
-   Red abierta frente a red cerrada. ¿La red es independiente o está abierta al exterior? Si es así, ¿está protegido por un firewall?
-   Acceso remoto. ¿Necesitarán los usuarios acceder a la red desde una ubicación remota?

Después de haber analizado la arquitectura del sistema o de la red, puede empezar a analizar cómo un atacante podría intentar atacarlo. Estas son algunas posibilidades:

-   Lee una contraseña sin cifrar del registro de un equipo.
-   Lea una contraseña sin cifrar codificada de forma segura en el software.
-   Lee una contraseña sin cifrar de la página de códigos intercambiada de un equipo.
-   Lee una contraseña del registro de eventos de un programa.
-   Lea una contraseña de un esquema extendido de microsoft Active Directory servicio de directorio que tenga objetos que contengan una contraseña de texto no cifrado.
-   Ejecute un depurador en un programa que requiera una contraseña.
-   Adivinar una contraseña. Se puede usar cualquiera de las distintas técnicas. Por ejemplo, el atacante podría conocer información personal sobre un usuario e intentar adivinar una contraseña a partir de esa información (por ejemplo, el nombre de un hijo, un compañero o un hijo). O bien, se puede probar un método de fuerza bruta, donde se prueban todas las combinaciones de letras, números y signos de puntuación (solo es factible cuando se usan contraseñas cortas).

La comparación de las posibles metodologías de ataque con la arquitectura del sistema o de la red probablemente revelará riesgos de seguridad. En ese momento, se puede establecer un factor de riesgo para cada riesgo y los factores de riesgo se pueden usar para realizar una evaluación de las correcciones.

 

 



