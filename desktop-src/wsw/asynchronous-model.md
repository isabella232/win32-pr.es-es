---
title: Modelo asincrónico
description: La mayoría de las Windows API de servicios web se pueden realizar de forma sincrónica o asincrónica.
ms.assetid: d0b3f154-2219-4085-a652-e9aeb126598c
keywords:
- Servicios web de modelo asincrónico para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c5e38dfbc0bc2ed397949da86f9a572a5b1ed5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360580"
---
# <a name="asynchronous-model"></a>Modelo asincrónico

La mayoría de las Windows API de servicios web se pueden realizar de forma sincrónica o asincrónica. Para llamar a una función sincrónicamente, pase un valor NULL para la [**estructura CONTEXT de WS \_ ASYNC. \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) Para especificar que una función se puede realizar de forma asincrónica, pase un **WS \_ ASYNC \_ CONTEXT** no NULL a la función.

Cuando se llama de forma asincrónica, una función puede completarse sincrónica o asincrónicamente. Si la función se completa de forma sincrónica, devuelve un valor que indica el éxito o error finales, y este valor siempre es algo distinto de **WS \_ S \_ ASYNC** (vea valores devueltos de servicios web de [Windows](windows-web-services-return-values.md)). Sin embargo, un valor devuelto **de WS \_ S \_ ASYNC** indica que la función se completará de forma asincrónica. Cuando la función se completa de forma asincrónica, se invoca una devolución de llamada para indicar la finalización de la operación. Esta devolución de llamada indica el valor final correcto o error. No se llama a la devolución de llamada si la operación se completa sincrónicamente.

Para crear un contexto asincrónico, inicialice los campos **callback** **y callbackState** de la [**estructura CONTEXT de WS \_ ASYNC. \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) El **campo callbackState** se usa para especificar un puntero a datos definidos por el usuario que se pasan a la función [**WS \_ ASYNC \_ CALLBACK.**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)

En el ejemplo siguiente se muestra cómo llamar a una función de forma asincrónica pasando un puntero a una estructura CONTEXT de [**WS \_ ASYNC \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) que contiene la devolución de llamada y un puntero a los datos de estado.

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

La estructura CONTEXT de [**WS \_ ASYNC \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) solo la usa la función asincrónica durante la llamada de función (no durante la operación asincrónica), por lo que puede declararla de forma segura en la pila.

Si otros parámetros, además de la estructura CONTEXT de [**WS \_ ASYNC, \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) se pasan a una función asincrónica como punteros y la función se completa de forma asincrónica, es responsabilidad del autor de la llamada mantener los valores a los que apuntan estos parámetros (no se liberan) hasta que se invoca la devolución de llamada asincrónica.

Hay limitaciones en las operaciones que puede realizar una devolución de llamada. Para obtener más información sobre las posibles operaciones , vea [**WS \_ CALLBACK \_ MODEL**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model).

Cuando implemente una función asincrónica, no invoque la devolución de llamada en el mismo subproceso que llamó a la función asincrónica antes de que la función asincrónica haya vuelto al llamador, ya que esto interrumpe el modelo asincrónico.

Al implementar una función que necesita ejecutar una serie de operaciones asincrónicas, considere la posibilidad de usar la función [**auxiliar WsAsyncExecute.**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute)

El [ejemplo de función asincrónica](asyncmodelexample.md) muestra cómo implementar y consumir funciones que siguen el modelo asincrónico.

Iniciar una operación asincrónica de E/S consume recursos del sistema. Si se inician suficientes operaciones de E/S, el sistema puede dejar de responder. Para evitarlo, una aplicación debe limitar el número de operaciones asincrónicas que inicia.

El modelo asincrónico usa los siguientes elementos de API.

| Devolución de llamada                                         | Descripción                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**DEVOLUCIÓN DE \_ LLAMADA DE WS \_ ASYNC**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) | Parámetro de función de devolución de llamada utilizado con el modelo asincrónico.                                                                     |
| [**WS \_ ASYNC \_ (FUNCIÓN)**](/windows/desktop/api/WebServices/nc-webservices-ws_async_function) | Se usa con [**WsAsyncExecute para**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) especificar la siguiente función que se invocará en una serie de operaciones asincrónicas. |



 



| Enumeración                                      | Descripción                                                                                                       |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**MODELO DE DEVOLUCIÓN DE LLAMADA DE WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model) | Especifica el comportamiento de subprocesos de una devolución de llamada (por ejemplo, [**WS \_ ASYNC \_ CALLBACK).**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) |



 



| Función                                 | Descripción                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) | Invoca una devolución de llamada definida por el usuario que puede iniciar una operación asincrónica e indicar una función a la que se debe llamar cuando se haya completado la operación asincrónica. |



 



| Estructura                                          | Descripción                                                                                                                           |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**CONTEXTO \_ DE WS \_ ASYNC**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)     | Especifica la devolución de llamada asincrónica y un puntero a los datos definidos por el usuario, que se pasarán a la devolución de llamada asincrónica.            |
| [**WS \_ ASYNC \_ OPERATION**](/windows/desktop/api/WebServices/ns-webservices-ws_async_operation) | Se usa con [**WsAsyncExecute para**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) especificar la siguiente función que se invocará en una serie de operaciones asincrónicas. |
| [**WS \_ ASYNC \_ STATE**](/windows/desktop/api/WebServices/ns-webservices-ws_async_state)         | Lo usa [**WsAsyncExecute para**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) administrar el estado de una operación asincrónica.                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplo de función asincrónica](asyncmodelexample.md)
</dt> <dt>

[**DEVOLUCIÓN DE \_ LLAMADA DE WS \_ ASYNC**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
</dt> <dt>

[**CONTEXTO \_ DE WS \_ ASYNC**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)
</dt> <dt>

[**MODELO DE DEVOLUCIÓN DE LLAMADA DE WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model)
</dt> <dt>

[**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute)
</dt> </dl>

 

 




