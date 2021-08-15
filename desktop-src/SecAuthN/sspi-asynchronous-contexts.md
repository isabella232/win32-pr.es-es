---
title: Contextos asincrónicos
description: Información general de los contextos asincrónicos y el encabezado SSPI asincrónico.
ms.topic: article
ms.keywords: SSPI, Asynchronous Contexts, async contexts, Async SSPI, SSPI Async, Asynchronous SSPI, sspi,SspiAcceptSecurityContextAsync, SspiAcquireCredentialsHandleAsync, SspiAsyncContextRequiresNotify, SspiAsyncNotifyCallback, SspiCreateAsyncContext,SspiDeleteSecurityContextAsync, SspiFreeAsyncContext, SspiFreeCredentialsHandleAsync, SspiGetAsyncCallStatus, SspiInitializeSecurityContextAsync, SspiReinitAsyncContext, SspiSetAsyncNotifyCallback
ms.date: 06/23/2020
ms.openlocfilehash: e83dbab8c20dd9f9cfe13ec579db304aabd491cba92ab0cd6a9c8afcf4e4af8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917234"
---
# <a name="asynchronous-contexts"></a>Contextos asincrónicos

Los contextos de seguridad SSPI asincrónicos permiten a los llamadores continuar sin bloquear y recibir notificaciones una vez completada la llamada. Actualmente, los contextos asincrónicos solo se admiten para clientes y servidores TLS en modo kernel. Las siguientes funciones asincrónicas de SSPI funcionan en contextos de seguridad asincrónicos:

## <a name="async-context-management-types"></a>Tipos de administración de contexto asincrónico

| Nombre de objeto | Descripción |
|-------------|--------------|
| [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nc-sspi-sspiasyncnotifycallback) | Devolución de llamada usada para notificar la finalización de una llamada SSPI asincrónica. |


## <a name="async-context-management-functions"></a>Funciones de administración asincrónica de contexto

| Nombre de la API | Descripción |
|-------------|--------------|
| [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext) | Crea una instancia de SspiAsyncContext que se usa para realizar un seguimiento de la llamada asincrónica. |
| [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext) | Marca un contexto asincrónico para su reutilización. |
| [SspiSetAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) | Registra una devolución de llamada que se notifica al finalizar la llamada asincrónica. |
| [SspiAsyncContextRequiresNotify](/windows/win32/api/sspi/nf-sspi-sspiasynccontextrequiresnotify) | Determina si un contexto asincrónico determinado requiere notificación al finalizar la llamada. |
| [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus) | Obtiene el estado actual de una llamada asincrónica asociada al contexto proporcionado.  |
| [SspiFreeAsyncContext](/windows/win32/api/sspi/nf-sspi-sspifreeasynccontext) | Libera un contexto creado en la llamada a la función SspiCreateAsyncContext. |

## <a name="async-sspi-functions"></a>Funciones de SSPI asincrónicas

Las funciones siguientes aceptan un contexto asincrónico además de todos los mismos parámetros que su homólogo sincrónico.

| Nombre de la API | Descripción |
|-------------|--------------|
| [SspiAcquireCredentialsHandleAsync](/windows/win32/api/sspi/nf-sspi-sspiacquirecredentialshandleasynca) | Adquiere de forma asincrónica un identificador para las credenciales preexistentes de una entidad de seguridad. |
| [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync) | Permite que el componente de servidor de una aplicación de transporte establezca de forma asincrónica un contexto de seguridad entre el servidor y un cliente remoto. |
| [SspiInitializeSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiinitializesecuritycontextasynca) | Inicializa un contexto de seguridad asincrónico. |
| [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync) | Elimina las estructuras de datos locales asociadas al contexto de seguridad especificado iniciado por una llamada anterior a la función SspiInitializeSecurityContextAsync o a la función SspiAcceptSecurityContextAsync. |
| [SspiFreeCredentialsHandleAsync](/windows/win32/api/sspi/nf-sspi-sspifreecredentialshandleasync) | Libera un identificador de credenciales. |

## <a name="api-sample"></a>Ejemplo de API

Un flujo de llamadas típico funciona de la siguiente manera:
1) Creación de contexto de SspiAsyncContext para realizar un seguimiento de la llamada [mediante SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)
2) Registro de [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) para el contexto
3) Realización de la llamada asincrónica mediante [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)
4) En la devolución de llamada, recupere el resultado [mediante SspiGetAsyncCallStatus.](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)
5) Elimine SspiAsyncContext mediante [SspiDeleteSecurityContextAsync.](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync) Si vuelve a usar el contexto [con SspiReinitAsyncContext,](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext)vuelva al paso 2.

En el ejemplo siguiente se muestra una invocación de SspiAcceptSecurityContextAsync. El ejemplo espera a que se complete la llamada y recupera el resultado.

En un protocolo de enlace SSPI completo, se llamaría a SspiAcceptSecurityContextAsync y SspiInitializeSecurityContextAsync varias veces hasta que SEC_E_OK se devuelva. SspiReinitAsyncContext se ha proporcionado para facilitar su uso y facilitar el rendimiento en este caso.

Las aserciones se usan para resaltar lo que se esperaría en caso de éxito.

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

[Encabezado sspi.h](/windows/win32/api/sspi/)

[Funciones de SSPI](/windows/win32/api/sspi/#functions)

[Estructuras SSPI](/windows/win32/api/sspi/#structures)


