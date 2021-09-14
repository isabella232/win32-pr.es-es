---
description: La escalabilidad es la capacidad de una aplicación para dar servicio a una carga adicional con un aumento lineal en el uso de recursos.
ms.assetid: 8249f1af-9c96-4545-ad6a-3736c6e63c6d
title: Diseño para la escalabilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ab0aa9d67afaac14c6d8f59df34183bde36113
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966939"
---
# <a name="designing-for-scalability"></a>Diseño para la escalabilidad

La escalabilidad es la capacidad de una aplicación para dar servicio a una carga adicional con un aumento lineal en el uso de recursos. La escalabilidad es importante en cualquier aplicación distribuida. Los límites de escalabilidad suelen estar centrados en el uso de recursos y las dependencias creadas accidentalmente en el diseño de la aplicación.

En la lista siguiente se describen los problemas de escalabilidad y se sugieren soluciones:

-   Recursos dentro del equipo. El número de subprocesos y memoria disponibles puede limitar la escalabilidad. Use un modelo de subprocesos que sea más eficaz para la aplicación.
-   Recursos entre equipos. El número de equipos disponibles para distribuir la carga de trabajo de la aplicación puede afectar a la escalabilidad.
-   Afinidad de cliente. Una aplicación puede crear involuntariamente dos situaciones de afinidad: una situación en la que la aplicación depende del estado de los datos que el cliente envía con su solicitud; y una situación en la que la aplicación requiere un estado específico del cliente. Evite diseñar dependencias de estado entre el cliente y la aplicación.
-   Afinidad de servidor. Una aplicación COM+ puede limitar su escalabilidad mediante la creación de una afinidad de servidor, donde la aplicación depende de ir a un equipo servidor determinado para obtener información. Esta afinidad puede producirse con muchas aplicaciones orientadas a bases de datos. La mejor manera de evitar un cuello de botella de afinidad de servidor es crear particiones de datos en varios equipos servidor. Por ejemplo, divida los datos del cliente entre los servidores por la clave a la que se accede con más frecuencia o abarque una base de datos de cliente en varios servidores con el apellido del cliente (por ejemplo, Server1: a-f, Server2: g-m, Server3: n-z).
    > [!Note]  
    > La creación de particiones de datos puede agregar una gran complejidad a la lógica de programación y solo debe realizarse después de que se hayan probado otras opciones para aumentar la escalabilidad.

     

-   Duración del objeto. Para ser escalable, una aplicación COM+ debe prestar mucha atención al intervalo de vida de los objetos. Mientras existe un objeto, consume recursos. Es importante asegurarse de que las duraciones de los objetos que se mantienen en recursos costosos se administran cuidadosamente. En el caso de los objetos de alta demanda que no consumen recursos costosos, la agrupación de objetos [COM+](com--object-pooling.md) puede aumentar la escalabilidad porque puede ajustar administrativamente los valores de agrupación para aprovechar el hardware que pueda tener. Y es una manera natural de regular las conexiones: por ejemplo, si tiene una licencia para 20 conexiones SQL, puede dictar eso con la configuración Grupo máximo.
-   Agrupación de componentes de aplicación. Para mejorar la escalabilidad de una aplicación COM+, los componentes de nivel intermedio deben dividirse en servicios dependientes del tiempo e independientes del tiempo. Esto le permite centrarse posiblemente en el uso de un servicio Windows Microsoft para implementar una acción de componente necesaria. Por ejemplo, podría optar por usar un servicio como [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) o componentes en cola de [COM+](com--queued-components.md) para controlar tareas asincrónicas independientes del tiempo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseño para disponibilidad](designing-for-availability.md)
</dt> <dt>

[Diseño para la implementación](designing-for-deployment.md)
</dt> <dt>

[Diseño para la seguridad](designing-for-security.md)
</dt> </dl>

 

 



