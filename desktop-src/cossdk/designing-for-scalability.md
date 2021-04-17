---
description: La escalabilidad es la capacidad de una aplicación para atender una carga adicional con un aumento lineal del uso de recursos.
ms.assetid: 8249f1af-9c96-4545-ad6a-3736c6e63c6d
title: Diseño para la escalabilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ab0aa9d67afaac14c6d8f59df34183bde36113
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705266"
---
# <a name="designing-for-scalability"></a>Diseño para la escalabilidad

La escalabilidad es la capacidad de una aplicación para atender una carga adicional con un aumento lineal del uso de recursos. La escalabilidad es importante en cualquier aplicación distribuida. Los límites de escalabilidad normalmente se centran en el uso de recursos y las dependencias que se crean involuntariamente en el diseño de la aplicación.

En la lista siguiente se describen los problemas de escalabilidad y se sugieren soluciones:

-   Recursos dentro del equipo. El número de subprocesos y memoria disponible puede limitar la escalabilidad. Use un modelo de subprocesos que sea más eficaz para su aplicación.
-   Recursos entre equipos. El número de equipos disponibles para distribuir la carga de trabajo de la aplicación puede afectar a la escalabilidad.
-   Afinidad de cliente. Una aplicación puede crear de forma inadvertida dos situaciones de afinidad: una situación en la que la aplicación depende del estado de los datos que envía el cliente con su solicitud; y una situación en la que la aplicación requiere un estado específico del cliente. Evite diseñar la dependencia del estado entre el cliente y la aplicación.
-   Afinidad de servidor. Una aplicación COM+ puede limitar su escalabilidad mediante la creación de una afinidad de servidor, en la que la aplicación depende de ir a un equipo servidor determinado para obtener información. Esta afinidad puede producirse con muchas aplicaciones orientadas a bases de datos. La mejor manera de evitar un cuello de botella de afinidad de servidor es particionar los datos en varios equipos servidor. Por ejemplo, divida los datos del cliente entre servidores por la clave a la que se accede con mayor frecuencia o que abarquen una base de datos de clientes a través de varios servidores con el apellido del cliente (por ejemplo, Servidor1: a-f, servidor2: g-m, Server3: n-z).
    > [!Note]  
    > La creación de particiones de datos puede Agregar una gran cantidad de complejidad a la lógica de programación y debe realizarse solo después de que se hayan probado otras opciones para aumentar la escalabilidad.

     

-   Duración del objeto. Para ser escalables, una aplicación COM+ debe prestar mucha atención a la duración de los objetos. Mientras exista un objeto, consume recursos. Es importante asegurarse de que las duraciones de los objetos que se encuentran en recursos caros se administran cuidadosamente. En el caso de los objetos de alta demanda que no consumen recursos caros, la [agrupación de objetos com+](com--object-pooling.md) puede aumentar la escalabilidad, ya que puede ajustar de forma administrativa los valores de agrupación para aprovechar el hardware que pueda tener. Y es una forma natural de controlar las conexiones: por ejemplo, si tiene una licencia para 20 conexiones SQL, puede dictarla con la configuración de grupo máximo.
-   Agrupación de componentes de aplicación. Para mejorar la escalabilidad de una aplicación COM+, los componentes de nivel intermedio deben dividirse en servicios independientes del tiempo y dependientes del tiempo. Esto le permite centrarse en la posibilidad de usar un servicio de Microsoft Windows para implementar una acción de componente necesaria. Por ejemplo, puede optar por usar un servicio como [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) o [componentes en cola com+](com--queued-components.md) para controlar tareas asincrónicas independientes del tiempo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseño para disponibilidad](designing-for-availability.md)
</dt> <dt>

[Diseñar para la implementación](designing-for-deployment.md)
</dt> <dt>

[Diseñar para la seguridad](designing-for-security.md)
</dt> </dl>

 

 



