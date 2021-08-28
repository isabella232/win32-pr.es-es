---
description: Los componentes suelen estar diseñados para realizar tareas de inicialización cuando se llaman por primera vez, en lugar de cuando se cargan.
ms.assetid: 404c083c-7bee-44c2-b8e7-da1901b6ab2f
title: One-Time inicialización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e513c18be3fcce85c8d2cde16bbe11edcf6a1597bb06c37279ecaa8add6598
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073085"
---
# <a name="one-time-initialization"></a>One-Time inicialización

Los componentes suelen estar diseñados para realizar tareas de inicialización cuando se llaman por primera vez, en lugar de cuando se cargan. Las funciones de inicialización única garantizan que esta inicialización se produce solo una vez, incluso cuando varios subprocesos pueden intentar la inicialización.

**Windows Server 2003 y Windows XP:** Las aplicaciones deben proporcionar su propia sincronización para la inicialización única mediante las [funciones](interlocked-variable-access.md) entrelazados u otro mecanismo de sincronización. Las funciones de inicialización única están disponibles a partir de Windows Vista y Windows Server 2008.

Las funciones de inicialización única proporcionan ventajas significativas para asegurarse de que solo un subproceso realiza la inicialización:

-   Están optimizados para la velocidad.
-   Crean las barreras adecuadas en las arquitecturas de procesador que las requieren.
-   Admiten la inicialización bloqueada y en paralelo.
-   Evitan el bloqueo interno para que el código pueda funcionar de forma asincrónica o sincrónica.

El sistema administra el proceso de inicialización a través de una estructura **INIT \_ ONCE** opaca que contiene información de datos y estado. El autor de la llamada asigna esta estructura y la inicializa llamando a [**InitOnceInitialize**](/windows/win32/api/synchapi/nf-synchapi-initonceinitialize) (para inicializar la estructura dinámicamente) o asignando la constante **INIT \_ ONCE STATIC \_ \_ INIT** a la variable de estructura (para inicializar la estructura estáticamente). Inicialmente, los datos almacenados en la estructura de inicialización única son NULL y su estado no está inicializado.

Las estructuras de inicialización única no se pueden compartir entre procesos.

El subproceso que realiza la inicialización puede establecer opcionalmente un contexto que esté disponible para el autor de la llamada una vez completada la inicialización. El contexto puede ser un objeto de sincronización o puede ser un valor o una estructura de datos. Si el contexto es un valor, sus **BITS RESERVADOs INIT \_ ONCE \_ CTX \_ de \_** orden bajo deben ser cero. Si el contexto es una estructura de datos, la estructura de datos debe estar **alineada con DWORD.** El contexto se devuelve al autor de la llamada en el parámetro *de salida lpContext* de la función [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) [**o InitOnceExecuteOnce.**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce)

La inicialización única se puede realizar de forma sincrónica o asincrónica. Se puede usar una función de devolución de llamada opcional para la inicialización sincrónica de una sola vez.

## <a name="synchronous-one-time-initialization"></a>Inicialización sincrónica única

En los pasos siguientes se describe la inicialización sincrónica de un solo uso que no usa una función de devolución de llamada.

1.  El primer subproceso que llama a la [**función InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) hace que se inicie correctamente la inicialización única. Para la inicialización sincrónica de una sola vez, se debe llamar a **InitOnceBeginInitialize** sin la marca **INIT \_ ONCE \_ ASYNC.**
2.  Los subprocesos subsiguientes que intentan inicializar se bloquean hasta que el primer subproceso completa la inicialización o produce un error. Si se produce un error en el primer subproceso, el siguiente puede intentar la inicialización, y así sucesivamente.
3.  Cuando finaliza la inicialización, el subproceso llama a [**la función InitOnceComplete.**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) Opcionalmente, el subproceso puede crear un objeto de sincronización (u otros datos de contexto) y especificarlo en el parámetro *lpContext* de la **función InitOnceComplete.**
4.  Si la inicialización se realiza correctamente, el estado de la estructura de inicialización única cambia a inicializado y el identificador *lpContext* (si existe) se almacena en la estructura de inicialización. Los intentos de inicialización posteriores devuelven estos datos de contexto. Si se produce un error en la inicialización, los datos son **NULL.**

En los pasos siguientes se describe la inicialización sincrónica de un solo uso que usa una función de devolución de llamada.

1.  El primer subproceso que llama correctamente a la función [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) pasa un puntero a una función de devolución de llamada [*InitOnceCallback*](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn) definida por la aplicación y a los datos requeridos por la función de devolución de llamada. Si la llamada se realiza correctamente, se ejecuta la función de devolución de llamada *InitOnceCallback.*
2.  Los subprocesos subsiguientes que intentan inicializar se bloquean hasta que el primer subproceso completa la inicialización o produce un error. Si se produce un error en el primer subproceso, el siguiente puede intentar la inicialización, y así sucesivamente.
3.  Cuando finaliza la inicialización, se devuelve la función de devolución de llamada. Opcionalmente, la función de devolución de llamada puede crear un objeto de sincronización (u otros datos de contexto) y especificarlo en su *parámetro de salida Context.*
4.  Si la inicialización se realiza correctamente, el estado de la  estructura de inicialización única se cambia a inicializado y el identificador de contexto (si existe) se almacena en la estructura de inicialización. Los intentos de inicialización posteriores devuelven estos datos de contexto. Si se produce un error en la inicialización, los datos son **NULL.**

## <a name="asynchronous-one-time-initialization"></a>Inicialización asincrónica de una sola vez

En los pasos siguientes se describe la inicialización asincrónica de una sola vez.

1.  Si varios subprocesos intentan iniciar simultáneamente la inicialización mediante una llamada a [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) con **INIT \_ ONCE \_ ASYNC**, la función se realiza correctamente para todos los subprocesos con el parámetro *fPending* establecido en **TRUE.** Solo un subproceso se realizará correctamente en la inicialización; otros intentos simultáneos no cambian el estado de inicialización.
2.  Cuando [**se devuelve InitOnceBeginInitialize,**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) el *parámetro fPending* indica el estado de inicialización:
    -   Si *fPending es* **FALSE,** un subproceso se ha inicializado correctamente. Otros subprocesos deben limpiar los datos de contexto que han creado y usar los datos de contexto en el parámetro de salida *lpContext* [**de InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize).
    -   Si *fPending es* **TRUE,** la inicialización aún no se ha completado y otros subprocesos deben continuar.
3.  Cada subproceso llama a la [**función InitOnceComplete.**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) Opcionalmente, el subproceso puede crear un objeto de sincronización (u otros datos de contexto) y especificarlo en el parámetro *lpContext* **de InitOnceComplete**.
4.  Cuando [**InitOnceComplete devuelve**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) un valor, su valor devuelto indica si el subproceso que realiza la llamada se ha inicializado correctamente.
    -   Si [**InitOnceComplete se**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) realiza correctamente, el subproceso que realiza la llamada se ha inicializado correctamente. El estado de la estructura de inicialización única se cambia a inicializado y el identificador *lpContext* (si existe) se almacena en la estructura de inicialización.
    -   Si [**Se produce un error en InitOnceComplete,**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) otro subproceso se ha inicializado correctamente. El subproceso que realiza la llamada debe limpiar todos los datos de contexto que haya creado y llamar a [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) con **INIT \_ ONCE CHECK \_ \_ ONLY** para recuperar los datos de contexto almacenados en la estructura de inicialización única.

## <a name="calling-one-time-initialization-from-multiple-sites"></a>Llamada a One-Time inicialización desde varios sitios

La inicialización única que protege una sola estructura **INIT \_ ONCE** se puede realizar desde sitios mutiple; se puede pasar una devolución de llamada diferente desde cada sitio y se puede mezclar la sincronización con y sin devolución de llamada. La inicialización todavía está en proceso para realizarse correctamente una sola vez.

Sin embargo, la inicialización asincrónica y sincrónica no se puede mezclar: una vez que se intenta la inicialización asincrónica, se produciría un error al intentar iniciar la inicialización sincrónica.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de One-Time inicialización](using-one-time-initialization.md)
</dt> </dl>

 

 
