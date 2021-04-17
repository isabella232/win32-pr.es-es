---
title: Modelo asincrónico
description: La mayoría de las operaciones en la API de servicios Web de Windows se pueden realizar de forma sincrónica o asincrónica.
ms.assetid: d0b3f154-2219-4085-a652-e9aeb126598c
keywords:
- Servicios Web de modelo asincrónicos para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c5e38dfbc0bc2ed397949da86f9a572a5b1ed5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704677"
---
# <a name="asynchronous-model"></a>Modelo asincrónico

La mayoría de las operaciones en la API de servicios Web de Windows se pueden realizar de forma sincrónica o asincrónica. Para llamar a una función sincrónicamente, pase un valor null para la estructura de [**\_ \_ contexto WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) . Para especificar que una función se puede realizar de forma asincrónica, pase un **contexto WS \_ Async \_** que no sea NULL a la función.

Cuando se llama de forma asincrónica, una función puede completarse de forma sincrónica o asincrónica. Si la función se completa sincrónicamente, devuelve un valor que indica el éxito o el error final, y este valor siempre es algo distinto de **WS \_ S \_ Async** (vea [valores devueltos de servicios Web de Windows](windows-web-services-return-values.md)). Sin embargo, un valor devuelto de **WS \_ S \_ Async** indica que la función se completará de forma asincrónica. Cuando la función se completa de forma asincrónica, se invoca una devolución de llamada para indicar la finalización de la operación. Esta devolución de llamada indica el valor final correcto o error. No se llama a la devolución de llamada si la operación se completa de forma sincrónica.

Para crear un contexto asincrónico, inicialice los campos de **devolución de llamada** y **callbackState** de la estructura de [**contexto de WS \_ Async \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) . El campo **callbackState** se usa para especificar un puntero a datos definidos por el usuario que se pasa a la función de [**devolución de \_ \_ llamada de WS Async**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) .

En el ejemplo siguiente se muestra cómo llamar a una función de forma asincrónica pasando un puntero a una estructura de [**\_ \_ contexto WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) que contiene la devolución de llamada y un puntero a los datos de estado.

``` syntax
HRESULT ExampleAsyncFunction(WS_ASYNC_CONTEXT* asyncContext);
void ExampleAsyncFunction()
{
    // Set up the WS_ASYNC_CONTEXT structure.
    MyState* myState = ...;  \\ Declare a pointer to user-defined data.
    WS_ASYNC_CONTEXT asyncContext;
    asyncContext.callback = MyCallback;  \\ Set the callback.
    asyncContext.callbackState = myState; \\ Set the pointer to the user-defined data.

    // Start the asynchronous operation
    HRESULT hr = SomeFunction(&asyncContext);

    if (hr == WS_S_ASYNC)
    {
        // The operation is completing asynchronously.  The callback is called 
        // when the operation is complete.
    }
    else
    {
        // The operation completed synchronously.  The callback is not called.
    }
}
void CALLBACK MyCallback(HRESULT hr, WS_CALLBACK_MODEL callbackModel, void* callbackState)
{
    MyState* myState = (MyState*)callbackState;

    // The operation completed asynchronously.
}
```

La función asincrónica utiliza la estructura de [**\_ \_ contexto de WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) solo mientras dure la llamada de función (no mientras dure la operación asincrónica), por lo que puede declararla de forma segura en la pila.

Si cualquier otro parámetro, además de la estructura de [**\_ \_ contexto de WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) , se pasa a una función asincrónica como punteros y la función se completa de forma asincrónica, es responsabilidad del llamador mantener activos los valores a los que apuntan estos parámetros (no liberado) hasta que se invoque la devolución de llamada asincrónica.

Existen limitaciones en cuanto a las operaciones que puede realizar una devolución de llamada. Para obtener más información sobre las operaciones posibles, vea el [**\_ \_ modelo de devolución de llamada WS**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model).

Cuando implemente una función asincrónica, no invoque la devolución de llamada en el mismo subproceso que llamó a la función asincrónica antes de que la función asincrónica haya devuelto al autor de la llamada, ya que esto interrumpe el modelo asincrónico.

Al implementar una función que necesita ejecutar una serie de operaciones asincrónicas, considere la posibilidad de usar la función auxiliar [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) .

En el ejemplo de la [función asincrónica](asyncmodelexample.md) se muestra cómo implementar y consumir funciones que siguen el modelo asincrónico.

Al iniciar una operación de e/s asincrónica, se consumen recursos del sistema. Si se inician suficientes operaciones de e/s, el sistema puede dejar de responder. Para evitar esto, una aplicación debe limitar el número de operaciones asincrónicas que se inician.

El modelo asincrónico usa los siguientes elementos de la API.

| Devolución de llamada                                         | Descripción                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**devolución de llamada de WS \_ Async \_**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) | Parámetro de la función de devolución de llamada que se usa con el modelo asincrónico.                                                                     |
| [**función de WS \_ Async \_**](/windows/desktop/api/WebServices/nc-webservices-ws_async_function) | Se usa con [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) para especificar la función siguiente que se va a invocar en una serie de operaciones asincrónicas. |



 



| Enumeración                                      | Descripción                                                                                                       |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**\_modelo de devolución de llamada WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model) | Especifica el comportamiento de subprocesos de una devolución de llamada (por ejemplo, una [**\_ devolución de \_ llamada de WS Async**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)). |



 



| Función                                 | Descripción                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) | Invoca una devolución de llamada definida por el usuario que puede iniciar una operación asincrónica e indicar una función a la que se debe llamar cuando se haya completado la operación asincrónica. |



 



| Estructura                                          | Descripción                                                                                                                           |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**contexto de WS \_ Async \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)     | Especifica la devolución de llamada asincrónica y un puntero a los datos definidos por el usuario, que se pasarán a la devolución de llamada asincrónica.            |
| [**operación de WS \_ Async \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_operation) | Se usa con [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) para especificar la función siguiente que se va a invocar en una serie de operaciones asincrónicas. |
| [**Estado de WS \_ Async \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_state)         | Usado por [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) para administrar el estado de una operación asincrónica.                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplo de función asincrónica](asyncmodelexample.md)
</dt> <dt>

[**devolución de llamada de WS \_ Async \_**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
</dt> <dt>

[**contexto de WS \_ Async \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)
</dt> <dt>

[**\_modelo de devolución de llamada WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model)
</dt> <dt>

[**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute)
</dt> </dl>

 

 




