---
description: Mejorar el rendimiento con la agrupación de objetos
ms.assetid: 7a8a38d8-6549-4686-a298-f3b427b380e3
title: Mejorar el rendimiento con la agrupación de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398b9140080d3a439293b5152b4da7251978e800
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705326"
---
# <a name="improving-performance-with-object-pooling"></a>Mejorar el rendimiento con la agrupación de objetos

La agrupación de objetos puede ser muy eficaz en determinadas circunstancias, produciendo aumentos sustanciales en el rendimiento. La idea general de volver a usar los objetos para obtener la mejor ventaja es agrupar tantos recursos como sea posible, Factorizando la inicialización del trabajo real realizado y, a continuación, personalizando administrativamente las características del grupo en el hardware real en el momento de la implementación. Es decir, debe continuar según los pasos siguientes:

1.  Escriba el objeto para factorizar una inicialización costosa y la adquisición de recursos que se realiza para cualquier cliente como requisito previo para realizar el trabajo real en nombre del cliente. Escriba constructores de objetos pesados para agrupar tantos recursos como sea posible, de modo que los requiera el objeto y estén inmediatamente disponibles cuando los clientes obtengan un objeto del grupo.
2.  Configure el grupo de forma administrativa para lograr el mejor equilibrio en los recursos de hardware disponibles, por lo que normalmente comercia la memoria dedicada al mantenimiento de un grupo de un tamaño determinado en Exchange para agilizar el acceso de cliente y el uso de los objetos. En un momento determinado, la agrupación alcanzará las devoluciones más reducidas y podrá obtener un buen rendimiento suficiente a la vez que se limite el posible uso de recursos por parte de un componente determinado.

## <a name="doing-actual-work-or-acquiring-resources"></a>Realizar trabajo real o adquirir recursos

Si tiene un componente que los clientes usarán brevemente y en rápida sucesión, donde una parte significativa del tiempo de uso de los objetos se invierte en la adquisición de recursos o en la inicialización antes de realizar un trabajo específico para el cliente, lo más probable es que escribir el componente para usar la agrupación de objetos es una gran victoria para usted.

Puede escribir el componente de modo que en el constructor del objeto realice todo el trabajo que consume mucho tiempo y que sea uniforme para todos los clientes como sea posible: adquirir una o varias conexiones, ejecutar scripts, capturar datos de inicialización de archivos o a través de una red, etc. Esto tiene el efecto de agrupar cada uno de estos recursos. Está agrupando la combinación de recursos y el estado genérico necesario para realizar algún trabajo.

En este caso, cuando los clientes obtienen un objeto del grupo, tienen esos recursos inmediatamente disponibles. Normalmente, usarán el objeto para realizar algunas unidades pequeñas de trabajo, insertar o extraer datos y, a continuación, el objeto llamará a [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) o [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) y devolverá. Con patrones de uso rápido, como esto, la agrupación proporciona excelentes ventajas de rendimiento. Puede aprovechar por completo la simplicidad del modelo de programación de transacciones automáticas sin estado y, a la vez, conseguir un rendimiento equivalente a los componentes con estado tradicionales.

Sin embargo, si los clientes usan un objeto durante mucho tiempo cada vez que lo llaman, la agrupación tendrá menos sentido. La ventaja de velocidad que se obtiene es marginal, ya que aumenta el tiempo de uso en relación con el tiempo de inicialización. Obtiene devoluciones más reducidas que podrían no justificar el costo de la memoria necesaria para contener un grupo de objetos activos.

## <a name="sharing-cost-across-multiple-clients"></a>Uso compartido de costos entre varios clientes

Una variación en la factorización de la inicialización es que puede usar la agrupación para amortizar estadísticamente el costo de adquirir recursos caros. Si toma el acierto de adquisición o inicialización una vez y, después, vuelve a usar el objeto, comparte ese costo entre todos los clientes que usan el objeto durante su duración. El tiempo de construcción pesado se produce solo una vez por objeto.

## <a name="preallocating-objects"></a>Asignación previa de objetos

Si especifica un tamaño mínimo de grupo distinto de cero, se creará el número mínimo de objetos y se agrupará cuando se inicie la aplicación, listos para los clientes que llamen a la aplicación.

## <a name="governing-resource-use-with-pool-management"></a>Controlar el uso de recursos con la administración de grupos

Puede usar el tamaño máximo del grupo para controlar con precisión cómo se usan los recursos. Por ejemplo, si tiene una licencia de un determinado número de conexiones de base de datos, puede controlar Cuántas conexiones tiene abiertas en cualquier momento.

Cuando tenga en cuenta los patrones de uso de los clientes, las características de uso de objetos y los recursos físicos, como la memoria y las conexiones, es probable que encuentre un punto de equilibrio óptimo al ajustar el rendimiento. Los objetos de agrupación producirán devoluciones decrecientes después de un determinado punto. Puede determinar qué nivel de rendimiento necesita y equilibrar con qué recursos son necesarios para lograrlo.

Para facilitar el ajuste del rendimiento al configurar la agrupación de objetos, puede supervisar las estadísticas de objetos de los componentes de una aplicación. Para obtener más información, consulte [supervisión de estadísticas de objetos](monitoring-object-statistics.md).

## <a name="improve-performance-of-jit-activated-components"></a>Mejorar el rendimiento de los componentes de JIT-Activated

La agrupación de objetos funciona muy bien con el servicio de [activación Just-in-Time de com+](com--just-in-time-activation.md) . Al agrupar los objetos que se están activando con JIT, puede acelerar la reactivación de objetos. Se obtienen las ventajas de mantener el canal abierto por la activación JIT, a la vez que se mitiga el costo de la reactivación. En este caso, puede usar la agrupación para controlar la cantidad de memoria que desea asignar a los objetos que tienen referencias activas.

Lo más probable es que esté agrupando los componentes activados con JIT cuando sean transaccionales. La agrupación de objetos está optimizada para controlar los componentes transaccionales. Para obtener más información, vea [agrupar objetos transaccionales](pooling-transactional-objects.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cadenas del constructor de objetos COM+](com--object-constructor-strings.md)
</dt> <dt>

[Controlar la duración y el estado de los objetos](controlling-object-lifetime-and-state.md)
</dt> <dt>

[Cómo funciona la agrupación de objetos](how-object-pooling-works.md)
</dt> <dt>

[Agrupar objetos transaccionales](pooling-transactional-objects.md)
</dt> <dt>

[Requisitos para objetos agrupables](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



