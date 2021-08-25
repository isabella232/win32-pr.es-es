---
description: Llamar a métodos asincrónicos
ms.assetid: 1d8688a5-d476-457d-a0ad-e4f106ac3484
title: Llamar a métodos asincrónicos
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a53f5f0a3062ad6af955fbbfdd8cd05c82b30271cf680d6434bc652d567325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959205"
---
# <a name="calling-asynchronous-methods"></a>Llamar a métodos asincrónicos

En Media Foundation, muchas operaciones se realizan de forma asincrónica. Las operaciones asincrónicas pueden mejorar el rendimiento, ya que no bloquean el subproceso que realiza la llamada. Una operación asincrónica en Media Foundation se define mediante un par de métodos con la convención de nomenclatura **Begin...** y **End....** Juntos, estos dos métodos definen una operación de lectura asincrónica en la secuencia.

Para iniciar una operación asincrónica, llame al **método Begin.** El **método Begin** siempre contiene al menos dos parámetros:

-   Puntero a la interfaz [**IMFAsyncCallback.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) La aplicación debe implementar esta interfaz.
-   Puntero a un objeto de estado opcional.

La [**interfaz IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) notifica a la aplicación cuando se completa la operación. Para obtener un ejemplo de cómo implementar esta interfaz, vea [Implementing the Asynchronous Callback](implementing-the-asynchronous-callback.md). El objeto de estado es opcional. Si se especifica, debe implementar la **interfaz IUnknown.** Puede usar el objeto de estado para almacenar cualquier información de estado necesaria para la devolución de llamada. Si no necesita información de estado, puede establecer este parámetro en **NULL.** El **método Begin** puede contener parámetros adicionales que son específicos de ese método.

Si el **método Begin** devuelve un código de error, significa que la operación ha dado error inmediatamente y no se invocará la devolución de llamada. Si el **método Begin** se realiza correctamente, significa que la operación está pendiente y la devolución de llamada se invocará cuando se complete la operación.

Por ejemplo, el [**método IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) inicia una operación de lectura asincrónica en una secuencia de bytes:


```C++
    BYTE data[DATA_SIZE];
    ULONG cbRead = 0;

    CMyCallback *pCB = new (std::nothrow) CMyCallback(pStream, &hr);

    if (pCB == NULL)
    {
        hr = E_OUTOFMEMORY;
    }

    // Start an asynchronous request to read data.
    if (SUCCEEDED(hr))
    {
        hr = pStream->BeginRead(data, DATA_SIZE, pCB, NULL);
    }
```



El método de devolución de llamada [**es IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke). Tiene un único parámetro, *pAsyncResult,* que es un puntero a la [**interfaz DEASYNCAsyncResult.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) Para completar la operación asincrónica, llame al **método End** que coincida con el **método Begin** asincrónico. El **método End** siempre toma un puntero **IMFAsyncResult.** Pase siempre el mismo puntero que recibió en el **método Invoke.** La operación asincrónica no se completa hasta que se llama al **método** End. Puede llamar al **método End** desde dentro del **método Invoke** o puede llamarlo desde otro subproceso.

Por ejemplo, para completar [**EL ARCHIVO DEDABYTEStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) en una secuencia de bytes, llame a [**IMFByteStream::EndRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endread):


```C++
    STDMETHODIMP Invoke(IMFAsyncResult* pResult)
    {
        m_hrStatus = m_pStream->EndRead(pResult, &m_cbRead);

        SetEvent(m_hEvent);

        return S_OK;
    }
```



El valor devuelto del **método End** indica el estado de la operación asincrónica. En la mayoría de los casos, la aplicación realizará algún trabajo una vez completada la operación asincrónica, tanto si se completa correctamente como si no. Tiene varias opciones:

-   Realice el trabajo dentro del [**método Invoke.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Este enfoque es aceptable siempre que la aplicación nunca bloquee el subproceso de llamada o espere algo dentro del **método Invoke.** Si bloquea el subproceso de llamada, podría bloquear la canalización de streaming. Por ejemplo, puede actualizar algunas variables de estado, pero no realizar una operación de lectura sincrónica ni esperar en un objeto mutex.
-   En el [**método Invoke,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) establezca un evento y vuelva inmediatamente. El subproceso de llamada de la aplicación espera el evento y realiza el trabajo cuando se señala el evento.
-   En el [**método Invoke,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) publique un mensaje de ventana privada en la ventana de la aplicación y vuelva inmediatamente. La aplicación realiza el trabajo en su bucle de mensajes. (Asegúrese de publicar el mensaje llamando a **PostMessage**, no **a SendMessage**, porque **SendMessage** puede bloquear el subproceso de devolución de llamada).

Es importante recordar que se llama [**a Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) desde otro subproceso. La aplicación es responsable de garantizar que cualquier trabajo realizado dentro de **Invoke** sea seguro para subprocesos.

De forma predeterminada, el subproceso que llama a [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) no realiza suposiciones sobre el comportamiento del objeto de devolución de llamada. Opcionalmente, puede implementar el método [**IMFAsyncCallback::GetParameters**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters) para devolver información sobre la implementación de devolución de llamada. De lo contrario, este método puede devolver **E \_ NOTIMPL**:


```C++
    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
```



Si especificó un objeto de estado en el método **Begin,** puede recuperarlo desde dentro del método de devolución de llamada mediante una llamada a [**IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Métodos de devolución de llamada asincrónicos](asynchronous-callback-methods.md)
</dt> </dl>

 

 



