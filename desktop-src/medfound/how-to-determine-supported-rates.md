---
description: Cómo determinar las tarifas admitidas
ms.assetid: 7f2b64e1-1062-4f77-b8e0-62b6d962ae8b
title: Cómo determinar las tarifas admitidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f67e9753604f51e85c641e616e8b69944b96618
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275770"
---
# <a name="how-to-determine-supported-rates"></a>Cómo determinar las tarifas admitidas

Antes de cambiar la velocidad de reproducción, una aplicación debe comprobar si la velocidad de reproducción es compatible con los objetos de la canalización. La interfaz [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) proporciona métodos para obtener las tasas máximas hacia delante y hacia atrás, la velocidad admitida más cercana a la tarifa solicitada y la velocidad más lenta. Cada una de estas consultas de tarifas puede especificar la dirección de reproducción y si se va a usar el ligero. La velocidad de reproducción exacta se consulta mediante la interfaz [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) .

Para obtener información acerca de cómo cambiar las velocidades de reproducción, consulte [cómo establecer la velocidad de reproducción en la sesión multimedia](how-to-set-the-playback-rate-on-the-media-session.md).

Para obtener información general acerca de las velocidades de reproducción, consulte [About Rate Control](about-rate-control.md).

## <a name="to-determine-the-current-playback-rate"></a>Para determinar la velocidad de reproducción actual

1.  Obtiene el servicio de control de velocidad de la sesión multimedia.

    ```C++
    IMFRateControl *pRateControl = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateControl, 
           (void**) &pRateControl );
    ```

    

    Pase un puntero de interfaz [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inicializado en el parámetro *punkObject* de [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).

    La aplicación debe consultar el servicio de control de tarifas a través de la sesión multimedia. Internamente, la sesión multimedia consulta los objetos en la topología.

2.  Llame al método [**IMFRateControl:: GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) para obtener la velocidad de reproducción actual.

    ```C++
    hr = pRateControl->GetRate(&bThin, &rate);
    ```

    

    El parámetro *pfThin* de [**GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) recibe un valor **booleano** que indica si la secuencia se está simplificando actualmente. La aplicación debe pasar un **valor null** si no desea consultar la compatibilidad de la secuencia. El parámetro *pflRate* recibe la velocidad de reproducción actual.

## <a name="to-determine-the-nearest-supported-rate"></a>Para determinar la velocidad admitida más cercana

1.  Obtiene el servicio de soporte técnico de tarifas de la sesión multimedia.

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    Pase un puntero de interfaz [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inicializado en el parámetro *punkObject* de [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).

2.  Llame al método [**IMFRateSupport:: IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) para recuperar la velocidad admitida más cercana a la velocidad de reproducción solicitada.

    ```C++
    float rateRequested = 4.0;
    float actualRate = 0;
    hr = pRateSupport->IsRateSupported(
           TRUE, 
           rateRequested, 
           &actualRate );
    ```

    

    En el ejemplo se consulta si se admite una velocidad de reproducción de 4,0 con un ligero. Esto se indica mediante el paso de **true** en el parámetro *fThin* de [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported). Si se admite esta velocidad, *actualRate* contiene la velocidad de reproducción de 4,0 y la llamada se realiza correctamente con un valor devuelto de S \_ OK. Si no se admite la velocidad de reproducción exacta, se recibirá la tarifa admitida más cercana en *actualRate*. Si no se admite la velocidad y no hay ninguna velocidad de reproducción más cercana disponible, la llamada devuelve un código de error adecuado.

    Estos valores pueden cambiar en función de los componentes de canalización que se carguen. Por lo tanto, debe consultar los valores de nuevo siempre que cargue un nuevo topololgy.

    Si no se admite la velocidad de reproducción deseada, una opción es consultar cada objeto en la topología individualmente para averiguar si un componente determinado no admite la velocidad. Es posible que pueda volver a generar la topología sin este componente y, a continuación, reproducirla a la tarifa deseada. Por ejemplo, si todos los componentes excepto el procesador de audio admiten una tasa determinada, puede volver a generar la topología sin la rama de audio y reproducir a la velocidad deseada sin audio.

## <a name="to-determine-the-slowest-supported-rate"></a>Para determinar la velocidad compatible más lenta

1.  Obtiene el servicio de soporte técnico de tarifas de la sesión multimedia.

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    Pase un puntero de interfaz [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inicializado en el parámetro *punkObject* de [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).

2.  Llame al método [**IMFRateSupport:: GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate) para recuperar la velocidad compatible más lenta.

    ```C++
    float slowestRate = 0;
    hr = pRateSupport->GetSlowestRate(
           MFRATE_REVERSE, 
           TRUE, 
           &slowestRate);
    ```

    

    En el ejemplo se consulta la velocidad de reproducción inversa más lenta con un ligero. La tasa de límite inferior se recibe en el parámetro *slowestRate* de [**GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate).

    Si no se admite la reproducción inversa o el simplificado, la llamada devuelve un código de error adecuado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sesión de medios](media-session.md)
</dt> <dt>

[Control de tasa](rate-control.md)
</dt> <dt>

[Búsqueda, avance rápido y reproducción inversa](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



