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
# <a name="how-to-determine-supported-rates"></a><span data-ttu-id="ad10c-103">Cómo determinar las tarifas admitidas</span><span class="sxs-lookup"><span data-stu-id="ad10c-103">How to Determine Supported Rates</span></span>

<span data-ttu-id="ad10c-104">Antes de cambiar la velocidad de reproducción, una aplicación debe comprobar si la velocidad de reproducción es compatible con los objetos de la canalización.</span><span class="sxs-lookup"><span data-stu-id="ad10c-104">Before changing the playback rate, an application should check whether the playback rate is supported by the objects in the pipeline.</span></span> <span data-ttu-id="ad10c-105">La interfaz [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) proporciona métodos para obtener las tasas máximas hacia delante y hacia atrás, la velocidad admitida más cercana a la tarifa solicitada y la velocidad más lenta.</span><span class="sxs-lookup"><span data-stu-id="ad10c-105">The [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) interface provides methods to get the maximum forward and reverse rates, the supported rate nearest to a requested rate, and the slowest rate.</span></span> <span data-ttu-id="ad10c-106">Cada una de estas consultas de tarifas puede especificar la dirección de reproducción y si se va a usar el ligero.</span><span class="sxs-lookup"><span data-stu-id="ad10c-106">Each of these rate queries can specify the playback direction and whether to use thinning.</span></span> <span data-ttu-id="ad10c-107">La velocidad de reproducción exacta se consulta mediante la interfaz [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) .</span><span class="sxs-lookup"><span data-stu-id="ad10c-107">The exact playback rate is queried by using the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interface.</span></span>

<span data-ttu-id="ad10c-108">Para obtener información acerca de cómo cambiar las velocidades de reproducción, consulte [cómo establecer la velocidad de reproducción en la sesión multimedia](how-to-set-the-playback-rate-on-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="ad10c-108">For information about changing playback rates, see [How to Set the Playback Rate on the Media Session](how-to-set-the-playback-rate-on-the-media-session.md).</span></span>

<span data-ttu-id="ad10c-109">Para obtener información general acerca de las velocidades de reproducción, consulte [About Rate Control](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="ad10c-109">For general information about playback rates, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="to-determine-the-current-playback-rate"></a><span data-ttu-id="ad10c-110">Para determinar la velocidad de reproducción actual</span><span class="sxs-lookup"><span data-stu-id="ad10c-110">To determine the current playback rate</span></span>

1.  <span data-ttu-id="ad10c-111">Obtiene el servicio de control de velocidad de la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="ad10c-111">Get the rate control service from the Media Session.</span></span>

    ```C++
    IMFRateControl *pRateControl = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateControl, 
           (void**) &pRateControl );
    ```

    

    <span data-ttu-id="ad10c-112">Pase un puntero de interfaz [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inicializado en el parámetro *punkObject* de [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span><span class="sxs-lookup"><span data-stu-id="ad10c-112">Pass an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer in the *punkObject* parameter of [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span></span>

    <span data-ttu-id="ad10c-113">La aplicación debe consultar el servicio de control de tarifas a través de la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="ad10c-113">The application must query for the rate control service through the Media Session.</span></span> <span data-ttu-id="ad10c-114">Internamente, la sesión multimedia consulta los objetos en la topología.</span><span class="sxs-lookup"><span data-stu-id="ad10c-114">Internally, the Media Session queries the objects in the topology.</span></span>

2.  <span data-ttu-id="ad10c-115">Llame al método [**IMFRateControl:: GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) para obtener la velocidad de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="ad10c-115">Call the [**IMFRateControl::GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) method to get the current playback rate.</span></span>

    ```C++
    hr = pRateControl->GetRate(&bThin, &rate);
    ```

    

    <span data-ttu-id="ad10c-116">El parámetro *pfThin* de [**GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) recibe un valor **booleano** que indica si la secuencia se está simplificando actualmente.</span><span class="sxs-lookup"><span data-stu-id="ad10c-116">The *pfThin* parameter of [**GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) receives a **BOOL** value that indicates whether the stream is currently being thinned.</span></span> <span data-ttu-id="ad10c-117">La aplicación debe pasar un **valor null** si no desea consultar la compatibilidad de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="ad10c-117">The application must pass **NULL** if it does not want to query thinning support for the stream.</span></span> <span data-ttu-id="ad10c-118">El parámetro *pflRate* recibe la velocidad de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="ad10c-118">The *pflRate* parameter receives the current playback rate.</span></span>

## <a name="to-determine-the-nearest-supported-rate"></a><span data-ttu-id="ad10c-119">Para determinar la velocidad admitida más cercana</span><span class="sxs-lookup"><span data-stu-id="ad10c-119">To determine the nearest supported rate</span></span>

1.  <span data-ttu-id="ad10c-120">Obtiene el servicio de soporte técnico de tarifas de la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="ad10c-120">Get the rate support service from the Media Session.</span></span>

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    <span data-ttu-id="ad10c-121">Pase un puntero de interfaz [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inicializado en el parámetro *punkObject* de [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span><span class="sxs-lookup"><span data-stu-id="ad10c-121">Pass an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer in the *punkObject* parameter of [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span></span>

2.  <span data-ttu-id="ad10c-122">Llame al método [**IMFRateSupport:: IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) para recuperar la velocidad admitida más cercana a la velocidad de reproducción solicitada.</span><span class="sxs-lookup"><span data-stu-id="ad10c-122">Call the [**IMFRateSupport::IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) method to retrieve the supported rate nearest to a requested playback rate.</span></span>

    ```C++
    float rateRequested = 4.0;
    float actualRate = 0;
    hr = pRateSupport->IsRateSupported(
           TRUE, 
           rateRequested, 
           &actualRate );
    ```

    

    <span data-ttu-id="ad10c-123">En el ejemplo se consulta si se admite una velocidad de reproducción de 4,0 con un ligero.</span><span class="sxs-lookup"><span data-stu-id="ad10c-123">The example queries whether a playback rate of 4.0 is supported with thinning.</span></span> <span data-ttu-id="ad10c-124">Esto se indica mediante el paso de **true** en el parámetro *fThin* de [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported).</span><span class="sxs-lookup"><span data-stu-id="ad10c-124">This is indicated by passing **TRUE** in the *fThin* parameter of [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported).</span></span> <span data-ttu-id="ad10c-125">Si se admite esta velocidad, *actualRate* contiene la velocidad de reproducción de 4,0 y la llamada se realiza correctamente con un valor devuelto de S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ad10c-125">If this rate is supported, *actualRate* contains the playback rate of 4.0, and the call succeeds with a return value of S\_OK.</span></span> <span data-ttu-id="ad10c-126">Si no se admite la velocidad de reproducción exacta, se recibirá la tarifa admitida más cercana en *actualRate*.</span><span class="sxs-lookup"><span data-stu-id="ad10c-126">If the exact playback rate is not supported, the nearest supported rate is received in *actualRate*.</span></span> <span data-ttu-id="ad10c-127">Si no se admite la velocidad y no hay ninguna velocidad de reproducción más cercana disponible, la llamada devuelve un código de error adecuado.</span><span class="sxs-lookup"><span data-stu-id="ad10c-127">If the rate is not supported and there is no available nearest playback rate, the call returns an appropriate error code.</span></span>

    <span data-ttu-id="ad10c-128">Estos valores pueden cambiar en función de los componentes de canalización que se carguen.</span><span class="sxs-lookup"><span data-stu-id="ad10c-128">These values can change depending on which pipeline components are loaded.</span></span> <span data-ttu-id="ad10c-129">Por lo tanto, debe consultar los valores de nuevo siempre que cargue un nuevo topololgy.</span><span class="sxs-lookup"><span data-stu-id="ad10c-129">Therefore, you should query the values again whenever you load a new topololgy.</span></span>

    <span data-ttu-id="ad10c-130">Si no se admite la velocidad de reproducción deseada, una opción es consultar cada objeto en la topología individualmente para averiguar si un componente determinado no admite la velocidad.</span><span class="sxs-lookup"><span data-stu-id="ad10c-130">If the desired playback rate is not supported, one option is to query each object in the topology individually, to find out if a particular component does not support the rate.</span></span> <span data-ttu-id="ad10c-131">Es posible que pueda volver a generar la topología sin este componente y, a continuación, reproducirla a la tarifa deseada.</span><span class="sxs-lookup"><span data-stu-id="ad10c-131">You might be able to rebuild the topology without this component and then play at the desired rate.</span></span> <span data-ttu-id="ad10c-132">Por ejemplo, si todos los componentes excepto el procesador de audio admiten una tasa determinada, puede volver a generar la topología sin la rama de audio y reproducir a la velocidad deseada sin audio.</span><span class="sxs-lookup"><span data-stu-id="ad10c-132">For example, if every component except the audio renderer supports a given rate, you could rebuild the topology without the audio branch and play at the desired rate without audio.</span></span>

## <a name="to-determine-the-slowest-supported-rate"></a><span data-ttu-id="ad10c-133">Para determinar la velocidad compatible más lenta</span><span class="sxs-lookup"><span data-stu-id="ad10c-133">To determine the slowest supported rate</span></span>

1.  <span data-ttu-id="ad10c-134">Obtiene el servicio de soporte técnico de tarifas de la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="ad10c-134">Get the rate support service from the Media Session.</span></span>

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    <span data-ttu-id="ad10c-135">Pase un puntero de interfaz [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inicializado en el parámetro *punkObject* de [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span><span class="sxs-lookup"><span data-stu-id="ad10c-135">Pass an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer in the *punkObject* parameter of [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span></span>

2.  <span data-ttu-id="ad10c-136">Llame al método [**IMFRateSupport:: GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate) para recuperar la velocidad compatible más lenta.</span><span class="sxs-lookup"><span data-stu-id="ad10c-136">Call the [**IMFRateSupport::GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate) method to retrieve the slowest supported rate.</span></span>

    ```C++
    float slowestRate = 0;
    hr = pRateSupport->GetSlowestRate(
           MFRATE_REVERSE, 
           TRUE, 
           &slowestRate);
    ```

    

    <span data-ttu-id="ad10c-137">En el ejemplo se consulta la velocidad de reproducción inversa más lenta con un ligero.</span><span class="sxs-lookup"><span data-stu-id="ad10c-137">The example queries for the slowest reverse playback rate with thinning.</span></span> <span data-ttu-id="ad10c-138">La tasa de límite inferior se recibe en el parámetro *slowestRate* de [**GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate).</span><span class="sxs-lookup"><span data-stu-id="ad10c-138">The lower bound rate is received in *slowestRate* parameter of [**GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate).</span></span>

    <span data-ttu-id="ad10c-139">Si no se admite la reproducción inversa o el simplificado, la llamada devuelve un código de error adecuado.</span><span class="sxs-lookup"><span data-stu-id="ad10c-139">If reverse playback or thinning is not supported, the call returns an appropriate error code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad10c-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ad10c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad10c-141">Sesión de medios</span><span class="sxs-lookup"><span data-stu-id="ad10c-141">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="ad10c-142">Control de tasa</span><span class="sxs-lookup"><span data-stu-id="ad10c-142">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="ad10c-143">Búsqueda, avance rápido y reproducción inversa</span><span class="sxs-lookup"><span data-stu-id="ad10c-143">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



