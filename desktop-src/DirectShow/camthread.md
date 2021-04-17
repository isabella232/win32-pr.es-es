---
description: La clase CAMThread es una clase abstracta para la administración de subprocesos de trabajo.
ms.assetid: c217d879-0203-4566-96ad-7463b05bc990
title: Clase CAMThread (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5c2bde058267ae4c530f33a96778792d5fe247b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670739"
---
# <a name="camthread-class"></a>Clase CAMThread

La `CAMThread` clase es una clase abstracta para la administración de subprocesos de trabajo.



| Variables de miembro protegidas                                 | Descripción                                                                  |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| [**m \_ hThread**](camthread-m-hthread.md)                  | Identificador del subproceso.                                                        |
| Variables de miembro público                                    | Descripción                                                                  |
| [**m \_ AccessLock**](camthread-m-accesslock.md)            | Sección crítica que bloquea el subproceso para que no tenga acceso a otros subprocesos. |
| [**m \_ WorkerLock**](camthread-m-workerlock.md)            | Sección crítica que bloquea los datos compartidos entre subprocesos.                       |
| Métodos públicos                                             | Descripción                                                                  |
| [**CAMThread**](camthread-camthread.md)                   | Método de constructor.                                                          |
| [**~ CAMThread**](camthread--camthread.md)                | Método de destructor. Virtualiza.                                                  |
| [**InitialThreadProc**](camthread-initialthreadproc.md)   | Llama al método ThreadProc cuando se crea el subproceso.                      |
| [**A**](camthread-create.md)                         | Crea el subproceso.                                                          |
| [**CallWorker**](camthread-callworker.md)                 | Señala el subproceso con una solicitud.                                           |
| [**Cercanos**](camthread-close.md)                           | Espera a que se cierre el subproceso y, a continuación, libera sus recursos.                   |
| [**ThreadExists**](camthread-threadexists.md)             | Consulta si el subproceso existe.                                           |
| [**GetRequest**](camthread-getrequest.md)                 | Espera la siguiente solicitud.                                                  |
| [**CheckRequest**](camthread-checkrequest.md)             | Comprueba si hay una solicitud, sin bloqueos.                              |
| [**Responder**](camthread-reply.md)                           | Responde a una solicitud.                                                        |
| [**GetRequestHandle**](camthread-getrequesthandle.md)     | Recupera un identificador para el evento señalado por el método CallWorker.           |
| [**GetRequestParam**](camthread-getrequestparam.md)       | Recupera la solicitud más reciente.                                                |
| [**CoInitializeHelper**](camthread-coinitializehelper.md) | Llama a CoInitializeEx al inicio del subproceso.                             |
| Métodos virtuales puros                                       | Descripción                                                                  |
| [**ThreadProc**](camthread-threadproc.md)                 | Procedimiento de subproceso.                                                            |



 

## <a name="remarks"></a>Observaciones

Esta clase proporciona métodos para crear un subproceso de trabajo, pasar solicitudes al subproceso y esperar a que el subproceso salga. Para usar esta clase, haga lo siguiente:

-   Derive una clase de `CAMThread` e invalide el método virtual puro [**CAMThread:: ThreadProc**](camthread-threadproc.md). Este método es el procedimiento de subproceso al que se llama al principio del subproceso.
-   En la aplicación, cree una instancia de la clase derivada. Al crear el objeto, no se crea el subproceso. Para crear el subproceso, llame al método [**CAMThread:: Create**](camthread-create.md) .
-   Para enviar solicitudes al subproceso, llame al método [**CAMThread:: CallWorker**](camthread-callworker.md) . Este método toma un parámetro DWORD, cuyo significado está definido por la clase. El método se bloquea hasta que el subproceso responde (consulte a continuación).
-   En el procedimiento de subproceso, responda a las solicitudes llamando a [**CAMThread:: GetRequest**](camthread-getrequest.md) o [**CAMThread:: CheckRequest**](camthread-checkrequest.md). El método GetRequest se bloquea hasta que otro subproceso llama a CallWorker. El método CheckRequest no es de bloqueo, lo que permite al subproceso comprobar si hay nuevas solicitudes mientras se trabaja de forma asincrónica.
-   Cuando el subproceso recibe una solicitud, llame a [**CAMThread:: reply**](camthread-reply.md) para desbloquear el subproceso que realiza la llamada. El método reply toma un parámetro DWORD, que se pasa al subproceso que realiza la llamada como el valor devuelto para CallWorker.

Cuando haya terminado con el subproceso, llame al método [**CAMThread:: Close**](camthread-close.md) . Este método espera a que se cierre el subproceso y, a continuación, cierra el identificador del subproceso. Se debe garantizar que el mensaje ThreadProc se cierre, ya sea por sí mismo o en respuesta a una solicitud CallWorker. El método de destructor también llama a Close.

En el ejemplo siguiente se muestran estos pasos:


```C++
class MyThread : public CAMThread
{
protected:
    DWORD ThreadProc(void);
};

DWORD MyThread::ThreadProc()
{
    BOOL bShutDown = FALSE;
    while (!bShutDown)
    {
        DWORD req = GetRequest();
        printf("Request: %d\n", req);
        bShutDown = (req == 0);
        Reply(bShutDown ? S_FALSE : S_OK);
    }
    printf("Quitting Thread\n");
    return 1;
}

void main()
{
    MyThread thread;
    DWORD reply;
    
    thread.Create();
    reply = thread.CallWorker(3);
    reply = thread.CallWorker(0); // Thread exits.
}
```



En la clase derivada, también puede definir funciones miembro que validan los parámetros en CallWorker. En el ejemplo siguiente se muestra una forma típica de hacerlo:


```C++
enum Command {CMD_INIT, CMD_RUN, CMD_STOP, CMD_EXIT};

HRESULT Init(void)  { return CallWorker(CMD_INIT); }
HRESULT Run(void)   { return CallWorker(CMD_RUN); }
HRESULT Stop(void)  { return CallWorker(CMD_STOP); }
HRESULT Exit(void)  { return CallWorker(CMD_EXIT); }
```



La `CAMThread` clase proporciona dos secciones críticas como variables de miembro público. Use `CAMThread::m_AccessLock` para impedir que otros subprocesos accedan al subproceso. (Por ejemplo, los métodos Create y CallWorker contienen este bloqueo para serializar las operaciones en el subproceso). Use [**CAMThread:: m \_ WorkerLock**](camthread-m-workerlock.md) para bloquear los datos que se comparten entre los subprocesos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




