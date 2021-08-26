---
description: Antes de implementar código que proteja las contraseñas, es mejor analizar su entorno en particular para ver las formas en que un atacante podría intentar traspasar las defensas de software.
ms.assetid: 4ebf7185-0179-4754-80da-63b0002c883f
title: Evaluación de amenazas de contraseña
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9042efa524b0503a648a195e77669b19231fec0445c4b0c8347b802b323076
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977155"
---
# <a name="password-threat-assessment"></a>Evaluación de amenazas de contraseña

Antes de implementar código que proteja las contraseñas, es mejor analizar su entorno en particular para ver las formas en que un atacante podría intentar traspasar las defensas de software.

Empiece por analizar la arquitectura de red o del sistema. Estos son algunos ejemplos:

-   Número de contraseñas que se deben proteger. ¿Se requiere una contraseña para iniciar sesión en el equipo local? ¿Se usa la misma contraseña para iniciar sesión en la red? ¿Las contraseñas se propagan a más de un servidor de la red? ¿Cuántas contraseñas se deben alojar?
-   Tipo de red (si hay alguna) que se usará. ¿La red se implementa mediante un sistema de directorios corporativos (como LDAP) y se usa su arquitectura de contraseña? ¿Hay objetos que almacenan contraseñas sin cifrar?
-   Red abierta frente a red cerrada. ¿La red es independiente o está abierta al exterior? Si es así, ¿está protegido por un firewall?
-   Acceso remoto. ¿Necesitarán los usuarios acceder a la red desde una ubicación remota?

Después de haber analizado la arquitectura del sistema o la red, puede empezar a analizar cómo un atacante podría intentar atacarlo. Estas son algunas posibilidades:

-   Leer una contraseña sin cifrar del registro de un equipo.
-   Lee una contraseña sin cifrar que está codificada de forma segura en el software.
-   Lee una contraseña sin cifrar de la página de códigos intercambiada de un equipo.
-   Lee una contraseña del registro de eventos de un programa.
-   Lea una contraseña de un esquema extendido de microsoft Active Directory de servicio de directorio que tiene objetos que contienen una contraseña de texto no cifrado.
-   Ejecute un depurador en un programa que requiera una contraseña.
-   Adivinar una contraseña. Se puede usar cualquiera de las diversas técnicas. Por ejemplo, es posible que el atacante conozca información personal sobre un usuario e intente adivinar una contraseña a partir de esa información (por ejemplo, el nombre de un padre, asociado o secundario). O bien, se puede probar un método de fuerza bruta, donde se prueban todas las combinaciones de letras, números y signos de puntuación (solo es factible cuando se usan contraseñas cortas).

La comparación de las posibles metodologías de ataque con la arquitectura del sistema o de la red probablemente revelará riesgos de seguridad. En ese momento, se puede establecer un factor de riesgo para cada riesgo y los factores de riesgo se pueden usar para realizar una evaluación de las correcciones.

 

 



