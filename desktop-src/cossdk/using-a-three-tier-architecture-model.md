---
description: El modelo de arquitectura de tres niveles, que es el marco fundamental para el modelo de diseño lógico, segmenta los componentes de una aplicación en tres niveles de servicios.
ms.assetid: a03327c1-e427-4c07-b3d4-808ce81c2c96
title: Usar un modelo Three-Tier arquitectura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bd08ee1363504c610ed650d59b3837d292fb3a1d447c882dbd39ddba6229503
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546062"
---
# <a name="using-a-three-tier-architecture-model"></a>Usar un modelo Three-Tier arquitectura

El modelo de arquitectura de tres niveles, que es el marco fundamental para el modelo de diseño [lógico,](the-logical-model--application-definition-and-planning.md)segmenta los componentes de una aplicación en tres niveles de servicios. Estos niveles no se corresponden necesariamente con ubicaciones físicas en varios equipos de una red, sino con capas lógicas de la aplicación. La forma en que las partes de una aplicación se distribuyen en una topología física puede cambiar, en función de los requisitos del sistema.

A continuación se descripciones breves de los servicios asignados a cada nivel:

-   **El nivel de presentación, o capa de servicios de usuario, proporciona a un usuario acceso a la aplicación.** Esta capa presenta los datos al usuario y, opcionalmente, permite la manipulación de datos y la entrada de datos. Los dos tipos principales de interfaz de usuario para esta capa son la aplicación tradicional y la aplicación basada en web. Las aplicaciones basadas en web ahora suelen contener la mayoría de las características de manipulación de datos que usan las aplicaciones tradicionales. Esto se logra mediante el uso de html dinámico y orígenes de datos del lado cliente y cursores de datos.

    > [!Note]  
    > En una aplicación de tres niveles, la aplicación del lado cliente será más clara que una aplicación cliente-servidor porque no contendrá los componentes de servicio que se encuentran ahora en el nivel intermedio. Esto da como resultado una menor sobrecarga para el usuario, pero más tráfico de red para el sistema porque los componentes se distribuyen entre diferentes máquinas.

     

-   **El nivel intermedio, o capa de servicios empresariales, consta de reglas de negocio y de datos.** También conocido como el nivel de lógica de negocios *,* el nivel intermedio es donde los desarrolladores de COM+ pueden resolver problemas empresariales críticos y lograr importantes ventajas de productividad. Los componentes que conste de esta capa pueden existir en un equipo servidor para ayudar a compartir recursos. Estos componentes se pueden usar para aplicar reglas de negocios, como algoritmos empresariales y regulaciones legales o gubernamentales, y reglas de datos, que están diseñadas para mantener la coherencia de las estructuras de datos dentro de bases de datos específicas o múltiples. Dado que estos componentes de nivel intermedio no están asociados a un cliente específico, todas las aplicaciones pueden usar estos componentes y se pueden mover a ubicaciones diferentes, como requiere el tiempo de respuesta y otras reglas. Por ejemplo, se pueden realizar modificaciones sencillas en el lado cliente para minimizar los recorridos de ida y vuelta de red, o bien se pueden colocar reglas de datos en procedimientos almacenados.

-   **La capa de datos, o capa de servicios de datos, interactúa con los datos persistentes almacenados normalmente en una base de datos o en un almacenamiento permanente.** Esta es la capa de acceso de DBMS real. Se puede acceder a él a través de la capa de servicios empresariales y, en ocasiones, mediante la capa de servicios de usuario. Esta capa consta de componentes de acceso a datos (en lugar de conexiones DBMS sin procesar) para ayudar en el uso compartido de recursos y para permitir que los clientes se configuren sin instalar las bibliotecas de DBMS y los controladores ODBC en cada cliente.

Durante el ciclo de vida de una aplicación, el enfoque de tres niveles proporciona ventajas como la reusabilidad, la flexibilidad, la manejabilidad, el mantenimiento y la escalabilidad. Puede compartir y reutilizar los componentes y servicios que cree, y puede distribuirlos a través de una red de equipos según sea necesario. Puede dividir proyectos grandes y complejos en proyectos más sencillos y asignarlos a distintos programadores o equipos de programación. También puede implementar componentes y servicios en un servidor para ayudar a mantenerse al día con los cambios, y puede volver a implementarlos a medida que aumenta el crecimiento de la base de usuarios, los datos y el volumen de transacciones de la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[El modelo lógico: definición y planeamiento de la aplicación](the-logical-model--application-definition-and-planning.md)
</dt> </dl>

 

 



