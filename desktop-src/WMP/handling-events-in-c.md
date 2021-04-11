---
title: Controlar eventos en C++
description: Controlar eventos en C++
ms.assetid: 5d9eb1c7-7022-4442-b67a-6a96fe5ce97f
keywords:
- Windows Media Player, C++
- Modelo de objetos de Windows Media Player, C++
- modelo de objetos, C++
- Windows Media Player Mobile, C++
- Control ActiveX de Windows Media Player, C++
- Control ActiveX móvil de Windows Media Player, C++
- Control ActiveX, C++
- Incrustación de programas de C++
- incrustación, programas de C++
- Control ActiveX de Windows Media Player, control de eventos
- Control ActiveX de Windows Media Player Mobile, control de eventos
- Control ActiveX, control de eventos
- eventos, C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16cbef547ab2604244c5c204707a08eb87a6b70a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148825"
---
# <a name="handling-events-in-c"></a>Controlar eventos en C++

Puede recibir eventos de Windows Media Player de dos maneras.

-   A **IDispatch** mediante la interfaz **\_ WMPOCXEvents** . Esta es la interfaz que se usa para la mayoría de los escenarios de inserción.
-   A través de la interfaz **IWMPEvents** . Esta interfaz está disponible cuando el código está conectado al reproductor en modo completo, por ejemplo, cuando la comunicación remota de Windows Media Player control o en un complemento de la interfaz de usuario.

En cada escenario, empieza a escuchar eventos mediante puntos de conexión COM.

En el ejemplo de código siguiente se usan tres variables miembro:


```C++
CComPtr<IWMPPlayer>         m_spWMPPlayer;
CComPtr<IConnectionPoint>   m_spConnectionPoint;
DWORD                       m_dwAdviseCookie;

```



Para recuperar un punto de conexión, primero debe **QueryInterface** para el contenedor de puntos de conexión.


```C++
HRESULT  hr = S_OK;
// Smart pointer to IConnectionPointContainer
CComPtr<IConnectionPointContainer>  spConnectionContainer;

hr = m_spWMPPlayer->QueryInterface(&spConnectionContainer);

```



A continuación, solicite el punto de conexión para la interfaz de eventos que desea usar. El siguiente código de ejemplo intenta usar primero **IWMPEvents**. Si esa interfaz no está disponible, utiliza **\_ WMPOCXEvents**.


```C++
// Test whether the control supports the IWMPEvents interface.
if(SUCCEEDED(hr))
{
    hr = spConnectionContainer->FindConnectionPoint(__uuidof(IWMPEvents), &m_spConnectionPoint);
    if (FAILED(hr))
    {
        // If not, try the _WMPOCXEvents interface, which uses IDispatch.
        hr = spConnectionContainer->FindConnectionPoint(__uuidof(_WMPOCXEvents), &m_spConnectionPoint);
    }
}

```



Por último, llame a **IConnectionPoint:: Advise** para solicitar eventos.


```C++
if(SUCCEEDED(hr))
{
    hr = m_spConnectionPoint->Advise(this, &m_dwAdviseCookie);
}

```



En el ejemplo anterior, el primer parámetro supone que la clase que realiza la llamada implementa **IWMPEvents** y **\_ WMPOCXEvents**. El segundo parámetro es un valor devuelto que se usa para dejar de escuchar eventos, como cuando el programa se cierra, mediante código similar al siguiente:


```C++
// Stop listening to events
if (m_spConnectionPoint)
{
    if (0 != m_dwAdviseCookie)
        m_spConnectionPoint->Unadvise(m_dwAdviseCookie);
        m_spConnectionPoint.Release();
}

```



La implementación de los controladores de eventos para **IWMPEvents** y **\_ WMPOCXEvents** es diferente. En el caso de **IWMPEvents**, debe implementar una función que controle todos los eventos definidos por la interfaz, incluso si no pretende utilizar el evento.


```C++
// IWMPEvents methods
void STDMETHODCALLTYPE OpenStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE PlayStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE AudioLanguageChange( long LangID ){ return; }
// And so on...

```



Para implementar controladores **\_ WMPOCXEvents** , debe usar **IDispatch:: Invoke**, que es una implementación de un solo controlador de eventos para todos los eventos que se producen en la interfaz **IDispatch** . Esto significa que puede elegir controlar solo determinados eventos y omitir otros. En el ejemplo de código siguiente se muestra un controlador de **\_ WMPOCXEvents** , mediante **Invoke**, que solo controla los eventos **OpenStateChange** y **PlayStateChange** :


```C++
HRESULT CMyClass::Invoke(
    DISPID  dispIdMember,      
    REFIID  riid,              
    LCID  lcid,                
    WORD  wFlags,              
    DISPPARAMS FAR*  pDispParams,  
    VARIANT FAR*  pVarResult,  
    EXCEPINFO FAR*  pExcepInfo,  
    unsigned int FAR*  puArgErr )
{
    if (!pDispParams)
        return E_POINTER;

    if (pDispParams->cNamedArgs != 0)
        return DISP_E_NONAMEDARGS;

    HRESULT hr = DISP_E_MEMBERNOTFOUND;

    switch (dispIdMember)
    {
        case DISPID_WMPCOREEVENT_OPENSTATECHANGE:
            OpenStateChange(pDispParams->rgvarg[0].lVal /* NewState */ );
            break;

        case DISPID_WMPCOREEVENT_PLAYSTATECHANGE:
            PlayStateChange(pDispParams->rgvarg[0].lVal /* NewState */);
            break;

        // Other cases can handle additional events by using DISPIDs.
    }

    return( hr );
}

```



En el código de ejemplo anterior, cada caso simplemente llama a a través del controlador **IWMPEvents** para el evento correspondiente. Si el código solo controla **\_ WMPOCXEvents**, puede llamar a una función personalizada o controlar el evento en línea después de la instrucción **Case** .

## <a name="receiving-events-from-windows-media-player-10-mobile"></a>Recibir eventos de Windows Media Player 10 Mobile

El control móvil de Windows Media Player 10 solo admite la recepción de ciertos eventos a través de **\_ WMPOCXEvents** y **IWMPEvents**. Para obtener más información, consulte la documentación de **IWMPEvents**.

## <a name="samples"></a>Ejemplos

El paquete de instalación de Windows Media Player instala un ejemplo que muestra el control de eventos. Vea el ejemplo WMPHost para obtener más información.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Ejemplos**](samples.md)
</dt> <dt>

[**Usar el control Media Player de Windows en un programa de C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




