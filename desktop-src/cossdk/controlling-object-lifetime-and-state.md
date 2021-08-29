---
description: Controlar la duración y el estado de los objetos
ms.assetid: 172e07a2-1711-4353-9099-ff9d31a564c6
title: Controlar la duración y el estado de los objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2159f491267ac4d83a75c003005bd6bf7707d0db769d467fcfdfc3799ea08d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128827"
---
# <a name="controlling-object-lifetime-and-state"></a>Controlar la duración y el estado de los objetos

Un objeto agrupado puede participar en la forma en que COM+ administra su actividad en el grupo mediante la implementación [**de IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol). Cuando se crea un objeto agrupado, se agrega a un objeto mayor que administrará el objeto llamando a los métodos siguientes en **IObjectControl** en puntos regulares del ciclo de vida del objeto:

-   [**Activate:**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)se llama cada vez que se devuelve el objeto a un cliente, activado en un contexto específico.
-   [**Desactivar**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate): se llama cada vez que el cliente libera un objeto o, en el caso de un objeto activado JIT, cuando se desactiva.
-   [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled): se llama cada vez que se devuelve un objeto al grupo general.

La implementación [**de IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) es opcional, excepto para los objetos transaccionales, que siempre deben implementar [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) para supervisar el estado de los recursos que tienen. Sin embargo, es aconsejable implementar **IObjectControl** en la mayoría de los casos porque proporciona una manera eficaz de administrar el comportamiento de un objeto agrupado, como se describe a continuación.

## <a name="performing-context-specific-initialization"></a>Realización de Context-Specific inicialización

Mediante [**Activar**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate), puede inicializar el objeto en el contexto en el que se activa para un cliente determinado. Por ejemplo, para determinar si el objeto tiene afinidad de transacción (es posible que sus recursos ya están dados de alta), puede obtener el identificador de transacción asociado al contexto.

Normalmente, usaría [**Activar**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)para realizar una inicialización coherente en todos los métodos expuestos por el objeto, tratándose como la parte específica del contexto del constructor del objeto.

## <a name="cleaning-up-any-client-state"></a>Limpieza de cualquier estado de cliente

Con [**Desactivar**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate), puede deshacerse de cualquier estado específico del cliente que pueda existir para que el objeto vuelva al grupo en un estado completamente genérico y, a continuación, cualquier cliente pueda usarlo sin poner en peligro la seguridad o el aislamiento.

## <a name="controlling-reuse-of-the-object"></a>Controlar la reutilización del objeto

Con [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), puede supervisar el estado interno del objeto e informar sobre si es adecuado para su reutilización. Si **CanBePooled** devuelve True y no se ha alcanzado el máximo del grupo, el objeto se vuelve a colocar en el grupo general. Si **CanBePooled** devuelve False, se descarta el objeto . En el caso de los componentes transaccionales, la devolución de False hará que la transacción actual se desescale.

Normalmente, conservaría algún miembro de datos global para el objeto y, si detecta que una conexión es mala o que un recurso de algún tipo se encuentra en un estado malo, establezca esta opción para reflejar la situación actual y devolverla a través de [**CanBePooled.**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)

Si un objeto no implementa [**CanBePooled,**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)las instancias se seguirán reutilizando hasta que se alcance el nivel máximo del grupo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cadenas del constructor de objetos COM+](com--object-constructor-strings.md)
</dt> <dt>

[Funcionamiento de la agrupación de objetos](how-object-pooling-works.md)
</dt> <dt>

[Mejorar el rendimiento con la agrupación de objetos](improving-performance-with-object-pooling.md)
</dt> <dt>

[Agrupación de objetos transaccionales](pooling-transactional-objects.md)
</dt> <dt>

[Requisitos para objetos agrupables](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



