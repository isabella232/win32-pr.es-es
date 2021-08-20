---
description: La escalabilidad es la capacidad de una aplicación para dar servicio a una carga adicional con un aumento lineal en el uso de recursos.
ms.assetid: 8249f1af-9c96-4545-ad6a-3736c6e63c6d
title: Diseño para escalabilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 344e4ce9afcc5f55430550d3ec71c5b56f0f5a4e15b29ef5ea86cea407aeb750
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118102288"
---
# <a name="designing-for-scalability"></a>Diseño para escalabilidad

La escalabilidad es la capacidad de una aplicación para dar servicio a una carga adicional con un aumento lineal en el uso de recursos. La escalabilidad es importante en cualquier aplicación distribuida. Los límites de escalabilidad suelen estar centrados en el uso de recursos y las dependencias creadas accidentalmente en el diseño de la aplicación.

En la lista siguiente se describen los problemas de escalabilidad y se sugieren soluciones:

-   Recursos dentro del equipo. El número de subprocesos y memoria disponibles puede limitar la escalabilidad. Use un modelo de subprocesamiento que sea más eficaz para la aplicación.
-   Recursos entre equipos. El número de equipos disponibles para distribuir la carga de trabajo de la aplicación puede afectar a la escalabilidad.
-   Afinidad de cliente. Una aplicación puede crear involuntariamente dos situaciones de afinidad: una situación en la que la aplicación depende del estado de los datos que el cliente envía con su solicitud; y una situación en la que la aplicación requiere un estado específico del cliente. Evite diseñar la dependencia de estado entre el cliente y la aplicación.
-   Afinidad de servidor. Una aplicación COM+ puede limitar su escalabilidad mediante la creación de una afinidad de servidor, donde la aplicación depende de ir a un equipo servidor determinado para obtener información. Esta afinidad puede producirse con muchas aplicaciones orientadas a bases de datos. La mejor manera de evitar un cuello de botella de afinidad de servidor es particionar datos en varios equipos servidor. Por ejemplo, divida los datos de cliente entre servidores por la clave a la que se accede con más frecuencia o abarque una base de datos de cliente en varios servidores con el apellido del cliente (por ejemplo, Server1: a-f, Server2: g-m, Server3: n-z).
    > [!Note]  
    > La creación de particiones de datos puede agregar una gran complejidad a la lógica de programación y solo debe realizarse después de que se hayan probado otras opciones para aumentar la escalabilidad.

     

-   Duración del objeto. Para que sea escalable, una aplicación COM+ debe prestar mucha atención a la duración de los objetos. Mientras existe un objeto, consume recursos. Es importante asegurarse de que las duraciones de los objetos que se mantienen en recursos caros se administran cuidadosamente. En el caso de los objetos de alta demanda que no consumen recursos costosos, la agrupación de objetos [COM+](com--object-pooling.md) puede aumentar la escalabilidad, ya que puede ajustar administrativamente los valores de agrupación para aprovechar el hardware que pueda tener. Y es una manera natural de regular las conexiones: por ejemplo, si tiene una licencia para 20 conexiones SQL, puede dictaminar eso con la configuración Grupo máximo.
-   Agrupación de componentes de aplicación. Para mejorar la escalabilidad de una aplicación COM+, los componentes de nivel intermedio deben dividirse en servicios dependientes del tiempo e independientes del tiempo. Esto le permite centrarse posiblemente en el uso de un servicio Windows Microsoft para implementar una acción de componente necesaria. Por ejemplo, podría optar por usar un servicio como [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) o componentes en cola [de COM+](com--queued-components.md) para controlar las tareas asincrónicas independientes del tiempo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseño para disponibilidad](designing-for-availability.md)
</dt> <dt>

[Diseño para la implementación](designing-for-deployment.md)
</dt> <dt>

[Diseño para la seguridad](designing-for-security.md)
</dt> </dl>

 

 



