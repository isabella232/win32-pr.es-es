---
title: Administración de objetos
description: En esta sección se trata el uso correcto de Windows de objetos de API de plataforma de filtrado de filtros (WFP).
ms.assetid: 2625ef9a-0e62-4e21-ba93-047965d0d782
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5cb51d4e78049d7911a4a5ed265091e05bc1cbb00ce470e332d59dd23c6026d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068855"
---
# <a name="object-management"></a>Administración de objetos

En esta sección se trata el uso correcto de Windows de objetos de API de plataforma de filtrado de filtros (WFP).

## <a name="sessions"></a>Sesiones

La API de WFP está orientada a sesiones y la mayoría de las llamadas a funciones se realizan en el contexto de una sesión. Se crea una nueva sesión de cliente mediante una llamada [**a FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0). La sesión finaliza cuando el cliente llama a [**FwpmEngineClose0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0) o el proceso de cliente finaliza. Cuando se destruye una sesión, ya sea a propósito o por el informe de RPC, el motor de filtrado base (BFE) anula primero cualquier transacción existente.

Al crear una nueva sesión, el autor de la llamada puede crear una sesión dinámica pasando la marca [**\_ FWPM SESSION \_ FLAG \_ DYNAMIC**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0) a [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0). Los objetos agregados durante una sesión dinámica se eliminan automáticamente cuando finaliza la sesión.

## <a name="transactions"></a>Transacciones

La API de WFP es transaccional y la mayoría de las llamadas de función se realizan en el contexto de una transacción. Los llamadores pueden usar [**FwpmTransactionBegin0,**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) [**FwpmTransactionCommit0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactioncommit0)y [**FwpmTransactionAbort0 para**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionabort0) controlar explícitamente las transacciones. Sin embargo, si una llamada de función se realiza fuera de una transacción explícita, se ejecutará dentro de una transacción implícita. Si una transacción está en curso, cuando finaliza una sesión, se anula automáticamente. Las transacciones implícitas nunca se anulan forzadamente.

Las transacciones son de solo lectura o de lectura y escritura y aplican una semántica atómica coherente y duradera aislada[(ACID).](../cossdk/acid-properties.md)

Cada sesión de cliente solo puede tener una transacción en curso a la vez. Si el autor de la llamada intenta iniciar una segunda transacción antes de confirmar o anular la primera, BFE devuelve un error.

Si se produce un error en una operación durante el transcurso de una transacción, no afecta al estado general de la transacción. Por ejemplo, suponga que el cliente comienza una transacción y llama correctamente a [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0) tres veces antes de que se produce un error en una cuarta llamada. El cliente ahora tiene la opción de:

-   Anular la transacción, en cuyo caso no se agregará ninguno de los filtros.
-   Confirmar la transacción, en cuyo caso se agregarán los tres primeros filtros.
-   Continuando con más operaciones, incluida la posibilidad de reintentar el [**fwpmFilterAdd0 con errores.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)

Al iniciar una transacción, BFE esperará hasta que expire [**el txnWaitTimeoutInMSec**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0) de la sesión para adquirir el bloqueo. Si el bloqueo no se adquiere dentro de este tiempo, se producirá un error en la adquisición del bloqueo (y la llamada [**FwpmTransactionBegin0).**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) Esto evita que los clientes no respondan indefinidamente. Si el cliente no especificó un tiempo de espera de bloqueo, el valor predeterminado es 15 segundos.

Cada transacción también tiene un tiempo de espera de bloqueo. Esta es la cantidad máxima de tiempo que puede poseer el bloqueo. Si el propietario no libera el bloqueo dentro de este tiempo, la transacción se anula forzadamente, lo que hace que se libere el bloqueo. El tiempo de espera de bloqueo no es configurable. Es infinito para los llamadores en modo kernel y una hora para los llamadores en modo de usuario. Si una transacción se anula forzablemente, la siguiente llamada realizada dentro de esa transacción producirá un error **con FWP \_ E \_ TXN \_ ABORTED**.

## <a name="object-lifetimes"></a>Duraciones de objetos

Los objetos pueden tener una de las cuatro duraciones posibles:

-   Dinámico: un objeto es dinámico solo si se agrega mediante un identificador de sesión dinámico. Los objetos dinámicos están en directo hasta que se eliminan o finaliza la sesión propietaria.
-   Static: los objetos son estáticos de forma predeterminada. Los objetos estáticos están en directo hasta que se eliminan, BFE se detiene o el sistema se apaga.
-   Persistente: los objetos persistentes se crean pasando la marca **FWPM \_ \* \_ FLAG \_ PERSISTENT** adecuada a una **función Fwpm \* Add0.** Los objetos persistentes se encuentran hasta que se eliminan.
-   Integrado: los objetos integrados están predefinidos por BFE y no se pueden agregar ni eliminar. Se han vivo para siempre.

Los filtros de las capas en modo kernel se pueden marcar como filtros de tiempo de arranque pasando la marca adecuada a [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0). Los filtros de tiempo de arranque se agregan al sistema cuando se inicia el controlador TCP/IP y se quitan cuando BFE finaliza la inicialización. Los objetos persistentes se agregan cuando se inicia BFE.

En muchos casos, es posible que un proveedor de directivas no quiera que se aplique su directiva persistente si el proveedor se ha deshabilitado. Al agregar un proveedor, el autor de la llamada puede especificar un nombre Windows servicio opcional. Al agregar objetos persistentes, el autor de la llamada puede especificar opcionalmente el proveedor que "posee" ese objeto. Al iniciar el servicio, BFE solo agrega objetos persistentes al sistema si no están asociados a un proveedor, si el proveedor asociado no tiene ningún nombre de servicio Windows o si el servicio Windows asociado está establecido en inicio automático.

## <a name="object-associations"></a>Asociaciones de objeto

Algunos objetos tienen referencias a otros objetos. Por ejemplo, un filtro siempre hace referencia a una capa y puede hacer referencia a una llamada y a un contexto de proveedor. Los objetos no pueden hacer referencia a objetos que pueden tener una duración más corta. Por lo tanto, un objeto dinámico no puede hacer referencia a un objeto dinámico desde una sesión diferente. Un objeto estático no puede hacer referencia a un objeto dinámico. Un objeto persistente no puede hacer referencia a un objeto dinámico, a un objeto estático o a un objeto persistente propiedad de un proveedor diferente.

Un objeto no se puede eliminar hasta que todos los objetos que hacen referencia a él se hayan eliminado por primera vez.

## <a name="luids-and-guids"></a>LUID y GUID

Todos los objetos de API WFP en modo de usuario (FWPM) se identifican mediante un identificador único global **(GUID)** y hacen referencia a otros objetos por sus **GUID.** El **GUID** solo debe ser único dentro del tipo de objeto. Por ejemplo, un filtro y un contexto de proveedor pueden tener el mismo **GUID,** pero dos filtros no. Al agregar un nuevo objeto, los autores de la llamada pueden asignar el **GUID** del objeto o dejarlo inicializado en cero y permitir que BFE asigne el **GUID**.

Todos los objetos de API WFP (FWPS) en modo kernel se identifican mediante un identificador único local **(LUID)** y hacen referencia a otros objetos por su LUID. El cambio de **GUID** a **LUID** permite a WFP conservar el grupo no paginado y optimizar el procesamiento en tiempo de ejecución. El ancho del **LUID** depende del tipo de objeto y de los intervalos de **UINT16** a **UINT64.** BFE siempre asigna los **LUID.**

 

 