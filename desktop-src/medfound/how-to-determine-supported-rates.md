---
description: Cómo determinar las tarifas admitidas
ms.assetid: 7f2b64e1-1062-4f77-b8e0-62b6d962ae8b
title: Cómo determinar las tarifas admitidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f67e9753604f51e85c641e616e8b69944b96618
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580452"
---
# <a name="how-to-determine-supported-rates"></a>Cómo determinar las tarifas admitidas

Antes de cambiar la velocidad de reproducción, una aplicación debe comprobar si los objetos de la canalización admiten la velocidad de reproducción. La [**interfaz IMFRateSupport proporciona**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) métodos para obtener las tasas máximas de avance e inverso, la tasa admitida más cercana a una tasa solicitada y la velocidad más lenta. Cada una de estas consultas de velocidad puede especificar la dirección de reproducción y si se debe usar la simplificación. La velocidad de reproducción exacta se consulta mediante la interfaz [**DECONTROLRATECONTROL.**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)

Para obtener información sobre cómo cambiar las velocidades de reproducción, [vea Cómo establecer la velocidad de reproducción en la sesión multimedia.](how-to-set-the-playback-rate-on-the-media-session.md)

Para obtener información general sobre las velocidades de reproducción, vea [Acerca del control de velocidad.](about-rate-control.md)

## <a name="to-determine-the-current-playback-rate"></a>Para determinar la velocidad de reproducción actual

1.  Obtenga el servicio de control de velocidad de la sesión multimedia.

    ```C++
    IMFRateControl *pRateControl = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateControl, 
           (void**) &pRateControl );
    ```

    

    Pase un puntero de interfaz [**DEFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inicializado en el *parámetroobjetoobject* [**de MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).

    La aplicación debe consultar el servicio de control de velocidad a través de la sesión multimedia. Internamente, la sesión multimedia consulta los objetos de la topología.

2.  Llame al [**método IMFRateControl::GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) para obtener la velocidad de reproducción actual.

    ```C++
    hr = pRateControl->GetRate(&bThin, &rate);
    ```

    

    El *parámetro pfThin* de [**GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) recibe un **valor BOOL** que indica si la secuencia se está thinned actualmente. La aplicación debe pasar **NULL** si no desea consultar la compatibilidad con la simplificación de la secuencia. El *parámetro pflRate* recibe la velocidad de reproducción actual.

## <a name="to-determine-the-nearest-supported-rate"></a>Para determinar la tasa admitida más cercana

1.  Obtenga el servicio de compatibilidad de velocidad de la sesión multimedia.

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    Pase un puntero de interfaz [**DEFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inicializado en el *parámetroobjetoobject* [**de MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).

2.  Llame al [**método IMFRateSupport::IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) para recuperar la velocidad admitida más cercana a la tasa de reproducción solicitada.

    ```C++
    float rateRequested = 4.0;
    float actualRate = 0;
    hr = pRateSupport->IsRateSupported(
           TRUE, 
           rateRequested, 
           &actualRate );
    ```

    

    En el ejemplo se consulta si se admite una velocidad de reproducción de 4.0 con la simplificación. Esto se indica pasando **TRUE en** el *parámetro fThin* de [**IsRateSupported.**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) Si se admite esta velocidad, *actualRate* contiene la velocidad de reproducción de 4,0 y la llamada se realiza correctamente con un valor devuelto de S \_ OK. Si no se admite la velocidad de reproducción exacta, se recibe la tasa admitida más cercana en *realRate*. Si no se admite la velocidad y no hay ninguna velocidad de reproducción más cercana disponible, la llamada devuelve un código de error adecuado.

    Estos valores pueden cambiar en función de los componentes de canalización que se carguen. Por lo tanto, debe consultar los valores de nuevo cada vez que cargue un nuevo elemento tolgy.

    Si no se admite la velocidad de reproducción deseada, una opción es consultar cada objeto de la topología individualmente para averiguar si un componente determinado no admite la velocidad. Es posible que pueda recompilar la topología sin este componente y, a continuación, reproducir a la velocidad deseada. Por ejemplo, si todos los componentes excepto el representador de audio admiten una velocidad determinada, podría recompilar la topología sin la rama de audio y reproducirla a la velocidad deseada sin audio.

## <a name="to-determine-the-slowest-supported-rate"></a>Para determinar la velocidad admitida más lenta

1.  Obtenga el servicio de compatibilidad de velocidad de la sesión multimedia.

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    Pase un puntero de interfaz [**DEFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inicializado en el *parámetroobjetoobject* [**de MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).

2.  Llame al [**método IMFRateSupport::GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate) para recuperar la velocidad admitida más lenta.

    ```C++
    float slowestRate = 0;
    hr = pRateSupport->GetSlowestRate(
           MFRATE_REVERSE, 
           TRUE, 
           &slowestRate);
    ```

    

    En el ejemplo se consulta la velocidad de reproducción inversa más lenta con la ralentización. La velocidad de límite inferior se recibe en *el parámetro slowestRate* [**de GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate).

    Si no se admite la reproducción inversa o la simplificación, la llamada devuelve un código de error adecuado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sesión multimedia](media-session.md)
</dt> <dt>

[Control de velocidad](rate-control.md)
</dt> <dt>

[Búsqueda, Inserción rápida y reproducción inversa](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



