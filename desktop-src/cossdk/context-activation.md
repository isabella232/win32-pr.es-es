---
description: En COM+, cada objeto COM se crea con un contexto asociado.
ms.assetid: e5602af2-5852-4c34-a792-6742e90b7d41
title: Activación de contexto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a652615d6c1288887085c857817e32e3a3b4081c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153262"
---
# <a name="context-activation"></a>Activación de contexto

En COM+, cada objeto COM se crea con un contexto asociado. Esto significa que se debe crear e inicializar un nuevo contexto, o usar un contexto existente adecuado. Este proceso se conoce como *activación*. En COM+, un objeto se activa en su propio contexto o en el de su creador (un objeto que ha solicitado que se active el objeto, por ejemplo, llamando a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)).

En algunas circunstancias, como con la [agrupación de objetos](com--object-pooling.md), un objeto se activa sin crearse desde cero. En este caso, una instancia en ejecución se activa dentro de un contexto. A lo largo de su duración, se puede activar repetidamente en contextos diferentes.

El mecanismo básico es el mismo en cualquier caso: un objeto está asociado a un contexto y ese contexto se inicializa correctamente para representar las necesidades de tiempo de ejecución del objeto.

## <a name="flowing-of-context-properties"></a>Flujo de propiedades de contexto

Cuando un objeto se activa en respuesta a una solicitud de creación de otro objeto, COM+ debe mediar entre ellos para activar correctamente el objeto de nivel inferior. COM+ tiene que comparar el contexto del llamador con la configuración del componente llamado y, a continuación, decidir dónde activar el componente de nivel inferior y cómo inicializar sus propiedades de contexto.

Para detectar la configuración del componente, COM+ lo busca en la base de datos de registro de clase COM+, que está optimizada para búsquedas de tiempo de ejecución extremadamente rápidas. (Esto viene determinado por el modo en que configuró un componente al instalarlo en una aplicación COM+). A continuación, la configuración del componente se examina con el estado de las propiedades de contexto del llamador.

En algunos casos, la configuración es coherente con el contexto del autor de la llamada y el componente se puede activar en el contexto del llamador. Esto solo puede ocurrir si el contexto del autor de la llamada cumple todos los requisitos de tiempo de ejecución del nuevo objeto.

Cuando el componente de nivel inferior no se puede activar en el contexto del autor de la llamada, se activa en su propio contexto en un apartamento adecuado. Cuando esto ocurre, algunas propiedades de contexto pueden fluir del llamador al destinatario. Por ejemplo, si el autor de la llamada está asociado a una transacción y el destinatario admite transacciones, el nuevo objeto obtiene su propio contexto (para votar en la transacción, debe tener su propia marca coherente) y hereda el ID. de la transacción del llamador y el ID. de actividad (que residen en la misma transacción y dominio de sincronización).

## <a name="ignored-context-properties"></a>Propiedades de contexto omitidas

Dependiendo de cómo se configure un componente, algunas propiedades de contexto pueden no desempeñar ningún rol para determinar si está activada en el contexto del creador o en su propio contexto. Por ejemplo, las transacciones deshabilitadas y la sincronización deshabilitada, que indican la presencia de una transacción o un dominio de sincronización, no reproducirán ningún rol en la activación del componente. Estas propiedades se omiten fundamentalmente cuando se fluye el contexto. O bien, si un componente solo usa la comprobación de acceso de nivel de proceso, se omite su propiedad de contexto de seguridad; la configuración de seguridad del componente nunca reproducirá un rol en su activación.

## <a name="forcing-activation-in-the-callers-context"></a>Forzar la activación en el contexto del autor de la llamada

En algunas circunstancias, es posible que quiera que un objeto se active solo en el contexto del autor de la llamada, es decir, nunca se active en su propio contexto. Por ejemplo, puede que desee controlar el comportamiento del objeto cuando se llama a través de un límite de contexto.

Puede asegurarse de que un objeto no se puede activar en su propio contexto seleccionando la opción **debe activarse en el contexto de llamadores** en la pestaña **activación** de la página de **propiedades** del componente, mediante la herramienta administrativa Servicios de componentes. (Vea [forzar la activación en el contexto del autor de la llamada](enforcing-activation-in-the-caller-s-context.md) para obtener instrucciones paso a paso). Cuando se selecciona esta opción, si el objeto no se puede activar en el contexto del autor de la llamada, se produce un error de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) y se devuelve el \_ intento de crear un conjunto de \_ \_ \_ \_ clientes fuera del \_ \_ contexto.

## <a name="default-context"></a>Contexto predeterminado

Existen contextos predeterminados para admitir componentes sin configurar, es decir, componentes COM no instalados en aplicaciones COM+ y no registrados en la base de datos de registro de clases COM+. Si los componentes sin configurar tienen un modelo de subprocesos compatible, se activan en el contexto del autor de la llamada. De lo contrario, se activan en un contexto predeterminado en el apartamento adecuado. Cada apartamento tiene un contexto predeterminado para admitir objetos COM que no utilizan servicios COM+.

## <a name="hooking-activation"></a>Activación de enlace

Mediante la implementación de [**IObjectControl:: Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) y [**IObjectControl::D eactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate), puede enlazar la activación y desactivación juntas para realizar una inicialización especial en el nuevo contexto. COM+ llama a estos métodos en determinados puntos del ciclo de vida de un objeto, cuando el objeto está configurado para usar la activación JIT o la agrupación de objetos. Consulte [activación Just-in-Time de com+](com--just-in-time-activation.md) y [agrupación de objetos com+](com--object-pooling.md) para obtener más detalles.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interceptación de llamadas entre contextos](interception-of-cross-context-calls.md)
</dt> </dl>

 

 
