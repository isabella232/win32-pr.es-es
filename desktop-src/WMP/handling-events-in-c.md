---
title: Controlar eventos en C++
description: Controlar eventos en C++
ms.assetid: 5d9eb1c7-7022-4442-b67a-6a96fe5ce97f
keywords:
- Reproductor de Windows Media,C++
- Reproductor de Windows Media de objetos, C++
- object model,C++
- Reproductor de Windows Media Mobile,C++
- Reproductor de Windows Media ActiveX control, C++
- Reproductor de Windows Media Control de ActiveX móvil,C++
- ActiveX control, C++
- Inserción de programas de C++
- inserción, programas de C++
- Reproductor de Windows Media ActiveX control de eventos, control de eventos
- Reproductor de Windows Media Control de ActiveX móvil, control de eventos
- ActiveX control de eventos, control de eventos
- events,C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5d50be4622cee9ee455710f8b9d2e4cafc63d6560e08faf5c3deaddcdaccc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748410"
---
# <a name="handling-events-in-c"></a>Controlar eventos en C++

Puede recibir eventos de Reproductor de Windows Media de dos maneras.

-   A **través de IDispatch** mediante la **\_ interfaz WMPOCXEvents.** Esta es la interfaz que se va a usar en la mayoría de los escenarios de inserción.
-   A través **de la interfaz IWMPEvents.** Esta interfaz está disponible cuando el código está conectado al reproductor en modo completo, como al conectarse remotamente al control Reproductor de Windows Media o en un complemento de interfaz de usuario.

En cada escenario, se empieza a escuchar eventos mediante puntos de conexión COM.

En el código de ejemplo siguiente se usan tres variables miembro:


```C++
CComPtr<IWMPPlayer>         m_spWMPPlayer;
CComPtr<IConnectionPoint>   m_spConnectionPoint;
DWORD                       m_dwAdviseCookie;

```



Para recuperar un punto de conexión, primero **debe usar QueryInterface** para el contenedor de puntos de conexión.


```C++
HRESULT  hr = S_OK;
// Smart pointer to IConnectionPointContainer
CComPtr<IConnectionPointContainer>  spConnectionContainer;

hr = m_spWMPPlayer->QueryInterface(&spConnectionContainer);

```



A continuación, solicite el punto de conexión para la interfaz de eventos que desea usar. En primer lugar, el código de ejemplo siguiente intenta usar **IWMPEvents**. Si esa interfaz no está disponible, usa **\_ WMPOCXEvents**.


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



Por último, llame **a IConnectionPoint::Advise para** solicitar eventos.


```C++
if(SUCCEEDED(hr))
{
    hr = m_spConnectionPoint->Advise(this, &m_dwAdviseCookie);
}

```



En el ejemplo anterior, el primer parámetro supone que la clase que realiza la llamada implementa **IWMPEvents** y **\_ WMPOCXEvents**. El segundo parámetro es un valor devuelto que se usa para dejar de escuchar eventos, como cuando se cierra el programa, mediante código similar al siguiente:


```C++
// Stop listening to events
if (m_spConnectionPoint)
{
    if (0 != m_dwAdviseCookie)
        m_spConnectionPoint->Unadvise(m_dwAdviseCookie);
        m_spConnectionPoint.Release();
}

```



La implementación de los controladores de eventos **para IWMPEvents** y **\_ WMPOCXEvents** difiere. Para **IWMPEvents**, debe implementar una función para controlar todos los eventos definidos por la interfaz , incluso si no piensa usar el evento .


```C++
// IWMPEvents methods
void STDMETHODCALLTYPE OpenStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE PlayStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE AudioLanguageChange( long LangID ){ return; }
// And so on...

```



Para implementar **\_ controladores WMPOCXEvents,** debe usar **IDispatch::Invoke**, que es una implementación de controlador de eventos única para todos los eventos que se están produciendo en la interfaz **IDispatch.** Esto significa que puede elegir controlar solo determinados eventos y omitir otros. En el código de ejemplo siguiente se muestra un **\_ controlador WMPOCXEvents,** mediante **Invoke**, que controla solo los eventos **OpenStateChange** y **PlayStateChange:**


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



En el código de ejemplo anterior, cada caso simplemente llama al controlador **IWMPEvents** para el evento correspondiente. Si el código solo controla **\_ WMPOCXEvents,** simplemente puede llamar a una función personalizada o controlar el evento en línea después de la instrucción **case.**

## <a name="receiving-events-from-windows-media-player-10-mobile"></a>Recepción de eventos desde Reproductor de Windows Media 10 Mobile

El Reproductor de Windows Media 10 Mobile solo admite la recepción de determinados eventos a través de **\_ WMPOCXEvents** e **IWMPEvents**. Para obtener más información, consulte la documentación de **IWMPEvents**.

## <a name="samples"></a>Ejemplos

El Reproductor de Windows Media instalación instala un ejemplo que muestra el control de eventos. Consulte el ejemplo WMPHost para obtener más información.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Ejemplos**](samples.md)
</dt> <dt>

[**Usar el control Reproductor de Windows Media en un programa de C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




