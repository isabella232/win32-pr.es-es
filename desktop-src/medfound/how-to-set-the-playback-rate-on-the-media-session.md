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
# <a name="how-to-set-the-playback-rate-on-the-media-session"></a><span data-ttu-id="08ce8-103">Cómo establecer la velocidad de reproducción en la sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="08ce8-103">How to Set the Playback Rate on the Media Session</span></span>

<span data-ttu-id="08ce8-104">Para implementar la funcionalidad de reproducción, como el avance rápido y el rebobinado, es posible que las aplicaciones necesiten cambiar la velocidad de reproducción de un flujo multimedia.</span><span class="sxs-lookup"><span data-stu-id="08ce8-104">To implement playback functionality such as fast forward and rewind, applications may need to change the playback rate for a media stream.</span></span> <span data-ttu-id="08ce8-105">Media Foundation proporciona el servicio de control de tarifas que las aplicaciones deben usar para establecer la velocidad de reproducción dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="08ce8-105">Media Foundation provides the rate control service that the applications must use to set the playback rate dynamically.</span></span>

<span data-ttu-id="08ce8-106">Antes de establecer la velocidad de reproducción, una aplicación debe comprobar si la velocidad es compatible con el origen del medio.</span><span class="sxs-lookup"><span data-stu-id="08ce8-106">Before setting the playback rate, an application should check whether the rate is supported by the media source.</span></span> <span data-ttu-id="08ce8-107">Para obtener información sobre cómo consultar las tarifas admitidas, consulte [cómo determinar las tarifas admitidas](how-to-determine-supported-rates.md).</span><span class="sxs-lookup"><span data-stu-id="08ce8-107">For information about querying for supported rates, see [How to Determine Supported Rates](how-to-determine-supported-rates.md).</span></span>

<span data-ttu-id="08ce8-108">Para obtener información acerca de las velocidades de reproducción, consulte [About Rate Control](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="08ce8-108">For information about playback rates, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="to-set-the-playback-rate"></a><span data-ttu-id="08ce8-109">Para establecer la velocidad de reproducción</span><span class="sxs-lookup"><span data-stu-id="08ce8-109">To set the playback rate</span></span>

1.  <span data-ttu-id="08ce8-110">Llame a [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obtener el objeto de control de velocidad de la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="08ce8-110">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the rate control object from the Media Session.</span></span>

    <span data-ttu-id="08ce8-111">Las aplicaciones que llaman a [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) deben asegurarse de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="08ce8-111">Applications calling [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) must ensure the following:</span></span>

    -   <span data-ttu-id="08ce8-112">El parámetro *punkObject* contiene un puntero de interfaz [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inicializado.</span><span class="sxs-lookup"><span data-stu-id="08ce8-112">The *punkObject* parameter contains an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer.</span></span>
    -   <span data-ttu-id="08ce8-113">Se libera el objeto de control de tasa recibido en el parámetro *ppvObject* para evitar pérdidas de memoria.</span><span class="sxs-lookup"><span data-stu-id="08ce8-113">The rate control object received in the *ppvObject* parameter is released to avoid memory leaks.</span></span>

2.  <span data-ttu-id="08ce8-114">Llame al método [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) para establecer la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="08ce8-114">Call the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method to set the playback rate.</span></span> <span data-ttu-id="08ce8-115">Una vez que **SetRate** se completa de forma asincrónica, la aplicación recibe el evento [MESessionRateChanged](mesessionratechanged.md) .</span><span class="sxs-lookup"><span data-stu-id="08ce8-115">After **SetRate** completes asynchronously, the application receives the [MESessionRateChanged](mesessionratechanged.md) event.</span></span>

## <a name="example"></a><span data-ttu-id="08ce8-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="08ce8-116">Example</span></span>

<span data-ttu-id="08ce8-117">En el código siguiente se muestra cómo establecer la velocidad de reproducción llamando al método [**SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) .</span><span class="sxs-lookup"><span data-stu-id="08ce8-117">The following code shows how to set the playback rate by calling the [**SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) method.</span></span>


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



<span data-ttu-id="08ce8-118">La aplicación se debe detener o pausar antes de poder realizar una transición de una tasa negativa o de cero a una tasa positiva.</span><span class="sxs-lookup"><span data-stu-id="08ce8-118">The application must be stopped or paused before it can make a transition from a negative or zero rate to a positive rate.</span></span> <span data-ttu-id="08ce8-119">Para obtener información acerca de estos Estados, consulte [Cómo controlar los Estados de presentación](how-to-control-presentation-states.md).</span><span class="sxs-lookup"><span data-stu-id="08ce8-119">For information about these states, see [How to Control Presentation States](how-to-control-presentation-states.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="08ce8-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="08ce8-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08ce8-121">Sesión de medios</span><span class="sxs-lookup"><span data-stu-id="08ce8-121">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="08ce8-122">Control de tasa</span><span class="sxs-lookup"><span data-stu-id="08ce8-122">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="08ce8-123">Búsqueda, avance rápido y reproducción inversa</span><span class="sxs-lookup"><span data-stu-id="08ce8-123">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



