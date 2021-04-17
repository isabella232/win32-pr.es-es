---
title: Ciclo de vida de un trabajo de BITS
description: El ciclo de vida de un trabajo de BITS comienza cuando se crea un trabajo.
ms.assetid: b765a8ef-74bd-475e-9cd9-e9e2cf4f0305
ms.topic: article
ms.date: 11/13/2018
ms.openlocfilehash: c6ac23c598d28681968e9c0cbed776ba24c57e98
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105660013"
---
# <a name="bits-job-states"></a>Estados de trabajo de BITS
Hay cuatro clases de [**Estados**](/windows/desktop/api/Bits/ne-bits-bg_job_state)de bits: Starting, Action, transfiriód y final. A medida que se ejecuta un trabajo, realiza la transición entre los Estados de las distintas clases de estado. Una vez que un trabajo se encuentra en un estado final, no sale del estado final y no se muestra en una [enumeración de trabajos](/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-enumjobs).

## <a name="state-changing-methods"></a>Métodos de cambio de estado
Hay cuatro métodos de cambio de estado en un trabajo: [**Cancelar**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel), [**completar**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete), [**reanudar**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)y [**suspender**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-suspend). Siempre que un trabajo no esté en un estado final, puede llamar a cualquiera de los métodos de cambio de estado. 

El método [**Suspend**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-suspend) se usa para cambiar un trabajo al estado Suspended. Cuando se suspende un trabajo, todas sus transferencias se detendrán y no se reanudarán hasta que llame a resume.
Un trabajo que ya está suspendido permanecerá suspendido.

El método [**resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) se usa para iniciar un trabajo que está suspendido. Los trabajos en un estado de error o transitorio se configurarán para que se vuelvan a intentar. Los trabajos que están actualmente en estado de acción permanecerán en ese estado.

El método [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) se usa para cancelar un trabajo. El estado cambiará a cancelado. Los archivos que se están transfiriendo actualmente no se completarán. Se eliminarán todos los archivos transferidos completamente y transferidos parcialmente.

El método [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) finalizará una transferencia. Se conservarán los archivos totalmente descargados; se eliminarán los archivos que no se hayan transferido completamente.

Debe llamar a Cancel o complete para pasar el trabajo a un estado final y limpiarlo. Los trabajos que no pasan a un estado final perderán los recursos del sistema. Los BITS cancelarán automáticamente los trabajos antiguos. El valor predeterminado de [valor jobinactivitytimeout](/windows/desktop/Bits/group-policies) es cancelar los trabajos después de 90 días.


## <a name="starting-state"></a>Estado inicial 
El estado de inicio es **Suspended**. Desde aquí, puede Agregar archivos al trabajo y establecer las propiedades del trabajo y del archivo. Para iniciar un trabajo que transfiere, llame a resume en el trabajo. Si reanuda un trabajo sin archivos, devolverá un código de error de BG_E_EMPTY y el trabajo permanecerá suspendido.

## <a name="action-states"></a>Estados de acción
Los Estados **en cola**, **conectando** y **transfiriendo** muestran la actividad interna actual del trabajo. Un trabajo que está en cola está listo para ser programado, posiblemente esperando al programador de BITS o a la espera de que el usuario inicie sesión. Un trabajo que se está CONECTAndo está intentando conectarse al servidor para iniciar la transferencia de archivos. Un trabajo que está transfiriendo está cargando o descargando los archivos activamente.

El estado de **error transitorio** significa que el trabajo ha intentado y no pudo transferir el archivo. Esto puede deberse a las razones de la Directiva de red; es posible que el trabajo esté bloqueado porque la red actual es demasiado costosa. También puede bloquearse por motivos del sistema, como el sistema está en el modo de ahorro de batería o de juego, o porque no hay conectividad a Internet. 

Los BITS volverán a intentar automáticamente los trabajos en el estado de error transitorio cuando sea necesario. BITS incluye un valor [MinimumRetryDelay](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay) y [NoProgressTimeout](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) para controlar cuándo se vuelve a intentar un trabajo y cuándo los bits dejarán de intentarlo.


## <a name="transferred-states"></a>Estados transferidos
Los Estados transferidos se producen cuando no se realiza ninguna operación de transferencia. Debe cancelar o completar un trabajo en este estado. También puede agregar más archivos para transferir y llamar a resume (), pero esto no es una práctica común.

El estado de **error** se produce cuando se realiza una transferencia (no se volverá a intentar), pero no se realizó correctamente. Todos los archivos deben transferirse para que sean correctos; Si se produce un error de forma permanente, el trabajo será erróneo. Normalmente llamará a Cancel o complete para trasladar el trabajo a un estado final. La diferencia práctica es que, cuando se llama a CANCEL, se eliminarán todos los archivos transferidos correctamente, pero si se llama a complete, no se eliminarán los archivos transferidos correctamente.

Los motivos para estar en un estado de ERROR son: 
* Se mantiene demasiado tiempo en un estado de ERROR transitorio (más allá del valor de [NoProgressTimeout](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) ).
* Obtención de un error BG_E_TOKEN_REQUIRED y necesidad de asistencia con [tokens auxiliares](/windows/desktop/Bits/helper-tokens-for-bits-transfer-jobs)

Es una práctica habitual volver a configurar un trabajo de ERROR y, a continuación, llamar a resume para volver a intentar el trabajo. Por ejemplo, es posible que la aplicación necesite actualizar el nombre remoto de un archivo a través de [SetRemoteName](/windows/desktop/api/bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename).

El estado **transferido** tiene lugar cuando se realiza una transferencia y se realiza correctamente. Debe llamar a complete para finalizar el trabajo; en el caso de los trabajos de descarga, los archivos descargados no estarán disponibles hasta que se llame a complete. La excepción a esta regla son los trabajos que son los trabajos de alto rendimiento (y debe seguir llamando a complete).

## <a name="final-states"></a>Estados finales
Una vez que un trabajo se encuentra en un estado final, no se puede llamar a ninguno de los métodos de cambio de estado. El trabajo se **confirmará** después de llamar a complete () y todos los archivos descargados finalizados estarán disponibles. El trabajo se **cancelará** después de llamar a CANCEL () y se eliminarán todos los archivos descargados. 


## <a name="life-cycle-of-a-bits-job"></a>Ciclo de vida de un trabajo de BITS

El ciclo de vida de un trabajo de BITS comienza cuando se crea un trabajo. Un trabajo es un contenedor que contiene uno o varios archivos que se van a transferir. Un trabajo también tiene propiedades que especifican cómo transfiere BITS los archivos e interactúa con la aplicación. Por ejemplo, puede especificar la prioridad del trabajo, si el trabajo es un trabajo de carga o descarga, y para qué eventos desea recibir la notificación.

Después de crear el trabajo, agregue uno o varios archivos (los trabajos de carga solo pueden contener un archivo) al trabajo y cambie cualquiera de los valores de propiedad según sea necesario para la aplicación. Al agregar un archivo al trabajo, especifique tanto el nombre local (cliente) como el nombre remoto (servidor) del archivo. El nombre de archivo remoto debe usar el protocolo HTTP, HTTPS o SMB. Los archivos dentro de un trabajo se procesan de forma secuencial (primero en, primero en salir).

BITS suspende automáticamente los trabajos cuando se crean. Debe reanudar el trabajo para activarlo en la cola de transferencia. Puede suspender o reanudar un trabajo en cualquier momento. Al reanudar el trabajo, el trabajo se mueve del estado suspendido al estado en cola. El trabajo permanece en el estado en cola hasta que el programador determina que es el turno del trabajo para transferir los archivos. Todos los trabajos en primer plano se ejecutan simultáneamente con un trabajo en segundo plano. BITS procesa los archivos dentro de los trabajos en primer plano en serie.

Cuando el trabajo de transferencia de archivos es un trabajo, el trabajo pasa al estado de conexión mientras BITS se conecta al servidor remoto (especificado en el nombre de archivo remoto). Si BITS puede conectarse al servidor remoto, el trabajo pasa al estado de transferencia cuando permanece hasta que finaliza su intervalo de tiempo, se completa la transferencia, se produce un error o la aplicación suspende el trabajo.

El trabajo se mueve entre la cola, la conexión y la transferencia de Estados hasta que BITS transfiere todos los archivos del trabajo. En ese momento, el trabajo pasa al estado transferido. BITS usa la programación Round Robin para programar trabajos que se encuentran en el mismo nivel de prioridad. A cada trabajo se le asigna un segmento de tiempo para procesar sus archivos. Si el trabajo no se completa durante su intervalo de tiempo, el trabajo vuelve al estado en cola y se activa el siguiente trabajo de la cola. Esto evita que los trabajos grandes bloqueen trabajos más pequeños. Los trabajos se procesan en gran medida en la primera parte, primero en salir (FIFO). sin embargo, BITS no puede garantizar el procesamiento FIFO debido a la programación Round Robin, los errores de trabajo y los reinicios del servicio.

Los archivos transferidos no están disponibles para el cliente hasta que la aplicación llama al método [**IBackgroundCopyJob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) para transferir la propiedad de los archivos de bits al usuario. Los trabajos de carga también se establecen en el estado transferido cuando el servidor recibe correctamente el archivo. Los trabajos de carga y respuesta se establecen en el estado transferido después de que el archivo se haya enviado correctamente al servidor y la respuesta de la aplicación de servidor se haya transferido correctamente al cliente.

Si se produce un error, el trabajo pasa al estado de error grave o transitorio. Los errores irrecuperables son errores que no pueden recuperar BITS de o que requieren la intervención de corregir. Si la aplicación puede corregir el error, la aplicación reanuda el trabajo y BITS mueve el trabajo al estado en cola. Los errores transitorios son errores que pueden resolverse por sí mismos. BITS reintenta los trabajos en el estado de error transitorio hasta que la transferencia se realiza correctamente o se agota el tiempo de espera del trabajo. El trabajo agota el tiempo de espera cuando no se realiza ningún progreso dentro de un período especificado por la aplicación. Si se agota el tiempo de espera del trabajo, BITS mueve el trabajo a un estado de error irrecuperable.

Para más información sobre los Estados de trabajo, consulte [**\_ \_ Estado del trabajo de BG**](/windows/desktop/api/Bits/ne-bits-bg_job_state).
