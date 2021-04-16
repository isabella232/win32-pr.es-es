---
title: SSPI asincrónico
description: Información general sobre el encabezado SSPI asincrónico.
ms.topic: article
ms.keywords: SSPI, Async SSPI, SSPI Async, Asynchronous SSPI, sspi,SspiAcceptSecurityContextAsync, SspiAcquireCredentialsHandleAsync, SspiAsyncContextRequiresNotify, SspiAsyncNotifyCallback, SspiCreateAsyncContext,SspiDeleteSecurityContextAsync, SspiFreeAsyncContext, SspiFreeCredentialsHandleAsync, SspiGetAsyncCallStatus, SspiInitializeSecurityContextAsync, SspiReinitAsyncContext, SspiSetAsyncNotifyCallback
ms.date: 06/23/2020
ms.openlocfilehash: acd1fedff605706dc5b20c3c2604a51d5cead27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720658"
---
# <a name="asynchronous-sspi"></a>SSPI asincrónico

El encabezado SSPI asincrónico incluye funciones que admiten objetos de contexto asincrónicos, lo que permite a los autores de llamadas establecer contextos de seguridad entre el servidor y los clientes remotos simultáneamente a través de un ciclo de vida de llamadas asincrónicas de SSPI.

## <a name="async-context-management-types"></a>Tipos de administración de contexto asincrónico

| Nombre de objeto | Descripción |
|-------------|--------------|
| [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nc-sspi-sspiasyncnotifycallback) | Devolución de llamada usada para notificar la finalización de una llamada SSPI asincrónica. |


## <a name="async-context-management-functions"></a>Funciones de administración de contexto Async

| Nombre de la API | Descripción |
|-------------|--------------|
| [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext) | Crea una instancia de SspiAsyncContext que se usa para realizar el seguimiento de la llamada asincrónica. |
| [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext) | Marca un contexto asincrónico para reutilizarlo. |
| [SspiSetAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) | Registra una devolución de llamada a la que se notifica en la finalización de la llamada asincrónica. |
| [SspiAsyncContextRequiresNotify](/windows/win32/api/sspi/nf-sspi-sspiasynccontextrequiresnotify) | Determina si un contexto asincrónico determinado requiere una notificación de la finalización de la llamada. |
| [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus) | Obtiene el estado actual de una llamada asincrónica asociada al contexto proporcionado.  |
| [SspiFreeAsyncContext](/windows/win32/api/sspi/nf-sspi-sspifreeasynccontext) | Libera un contexto creado en la llamada a la función SspiCreateAsyncContext. |

## <a name="async-sspi-functions"></a>Funciones SSPI asincrónicas

Las siguientes funciones aceptan un contexto asincrónico además de todos los mismos parámetros que su homólogo sincrónico.

| Nombre de la API | Descripción |
|-------------|--------------|
| [SspiAcquireCredentialsHandleAsync](/windows/win32/api/sspi/nf-sspi-sspiacquirecredentialshandleasynca) | Adquiere de forma asincrónica un identificador a las credenciales preexistentes de una entidad de seguridad. |
| [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync) | Permite que el componente de servidor de una aplicación de transporte establezca de forma asincrónica un contexto de seguridad entre el servidor y un cliente remoto. |
| [SspiInitializeSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiinitializesecuritycontextasynca) | Inicializa un contexto de seguridad Async. |
| [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync) | Elimina las estructuras de datos locales asociadas al contexto de seguridad especificado Iniciado por una llamada anterior a la función SspiInitializeSecurityContextAsync o la función SspiAcceptSecurityContextAsync. |
| [SspiFreeCredentialsHandleAsync](/windows/win32/api/sspi/nf-sspi-sspifreecredentialshandleasync) | Libera un identificador de credencial. |

## <a name="api-sample"></a>Ejemplo de API

Un flujo de llamadas típico funciona de la siguiente manera:
1) Crear contexto de SspiAsyncContext para realizar un seguimiento de la llamada mediante [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)
2) Registrar un [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) para el contexto
3) Hacer la llamada asincrónica mediante [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)
4) En la devolución de llamada, recupere el resultado mediante [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)
5) Elimine SspiAsyncContext con [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync). Si reutiliza el contexto con [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext), vuelva al paso 2.

En el ejemplo siguiente se muestra una invocación de SspiAcceptSecurityContextAsync. El ejemplo espera a que se complete la llamada y recupera el resultado.

En un protocolo de enlace SSPI completo, se llamará a SspiAcceptSecurityContextAsync y SspiInitializeSecurityContextAsync varias veces hasta que se devuelva SEC_E_OK. SspiReinitAsyncContext se ha proporcionado para facilitar el uso y facilitar el rendimiento en este caso.

Las aserciones se utilizan para resaltar lo que se esperaría en caso de éxito.

```cpp
#include <sspi.h>

void AsyncCallCompleted(
    _In_     SspiAsyncContext* AsyncContext,
    _In_opt_ PVOID pCallbackData
)
{
    // Get result.
    SECURITY_STATUS Status = SspiGetAsyncCallStatus(AsyncContext);
    ASSERT(SEC_E_OK == Status);

    // *Perform any needed callback actions, use pCallbackData if needed*

    // Clean up async context when done.
    SspiFreeAsyncContext(AsyncContext);
}

void DoASCCall(
    _In_opt_  PCredHandle    phCred,
    _In_opt_  PCtxtHandle    phContext,
    _In_opt_  PSecBufferDesc pInput,
    _In_opt_  PSecBufferDesc pOutput,
    _Out_     unsigned long* pfContextAttr,
    _Out_opt_ PTimeStamp     ptsExpiry
)
{
    // Create context for async call
    SspiAsyncContext* AsyncContext = SspiCreateAsyncContext();

    // Check for out of memory condition
    ASSERT(AsyncContext);

    // Register callback that continues execution upon completion.
    PVOID pCallbackData = … ; // *Setup any state needed for callback.*
    SECURITY_STATUS Status = SspiSetAsyncNotifyCallback(AsyncContext,
                                        AsyncCallCompleted,
                                        pCallbackData);
    ASSERT(SEC_E_OK == Status);

    // Queue asynchronous call.
    Status = SspiAcceptSecurityContextAsync(AsyncContext,
                                            phCred,
                                            phContext,
                                            pInput,
                                            ASC_REQ_CONNECTION,
                                            SECURITY_NATIVE_DREP,
                                            phContext,
                                            pOutput,
                                            pfContextAttr,
                                            ptsExpiry);

    // All async functions return the status of queueing the async call,
    // not the call’s result.
    ASSERT(SEC_E_OK == Status);

    // At this point, the call can be pending or complete.
    // If complete, the result or error is returned.
    // For this example, we assume if it finished, it finished with SEC_E_OK.
    Status = SspiGetAsyncCallStatus(AsyncContext);
    ASSERT(SEC_I_ASYNC_CALL_PENDING == Status ||
           SEC_E_OK == Status);

    // Execution will continue in the callback upon completion
}

```

## <a name="see-also"></a>Consulte también

[encabezado SSPI. h](/windows/win32/api/sspi/)

[Funciones SSPI](/windows/win32/api/sspi/#functions)

[Estructuras SSPI](/windows/win32/api/sspi/#structures)


