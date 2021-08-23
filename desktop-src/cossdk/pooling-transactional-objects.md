---
description: Los componentes transaccionales que se van a agrupar tienen requisitos especiales.
ms.assetid: 32e2f830-c30a-4dbc-8e69-dd2038851998
title: Agrupación de objetos transaccionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c60180011305d0a03fee10fe1a4838f847306393709dc1bfef39f0ea8f69e18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047313"
---
# <a name="pooling-transactional-objects"></a>Agrupación de objetos transaccionales

Los componentes transaccionales que se van a agrupar tienen requisitos especiales.

## <a name="manually-enlisting-resources"></a>Registro manual de recursos

Los objetos agrupables que participan en transacciones deben dar de alta manualmente los recursos administrados. Si un objeto contiene recursos administrados entre clientes, no habrá ninguna manera de que el administrador de recursos se sume automáticamente a una transacción cuando el objeto se activa en un contexto determinado.

El propio objeto debe controlar la lógica de detectar la transacción, desactivar la alistación automática del administrador de recursos y dar de alta manualmente los recursos que contiene. Los pasos para hacerlo son específicos del administrador de recursos que está usando. Si necesita realizar la alta manual, consulte la documentación del administrador de recursos.

Como se describe a continuación, los objetos se pueden agrupar con afinidad de transacción mientras una transacción está activa y se pueden activar con afinidad de transacción si lo llama un cliente asociado a esa transacción. Antes de la lista de recursos, primero debe comprobar la afinidad de transacción. Si el objeto se ha tomado del grupo específico de esa transacción, ya ha realizado el trabajo en esa transacción y ha dado de alta sus recursos.

## <a name="turning-off-automatic-enlistment"></a>Desactivar la alistación automática

La alistación automática debe desactivarse después de adquirir el recurso, normalmente en el constructor del objeto. Es decir, se deshabilita la alistación automática y, a continuación, se conecta.

Deshabilitar la alta automática a veces puede ser un procedimiento sutil, especialmente en el caso de los proveedores de acceso a datos en capas. La alta automática a veces se combina con la agrupación de conexiones, como con ODBC, y a veces no, como con OLE DB. Es posible que tenga que asegurarse de que la alta automática está desactivada en varios niveles de proveedores.

## <a name="implementing-iobjectcontrol"></a>Implementación de IObjectControl

Los objetos agrupables que participan en transacciones deben supervisar el estado actual de los recursos que están manteniendo. Si el objeto detecta que está en un estado no reutilizable (por ejemplo, si una conexión es mala), debe devolver False para [**IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled). Esto tendrá el efecto de descartar la instancia del objeto y de desatentar la transacción actual.

## <a name="transaction-specific-pools"></a>Transaction-Specific grupos

Un grupo de objetos suele ser homogéneo y cualquier objeto agrupado que no esté actualmente en uso es bueno para volver a cualquier cliente. La única excepción a esta regla es en el caso de los objetos transaccionales, para los que se optimiza la agrupación de objetos. Cuando el cliente que solicita un objeto tiene una transacción asociada, COM+ examinará el grupo en busca de un objeto disponible que ya esté asociado a esa transacción. Si se encuentra un objeto con afinidad de transacción, se devuelve al cliente; De lo contrario, se devuelve un objeto del grupo general.

De esta manera, se mantienen subpools especiales que contienen objetos con afinidad para una transacción determinada. Cuando la transacción se confirma o anula, estos objetos se devuelven al grupo general sin afinidad de transacción, listo para que lo utilice cualquier cliente.

Por este motivo, cuando el componente da de alta manualmente sus recursos administrados en una transacción, primero debe comprobar si ya están dados de alta. Si es así, no es necesario dar de alta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cadenas del constructor de objetos COM+](com--object-constructor-strings.md)
</dt> <dt>

[Controlar la duración y el estado de los objetos](controlling-object-lifetime-and-state.md)
</dt> <dt>

[Funcionamiento de la agrupación de objetos](how-object-pooling-works.md)
</dt> <dt>

[Mejora del rendimiento con la agrupación de objetos](improving-performance-with-object-pooling.md)
</dt> <dt>

[Requisitos para objetos agrupables](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



