---
description: Mejora del rendimiento con la agrupación de objetos
ms.assetid: 7a8a38d8-6549-4686-a298-f3b427b380e3
title: Mejora del rendimiento con la agrupación de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ce6a86e76f7a97395973cc9cab4c4e9e81177f4312a389c2b01ec2d88eb7a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547852"
---
# <a name="improving-performance-with-object-pooling"></a>Mejora del rendimiento con la agrupación de objetos

La agrupación de objetos puede ser muy eficaz en determinadas circunstancias, lo que produce aumentos sustanciales en el rendimiento. La idea general para volver a usar objetos para aprovechar mejor es agrupar tantos recursos como sea posible, factorización de la inicialización del trabajo real realizado y, a continuación, adaptar administrativamente las características del grupo al hardware real en el momento de la implementación. Es decir, debe continuar según los pasos siguientes:

1.  Escriba el objeto para factorización de la inicialización costosa y la adquisición de recursos que se realiza para cualquier cliente como requisito previo para realizar el trabajo real en nombre del cliente. Escriba constructores de objetos pesados en el grupo tantos recursos como sea posible para que estén retenidos por el objeto y estén disponibles inmediatamente cuando los clientes obtengan un objeto del grupo.
2.  Configure administrativamente el grupo para lograr el mejor equilibrio en los recursos de hardware disponibles, normalmente intercambiando la memoria dedicada a mantener un grupo de un tamaño determinado a cambio de un acceso de cliente más rápido y el uso de objetos. En un momento determinado, la agrupación logrará una disminución de los resultados y puede obtener un rendimiento lo suficientemente bueno como para limitar el posible uso de recursos por un componente determinado.

## <a name="doing-actual-work-or-acquiring-resources"></a>Realizar trabajo real o adquirir recursos

Si tiene un componente que los clientes usarán brevemente y en sucesión rápida, donde una parte significativa del tiempo de uso de objetos se dedica a adquirir recursos o inicializar antes de realizar un trabajo específico para el cliente, lo más probable es que escribir el componente para usar la agrupación de objetos sea una gran ventaja para usted.

Puede escribir el componente para que en el constructor del objeto realice tanto trabajo lento que sea uniforme para todos los clientes como sea posible: adquirir una o varias conexiones, ejecutar scripts, capturar datos de inicialización de archivos o a través de una red, etc. Esto tiene el efecto de la agrupación de todos estos recursos. Está agrupando la combinación de recursos y el estado genérico necesario para realizar algún trabajo.

En esta circunstancia, cuando los clientes obtienen un objeto del grupo, tienen esos recursos disponibles inmediatamente. Normalmente, usarán el objeto para realizar una pequeña unidad de trabajo, insertar o extraer datos y, a continuación, el objeto llamará a [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) o [**IObjectContext::SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) y devolverá. Con patrones de uso rápido como este, la agrupación ofrece excelentes ventajas de rendimiento. Puede aprovechar completamente la simplicidad del modelo de programación automática de transacciones sin estado, pero lograr el rendimiento a la par que los componentes con estado tradicionales.

Sin embargo, si los clientes usan un objeto durante mucho tiempo cada vez que lo llaman, la agrupación tendrá menos sentido. La ventaja de velocidad que obtiene es marginal a medida que aumenta el tiempo de uso en relación con el tiempo de inicialización. Obtiene una disminución de los resultados que pueden no justificar el costo de la memoria necesaria para contener un grupo de objetos activos.

## <a name="sharing-cost-across-multiple-clients"></a>Costo de uso compartido entre varios clientes

Una variación en la inicialización de factorización de salida es que puede usar la agrupación para amortizar estadísticamente el costo de adquirir recursos costosos. Si alcanza la adquisición o inicialización una vez y, a continuación, reutiliza el objeto, comparte ese costo entre todos los clientes que usan el objeto durante su vigencia. El tiempo de construcción pesado se incurre solo una vez por objeto.

## <a name="preallocating-objects"></a>Preasignación de objetos

Si especifica un tamaño de grupo mínimo distinto de cero, ese número mínimo de objetos se creará y agrupará cuando se inicie la aplicación, listo para todos los clientes que llamen a la aplicación.

## <a name="governing-resource-use-with-pool-management"></a>Control del uso de recursos con la administración de grupos

Puede usar el tamaño máximo del grupo para regular con mucha precisión cómo se usan los recursos. Por ejemplo, si ha concedido licencia para un determinado número de conexiones de base de datos, puede controlar cuántas conexiones tiene abiertas en cualquier momento.

Al tener en cuenta los patrones de uso del cliente, las características de uso de objetos y los recursos físicos, como la memoria y las conexiones, es probable que encuentre algún punto de equilibrio óptimo al realizar el ajuste del rendimiento. La agrupación de objetos dará como resultado una disminución de los resultados después de un punto determinado. Puede determinar qué nivel de rendimiento necesita y equilibrarlo con los recursos necesarios para lograrlo.

Para facilitar el ajuste del rendimiento al configurar la agrupación de objetos, puede supervisar las estadísticas de objetos de los componentes de una aplicación. Para obtener más información, [vea Monitoring Object Statistics](monitoring-object-statistics.md).

## <a name="improve-performance-of-jit-activated-components"></a>Mejora del rendimiento de JIT-Activated componentes

La agrupación de objetos funciona muy bien con el servicio de activación [Just-In-Time de COM+.](com--just-in-time-activation.md) Al agrupar objetos que se activan con JIT, puede acelerar la reactivación de objetos. Obtiene las ventajas de mantener abierto el canal mediante la activación JIT al tiempo que mitiga el costo de reactivación. Puede usar la agrupación en este caso para regular la cantidad de memoria que desea asignar a los objetos que tienen referencias activas.

Es más probable que esté agrupando componentes activados por JIT cuando son transaccionales. La agrupación de objetos está optimizada para controlar los componentes transaccionales. Para obtener más información, vea [Agrupación de objetos transaccionales.](pooling-transactional-objects.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cadenas del constructor de objetos COM+](com--object-constructor-strings.md)
</dt> <dt>

[Controlar la duración y el estado de los objetos](controlling-object-lifetime-and-state.md)
</dt> <dt>

[Funcionamiento de la agrupación de objetos](how-object-pooling-works.md)
</dt> <dt>

[Agrupación de objetos transaccionales](pooling-transactional-objects.md)
</dt> <dt>

[Requisitos para objetos agrupables](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



