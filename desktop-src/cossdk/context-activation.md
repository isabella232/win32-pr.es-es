---
description: En COM+, cada objeto COM se crea con un contexto asociado.
ms.assetid: e5602af2-5852-4c34-a792-6742e90b7d41
title: Activación de contexto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab785040e6cf28b609fe80d4160da90bd3fe640b2229cf982993c8573378e4bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096855"
---
# <a name="context-activation"></a>Activación de contexto

En COM+, cada objeto COM se crea con un contexto asociado. Esto significa que se debe crear e inicializar un nuevo contexto o se usa un contexto existente adecuado. Este proceso se conoce como *activación.* En COM+, un objeto se activa en su propio contexto o en el de su creador (un objeto que ha solicitado que se active el objeto, por ejemplo, mediante una llamada a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)).

En algunas circunstancias, como con la agrupación [de](com--object-pooling.md)objetos , un objeto se activa sin crearse desde cero. En este caso, una instancia en ejecución se activa dentro de un contexto. A lo largo de su duración, se puede activar repetidamente en contextos diferentes.

El mecanismo básico es el mismo en cualquier caso: un objeto está asociado a un contexto y ese contexto se inicializa correctamente para representar las necesidades en tiempo de ejecución del objeto.

## <a name="flowing-of-context-properties"></a>Flujo de propiedades de contexto

Cuando se activa un objeto en respuesta a una solicitud de creación de otro objeto, COM+ debe mediar entre ellos para activar correctamente el objeto de bajada. COM+ tiene que comparar el contexto del autor de la llamada con la configuración del componente llamado y, a continuación, decidir dónde activar el componente de nivel inferior y cómo inicializar sus propiedades de contexto.

Para detectar la configuración del componente, COM+ lo busca en la base de datos de registro de clases COM+, que está optimizada para búsquedas en tiempo de ejecución extremadamente rápidas. (Esto viene determinado por cómo configuró un componente al instalarlo en una aplicación COM+). A continuación, la configuración del componente se examina en función del estado de las propiedades de contexto del autor de la llamada.

En algunos casos, la configuración es coherente con el contexto del autor de la llamada y el componente se puede activar dentro del contexto del autor de la llamada. Esto solo puede ocurrir si el contexto del autor de la llamada satisface todos los requisitos en tiempo de ejecución del nuevo objeto.

Cuando el componente de bajada no se puede activar dentro del contexto del autor de la llamada, se activa en su propio contexto en un apartamento adecuado. Cuando esto ocurre, ciertas propiedades de contexto pueden fluir del autor de la llamada al destinatario. Por ejemplo, si el autor de la llamada está asociado a una transacción y el destinatario admite transacciones, el nuevo objeto obtiene su propio contexto (para votar en la transacción, debe tener su propia marca coherente) y hereda el identificador de transacción y el identificador de actividad del autor de la llamada (que residen dentro del mismo dominio de transacción y sincronización).

## <a name="ignored-context-properties"></a>Propiedades de contexto omitido

En función de cómo se configure un componente, es posible que algunas propiedades de contexto no desempeñan ningún papel a la hora de determinar si se activa en el contexto del creador o en su propio contexto. Por ejemplo, la configuración Transacciones deshabilitadas y Sincronización deshabilitada, que indica la presencia de una transacción o un dominio de sincronización, no desempeñará ningún rol en la activación del componente. Estas propiedades se omiten fundamentalmente cuando el contexto fluye. O bien, si un componente solo usa la comprobación de acceso de nivel de proceso, se omite su propiedad de contexto de seguridad: la configuración de seguridad del componente nunca desempeñará un papel en su activación.

## <a name="forcing-activation-in-the-callers-context"></a>Forzar la activación en el contexto del autor de la llamada

En algunas circunstancias, es posible que quiera que un objeto se active solo en el contexto del autor de la llamada, es decir, nunca se active en su propio contexto. Por ejemplo, es posible que quiera controlar el comportamiento del objeto cuando se llama a través de un límite de contexto.

Para asegurarse de que un objeto no se puede activar en su propio contexto, seleccione la  opción Must **be activated in callers context** (Debe activarse en el contexto de los llamadores) en la pestaña Activación de la página Propiedades del componente mediante la herramienta administrativa Servicios de componentes.  (Consulte [Aplicación de la activación en el](enforcing-activation-in-the-caller-s-context.md) contexto del autor de la llamada para obtener instrucciones paso a paso). Al seleccionar esta opción, si el objeto no se puede activar en el contexto del autor de la llamada, Se produce un error [**en CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) y se devuelve CO \_ E ATTEMPT TO CREATE OUTSIDE CLIENT \_ \_ \_ \_ \_ \_ CONTEXT.

## <a name="default-context"></a>Contexto predeterminado

Existen contextos predeterminados para admitir componentes no configurados, es decir, componentes COM no instalados en aplicaciones COM+ y no registrados en la base de datos de registro de clases COM+. Si los componentes no configurados tienen un modelo de subprocesos compatible, se activan en el contexto del autor de la llamada. De lo contrario, se activan en un contexto predeterminado en el apartamento adecuado. Cada apartamento tiene un contexto predeterminado para admitir objetos COM que no usan servicios COM+.

## <a name="hooking-activation"></a>Activación de enlace

Al implementar [**IObjectControl::Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) e [**IObjectControl::D eactivate,**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate)puede enlazar la activación y desactivación para realizar una inicialización especial en el nuevo contexto. COM+ llama a estos métodos en determinados puntos del ciclo de vida de un objeto, cuando el objeto está configurado para usar la activación JIT o la agrupación de objetos. Consulte [Activación Just-In-Time](com--just-in-time-activation.md) de COM+ y Agrupación de objetos [COM+](com--object-pooling.md) para obtener más detalles.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interceptación de llamadas entre contextos](interception-of-cross-context-calls.md)
</dt> </dl>

 

 
