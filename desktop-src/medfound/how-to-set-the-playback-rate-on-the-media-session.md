---
description: Cómo establecer la velocidad de reproducción en la sesión multimedia
ms.assetid: 3663b63f-127c-49fc-923a-d05521fe3d35
title: Cómo establecer la velocidad de reproducción en la sesión multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deed8bf480bba1bf1e7d86a41a75b8f41f61046b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468754"
---
# <a name="how-to-set-the-playback-rate-on-the-media-session"></a>Cómo establecer la velocidad de reproducción en la sesión multimedia

Para implementar funcionalidades de reproducción como avance rápido y rebobinado, es posible que las aplicaciones deba cambiar la velocidad de reproducción de una secuencia multimedia. Media Foundation proporciona el servicio de control de velocidad que las aplicaciones deben usar para establecer dinámicamente la velocidad de reproducción.

Antes de establecer la velocidad de reproducción, una aplicación debe comprobar si la velocidad es compatible con el origen multimedia. Para obtener información sobre cómo consultar las tarifas admitidas, [vea How to Determine Supported Rates](how-to-determine-supported-rates.md).

Para obtener información sobre las velocidades de reproducción, vea [Acerca del control de velocidad.](about-rate-control.md)

## <a name="to-set-the-playback-rate"></a>Para establecer la velocidad de reproducción

1.  Llame [**a MFGetService para**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) obtener el objeto de control de velocidad de la sesión multimedia.

    Las aplicaciones que [**llaman a MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) deben asegurarse de lo siguiente:

    -   El *parámetroobjetoobject* contiene un puntero de interfaz [**INITIALIZEMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inicializado.
    -   El objeto de control de velocidad recibido en *el parámetro ppvObject* se libera para evitar pérdidas de memoria.

2.  Llame al [**método IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) para establecer la velocidad de reproducción. Una **vez que SetRate** se completa de forma asincrónica, la aplicación recibe el [evento MESessionRateChanged.](mesessionratechanged.md)

## <a name="example"></a>Ejemplo

En el código siguiente se muestra cómo establecer la velocidad de reproducción mediante una llamada al [**método SetRate.**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate)


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



La aplicación debe detenerse o pausarse para poder realizar una transición de una tasa negativa o cero a una tasa positiva. Para obtener información sobre estos estados, [vea Cómo controlar los estados de presentación](how-to-control-presentation-states.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sesión multimedia](media-session.md)
</dt> <dt>

[Control de velocidad](rate-control.md)
</dt> <dt>

[Búsqueda, Inserción rápida y reproducción inversa](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



