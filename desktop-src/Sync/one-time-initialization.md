---
description: Los componentes suelen diseñarse para realizar tareas de inicialización cuando se les llama por primera vez, en lugar de cuando se cargan.
ms.assetid: 404c083c-7bee-44c2-b8e7-da1901b6ab2f
title: Inicialización de One-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16f451e3c51716b4ff6f33b55d8d8602b5d5c28f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669779"
---
# <a name="one-time-initialization"></a>Inicialización de One-Time

Los componentes suelen diseñarse para realizar tareas de inicialización cuando se les llama por primera vez, en lugar de cuando se cargan. Las funciones de inicialización únicas garantizan que esta inicialización se produce una sola vez, incluso cuando varios subprocesos pueden intentar la inicialización.

**Windows Server 2003 y Windows XP:** Las aplicaciones deben proporcionar su propia sincronización para la inicialización única mediante el uso de las [funciones de interbloqueo](interlocked-variable-access.md) u otro mecanismo de sincronización. Las funciones de inicialización de un solo paso están disponibles a partir de Windows Vista y Windows Server 2008.

Las funciones de inicialización únicas proporcionan ventajas significativas para asegurarse de que solo un subproceso realiza la inicialización:

-   Están optimizados para la velocidad.
-   Crean las barreras adecuadas en las arquitecturas de procesador que las necesitan.
-   Admiten la inicialización en paralelo y bloqueada.
-   Evitan el bloqueo interno para que el código pueda funcionar de forma asincrónica o sincrónica.

El sistema administra el proceso de inicialización a través de una estructura de inicialización opaca **\_ una vez** que contiene datos e información de estado. El autor de la llamada asigna esta estructura y la inicializa mediante una llamada a [**InitOnceInitialize**](/windows/win32/api/synchapi/nf-synchapi-initonceinitialize) (para inicializar la estructura dinámicamente) o asigna la constante **init \_ una vez \_ a \_** la variable de estructura (para inicializar la estructura estáticamente). Inicialmente, los datos almacenados en la estructura de inicialización única son NULL y su estado es no inicializado.

Las estructuras de inicialización de un solo uso no se pueden compartir entre los procesos.

El subproceso que realiza la inicialización puede establecer opcionalmente un contexto que esté disponible para el autor de la llamada después de que se complete la inicialización. El contexto puede ser un objeto de sincronización o puede ser un valor o una estructura de datos. Si el contexto es un valor, su inicialización de orden inferior **\_ una vez que los \_ \_ \_ bits reservados de CTX** deben ser cero. Si el contexto es una estructura de datos, la estructura de datos debe alinearse con **DWORD**. El contexto se devuelve al autor de la llamada en el parámetro de salida *lpContext* de la función [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) o [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) .

La inicialización única puede realizarse de forma sincrónica o asincrónica. Se puede usar una función de devolución de llamada opcional para la inicialización única sincrónica.

## <a name="synchronous-one-time-initialization"></a>Inicialización única sincrónica

En los pasos siguientes se describe la inicialización única sincrónica que no utiliza una función de devolución de llamada.

1.  El primer subproceso que llama a la función [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) produce correctamente la inicialización de una sola vez. Para la inicialización única sincrónica, se debe llamar a **InitOnceBeginInitialize** sin el marcador de inicialización una **\_ vez \_** .
2.  Los subprocesos posteriores que intentan inicializarse se bloquean hasta que el primer subproceso complete la inicialización o se produzca un error. Si se produce un error en el primer subproceso, se permite que el siguiente subproceso intente la inicialización, etc.
3.  Una vez finalizada la inicialización, el subproceso llama a la función [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) . El subproceso puede crear opcionalmente un objeto de sincronización (u otros datos de contexto) y especificarlo en el parámetro *lpContext* de la función **InitOnceComplete** .
4.  Si la inicialización se realiza correctamente, el estado de la estructura de inicialización única se cambia a inicializado y el identificador de *lpContext* (si existe) se almacena en la estructura de inicialización. Los intentos de inicialización subsiguientes devuelven estos datos de contexto. Si se produce un error en la inicialización, los datos son **null**.

En los pasos siguientes se describe la inicialización única sincrónica que usa una función de devolución de llamada.

1.  El primer subproceso para llamar correctamente a la función [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) pasa un puntero a una función de devolución de llamada [*InitOnceCallback*](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn) definida por la aplicación y a los datos requeridos por la función de devolución de llamada. Si la llamada se realiza correctamente, se ejecuta la función de devolución de llamada *InitOnceCallback* .
2.  Los subprocesos posteriores que intentan inicializarse se bloquean hasta que el primer subproceso complete la inicialización o se produzca un error. Si se produce un error en el primer subproceso, se permite que el siguiente subproceso intente la inicialización, etc.
3.  Una vez finalizada la inicialización, la función de devolución de llamada devuelve. Opcionalmente, la función de devolución de llamada puede crear un objeto de sincronización (u otros datos de contexto) y especificarlo en su parámetro de salida de *contexto* .
4.  Si la inicialización se realiza correctamente, el estado de la estructura de inicialización única se cambia a inicializado y el identificador de *contexto* (si existe) se almacena en la estructura de inicialización. Los intentos de inicialización subsiguientes devuelven estos datos de contexto. Si se produce un error en la inicialización, los datos son **null**.

## <a name="asynchronous-one-time-initialization"></a>Inicialización única asincrónica

Los pasos siguientes describen la inicialización única asincrónica.

1.  Si varios subprocesos intentan iniciar la inicialización simultáneamente mediante una llamada a [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) con **init \_ una vez \_ Async**, la función se ejecuta correctamente para todos los subprocesos con el parámetro *fPending* establecido en **true**. En realidad, solo se realizará correctamente un subproceso durante la inicialización; otros intentos simultáneos no cambian el estado de inicialización.
2.  Cuando [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) devuelve, el parámetro *fPending* indica el estado de inicialización:
    -   Si *fPending* es **false**, un subproceso se ha realizado correctamente al inicializarse. Otros subprocesos deben limpiar todos los datos de contexto que hayan creado y usar los datos de contexto en el parámetro de salida *lpContext* de [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize).
    -   Si *fPending* es **true**, la inicialización aún no se ha completado y otros subprocesos deben continuar.
3.  Cada subproceso llama a la función [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) . El subproceso puede crear opcionalmente un objeto de sincronización (u otros datos de contexto) y especificarlo en el parámetro *lpContext* de **InitOnceComplete**.
4.  Cuando [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) devuelve, su valor devuelto indica si el subproceso que realiza la llamada se realizó correctamente en la inicialización.
    -   Si [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) se ejecuta correctamente, el subproceso que realiza la llamada se ha realizado correctamente en la inicialización. El estado de la estructura de inicialización única se cambia a inicializado y el identificador de *lpContext* (si existe) se almacena en la estructura de inicialización.
    -   Si [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) produce un error, otro subproceso se ha realizado correctamente al inicializarse. El subproceso que realiza la llamada debe limpiar todos los datos de contexto que haya creado y llamar a [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) con **init \_ una vez \_ \_ solo** para recuperar los datos de contexto almacenados en la estructura de inicialización única.

## <a name="calling-one-time-initialization-from-multiple-sites"></a>Llamar a One-Time inicialización desde varios sitios

Inicialización única que protege una sola **init \_ una vez** que la estructura puede realizarse desde sitios varias; se puede pasar una devolución de llamada diferente de cada sitio y se puede mezclar la sincronización con y sin devolución de llamada. La inicialización todavía está configurada para realizar sucesfully una sola vez.

Sin embargo, no se puede mezclar la inicialización asincrónica y sincrónica: una vez que se intenta la inicialización asincrónica, se producirá un error al intentar iniciar la inicialización sincrónica.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar la inicialización de One-Time](using-one-time-initialization.md)
</dt> </dl>

 

 
