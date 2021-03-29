---
description: El modelo de arquitectura de tres niveles, que es el marco fundamental para el modelo de diseño lógico, divide los componentes de las aplicaciones en tres niveles de servicios.
ms.assetid: a03327c1-e427-4c07-b3d4-808ce81c2c96
title: Usar un modelo de arquitectura de Three-Tier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20b765a6d103f3c349ffd9a44853f495c64a070
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423456"
---
# <a name="using-a-three-tier-architecture-model"></a>Usar un modelo de arquitectura de Three-Tier

El modelo de arquitectura de tres niveles, que es el marco fundamental para el [modelo de diseño lógico](the-logical-model--application-definition-and-planning.md), segmenta los componentes de una aplicación en tres niveles de servicios. Estos niveles no corresponden necesariamente a ubicaciones físicas en varios equipos de una red, sino a capas lógicas de la aplicación. La forma en que se distribuyen las partes de una aplicación en una topología física puede cambiar en función de los requisitos del sistema.

A continuación se muestran breves descripciones de los servicios asignados a cada nivel:

-   **El nivel de presentación o el nivel de servicios de usuario proporciona a un usuario acceso a la aplicación.** Este nivel presenta los datos al usuario y, opcionalmente, permite la manipulación de datos y la entrada de datos. Los dos tipos principales de interfaz de usuario para esta capa son la aplicación tradicional y la aplicación basada en Web. Las aplicaciones basadas en web ahora suelen contener la mayoría de las características de manipulación de datos que usan las aplicaciones tradicionales. Esto se logra mediante el uso de HTML dinámicos y de los orígenes de datos y los cursores de datos del lado cliente.

    > [!Note]  
    > En una aplicación de tres niveles, la aplicación del lado cliente será skinnier que una aplicación cliente-servidor, ya que no contendrá los componentes del servicio que se encuentran ahora en el nivel intermedio. Esto produce menos sobrecarga para el usuario, pero más tráfico de red para el sistema porque los componentes se distribuyen entre diferentes equipos.

     

-   **El nivel intermedio, o el nivel de servicios empresariales, consta de reglas empresariales y de datos.** También conocido como el *nivel de lógica de negocios*, el nivel intermedio es donde los desarrolladores de com+ pueden resolver problemas empresariales críticos y lograr importantes ventajas de productividad. Los componentes que constituyen esta capa pueden existir en un equipo servidor para facilitar el uso compartido de recursos. Estos componentes se pueden usar para aplicar reglas de negocios, como algoritmos empresariales y reglamentos legales o gubernamentales, y reglas de datos, que están diseñadas para mantener la coherencia de las estructuras de datos en bases de datos específicas o varias. Dado que estos componentes de nivel intermedio no están asociados a un cliente específico, pueden ser utilizados por todas las aplicaciones y pueden moverse a ubicaciones diferentes, ya que el tiempo de respuesta y otras reglas requieren. Por ejemplo, se pueden colocar ediciones simples en el lado cliente para minimizar los recorridos de ida y vuelta de red, o bien las reglas de datos se pueden colocar en procedimientos almacenados.

-   **La capa de datos o el nivel de servicios de datos interactúa con los datos persistentes almacenados normalmente en una base de datos o en un almacenamiento permanente.** Esta es la capa de acceso de DBMS real. Se puede tener acceso a ella a través del nivel de servicios empresariales y, en ocasiones, por parte de los servicios de usuario. Este nivel consta de componentes de acceso a datos (en lugar de conexiones DBMS sin formato) para ayudar en el uso compartido de recursos y para permitir que los clientes se configuren sin necesidad de instalar las bibliotecas DBMS y los controladores ODBC en cada cliente.

Durante el ciclo de vida de una aplicación, el enfoque de tres niveles ofrece ventajas como la reutilización, la flexibilidad, la facilidad de uso, el mantenimiento y la escalabilidad. Puede compartir y reutilizar los componentes y servicios que cree, y puede distribuirlos a través de una red de equipos según sea necesario. Puede dividir proyectos grandes y complejos en proyectos más sencillos y asignarlos a distintos programadores o equipos de programación. También puede implementar componentes y servicios en un servidor para ayudar a mantenerse al día de los cambios, y puede volver a implementarlos a medida que aumenta la base de usuarios, los datos y el volumen de transacciones de la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[El modelo lógico: definición y planeación de la aplicación](the-logical-model--application-definition-and-planning.md)
</dt> </dl>

 

 



