---
description: Los objetos agrupables deben cumplir ciertos requisitos para permitir que varios clientes puedan usar una única instancia de objeto.
ms.assetid: 2cd4211e-be12-4197-8b43-5cb9f2321016
title: Requisitos para objetos agrupables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d6834210f180ad8b514b51b6926b5cd30714fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000568"
---
# <a name="requirements-for-poolable-objects"></a>Requisitos para objetos agrupables

Los objetos agrupables deben cumplir ciertos requisitos para permitir que varios clientes puedan usar una única instancia de objeto.

## <a name="stateless"></a>Sin estado

Para mantener la seguridad, la coherencia y el aislamiento, los objetos agrupables no deben tener ningún estado específico del cliente del cliente al cliente. Puede administrar cualquier estado por cliente mediante [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol), realizando una inicialización específica del contexto con [**IObjectControl:: Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) y limpiando cualquier estado de cliente con [**IObjectControl::D eactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate). Para obtener más información, vea [controlar la duración y el estado](controlling-object-lifetime-and-state.md)de los objetos.

## <a name="no-thread-affinity"></a>Sin afinidad de subprocesos

Los objetos agrupables no se pueden enlazar a un subproceso determinado; de lo contrario, el rendimiento podría ser desastroso. Por esta razón, los objetos agrupables no se pueden marcar para ejecutarse en el modelo de apartamento; deben ejecutarse en el contenedor multiproceso o en el contenedor neutro. Además, los objetos agrupables no deben usar el almacenamiento local para el subproceso ni deben agregar el contador de referencias de subprocesamiento libre. Para obtener más información acerca de los subprocesos en COM+, vea [modelos de subprocesos com+](com--threading-models.md).

> [!Note]  
> Los entornos de desarrollo de Microsoft Visual Basic 6,0 y anteriores solo pueden crear componentes de modelo de apartamento. Sin embargo, en Visual Basic .NET, los componentes se pueden agrupar.

 

## <a name="aggregatable"></a>Aggregatable

Los objetos agrupables deben admitir la agregación; es decir, deben admitir que se creen mediante la invocación de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con un argumento *pUnkOuter* que no sea NULL. Cuando COM+ activa un objeto agrupado, crea un agregado para administrar la duración del objeto agrupado y llamar a métodos en [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol). Para obtener más información sobre cómo escribir objetos agregables, vea [agregación](/windows/desktop/com/aggregation).

## <a name="transactional-components"></a>Componentes transaccionales

Los objetos agrupables que participan en transacciones deben dar de alta manualmente los recursos administrados. Mientras está agrupado, si el objeto contiene un recurso administrado como una conexión de base de datos, no habrá forma de que el administrador de recursos dé de alta automáticamente en una transacción cuando el objeto se activa en el contexto especificado. Por lo tanto, el propio objeto debe controlar la lógica de detección de la transacción, desactivando la inscripción automática del administrador de recursos y dando de alta manualmente los recursos que contiene. Además, un objeto agrupado transaccional debe reflejar el estado actual de sus recursos en los valores de parámetro de [**IObjectControl:: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled). Para obtener más información, consulte [agrupación de objetos transaccionales](pooling-transactional-objects.md).

## <a name="implement-iobjectcontrol-to-manage-the-object-lifetime"></a>Implementar IObjectControl para administrar la duración de los objetos

Los objetos agrupables deben implementar [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol), aunque no es estrictamente necesario hacerlo. Los componentes transaccionales que se agrupan, sin embargo, deben implementar **IObjectControl**. Estos componentes deben supervisar el estado de los recursos que contienen e indicar cuándo no se pueden volver a usar. Cuando [**IObjectControl:: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) devuelve false, terminará una transacción. Para obtener más información, vea [controlar la duración y el estado](controlling-object-lifetime-and-state.md)de los objetos.

## <a name="language-restrictions"></a>Restricciones de lenguaje

Los componentes desarrollados con Microsoft Visual Basic 6,0 y versiones anteriores no se pueden agrupar porque estos componentes serán subprocesos de modelo apartamento. Sin embargo, en Visual Basic .NET, los componentes se pueden agrupar.

## <a name="legacy-components"></a>Componentes heredados

Siempre que sean no transaccionales y cumplan los requisitos anteriores, los componentes se pueden agrupar incluso si no se escribieron específicamente con la capacidad de agrupación en mente. No es necesario implementar [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol); un componente que no lo hace simplemente no participará en la administración de su duración. Si [**IObjectControl:: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) no está implementado, el objeto se seguirá reutilizando hasta que el grupo alcance el tamaño máximo.

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

[Agrupar objetos transaccionales](pooling-transactional-objects.md)
</dt> </dl>

 

 
