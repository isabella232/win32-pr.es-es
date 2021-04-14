---
title: Administración de objetos
description: En esta sección se describe el uso correcto de los tipos de objeto de la API de filtrado de Windows (WFP).
ms.assetid: 2625ef9a-0e62-4e21-ba93-047965d0d782
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc41560bb85a7e79c0262d77c0b34fe6c1d9bfd6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487615"
---
# <a name="object-management"></a>Administración de objetos

En esta sección se describe el uso correcto de los tipos de objeto de la API de filtrado de Windows (WFP).

## <a name="sessions"></a>Sesiones

La API de WFP está orientada a la sesión y la mayoría de las llamadas a funciones se realizan en el contexto de una sesión. Se crea una nueva sesión de cliente mediante una llamada a [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0). La sesión finaliza cuando el cliente llama a [**FwpmEngineClose0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0) o finaliza el proceso del cliente. Cuando se destruye una sesión, ya sea a propósito o por el informe detallado de RPC, el motor de filtrado de base (BFE) anula primero cualquier transacción existente.

Al crear una nueva sesión, el autor de la llamada puede crear una sesión dinámica pasando la marca dinámica de la [**marca de \_ sesión \_ \_ FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0) a [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0). Los objetos agregados durante una sesión dinámica se eliminan automáticamente cuando finaliza la sesión.

## <a name="transactions"></a>Transacciones

La API de WFP es transaccional y la mayoría de las llamadas a funciones se realizan en el contexto de una transacción. Los llamadores pueden usar [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0), [**FwpmTransactionCommit0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactioncommit0)y [**FwpmTransactionAbort0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionabort0) para controlar explícitamente las transacciones. Sin embargo, si una llamada de función se realiza fuera de una transacción explícita, se ejecutará dentro de una transacción implícita. Si una transacción está en curso, cuando una sesión finaliza, se anula automáticamente. Las transacciones implícitas nunca se anulan forzosamente.

Las transacciones son de solo lectura o de lectura y escritura, y aplican una semántica rigurosamente uniforme aislada ([acid](../cossdk/acid-properties.md)) de coherencia atómica.

Cada sesión de cliente solo puede tener una transacción en curso a la vez. Si el llamador intenta iniciar una segunda transacción antes de confirmar o anular la primera, BFE devuelve un error.

Si se produce un error en una operación durante el transcurso de una transacción, no afecta al estado general de la transacción. Por ejemplo, supongamos que el cliente inicia una transacción y llama correctamente a [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0) tres veces antes de que se produzca un error en la cuarta llamada. El cliente tiene ahora la opción de:

-   Anulando la transacción, en cuyo caso no se agregará ninguno de los filtros.
-   Confirmación de la transacción, en cuyo caso se agregarán los tres primeros filtros.
-   Continuando con más operaciones, como la posibilidad de volver a intentar el [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)con errores.

Al iniciar una transacción, BFE esperará hasta que la [**txnWaitTimeoutInMSec**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0) de la sesión expire para adquirir el bloqueo. Si el bloqueo no se adquiere dentro de este tiempo, se producirá un error en la adquisición del bloqueo (y la llamada a [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) ). Esto impide que los clientes no respondan indefinidamente. Si el cliente no especificó un tiempo de espera de bloqueo, el valor predeterminado es 15 segundos.

Cada transacción también tiene un tiempo de espera de bloqueo. Esta es la cantidad máxima de tiempo que puede poseer el bloqueo. Si el propietario no libera el bloqueo dentro de este tiempo, la transacción se anula forzosamente, lo que hace que se libere el bloqueo. No se puede configurar el tiempo de espera de bloqueo. Es infinito para los llamadores en modo kernel y una hora para los llamadores en modo de usuario. Si una transacción se anula forzosamente, se producirá un error en la siguiente llamada realizada dentro de esa transacción con el método **\_ \_ TXN \_ anulado**.

## <a name="object-lifetimes"></a>Duración de los objetos

Los objetos pueden tener una de las cuatro posibles duraciones:

-   Dinámica: un objeto es dinámico solo si se agrega mediante un identificador de sesión dinámica. Los objetos dinámicos se activan hasta que se eliminan o finaliza la sesión propietaria.
-   Estático: los objetos son estáticos de forma predeterminada. Los objetos estáticos se activan hasta que se eliminan, BFE se detiene o se apaga el sistema.
-   Persistente: los objetos persistentes se crean pasando la **marca \_ \* \_ \_ persistente** adecuada de la marca FWPM a una función **FWPM \* Add0** . Objetos persistentes activos hasta que se eliminan.
-   Integrado: los objetos integrados están predefinidos por BFE y no se pueden agregar ni eliminar. Siempre están activos.

Los filtros de las capas de modo kernel se pueden marcar como filtros en tiempo de arranque pasando la marca correspondiente a [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0). Los filtros en tiempo de arranque se agregan al sistema cuando se inicia el controlador TCP/IP y se quitan cuando BFE finaliza la inicialización. Los objetos persistentes se agregan cuando se inicia BFE.

En muchos casos, es posible que un proveedor de directivas no quiera que se aplique su directiva persistente si se ha deshabilitado el proveedor. Al agregar un proveedor, el llamador puede especificar un nombre de servicio de Windows opcional. Al agregar objetos persistentes, el llamador puede especificar opcionalmente el proveedor que "posee" ese objeto. En el inicio del servicio, BFE solo agrega objetos persistentes al sistema si no están asociados a un proveedor, o el proveedor asociado no tiene ningún nombre de servicio de Windows o el servicio de Windows asociado está establecido en Inicio automático.

## <a name="object-associations"></a>Asociaciones de objetos

Algunos objetos tienen referencias a otros objetos. Por ejemplo, un filtro siempre hace referencia a una capa y puede hacer referencia a una llamada y a un contexto de proveedor. Los objetos no pueden hacer referencia a objetos que pueden tener una duración más corta. Por lo tanto, un objeto dinámico no puede hacer referencia a un objeto dinámico desde una sesión diferente. Un objeto estático no puede hacer referencia a un objeto dinámico. Un objeto persistente no puede hacer referencia a un objeto dinámico, un objeto estático o un objeto persistente propiedad de un proveedor diferente.

No se puede eliminar un objeto hasta que se hayan eliminado todos los objetos que hacen referencia a él.

## <a name="luids-and-guids"></a>LUID y GUID

Todos los objetos de la API de WFP del modo de usuario (FWPM) se identifican mediante un identificador único global (**GUID**) y hacen referencia a otros objetos por sus **GUID**. El **GUID** solo debe ser único en el tipo de objeto. Por ejemplo, un filtro y un contexto de proveedor pueden tener el mismo **GUID**, pero no puede haber dos filtros. Al agregar un nuevo objeto, los llamadores pueden asignar el **GUID** del objeto o dejarlo inicializado con ceros y dejar que BFE asigne el **GUID**.

Todos los objetos de la API de WFP de modo kernel (FWPS) se identifican mediante un identificador local único (**LUID**) y hacen referencia a otros objetos por su LUID. El cambio del **GUID** al **LUID** permite a WFP conservar el bloque no paginado y optimizar el procesamiento en tiempo de ejecución. El ancho del **LUID** depende del tipo de objeto e intervalos de una **UINT16** a un **UINT64**. Los **LUID** s siempre se asignan mediante BFE.

 

 