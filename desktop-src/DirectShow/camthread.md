---
description: La clase CAMThread es una clase abstracta para administrar subprocesos de trabajo.
ms.assetid: c217d879-0203-4566-96ad-7463b05bc990
title: Clase CAMThread (Wxutil.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160235"
---
# <a name="camthread-class"></a>CLASE CAMThread

La `CAMThread` clase es una clase abstracta para administrar subprocesos de trabajo.



| Variables miembro protegidas                                 | Descripción                                                                  |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| [**m \_ hThread**](camthread-m-hthread.md)                  | Identificador del subproceso.                                                        |
| Variables de miembro público                                    | Descripción                                                                  |
| [**m \_ AccessLock**](camthread-m-accesslock.md)            | Sección crítica que bloquea el acceso al subproceso por parte de otros subprocesos. |
| [**m \_ WorkerLock**](camthread-m-workerlock.md)            | Sección crítica que bloquea los datos compartidos entre subprocesos.                       |
| Métodos públicos                                             | Descripción                                                                  |
| [**CAMThread**](camthread-camthread.md)                   | Método constructor.                                                          |
| [**~ CAMThread**](camthread--camthread.md)                | Método destructor. Virtual.                                                  |
| [**InitialThreadProc**](camthread-initialthreadproc.md)   | Llama al método ThreadProc cuando se crea el subproceso.                      |
| [**Crear**](camthread-create.md)                         | Crea el subproceso.                                                          |
| [**CallWorker**](camthread-callworker.md)                 | Señala el subproceso con una solicitud.                                           |
| [**Cerca**](camthread-close.md)                           | Espera a que se cierre el subproceso y, a continuación, libera sus recursos.                   |
| [**ThreadExists**](camthread-threadexists.md)             | Consulta si el subproceso existe.                                           |
| [**GetRequest**](camthread-getrequest.md)                 | Espera a la siguiente solicitud.                                                  |
| [**CheckRequest**](camthread-checkrequest.md)             | Comprueba si hay una solicitud, sin bloquear.                              |
| [**Respuesta**](camthread-reply.md)                           | Responde a una solicitud.                                                        |
| [**GetRequestHandle**](camthread-getrequesthandle.md)     | Recupera un identificador para el evento señalado por el método CallWorker.           |
| [**GetRequestParam**](camthread-getrequestparam.md)       | Recupera la solicitud más reciente.                                                |
| [**CoInitializeHelper**](camthread-coinitializehelper.md) | Llama a CoInitializeEx al principio del subproceso.                             |
| Métodos virtuales puros                                       | Descripción                                                                  |
| [**ThreadProc**](camthread-threadproc.md)                 | Procedimiento de subproceso.                                                            |



 

## <a name="remarks"></a>Observaciones

Esta clase proporciona métodos para crear un subproceso de trabajo, pasar solicitudes al subproceso y esperar a que se cierre el subproceso. Para usar esta clase, haga lo siguiente:

-   Derive una clase de `CAMThread` e invalide el método virtual [**puro CAMThread::ThreadProc**](camthread-threadproc.md). Este método es el procedimiento de subproceso al que se llama al principio del subproceso.
-   En la aplicación, cree una instancia de la clase derivada. La creación del objeto no crea el subproceso. Para crear el subproceso, llame al [**método CAMThread::Create.**](camthread-create.md)
-   Para enviar solicitudes al subproceso, llame al [**método CAMThread::CallWorker.**](camthread-callworker.md) Este método toma un parámetro DWORD, cuyo significado se define mediante la clase . El método se bloquea hasta que el subproceso responde (vea a continuación).
-   En el procedimiento del subproceso, responda a las solicitudes mediante una llamada [**a CAMThread::GetRequest**](camthread-getrequest.md) o [**a CAMThread::CheckRequest**](camthread-checkrequest.md). El método GetRequest se bloquea hasta que otro subproceso llama a CallWorker. El método CheckRequest no está bloqueado, lo que permite que el subproceso compruebe si hay nuevas solicitudes mientras se trabaja de forma asincrónica.
-   Cuando el subproceso recibe una solicitud, llame a [**CAMThread::Reply**](camthread-reply.md) para desbloquear el subproceso que realiza la llamada. El método Reply toma un parámetro DWORD, que se pasa al subproceso que realiza la llamada como valor devuelto para CallWorker.

Cuando haya terminado con el subproceso, llame al [**método CAMThread::Close.**](camthread-close.md) Este método espera a que se cierre el subproceso y, a continuación, cierra el identificador del subproceso. Se debe garantizar que el mensaje ThreadProc se cierre, ya sea por sí mismo o en respuesta a una solicitud de CallWorker. El método destructor también llama a Close.

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



En la clase derivada, también puede definir funciones miembro que validan los parámetros en CallWorker. En el ejemplo siguiente se muestra una manera típica de hacerlo:


```C++
enum Command {CMD_INIT, CMD_RUN, CMD_STOP, CMD_EXIT};

HRESULT Init(void)  { return CallWorker(CMD_INIT); }
HRESULT Run(void)   { return CallWorker(CMD_RUN); }
HRESULT Stop(void)  { return CallWorker(CMD_STOP); }
HRESULT Exit(void)  { return CallWorker(CMD_EXIT); }
```



La `CAMThread` clase proporciona dos secciones críticas como variables miembro públicas. Use `CAMThread::m_AccessLock` para evitar que otros subprocesos accedan al subproceso. (Por ejemplo, los métodos Create y CallWorker mantienen este bloqueo para serializar las operaciones en el subproceso). Use [**CAMThread::m \_ WorkerLock para**](camthread-m-workerlock.md) bloquear los datos que se comparten entre subprocesos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




