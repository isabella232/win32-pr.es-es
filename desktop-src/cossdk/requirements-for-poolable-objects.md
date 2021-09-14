---
description: Los objetos agrupables deben cumplir determinados requisitos para permitir que varios clientes utilicen una única instancia de objeto.
ms.assetid: 2cd4211e-be12-4197-8b43-5cb9f2321016
title: Requisitos para objetos agrupables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d6834210f180ad8b514b51b6926b5cd30714fd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973518"
---
# <a name="requirements-for-poolable-objects"></a>Requisitos para objetos agrupables

Los objetos agrupables deben cumplir determinados requisitos para permitir que varios clientes utilicen una única instancia de objeto.

## <a name="stateless"></a>Sin estado

Para mantener la seguridad, la coherencia y el aislamiento, los objetos agrupables no deben contener ningún estado específico del cliente del cliente al cliente. Puede administrar cualquier estado por cliente mediante [**IObjectControl,**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol)realizando la inicialización específica del contexto con [**IObjectControl::Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) y limpiando cualquier estado de cliente con [**IObjectControl::D eactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate). Para obtener más información, vea [Controlar la duración y el estado de los objetos.](controlling-object-lifetime-and-state.md)

## <a name="no-thread-affinity"></a>Sin afinidad de subproceso

Los objetos agrupables no se pueden enlazar a un subproceso determinado; De lo contrario, el rendimiento podría ser potencialmente desastroso. Por esta razón, los objetos agrupables no se pueden marcar para ejecutarse en el modelo de apartamento; deben ejecutarse en el apartamento multiproceso o en el apartamento neutro. Además, los objetos agrupables no deben usar el almacenamiento local de subprocesos ni deben agregar el serializador de subprocesos libres. Para obtener más información sobre el subprocesamiento en COM+, vea [Modelos de subprocesamiento de COM+.](com--threading-models.md)

> [!Note]  
> Microsoft Visual Basic 6.0 y entornos de desarrollo anteriores solo pueden crear componentes de modelos de apartamento. Sin embargo, en Visual Basic .NET, los componentes se pueden agrupar.

 

## <a name="aggregatable"></a>Aggregatable

Los objetos agrupables deben admitir la agregación, es decir, deben admitir la creación mediante la invocación de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con un *argumento pUnkOuter* que no sea NULL. Cuando COM+ activa un objeto agrupado, crea un agregado para administrar la duración del objeto agrupado y para llamar a métodos en [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol). Para obtener más información sobre cómo escribir objetos agregables, vea [Agregación](/windows/desktop/com/aggregation).

## <a name="transactional-components"></a>Componentes transaccionales

Los objetos agrupables que participan en transacciones deben dar de alta manualmente los recursos administrados. Mientras se agrupa, si el objeto contiene un recurso administrado como una conexión de base de datos, no habrá ninguna manera de que el administrador de recursos se inste automáticamente en una transacción cuando el objeto se active en un contexto determinado. Por lo tanto, el propio objeto debe controlar la lógica de detección de la transacción, desactivar la registro automática del administrador de recursos y dar de alta manualmente los recursos que contiene. Además, un objeto transaccional agrupado debe reflejar el estado actual de sus recursos en los valores de parámetro [**de IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled). Para obtener más información, vea [Agrupación de objetos transaccionales.](pooling-transactional-objects.md)

## <a name="implement-iobjectcontrol-to-manage-the-object-lifetime"></a>Implementar IObjectControl para administrar la duración del objeto

Los objetos agrupables deben implementar [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol), aunque no es estrictamente necesario hacerlo. Sin embargo, los componentes transaccionales que se agrupan deben implementar **IObjectControl**. Estos componentes deben supervisar el estado de los recursos que tienen e indicar cuándo no se pueden reutilizar. cuando [**IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) devuelve false, se descontrolará una transacción. Para obtener más información, vea [Controlar la duración y el estado de los objetos.](controlling-object-lifetime-and-state.md)

## <a name="language-restrictions"></a>Restricciones de lenguaje

Los componentes desarrollados con Microsoft Visual Basic 6.0 y versiones anteriores no se pueden agrupar porque estos componentes serán subprocesos de modelo de apartamento. Sin embargo, en Visual Basic .NET, los componentes se pueden agrupar.

## <a name="legacy-components"></a>Componentes heredados

Siempre que no sean transaccionales y cumplan los requisitos anteriores adecuados, los componentes se pueden agrupar incluso si no se escribieron específicamente con la funcionalidad de agrupación en mente. No es necesario implementar [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol); Un componente que no lo hace simplemente no participará en la administración de su duración. Si [**no se implementa IObjectControl::CanBePooled,**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) el objeto se seguirá reutilizando hasta que el grupo alcance el tamaño máximo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cadenas de constructor de objetos COM+](com--object-constructor-strings.md)
</dt> <dt>

[Controlar la duración y el estado de los objetos](controlling-object-lifetime-and-state.md)
</dt> <dt>

[Funcionamiento de la agrupación de objetos](how-object-pooling-works.md)
</dt> <dt>

[Mejora del rendimiento con la agrupación de objetos](improving-performance-with-object-pooling.md)
</dt> <dt>

[Agrupación de objetos transaccionales](pooling-transactional-objects.md)
</dt> </dl>

 

 
