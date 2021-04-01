---
description: 'El segundo paso de un proceso de diseño de aplicaciones COM+ es dividir el modelo conceptual en los niveles lógicos de la arquitectura de tres niveles: el nivel de presentación o los servicios de usuario; el nivel intermedio o servicios empresariales; y el nivel de datos o Data Services. Si no está familiarizado con la arquitectura de tres niveles, consulte uso de un modelo de arquitectura de Three-Tier.'
ms.assetid: 6dc0a0ab-2cfa-4cc9-92a6-0d7554dd3397
title: 'El modelo lógico: definición y planeación de la aplicación'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acb09b0d377fcd9bf5e2319868f4006b5dbfce75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153459"
---
# <a name="the-logical-model-application-definition-and-planning"></a>El modelo lógico: definición y planeación de la aplicación

El segundo paso de un proceso de diseño de aplicaciones COM+ es dividir el modelo conceptual en los niveles lógicos de la arquitectura de tres niveles: el *nivel de presentación* o los servicios de usuario; el *nivel intermedio* o servicios empresariales; y el *nivel de datos* o Data Services. Si no está familiarizado con la arquitectura de tres niveles, consulte [uso de un modelo de arquitectura de Three-Tier](using-a-three-tier-architecture-model.md).

Comience este proceso examinando el modelo conceptual para nombres y verbos. A menudo, los nombres se pueden traducir en objetos comerciales (clases) y los verbos asociados a ellos pueden traducirse en acciones (métodos de las clases). Aunque puede ser difícil definir todos los nombres como objetos de negocio, las omisiones o los errores se verán obvios en el momento en que se completa el modelo lógico.

La mayoría de los objetos empresariales terminarán en el nivel de servicios empresariales, con los objetos restantes divididos entre los objetos de la interfaz de usuario en el nivel de servicios de usuario y los objetos de datos en el nivel de servicios de datos. Al crear un modelo lógico con la arquitectura de tres niveles, tenga en cuenta lo siguiente:

-   Algunos de los nombres del diseño conceptual no representarán partes físicas reales de los datos, pero pueden representar una acción en el sistema o en el rol de un objeto comercial en el sistema. Un objeto comercial también puede ser un servicio que realiza algún tipo de control del sistema, como un identificador de inicio de sesión para la seguridad.
-   Evite crear objetos comerciales imprecisos "leyendo entre las líneas" en el [modelo conceptual](the-conceptual-model--application-requirements.md). Es posible que estos objetos comerciales no sean correctos y debe considerarlos detenidamente antes de incluirlos en el modelo lógico. Si parecen correctos, agréguelos explícitamente al modelo conceptual.
-   Evite crear objetos comerciales que expresen la misma información o función; la duplicación puede ser costosa en términos de rendimiento y velocidad de la aplicación.
-   Determinar las dependencias de los objetos. Algunos nombres del modelo conceptual pueden ser simplemente atributos de otros objetos comerciales. Decida si el atributo puede existir de forma independiente. Si es así, debe convertirse en su propio objeto comercial; en caso contrario, debe combinarse con el objeto comercial adecuado.
-   Evite crear objetos comerciales que intenten hacer demasiado. La sobrecarga de objetos empresariales puede significar más tiempo para separar el código más adelante y puede ser un dolor de cabeza. No se deben combinar objetos distintos en el modelo conceptual; deben seguir siendo objetos comerciales independientes. Puede controlar cualquier similitud mediante el uso de código para delegar sus funciones comunes a un objeto comercial.
-   Quite cualquier objeto comercial que no se use en ningún escenario de uso. Si los objetos están diseñados para adaptarse al crecimiento futuro, considere la posibilidad de implementarlos una vez completada la aplicación inicial.

Llegados a este punto, puede empezar a pensar en los equipos y el código. En estos servicios empresariales, determine la funcionalidad de entrada y visualización que necesita proporcionar como servicios de usuario. Defina qué tablas y procedimientos almacenados deben proporcionarse como servicios de datos. Para completar el modelo lógico, defina las interfaces para cada servicio e incluya las definiciones de cada campo de datos y sus reglas de validación. También incluye todas las funciones, su sintaxis y sus parámetros.

La definición del servicio o del objeto no debe incluir ningún aspecto de la implementación física. La intención es proporcionar una instrucción clara para que los generadores de componentes lógicos trabajen desde y para permitir que otros programadores codifiquen partes de la aplicación que puedan usar el componente antes de que se complete realmente. En el diseño del modelo lógico, debe documentar cada pantalla, función y objeto. No continúe con el modelo físico o la implementación hasta que cumpla estos criterios. Si continúa mientras el modelo conceptual y el modelo lógico no están en acuerdo, tendrá problemas graves más adelante en el ciclo de desarrollo.

Es habitual el desarrollo incremental de una aplicación COM+. Esto implica crear un subconjunto de los componentes finales y conocidos y probarlos a través de cada capa de la aplicación: las capas de cliente, empresa y datos, a través del almacenamiento de datos. Este modelo de trabajo proporciona información sobre los requisitos adicionales por parte del cliente y las consideraciones de implementación. A menudo, este modelo de trabajo se prueba en un único equipo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[El modelo conceptual: requisitos de la aplicación](the-conceptual-model--application-requirements.md)
</dt> <dt>

[El modelo físico: arquitectura de la aplicación](the-physical-model--application-architecture.md)
</dt> <dt>

[Usar un modelo de arquitectura de Three-Tier](using-a-three-tier-architecture-model.md)
</dt> </dl>

 

 



