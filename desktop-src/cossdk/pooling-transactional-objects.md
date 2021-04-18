---
description: Los componentes transaccionales que se van a agrupar tienen requisitos especiales.
ms.assetid: 32e2f830-c30a-4dbc-8e69-dd2038851998
title: Agrupar objetos transaccionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 006ba32ad2ac550be4fa4418dde322ded26c64c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705324"
---
# <a name="pooling-transactional-objects"></a>Agrupar objetos transaccionales

Los componentes transaccionales que se van a agrupar tienen requisitos especiales.

## <a name="manually-enlisting-resources"></a>Inscripción manual de recursos

Los objetos agrupables que participan en transacciones deben dar de alta manualmente los recursos administrados. Si un objeto contiene recursos administrados entre clientes, no habrá forma de que el administrador de recursos dé de alta automáticamente en una transacción cuando el objeto se activa en un contexto determinado.

El propio objeto debe controlar la lógica de detección de la transacción, la desactivación de la inscripción automática del administrador de recursos y la inscripción manual de los recursos que contiene. Los pasos para hacerlo son específicos del administrador de recursos que está usando. Si necesita realizar una inscripción manual, consulte la documentación del administrador de recursos.

Tal y como se describe a continuación, los objetos se pueden agrupar con afinidad de transacciones mientras una transacción está activa y se puede activar con la afinidad de transacciones si la llama un cliente asociado a esa transacción. Antes de dar de alta los recursos, primero debe comprobar la afinidad de la transacción. Si el objeto se ha tomado del grupo específico de esa transacción, ya ha hecho trabajo en esa transacción y dado de alta sus recursos.

## <a name="turning-off-automatic-enlistment"></a>Desactivación de la inscripción automática

La inscripción automática debe desactivarse después de adquirir el recurso, normalmente en el constructor del objeto. Es decir, deshabilite la inscripción automática y, a continuación, conéctese.

La deshabilitación de la inscripción automática a veces puede ser un procedimiento sutil, especialmente en el caso de los proveedores de acceso a datos por capas. La inscripción automática a veces se acopla con la agrupación de conexiones, como con ODBC y, a veces, no, como con OLE DB. Es posible que deba asegurarse de que la inscripción automática está desactivada en varios niveles de proveedores.

## <a name="implementing-iobjectcontrol"></a>Implementar IObjectControl

Los objetos agrupables que participan en transacciones deben supervisar el estado actual de los recursos que contienen. Si el objeto detecta que se encuentra en un estado no reutilizable (por ejemplo, si una conexión es incorrecta), debe devolver false para [**IObjectControl:: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled). Esto tendrá el efecto de descartar la instancia de objeto y desechar la transacción actual.

## <a name="transaction-specific-pools"></a>Grupos de Transaction-Specific

Un grupo de objetos es generalmente homogéneo y cualquier objeto agrupado que no esté en uso actualmente es adecuado para volver a cualquier cliente. La única excepción a esta regla es en el caso de los objetos transaccionales, para los que se optimiza la agrupación de objetos. Cuando el cliente que solicita un objeto tiene una transacción asociada, COM+ examinará el grupo en busca de un objeto disponible que ya esté asociado a esa transacción. Si se encuentra un objeto con afinidad de transacciones, se devuelve al cliente; de lo contrario, se devuelve un objeto del grupo general.

De esta manera, se mantienen subgrupos especiales que contienen objetos con afinidad para una transacción determinada. Cuando la transacción se confirma o se anula, estos objetos se devuelven al grupo general sin afinidad de transacciones, ya que se puede usar en cualquier cliente.

Por esta razón, cuando el componente da de alta manualmente sus recursos administrados en una transacción, debe comprobar primero si ya están inscritos. Si es así, no es necesario dar de alta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cadenas del constructor de objetos COM+](com--object-constructor-strings.md)
</dt> <dt>

[Controlar la duración y el estado de los objetos](controlling-object-lifetime-and-state.md)
</dt> <dt>

[Cómo funciona la agrupación de objetos](how-object-pooling-works.md)
</dt> <dt>

[Mejorar el rendimiento con la agrupación de objetos](improving-performance-with-object-pooling.md)
</dt> <dt>

[Requisitos para objetos agrupables](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



