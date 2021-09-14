---
description: En este tema se describe cómo implementar un método asincrónico en Microsoft Media Foundation.
ms.assetid: cd94280d-7267-4d35-8333-aa4a5bd81b73
title: Escribir un método asincrónico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d8360d0c15fe25661b8cd0f0f5adc9768db8ab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361108"
---
# <a name="writing-an-asynchronous-method"></a>Escribir un método asincrónico

En este tema se describe cómo implementar un método asincrónico en Microsoft Media Foundation.

Los métodos asincrónicos son ubicuos en la Media Foundation ejecución. Los métodos asincrónicos facilitan la distribución del trabajo entre varios subprocesos. Es especialmente importante realizar la E/S de forma asincrónica, para que la lectura desde un archivo o red no bloquee el resto de la canalización.

Si está escribiendo un origen multimedia o un receptor multimedia, es fundamental controlar correctamente las operaciones asincrónicas, ya que el rendimiento del componente tiene un impacto en toda la canalización.

> [!Note]  
> Media Foundation transformaciones (MFT) usan métodos sincrónicos de forma predeterminada.

 

### <a name="work-queues-for-asynchronous-operations"></a>Colas de trabajo para operaciones asincrónicas

En Media Foundation, hay una relación estrecha entre los métodos de devolución de llamada [asincrónicos](asynchronous-callback-methods.md) y [las colas de trabajo](work-queues.md). Una cola de trabajo es una abstracción para mover el trabajo del subproceso del autor de la llamada a un subproceso de trabajo. Para realizar el trabajo en una cola de trabajo, haga lo siguiente:

1.  Implemente [**la interfaz IMFAsyncCallback.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
2.  Llame [**a MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) para crear un *objeto de* resultado. El objeto de resultado expone [**EL VALOR DEASYNCASYNCRESULT.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) El objeto de resultado contiene tres punteros:

    -   Puntero a la interfaz [**DEVOLUCIÓNAsyncCallback del**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) autor de la llamada.
    -   Puntero opcional a un objeto de estado. Si se especifica, el objeto de estado debe implementar **IUnknown**.
    -   Puntero opcional a un objeto privado. Si se especifica, este objeto también debe implementar **IUnknown**.

    Los dos últimos punteros pueden ser **NULL.** De lo contrario, úsenlos para contener información sobre la operación asincrónica.

3.  Llame [**a MFPutWorkItemEx para**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) poner en cola el elemento de trabajo.
4.  El subproceso de cola de trabajo llama al [**método IMFAsyncCallback::Invoke.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)
5.  Realice el trabajo dentro del [**método Invoke.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) El *parámetro pAsyncResult* de este método es el puntero [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) del paso 2. Use este puntero para obtener el objeto de estado y el objeto privado:
    -   Para obtener el objeto de estado, llame [**a IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).
    -   Para obtener el objeto privado, llame [**a IMFAsyncResult::GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject).

Como alternativa, puede combinar los pasos 2 y 3 llamando a la [**función MFPutWorkItem.**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) Internamente, esta función llama [**a MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) para crear el objeto de resultado.

En el diagrama siguiente se muestran las relaciones entre el autor de la llamada, el objeto de resultado, el objeto de estado y el objeto privado.

![diagrama que muestra un objeto de resultado asincrónico](images/workqueues01.png)

En el siguiente diagrama de secuencia se muestra cómo un objeto pone en cola un elemento de trabajo. Cuando el subproceso de cola de trabajo [**llama a Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), el objeto realiza la operación asincrónica en ese subproceso.

![diagrama que muestra cómo un objeto pone en cola un elemento de trabajo](images/workqueues02.png)

Es importante recordar que [**se llama**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) a Invoke desde un subproceso que es propiedad de la cola de trabajo. La implementación de **Invoke debe** ser segura para subprocesos. Además, si usa la cola de trabajo de plataforma **(MFASYNC \_ CALLBACK \_ QUEUE \_ STANDARD),** es fundamental que nunca bloquee el subproceso, ya que esto puede impedir que toda la canalización de Media Foundation procese datos. Si necesita realizar una operación que bloquee o dedime mucho tiempo a completarse, use una cola de trabajo privada. Para crear una cola de trabajo privada, llame [**a MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue). Cualquier componente de canalización que realice operaciones de E/S debe evitar el bloqueo de llamadas de E/S por el mismo motivo. La [**interfaz IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) proporciona una abstracción útil para la E/S asincrónica de archivos.

### <a name="implementing-the-beginend-pattern"></a>Implementing the Begin.../End... Patrón

Como se describe en [Llamar a métodos asincrónicos,](calling-asynchronous-methods.md)los métodos asincrónicos Media Foundation a menudo usan **begin...** / **Final...** Patrón. En este patrón, una operación asincrónica usa dos métodos con firmas similares a las siguientes:

``` syntax
// Starts the asynchronous operation.
HRESULT BeginX(IMFAsyncCallback *pCallback, IUnknown *punkState);

// Completes the asynchronous operation. 
// Call this method from inside the caller's Invoke method.
HRESULT EndX(IMFAsyncResult *pResult);
```

Para que el método sea realmente asincrónico, la implementación de **BeginX** debe realizar el trabajo real en otro subproceso. Aquí es donde las colas de trabajo se incluyen en la imagen. En los pasos siguientes, el *autor de la llamada* es el código que llama a **BeginX** y **EndX.** Puede ser una aplicación o la Media Foundation canalización. El *componente* es el código que implementa **BeginX** y **EndX.**

1.  El autor de la llamada llama a **Begin...**, pasando un puntero a la interfaz [**DE DEVOLUCIÓNASYNCCALLBACK del**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) autor de la llamada.
2.  El componente crea un nuevo objeto de resultado asincrónico. Este objeto almacena la interfaz de devolución de llamada y el objeto de estado del autor de la llamada. Normalmente, también almacena cualquier información de estado privado que el componente necesita para completar la operación. El objeto de resultado de este paso se etiqueta como "Resultado 1" en el diagrama siguiente.
3.  El componente crea un segundo objeto de resultado. Este objeto de resultado almacena dos punteros: el primer objeto de resultado y la interfaz de devolución de llamada del destinatario. Este objeto de resultado se etiqueta como "Resultado 2" en el diagrama siguiente.
4.  El componente llama [**a MFPutWorkItemEx para**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) poner en cola un nuevo elemento de trabajo.
5.  En el [**método Invoke,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) el componente realiza el trabajo asincrónico.
6.  El componente llama a [**MFInvokeCallback para**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) invocar el método de devolución de llamada del autor de la llamada.
7.  El autor de la llamada llama **al método EndX.**

![diagrama que muestra cómo un objeto implementa el patrón de inicio y fin](images/workqueues03.png)

## <a name="asynchronous-method-example"></a>Ejemplo de método asincrónico

Para ilustrar esta explicación, usaremos un ejemplo derivado de . Considere un método asincrónico para calcular una raíz cuadrada:


```C++
    HRESULT BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState);
    HRESULT EndSquareRoot(IMFAsyncResult *pResult, double *pVal);
```



El *parámetro x* de es el valor cuya raíz cuadrada se `BeginSquareRoot` calculará. La raíz cuadrada se devuelve en el *parámetro pVal* de `EndSquareRoot` .

Esta es la declaración de una clase que implementa estos dos métodos:


```C++
class SqrRoot : public IMFAsyncCallback
{
    LONG    m_cRef;
    double  m_sqrt;

    HRESULT DoCalculateSquareRoot(AsyncOp *pOp);

public:

    SqrRoot() : m_cRef(1)
    {

    }

    HRESULT BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState);
    HRESULT EndSquareRoot(IMFAsyncResult *pResult, double *pVal);

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(SqrRoot, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    // IMFAsyncCallback methods.

    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;  
    }
    // Invoke is where the work is performed.
    STDMETHODIMP Invoke(IMFAsyncResult* pResult);
};
```



La `SqrRoot` clase implementa [**IMFAsyncCallback para**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) que pueda colocar la operación raíz cuadrada en una cola de trabajo. El `DoCalculateSquareRoot` método es el método de clase privada que calcula la raíz cuadrada. Se llamará a este método desde el subproceso de cola de trabajo.

En primer lugar, necesitamos una manera de almacenar el valor *de x* para que se pueda recuperar cuando el subproceso de cola de trabajo llame a `SqrRoot::Invoke` . Esta es una clase sencilla que almacena la información:


```C++
class AsyncOp : public IUnknown
{
    LONG    m_cRef;

public:

    double  m_value;

    AsyncOp(double val) : m_cRef(1), m_value(val) { }

    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(AsyncOp, IUnknown),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }
};
```



Esta clase implementa **IUnknown** para que se pueda almacenar en un objeto de resultado.

El código siguiente implementa el `BeginSquareRoot` método :


```C++
HRESULT SqrRoot::BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState)
{
    AsyncOp *pOp = new (std::nothrow) AsyncOp(x);
    if (pOp == NULL)
    {
        return E_OUTOFMEMORY;
    }

    IMFAsyncResult *pResult = NULL;

    // Create the inner result object. This object contains pointers to:
    // 
    //   1. The caller's callback interface and state object. 
    //   2. The AsyncOp object, which contains the operation data.
    //

    HRESULT hr = MFCreateAsyncResult(pOp, pCB, pState, &pResult);

    if (SUCCEEDED(hr))
    {
        // Queue a work item. The work item contains pointers to:
        // 
        // 1. The callback interface of the SqrRoot object.
        // 2. The inner result object.

        hr = MFPutWorkItem(MFASYNC_CALLBACK_QUEUE_STANDARD, this, pResult);

        pResult->Release();
    }

    return hr;
}
```



Este código hace lo siguiente:

1.  Crea una nueva instancia de la `AsyncOp` clase para contener el valor de *x*.
2.  Llama [**a MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) para crear un objeto de resultado. Este objeto contiene varios punteros:
    -   Puntero a la interfaz [**DEVOLUCIÓNAsyncCallback del**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) autor de la llamada.
    -   Puntero al objeto de estado del autor de la llamada (*pState*).
    -   Un puntero al objeto `AsyncOp`.
3.  Llama [**a MFPutWorkItem para**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) poner en cola un nuevo elemento de trabajo. Esta llamada crea implícitamente un objeto de resultado externo, que contiene los punteros siguientes:
    -   Puntero a la `SqrRoot` interfaz [**IMFAsyncCallback del**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) objeto.
    -   Puntero al objeto de resultado interno del paso 2.

El código siguiente implementa el `SqrRoot::Invoke` método :


```C++
// Invoke is called by the work queue. This is where the object performs the
// asynchronous operation.

STDMETHODIMP SqrRoot::Invoke(IMFAsyncResult* pResult)
{
    HRESULT hr = S_OK;

    IUnknown *pState = NULL;
    IUnknown *pUnk = NULL;
    IMFAsyncResult *pCallerResult = NULL;

    AsyncOp *pOp = NULL; 

    // Get the asynchronous result object for the application callback. 

    hr = pResult->GetState(&pState);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pState->QueryInterface(IID_PPV_ARGS(&pCallerResult));
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the object that holds the state information for the asynchronous method.
    hr = pCallerResult->GetObject(&pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    pOp = static_cast<AsyncOp*>(pUnk);

    // Do the work.

    hr = DoCalculateSquareRoot(pOp);

done:
    // Signal the application.
    if (pCallerResult)
    {
        pCallerResult->SetStatus(hr);
        MFInvokeCallback(pCallerResult);
    }

    SafeRelease(&pState);
    SafeRelease(&pUnk);
    SafeRelease(&pCallerResult);
    return S_OK;
}
```



Este método obtiene el objeto de resultado interno y el `AsyncOp` objeto . A continuación, pasa el `AsyncOp` objeto a `DoCalculateSquareRoot` . Por último, llama a [**MFAsyncResult::SetStatus para**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-setstatus) establecer el código de estado y [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) para invocar el método de devolución de llamada del autor de la llamada.

El `DoCalculateSquareRoot` método hace exactamente lo que se esperaría:


```C++
HRESULT SqrRoot::DoCalculateSquareRoot(AsyncOp *pOp)
{
    pOp->m_value = sqrt(pOp->m_value);

    return S_OK;
}
```



Cuando se invoca el método de devolución de llamada del autor de la llamada, es responsabilidad del autor de la llamada llamar al método **End...,** en este caso, `EndSquareRoot` . es la forma en que el autor de la llamada recupera el resultado de la operación asincrónica, que en `EndSquareRoot` este ejemplo es la raíz cuadrada calculada. Esta información se almacena en el objeto de resultado:


```C++
HRESULT SqrRoot::EndSquareRoot(IMFAsyncResult *pResult, double *pVal)
{
    *pVal = 0;

    IUnknown *pUnk = NULL;

    HRESULT hr = pResult->GetStatus();

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pResult->GetObject(&pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    AsyncOp *pOp = static_cast<AsyncOp*>(pUnk);

    // Get the result.
    *pVal = pOp->m_value;

done:
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="operation-queues"></a>Colas de operaciones

Hasta ahora, se ha asumido tácito que se podría realizar una operación asincrónica en cualquier momento, independientemente del estado actual del objeto. Por ejemplo, considere lo que sucede si una aplicación llama `BeginSquareRoot` a mientras una llamada anterior al mismo método sigue pendiente. La `SqrRoot` clase puede poner en cola el nuevo elemento de trabajo antes de que se haga el elemento de trabajo anterior. Sin embargo, no se garantiza que las colas de trabajo serializan elementos de trabajo. Recuerde que una cola de trabajo puede usar más de un subproceso para enviar elementos de trabajo. En un entorno multiproceso, se puede invocar un elemento de trabajo antes de que se haya completado el anterior. Incluso se pueden invocar elementos de trabajo fuera de orden, si se produce un cambio de contexto justo antes de que se invoque la devolución de llamada.

Por este motivo, es responsabilidad del objeto serializar las operaciones en sí mismo, si es necesario. En otras palabras, si el objeto requiere que la operación *A* finalice antes de que se pueda iniciar la operación *B,* el objeto no debe poner en cola un elemento de trabajo para *B* hasta que se haya completado la operación *A.* Un objeto puede cumplir este requisito si tiene su propia cola de operaciones pendientes. Cuando se llama a un método asincrónico en el objeto , el objeto coloca la solicitud en su propia cola. A medida que se completa cada operación asincrónica, el objeto extrae la siguiente solicitud de la cola. El [ejemplo MPEG1Source](mpeg1source-sample.md) muestra un ejemplo de cómo implementar este tipo de cola.

Un único método puede implicar varias operaciones asincrónicas, especialmente cuando se usan llamadas de E/S. Al implementar métodos asincrónicos, piense detenidamente en los requisitos de serialización. Por ejemplo, ¿es válido que el objeto inicie una nueva operación mientras una solicitud de E/S anterior sigue pendiente? Si la nueva operación cambia el estado interno del objeto, ¿qué ocurre cuando se completa una solicitud de E/S anterior y devuelve datos que podrían estar obsoletos? Un buen diagrama de estado puede ayudar a identificar las transiciones de estado válidas.

## <a name="cross-thread-and-cross-process-considerations"></a>Consideraciones entre subprocesos y entre procesos

Las colas de trabajo no usan la serialización COM para serializar punteros de interfaz a través de los límites del subproceso. Por lo tanto, incluso si un objeto está registrado como apartment-threaded o el subproceso de aplicación ha entrado en un apartamento de un solo subproceso (STA), las devoluciones de llamada DE DEVOLUCIÓN DE LLAMADA [**DE LA DEVOLUCIÓN**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) DE LLAMADA SE INVOCARÁN DESDE otro subproceso. En cualquier caso, todos los Media Foundation de canalización deben usar el modelo de subprocesos "Ambos".

Algunas interfaces de Media Foundation definen versiones remotas de algunos métodos asincrónicos. Cuando se llama Media Foundation uno de estos métodos a través de los límites del proceso, el archivo DLL de proxy o código auxiliar de Media Foundation llama a la versión remota del método, que realiza la serialización personalizada de los parámetros del método. En el proceso remoto, el código auxiliar convierte la llamada de nuevo en el método local en el objeto . Este proceso es transparente tanto para la aplicación como para el objeto remoto. Estos métodos de serialización personalizados se proporcionan principalmente para los objetos que se cargan en la ruta de acceso multimedia protegida (PMP). Para obtener más información sobre el PMP, vea [Ruta de acceso de medios protegidos.](protected-media-path.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Métodos de devolución de llamada asincrónicos](asynchronous-callback-methods.md)
</dt> <dt>

[Colas de trabajo](work-queues.md)
</dt> </dl>

 

 



