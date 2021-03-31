---
description: Cómo establecer la velocidad de reproducción en la sesión multimedia
ms.assetid: 3663b63f-127c-49fc-923a-d05521fe3d35
title: Cómo establecer la velocidad de reproducción en la sesión multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deed8bf480bba1bf1e7d86a41a75b8f41f61046b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820183"
---
# <a name="how-to-set-the-playback-rate-on-the-media-session"></a>Cómo establecer la velocidad de reproducción en la sesión multimedia

Para implementar la funcionalidad de reproducción, como el avance rápido y el rebobinado, es posible que las aplicaciones necesiten cambiar la velocidad de reproducción de un flujo multimedia. Media Foundation proporciona el servicio de control de tarifas que las aplicaciones deben usar para establecer la velocidad de reproducción dinámicamente.

Antes de establecer la velocidad de reproducción, una aplicación debe comprobar si la velocidad es compatible con el origen del medio. Para obtener información sobre cómo consultar las tarifas admitidas, consulte [cómo determinar las tarifas admitidas](how-to-determine-supported-rates.md).

Para obtener información acerca de las velocidades de reproducción, consulte [About Rate Control](about-rate-control.md).

## <a name="to-set-the-playback-rate"></a>Para establecer la velocidad de reproducción

1.  Llame a [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obtener el objeto de control de velocidad de la sesión multimedia.

    Las aplicaciones que llaman a [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) deben asegurarse de lo siguiente:

    -   El parámetro *punkObject* contiene un puntero de interfaz [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inicializado.
    -   Se libera el objeto de control de tasa recibido en el parámetro *ppvObject* para evitar pérdidas de memoria.

2.  Llame al método [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) para establecer la velocidad de reproducción. Una vez que **SetRate** se completa de forma asincrónica, la aplicación recibe el evento [MESessionRateChanged](mesessionratechanged.md) .

## <a name="example"></a>Ejemplo

En el código siguiente se muestra cómo establecer la velocidad de reproducción llamando al método [**SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) .


```C++
///////////////////////////////////////////////////////////////////////
//  Name: SetPlaybackRate
//  Description: 
//      Gets the rate control service from Media Session.
//      Sets the playback rate to the specified rate.
//  Parameter:
//      pMediaSession: [in] Media session object to query.
//      rateRequested: [in] Playback rate to set.
//      bThin: [in] Indicates whether to use thinning.
///////////////////////////////////////////////////////////////////////

HRESULT SetPlaybackRate(
          IMFMediaSession *pMediaSession, 
          float rateRequested, 
          BOOL bThin)
{
    HRESULT hr = S_OK;
    IMFRateControl *pRateControl = NULL;

    // Get the rate control object from the Media Session.
    hr = MFGetService( 
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE, 
           IID_IMFRateControl, 
           (void**) &pRateControl ); 

    // Set the playback rate.
    if(SUCCEEDED(hr))
    {
        hr = pRateControl ->SetRate( bThin, rateRequested); 
    }

    // Clean up.
    SAFE_RELEASE(pRateControl );

    return hr;
}
```



La aplicación se debe detener o pausar antes de poder realizar una transición de una tasa negativa o de cero a una tasa positiva. Para obtener información acerca de estos Estados, consulte [Cómo controlar los Estados de presentación](how-to-control-presentation-states.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sesión de medios](media-session.md)
</dt> <dt>

[Control de tasa](rate-control.md)
</dt> <dt>

[Búsqueda, avance rápido y reproducción inversa](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



