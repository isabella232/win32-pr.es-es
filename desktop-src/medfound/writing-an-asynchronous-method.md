---
description: En este tema se describe cómo implementar un método asincrónico en Microsoft Media Foundation.
ms.assetid: cd94280d-7267-4d35-8333-aa4a5bd81b73
title: Escribir un método asincrónico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d8360d0c15fe25661b8cd0f0f5adc9768db8ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361246"
---
# <a name="writing-an-asynchronous-method"></a>Escribir un método asincrónico

En este tema se describe cómo implementar un método asincrónico en Microsoft Media Foundation.

Los métodos asincrónicos están omnipresentes en la canalización de Media Foundation. Los métodos asincrónicos facilitan la distribución del trabajo entre varios subprocesos. Es especialmente importante realizar la e/s asincrónicamente, de modo que la lectura de un archivo o red no bloquee el resto de la canalización.

Si está escribiendo un origen multimedia o un receptor multimedia, es fundamental controlar las operaciones asincrónicas correctamente, ya que el rendimiento del componente afecta a toda la canalización.

> [!Note]  
> De forma predeterminada, las transformaciones de Media Foundation (MFTs) usan métodos sincrónicos.

 

### <a name="work-queues-for-asynchronous-operations"></a>Colas de trabajo para operaciones asincrónicas

En Media Foundation, hay una relación de cierre entre [los métodos de devolución de llamada asincrónicos](asynchronous-callback-methods.md) y las [colas de trabajos](work-queues.md). Una cola de trabajo es una abstracción para mover el trabajo del subproceso del llamador a un subproceso de trabajo. Para realizar el trabajo en una cola de trabajo, haga lo siguiente:

1.  Implemente la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .
2.  Llame a [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) para crear un objeto de *resultado* . El objeto de resultado expone [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult). El objeto de resultado contiene tres punteros:

    -   Puntero a la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) del llamador.
    -   Un puntero opcional a un objeto de estado. Si se especifica, el objeto de Estado debe implementar **IUnknown**.
    -   Un puntero opcional a un objeto privado. Si se especifica, este objeto también debe implementar **IUnknown**.

    Los dos últimos punteros pueden ser **null**. En caso contrario, úselos para almacenar información sobre la operación asincrónica.

3.  Llame a [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) para poner en cola el elemento de trabajo.
4.  El subproceso de cola de trabajo llama al método [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) .
5.  Realice el trabajo en el método de [**invocación**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) . El parámetro *pAsyncResult* de este método es el puntero [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) del paso 2. Use este puntero para obtener el objeto de estado y el objeto privado:
    -   Para obtener el objeto de estado, llame a [**IMFAsyncResult:: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).
    -   Para obtener el objeto privado, llame a [**IMFAsyncResult:: GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject).

Como alternativa, puede combinar los pasos 2 y 3 llamando a la función [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) . Internamente, esta función llama a [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) para crear el objeto de resultado.

En el diagrama siguiente se muestran las relaciones entre el autor de la llamada, el objeto de resultado, el objeto de estado y el objeto privado.

![diagrama que muestra un objeto de resultado asincrónico](images/workqueues01.png)

En el diagrama de secuencia siguiente se muestra cómo un objeto pone en cola un elemento de trabajo. Cuando el subproceso de cola de trabajo llama a [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), el objeto realiza la operación asincrónica en ese subproceso.

![diagrama que muestra cómo un objeto pone en cola un elemento de trabajo](images/workqueues02.png)

Es importante recordar que se llama a [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) desde un subproceso que pertenece a la cola de trabajo. La implementación de **Invoke** debe ser segura para subprocesos. Además, si usa la cola de trabajo de plataforma (**\_ estándar de \_ cola \_ de devolución de llamada de MFASYNC**), es fundamental que nunca bloquee el subproceso, ya que esto puede impedir que la canalización de Media Foundation completa procese los datos. Si necesita realizar una operación que se bloqueará o tardará mucho tiempo en completarse, utilice una cola de trabajo privada. Para crear una cola de trabajo privada, llame a [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue). Cualquier componente de canalización que realice operaciones de e/s debe evitar el bloqueo de las llamadas de e/s por el mismo motivo. La interfaz [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) proporciona una abstracción útil para la e/s asincrónica de archivos.

### <a name="implementing-the-beginend-pattern"></a>Implementar el ../end... Begin. Ajedrez

Como se describe en [llamar a métodos asincrónicos](calling-asynchronous-methods.md), los métodos asincrónicos de Media Foundation suelen usar la instrucción **Begin...** / **Finalizar.** ... ajedrez. En este patrón, una operación asincrónica utiliza dos métodos con firmas similares a las siguientes:

``` syntax
// Starts the asynchronous operation.
HRESULT BeginX(IMFAsyncCallback *pCallback, IUnknown *punkState);

// Completes the asynchronous operation. 
// Call this method from inside the caller's Invoke method.
HRESULT EndX(IMFAsyncResult *pResult);
```

Para que el método sea realmente asincrónico, la implementación de **BeginX** debe realizar el trabajo real en otro subproceso. Aquí es donde entran en la imagen las colas de trabajos. En los pasos siguientes, el autor de la *llamada* es el código que llama a **BeginX** y **EndX**. Puede tratarse de una aplicación o de la canalización Media Foundation. El *componente* es el código que implementa **BeginX** y **EndX**.

1.  El llamador llama a **Begin...**, pasando un puntero a la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) del llamador.
2.  El componente crea un nuevo objeto de resultado asincrónico. Este objeto almacena la interfaz de devolución de llamada y el objeto de estado del llamador. Normalmente, también almacena información de estado privado que el componente necesita para completar la operación. El objeto de resultado de este paso tiene la etiqueta "resultado 1" en el diagrama siguiente.
3.  El componente crea un segundo objeto de resultado. Este objeto de resultado almacena dos punteros: el primer objeto de resultado y la interfaz de devolución de llamada del destinatario. Este objeto de resultado tiene la etiqueta "resultado 2" en el diagrama siguiente.
4.  El componente llama a [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) para poner en cola un nuevo elemento de trabajo.
5.  En el método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) , el componente realiza el trabajo asincrónico.
6.  El componente llama a [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) para invocar el método de devolución de llamada del llamador.
7.  El llamador llama al método **EndX** .

![diagrama que muestra cómo un objeto implementa el patrón Begin/end](images/workqueues03.png)

## <a name="asynchronous-method-example"></a>Ejemplo de método asincrónico

Para ilustrar este debate, usaremos un ejemplo de inventado. Considere un método asincrónico para calcular una raíz cuadrada:


```C++
    HRESULT BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState);
    HRESULT EndSquareRoot(IMFAsyncResult *pResult, double *pVal);
```



El parámetro *x* de `BeginSquareRoot` es el valor cuya raíz cuadrada se va a calcular. La raíz cuadrada se devuelve en el parámetro *pval* de `EndSquareRoot` .

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



La `SqrRoot` clase implementa [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) para que pueda colocar la operación de raíz cuadrada en una cola de trabajo. El `DoCalculateSquareRoot` método es el método de clase privada que calcula la raíz cuadrada. Se llamará a este método desde el subproceso de cola de trabajo.

En primer lugar, necesitamos una manera de almacenar el valor de *x*, de modo que se pueda recuperar cuando el subproceso de cola de trabajo llame a `SqrRoot::Invoke` . A continuación se muestra una clase simple que almacena la información:


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

El código siguiente implementa el `BeginSquareRoot` método:


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
2.  Llama a [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) para crear un objeto de resultado. Este objeto contiene varios punteros:
    -   Puntero a la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) del llamador.
    -   Puntero al objeto de estado del llamador (*pState*).
    -   Un puntero al objeto `AsyncOp`.
3.  Llama a [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) para poner en cola un nuevo elemento de trabajo. Esta llamada crea implícitamente un objeto de resultado externo, que contiene los siguientes punteros:
    -   Puntero a la `SqrRoot` interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) del objeto.
    -   Un puntero al objeto de resultado interno del paso 2.

El código siguiente implementa el `SqrRoot::Invoke` método:


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



Este método obtiene el objeto de resultado interno y el `AsyncOp` objeto. A continuación, pasa el `AsyncOp` objeto a `DoCalculateSquareRoot` . Finalmente, llama a [**IMFAsyncResult:: SetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-setstatus) para establecer el código de estado y [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) para invocar el método de devolución de llamada del llamador.

El `DoCalculateSquareRoot` método hace exactamente lo que cabría esperar:


```C++
HRESULT SqrRoot::DoCalculateSquareRoot(AsyncOp *pOp)
{
    pOp->m_value = sqrt(pOp->m_value);

    return S_OK;
}
```



Cuando se invoca el método de devolución de llamada del llamador, es responsabilidad del llamador llamar al método **End...** (en este caso,) `EndSquareRoot` . `EndSquareRoot`Es cómo el autor de la llamada recupera el resultado de la operación asincrónica, que en este ejemplo es la raíz cuadrada calculada. Esta información se almacena en el objeto de resultado:


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

Hasta ahora, se ha asumido tácitamente que una operación asincrónica podría realizarse en cualquier momento, independientemente del estado actual del objeto. Por ejemplo, tenga en cuenta lo que sucede si una aplicación llama a `BeginSquareRoot` mientras una llamada anterior al mismo método todavía está pendiente. La `SqrRoot` clase puede poner en cola el nuevo elemento de trabajo antes de que se realice el elemento de trabajo anterior. Sin embargo, no se garantiza que las colas de trabajo serialicen los elementos de trabajo. Recuerde que una cola de trabajo puede utilizar más de un subproceso para enviar elementos de trabajo. En un entorno multiproceso, se podría invocar un elemento de trabajo antes de que se completase el anterior. Los elementos de trabajo incluso se pueden invocar sin orden, si se produce un cambio de contexto justo antes de que se invoque la devolución de llamada.

Por esta razón, es responsabilidad del objeto serializar las operaciones en sí misma, si es necesario. En otras palabras, si el objeto requiere la operación a para finalizar antes de que se pueda iniciar la operación *B* , el objeto no debe *poner en cola* un elemento de trabajo para *B* hasta que se haya completado la operación *A* . Un objeto puede cumplir este requisito si tiene su propia cola de operaciones pendientes. Cuando se llama a un método asincrónico en el objeto, el objeto coloca la solicitud en su propia cola. A medida que se completa cada operación asincrónica, el objeto extrae la siguiente solicitud de la cola. En el [ejemplo MPEG1Source](mpeg1source-sample.md) se muestra un ejemplo de cómo implementar este tipo de cola.

Un único método puede implicar varias operaciones asincrónicas, especialmente cuando se usan llamadas de e/s. Cuando implemente métodos asincrónicos, piense detenidamente los requisitos de serialización. Por ejemplo, ¿es válido para el objeto iniciar una nueva operación mientras una solicitud de e/s anterior todavía está pendiente? Si la nueva operación cambia el estado interno del objeto, ¿qué ocurre cuando se completa una solicitud de e/s anterior y devuelve datos que ahora pueden estar obsoletos? Un buen diagrama de estado puede ayudar a identificar las transiciones de estado válidas.

## <a name="cross-thread-and-cross-process-considerations"></a>Consideraciones entre subprocesos y entre procesos

Las colas de trabajo no utilizan el cálculo de referencias COM para calcular las referencias de punteros de interfaz a través de los límites de subprocesos. Por lo tanto, aunque un objeto se registre como subproceso controlado por apartamento o el subproceso de aplicación haya entrado en un contenedor uniproceso (STA), las devoluciones de llamada de [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) se invocarán desde un subproceso diferente. En cualquier caso, todos los componentes de canalización de Media Foundation deben usar el modelo de subprocesos "ambos".

Algunas interfaces de Media Foundation definen versiones remotas de algunos métodos asincrónicos. Cuando se llama a uno de estos métodos a través de los límites del proceso, la Media Foundation DLL de proxy/código auxiliar llama a la versión remota del método, que realiza el cálculo de referencias personalizado de los parámetros del método. En el proceso remoto, el código auxiliar vuelve a trasladar la llamada al método local en el objeto. Este proceso es transparente para la aplicación y el objeto remoto. Estos métodos de serialización personalizados se proporcionan principalmente para los objetos que se cargan en la ruta de acceso a medios protegidos (PMP). Para obtener más información sobre el PMP, vea [ruta de acceso a medios protegidos](protected-media-path.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Métodos de devolución de llamada asincrónica](asynchronous-callback-methods.md)
</dt> <dt>

[Colas de trabajo](work-queues.md)
</dt> </dl>

 

 



