---
description: 'El segundo paso de un proceso de diseño de aplicaciones COM+ es dividir el modelo conceptual en los niveles lógicos de la arquitectura de tres niveles: el nivel de presentación o los servicios de usuario. el nivel intermedio, o servicios empresariales; y la capa de datos o los servicios de datos. Si no está familiarizado con la arquitectura de tres niveles, consulte Uso de un modelo Three-Tier arquitectura.'
ms.assetid: 6dc0a0ab-2cfa-4cc9-92a6-0d7554dd3397
title: 'El modelo lógico: definición y planeamiento de la aplicación'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d19a493ebdacebac27edd291e747b5c42612f5fffd3ac7ea489f99b41de272b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120335"
---
# <a name="the-logical-model-application-definition-and-planning"></a>El modelo lógico: definición y planeamiento de la aplicación

El segundo paso de un proceso de diseño de aplicaciones COM+ es dividir el modelo conceptual en los niveles lógicos de la arquitectura de tres niveles: el nivel de presentación *o* los servicios de usuario. el *nivel intermedio*, o servicios empresariales; y la *capa de datos*, o los servicios de datos. Si no está familiarizado con la arquitectura de tres niveles, consulte Using a Three-Tier Architecture Model (Uso de [un modelo de arquitectura de Three-Tier estándar).](using-a-three-tier-architecture-model.md)

Para comenzar este proceso, busque nombres y verbos en el modelo conceptual. Los nombres a menudo se pueden traducir en objetos empresariales (clases) y los verbos asociados a ellos pueden traducirse en acciones (métodos de las clases). Aunque puede ser difícil definir todos los nombres como objetos empresariales, las omisións o los errores se volverán obvios cuando complete el modelo lógico.

La mayoría de los objetos empresariales terminarán en el nivel de servicios empresariales, con los objetos restantes divididos entre los objetos de interfaz de usuario en el nivel de servicios de usuario y los objetos de datos en el nivel de servicios de datos. Al crear un modelo lógico con la arquitectura de tres niveles, tenga en cuenta lo siguiente:

-   Algunos de los nombres del diseño conceptual no representarán fragmentos físicos reales de datos, sino que pueden representar una acción en el sistema o en el rol de un objeto empresarial en el sistema. Un objeto empresarial también puede ser un servicio que realiza algún tipo de control del sistema, como un identificador de inicio de sesión para la seguridad.
-   Evite crear objetos empresariales imprecisos "leyendo entre líneas" en el [modelo conceptual](the-conceptual-model--application-requirements.md). Es posible que estos objetos empresariales no sean correctos y debe considerarlos cuidadosamente antes de incluirlos en el modelo lógico. Si parecen correctos, agrégrelos al modelo conceptual explícitamente.
-   Evite crear objetos empresariales que expresan la misma información o función; La duplicación puede ser costosa en términos de velocidad y rendimiento de la aplicación.
-   Determine las dependencias de objetos. Algunos nombres del modelo conceptual pueden ser simplemente atributos de otros objetos empresariales. Decida si el atributo puede existir de forma independiente. Si es así, debe convertirse en su propio objeto empresarial; Si no es así, debe combinarse con el objeto de negocio adecuado.
-   Evite crear objetos empresariales que intenten hacer demasiado. Sobrecargar objetos empresariales puede significar más tiempo dedicado a separar el código más adelante y puede ser un problema de mantenimiento. No se deben combinar objetos distintos en el modelo conceptual; deben permanecer objetos empresariales independientes. Puede controlar cualquier similitud mediante el código para delegar sus funciones comunes en un objeto empresarial.
-   Quite los objetos empresariales que no se usan en ningún escenario de uso. Si los objetos están diseñados para dar cabida al crecimiento futuro, considere la posibilidad de implementarlos una vez completada la aplicación inicial.

En este punto, puede empezar a pensar en términos de los equipos y el código. A partir de estos servicios empresariales, determine la funcionalidad de pantalla y entrada que debe proporcionar como servicios de usuario. Defina qué tablas y procedimientos almacenados deben proporcionarse como servicios de datos. Para completar el modelo lógico, defina las interfaces de cada servicio e incluya definiciones de cada campo de datos y sus reglas de validación. Incluya también todas las funciones, su sintaxis y sus parámetros.

La definición de servicio o objeto no debe incluir ningún aspecto de la implementación física. La intención es proporcionar una guía clara para que los generadores de componentes lógicos trabajen desde y permitir que otros programadores codimenten partes de la aplicación que pueden usar el componente antes de que se complete realmente. En el diseño del modelo lógico, debe documentar cada pantalla, función y objeto. No continúe con el modelo físico o la implementación hasta que cumpla estos criterios. Si continúa mientras el modelo conceptual y el modelo lógico no están de acuerdo, tendrá problemas graves más adelante en el ciclo de desarrollo.

El desarrollo incremental de una aplicación COM+ es habitual. Esto implica crear un subconjunto de los componentes finales conocidos y probarlos a través de cada capa de la aplicación: niveles de cliente, negocio y datos, hasta el almacenamiento de datos. Este modelo de trabajo proporciona información sobre los requisitos adicionales por parte del cliente y las consideraciones de implementación. A menudo, este modelo de trabajo se prueba en un solo equipo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo conceptual: requisitos de la aplicación](the-conceptual-model--application-requirements.md)
</dt> <dt>

[Modelo físico: arquitectura de aplicación](the-physical-model--application-architecture.md)
</dt> <dt>

[Usar un modelo Three-Tier arquitectura](using-a-three-tier-architecture-model.md)
</dt> </dl>

 

 



