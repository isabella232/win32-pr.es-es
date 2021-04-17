---
description: Controlar la duración y el estado de los objetos
ms.assetid: 172e07a2-1711-4353-9099-ff9d31a564c6
title: Controlar la duración y el estado de los objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525cc1d582d85bc84ef2b1749a427711d1fe26fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705333"
---
# <a name="controlling-object-lifetime-and-state"></a>Controlar la duración y el estado de los objetos

Un objeto agrupado puede participar en el modo en que COM+ administra su actividad en el grupo implementando [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol). Cuando se crea un objeto agrupado, se agrega a un objeto más grande que administrará el objeto llamando a los métodos siguientes en **IObjectControl** en los puntos normales del ciclo de vida del objeto:

-   [**Activar**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate): se llama siempre que el objeto se devuelve a un cliente, que se activa en un contexto específico.
-   [**Desactivar**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate): se llama cada vez que el cliente libera un objeto o, en el caso de un objeto activado en JIT, cuando se desactiva.
-   [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled): se llama siempre que se va a devolver un objeto al grupo general.

La implementación de [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) es opcional, salvo en el caso de los objetos transaccionales, que siempre deben implementar [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) para supervisar el estado de los recursos que contienen. Sin embargo, es aconsejable implementar **IObjectControl** en la mayoría de los casos, ya que proporciona una manera eficaz de administrar el comportamiento de un objeto agrupado, tal y como se describe a continuación.

## <a name="performing-context-specific-initialization"></a>Realización de Context-Specific inicialización

Mediante [**Activar**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate), puede inicializar el objeto en el contexto en el que se activa para un cliente determinado. Por ejemplo, para determinar si el objeto tiene afinidad de transacción (es posible que sus recursos ya estén en la lista), podría obtener el ID. de transacción asociado al contexto.

Normalmente se usaría [**Activar**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)para realizar la inicialización que sea coherente en todos los métodos expuestos por el objeto, tratando como la parte específica del contexto del constructor del objeto.

## <a name="cleaning-up-any-client-state"></a>Limpiar cualquier estado de cliente

Con [**desactivación**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate), puede deshacerse de cualquier estado específico del cliente que pueda existir para que el objeto vuelva al grupo en un estado totalmente genérico y pueda ser utilizado por cualquier cliente sin poner en peligro la seguridad o el aislamiento.

## <a name="controlling-reuse-of-the-object"></a>Controlar la reutilización del objeto

Con [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), puede supervisar el estado interno del objeto e informar sobre si es adecuado para su reutilización. Si **CanBePooled** devuelve true y no se ha alcanzado el máximo del grupo, el objeto se vuelve a colocar en el grupo general. Si **CanBePooled** devuelve false, el objeto se descarta. En el caso de los componentes transaccionales, si se devuelve false, se desactivará la transacción actual.

Normalmente, conserve algunos miembros de datos globales para el objeto y, si detecta que una conexión es incorrecta o que un recurso de algún tipo está en mal estado, establézcalo para reflejar la situación actual y devolverla a través de [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).

Si un objeto no implementa [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), las instancias se seguirán reutilizando hasta que se alcance el nivel máximo del grupo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cadenas del constructor de objetos COM+](com--object-constructor-strings.md)
</dt> <dt>

[Cómo funciona la agrupación de objetos](how-object-pooling-works.md)
</dt> <dt>

[Mejorar el rendimiento con la agrupación de objetos](improving-performance-with-object-pooling.md)
</dt> <dt>

[Agrupar objetos transaccionales](pooling-transactional-objects.md)
</dt> <dt>

[Requisitos para objetos agrupables](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



