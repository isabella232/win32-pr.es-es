---
description: El servicio de activación Just-in-Time (JIT) permite a COM+ desactivar un objeto mientras un cliente todavía mantiene una referencia activa a ese objeto.
ms.assetid: dbc7b257-8506-42c8-8a78-3474c6d4f4b6
title: Conceptos de activación Just-in-Time de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c942bfeb342ea305083e0c7d7ebdea2fe96bf24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714801"
---
# <a name="com-just-in-time-activation-concepts"></a>Conceptos de activación Just-in-Time de COM+

El servicio de activación Just-in-Time (JIT) permite a COM+ desactivar un objeto mientras un cliente todavía mantiene una referencia activa a ese objeto. La próxima vez que el cliente llame a un método en el objeto, que el cliente considera que sigue activo, el servicio de activación JIT de COM+ reactiva el objeto de forma transparente para el cliente, justo a tiempo.

La principal ventaja de utilizar la activación COM + JIT es que puede permitir que los clientes mantengan referencias a objetos mientras los necesiten, sin necesidad de disponer de recursos de servidor valiosos, como la memoria. Otras ventajas importantes son las siguientes:

-   El uso del servicio de activación JIT de COM+ simplifica en gran medida el modelo de programación del cliente porque el cliente no tiene que pensar en cómo utiliza los recursos de servidor y los objetos de servidor costosos. Sin la activación JIT, los clientes pueden suponer una penalización significativa cuando suelen necesitar llamar a los objetos y liberarlos.
    > [!Note]  
    > Puede perfeccionar aún más esta ventaja de rendimiento mediante el servicio de [agrupación de objetos com+](com--object-pooling.md) . Al agrupar los objetos activados en JIT, puede acelerar considerablemente la reactivación de objetos para los clientes mientras se reutilizan los recursos que puedan contener, lo que le proporciona un control más preciso sobre la cantidad de memoria que utiliza un objeto determinado en el servidor. Para obtener más información, consulte [agrupación de objetos y activación JIT de com+](object-pooling-and-com--jit-activation.md).

     

-   Con las aplicaciones distribuidas, se requiere un ciclo de ida y vuelta de red costoso para la creación de todos los objetos, y cuanto más lejos es el cliente del servidor, mayores son los costos de activar y calcular las referencias del objeto de servidor, abrir el canal y configurar el proxy y el código auxiliar. Mediante el servicio de activación JIT de COM+, puede minimizar la frecuencia de creación de objetos para mejorar significativamente el rendimiento de la aplicación.
-   Cuando se usa la activación JIT de COM+ para activar los objetos en los que los clientes contienen referencias de larga duración, pero que no tienen que usar todo el tiempo, la memoria del servidor no siempre está ligada al mantenimiento de los objetos activos. Esto puede aumentar significativamente la escalabilidad de la aplicación. El único impacto en el rendimiento que los clientes ven es el tiempo que tarda COM+ en reactivar el objeto, por lo general, con un margen de tiempo mayor que el necesario para asignar memoria para el objeto y menos sustancialmente que el recorrido de ida y vuelta de red para la creación de objetos remotos.

## <a name="enabling-com-jit-activation"></a>Habilitación de la activación JIT de COM+

Puede habilitar el servicio de activación JIT de COM+ para un componente mediante la herramienta administrativa Servicios de componentes o las funciones administrativas. Para obtener más información sobre cómo hacerlo, vea [Habilitar la activación JIT para un componente](enabling-jit-activation-for-a-component.md).

La activación JIT de COM+ puede interactuar con otros servicios COM+, como los siguientes:

-   Cuando el componente requiere transacciones, la activación JIT se habilita automáticamente. Para obtener más detalles, consulte [transacciones y activación JIT de com+](transactions-and-com--jit-activation.md).
-   Cuando el componente está habilitado para la activación JIT, la sincronización se establece automáticamente en requerido. Esto significa que, si dos clientes llaman simultáneamente a un componente activado en JIT y una llamada al método para uno de ellos devuelven, lo que provoca que el objeto se desactive, el otro no se deja en desuso.

## <a name="how-deactivation-is-triggered"></a>Cómo se desencadena la desactivación

COM+ desactiva un objeto basándose en el estado del bit de realización en el contexto del objeto. El objeto puede utilizar este bit para indicar si se ha hecho, es decir, está listo para desactivarse, durante una llamada al método determinado. Para obtener más información, vea [establecer el bit Done](setting-the-done-bit.md).

## <a name="using-the-auto-done-property"></a>Usar la propiedad auto-Done

Con la herramienta administrativa Servicios de componentes, puede configurar un método de forma que el objeto se desactive automáticamente en la devolución del método. (Vea [Habilitar auto-Done para un método](enabling-auto-done-for-a-method.md) para obtener instrucciones sobre cómo establecer esta propiedad). Al seleccionar esta opción, puede eliminar las llamadas de método repetitivas para votar en transacciones. Dado que la configuración predeterminada para el bit de coherencia es true, si ha cambiado el bit Done a true también y no realiza ninguna acción para cambiar esta configuración, se llama a [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) automáticamente después de que el método devuelva un valor.

Sin embargo, hay una advertencia en este comportamiento: COM+ examinará el valor HRESULT que devuelve el método. Si ese HRESULT indica un error, el bit de coherencia se establece en false y el resultado es el mismo que si hubiera llamado a [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort).

En Resumen, si selecciona auto-Done para un método y no realiza ninguna acción para establecer bits, y si se devuelve un valor HRESULT (HR), se aplica lo siguiente:

-   Si se realiza correctamente (HR), es como si se llamase a [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete).
-   Si se produce un error (HR), es como si hubiera llamado a [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort).

## <a name="using-iobjectcontrol-to-manage-object-activation-and-deactivation"></a>Usar IObjectControl para administrar la activación y desactivación de objetos

Puede implementar la interfaz [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) para que el tiempo de ejecución de com+ Administre automáticamente la desactivación y reactivación de los objetos. Cuando un objeto implementa esta interfaz, COM+ llama a [**IObjectControl::D eactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) cuando desactiva el objeto y [**IObjectControl:: Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) cuando lo vuelve a activar. Estos métodos permiten la inicialización de contexto automática en la activación de objetos y la limpieza del estado durante la desactivación.

Si está agrupando objetos que utilizan la activación JIT de COM+, se recomienda encarecidamente implementar [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol). Para obtener más información, consulte [agrupación de objetos y activación JIT de com+](object-pooling-and-com--jit-activation.md).

## <a name="statelessness-and-jit-activation"></a>Estados y activación JIT

Los objetos transaccionales no tienen estado necesariamente porque no se puede compartir el estado a través de un límite de transacción. Por lo tanto, solo se usaría la activación JIT si el objeto no tiene ningún Estado que se perdería en la desactivación; de lo contrario, se infringe el aislamiento de las transacciones. Debido a los patrones de uso natural de los objetos transaccionales, realizan alguna unidad de trabajo y liberan el objeto cuando la transacción se confirma o se anula: la activación JIT y las transacciones automáticas están estrechamente relacionadas. La configuración de un objeto para requerir transacciones habilita la activación JIT de COM+ automáticamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas de activación Just-in-Time de COM+](com--just-in-time-activation-tasks.md)
</dt> <dt>

[Agrupación de objetos y activación JIT de COM+](object-pooling-and-com--jit-activation.md)
</dt> <dt>

[Transacciones y activación JIT de COM+](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



