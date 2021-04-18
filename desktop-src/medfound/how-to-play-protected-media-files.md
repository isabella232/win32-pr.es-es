---
description: Cómo reproducir archivos que contienen medios protegidos con DRM.
ms.assetid: 85d98f49-8af2-42ce-9b36-a025aee93f73
title: Cómo reproducir archivos multimedia protegidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f8f7af78881e43f2f7f85e8f333ab31b1bc2de
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105707561"
---
# <a name="how-to-play-protected-media-files"></a><span data-ttu-id="b1469-103">Cómo reproducir archivos multimedia protegidos</span><span class="sxs-lookup"><span data-stu-id="b1469-103">How to Play Protected Media Files</span></span>

<span data-ttu-id="b1469-104">Un archivo multimedia protegido es cualquier archivo multimedia que tenga reglas asociadas para usar el contenido.</span><span class="sxs-lookup"><span data-stu-id="b1469-104">A protected media file is any media file that has associated rules for using the content.</span></span> <span data-ttu-id="b1469-105">En algunos casos, un archivo multimedia protegido se cifra mediante algún tipo de cifrado de administración de derechos digitales (DRM).</span><span class="sxs-lookup"><span data-stu-id="b1469-105">In some cases, a protected media file is encrypted using some form of digital rights management (DRM) encryption.</span></span> <span data-ttu-id="b1469-106">Para reproducir un archivo multimedia protegido, la reproducción debe realizarse dentro de la ruta de acceso a medios protegidos (PMP).</span><span class="sxs-lookup"><span data-stu-id="b1469-106">To play a protected media file, playback must occur inside the protected media path (PMP).</span></span> <span data-ttu-id="b1469-107">Además, es posible que el usuario tenga que adquirir derechos para el contenido.</span><span class="sxs-lookup"><span data-stu-id="b1469-107">In addition, the user might have to acquire rights to the content.</span></span>

<span data-ttu-id="b1469-108">El término adquisición de derechos hace referencia a cualquier acción que la aplicación debe realizar antes de que el usuario pueda reproducir el contenido.</span><span class="sxs-lookup"><span data-stu-id="b1469-108">The term rights acquisition refers to any action that the application must perform before the user can play the content.</span></span> <span data-ttu-id="b1469-109">El ejemplo más común es obtener una licencia DRM, pero Media Foundation define un mecanismo genérico que puede admitir otros tipos de adquisición de derechos.</span><span class="sxs-lookup"><span data-stu-id="b1469-109">The most common example is obtaining a DRM license, but Media Foundation defines a generic mechanism that can support other types of rights acquisition.</span></span> <span data-ttu-id="b1469-110">La interfaz [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) define este mecanismo genérico.</span><span class="sxs-lookup"><span data-stu-id="b1469-110">The [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface defines this generic mechanism.</span></span>

<span data-ttu-id="b1469-111">La adquisición de derechos debe realizarse fuera de la PMP, desde el proceso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1469-111">Rights acquisition must be done outside of the PMP, from the application process.</span></span> <span data-ttu-id="b1469-112">La sesión multimedia notifica a la aplicación a través de la interfaz [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) , implementada por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1469-112">The Media Session notifies the application through the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface, which is implemented by the application.</span></span> <span data-ttu-id="b1469-113">La sesión multimedia utiliza la interfaz **IMFContentProtectionManager** para reenviar un objeto de habilitador de contenido a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1469-113">The Media Session uses the **IMFContentProtectionManager** interface to forward a content enabler object to the application.</span></span> <span data-ttu-id="b1469-114">Los habilitadores de contenido implementan la interfaz [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) .</span><span class="sxs-lookup"><span data-stu-id="b1469-114">Content enablers implement the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface.</span></span> <span data-ttu-id="b1469-115">La aplicación usa esta interfaz para adquirir los derechos necesarios.</span><span class="sxs-lookup"><span data-stu-id="b1469-115">The application uses this interface to acquire the necessary rights.</span></span>

<span data-ttu-id="b1469-116">Un habilitador de contenido podría admitir la adquisición automática de derechos, en cuyo caso el habilitador de contenido implementa todo el proceso y la aplicación simplemente supervisa el estado.</span><span class="sxs-lookup"><span data-stu-id="b1469-116">A content enabler might support automatic rights acquisition, in which case the content enabler implements the entire process, and the application simply monitors the status.</span></span> <span data-ttu-id="b1469-117">De lo contrario, la aplicación debe usar la adquisición de derechos no silencioso, que es un proceso en el que la aplicación envía datos HTTP POST a una dirección URL proporcionada por el habilitador de contenido.</span><span class="sxs-lookup"><span data-stu-id="b1469-117">Otherwise, the application must use non-silent rights acquisition, which is a process where the application sends HTTP POST data to a URL provided by the content enabler.</span></span>

<span data-ttu-id="b1469-118">Para reproducir medios protegidos, una aplicación sigue los mismos pasos indicados en el tema [Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md), con los siguientes pasos adicionales:</span><span class="sxs-lookup"><span data-stu-id="b1469-118">To play protected media, an application follows the same steps given in the topic [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md), with the following additional steps:</span></span>

1.  <span data-ttu-id="b1469-119">Consulta si el origen multimedia contiene contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="b1469-119">Query whether the media source contains protected content.</span></span> <span data-ttu-id="b1469-120">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="b1469-120">(Optional.)</span></span>
2.  <span data-ttu-id="b1469-121">Cree la sesión multimedia en el proceso de PMP, en lugar del proceso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1469-121">Create the Media Session in the PMP process, instead of the application process.</span></span>
3.  <span data-ttu-id="b1469-122">Realice la adquisición de derechos, si la sesión multimedia lo notifica.</span><span class="sxs-lookup"><span data-stu-id="b1469-122">Perform rights acquisition, if notified to do so by the Media Session.</span></span> <span data-ttu-id="b1469-123">La aplicación realiza esta operación de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b1469-123">This operation is performed asynchronously by the application.</span></span>
4.  <span data-ttu-id="b1469-124">Complete la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b1469-124">Complete the asynchronous operation.</span></span>

## <a name="query-for-protected-content"></a><span data-ttu-id="b1469-125">Consultar contenido protegido</span><span class="sxs-lookup"><span data-stu-id="b1469-125">Query for Protected Content</span></span>

<span data-ttu-id="b1469-126">Para consultar si un origen multimedia contiene contenido protegido, llame a la función [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) en el descriptor de presentación del origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="b1469-126">To query whether a media source contains protected content, call the [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) function on the media source's presentation descriptor.</span></span> <span data-ttu-id="b1469-127">Si la función devuelve S \_ correcto, debe usar el PMP para reproducir el contenido.</span><span class="sxs-lookup"><span data-stu-id="b1469-127">If the function returns S\_OK, you must use the PMP to play the content.</span></span> <span data-ttu-id="b1469-128">Si la función devuelve S \_ false, el PMP no es necesario y puede crear la sesión multimedia en el proceso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1469-128">If the function returns S\_FALSE, the PMP is not required, and you can create the Media Session in the application process.</span></span> <span data-ttu-id="b1469-129">Como alternativa, puede usar el PMP para reproducir ambos tipos de contenido, protegidos y desprotegidos.</span><span class="sxs-lookup"><span data-stu-id="b1469-129">Alternatively, you can use the PMP to play both types of content, protected and unprotected.</span></span> <span data-ttu-id="b1469-130">Si lo hace, no necesita llamar a **MFRequireProtectedEnvironment**.</span><span class="sxs-lookup"><span data-stu-id="b1469-130">If you do that, you do not need to call **MFRequireProtectedEnvironment**.</span></span>

<span data-ttu-id="b1469-131">Para obtener más información acerca de los descriptores de presentación, vea [descriptores de presentación](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="b1469-131">For more information about presentation descriptors, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

## <a name="create-the-pmp-media-session"></a><span data-ttu-id="b1469-132">Crear la sesión de medios de PMP</span><span class="sxs-lookup"><span data-stu-id="b1469-132">Create the PMP Media Session</span></span>

<span data-ttu-id="b1469-133">Para crear la sesión multimedia en el PMP, llame a [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span><span class="sxs-lookup"><span data-stu-id="b1469-133">To create the Media Session in the PMP, call [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span></span> <span data-ttu-id="b1469-134">Esta función es similar a [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession), pero en lugar de crear la sesión multimedia en el proceso de la aplicación, crea la sesión multimedia en el proceso de PMP.</span><span class="sxs-lookup"><span data-stu-id="b1469-134">This function is similar to [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession), but instead of creating the Media Session in the application's process, it creates the Media Session in the PMP process.</span></span> <span data-ttu-id="b1469-135">La aplicación recibe un puntero a un objeto proxy para la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="b1469-135">The application receives a pointer to a proxy object for the Media Session.</span></span> <span data-ttu-id="b1469-136">La aplicación llama a los métodos [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) en el objeto proxy, tal como lo haría en la sesión de medios.</span><span class="sxs-lookup"><span data-stu-id="b1469-136">The application calls [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) methods on the proxy object, just as it would on the Media Session.</span></span> <span data-ttu-id="b1469-137">El objeto proxy reenvía las llamadas a la sesión multimedia a través del límite del proceso.</span><span class="sxs-lookup"><span data-stu-id="b1469-137">The proxy object forwards the calls to the Media Session across the process boundary.</span></span>

<span data-ttu-id="b1469-138">Cree la sesión de medios de PMP como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="b1469-138">Create the PMP Media Session as follows:</span></span>

1.  <span data-ttu-id="b1469-139">Cree un nuevo almacén de atributos mediante una llamada a [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span><span class="sxs-lookup"><span data-stu-id="b1469-139">Create a new attribute store by calling [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span></span>
2.  <span data-ttu-id="b1469-140">Establezca el atributo de administrador de protección de contenido de la [**\_ sesión \_ \_ \_ MF**](mf-session-content-protection-manager-attribute.md) en el almacén de atributos.</span><span class="sxs-lookup"><span data-stu-id="b1469-140">Set the [**MF\_SESSION\_CONTENT\_PROTECTION\_MANAGER**](mf-session-content-protection-manager-attribute.md) attribute on the attribute store.</span></span> <span data-ttu-id="b1469-141">El valor de este atributo es un puntero a la implementación de [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1469-141">The value of this attribute is a pointer to your application's implementation of [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager).</span></span> <span data-ttu-id="b1469-142">Llame a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) para establecer el atributo.</span><span class="sxs-lookup"><span data-stu-id="b1469-142">Call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) to set the attribute.</span></span>
3.  <span data-ttu-id="b1469-143">Llame a [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) para crear la sesión multimedia en el proceso de PMP.</span><span class="sxs-lookup"><span data-stu-id="b1469-143">Call [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) to create the Media Session in the PMP process.</span></span> <span data-ttu-id="b1469-144">El parámetro *pConfiguration* es un puntero a la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) del almacén de atributos.</span><span class="sxs-lookup"><span data-stu-id="b1469-144">The *pConfiguration* parameter is a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface of the attribute store.</span></span>


```C++
IMFAttributes *pAttributes = NULL;
IMFMediaSession *pSession = NULL;

// Create the attribute store.
hr = MFCreateAttributes(&pAttributes, 1);

// Set the IMFContentProtectionManager pointer.
if (SUCCEEDED(hr))
{
    hr = pAttributes->SetUnknown(
        MF_SESSION_CONTENT_PROTECTION_MANAGER, 
        pCPM  // Your implementation of IMFContentProtectionManager.
        );
}

// Create the Media Session.
if (SUCCEEDED(hr))
{
    hr = MFCreatePMPMediaSession(
        0,
        pAttributes, 
        &pSession,
        NULL
    );
}

SAFE_RELEASE(pAttributes); // Release the attribute store.
// Use the Media Session to control playback (not shown).
```



<span data-ttu-id="b1469-145">A continuación, cree una topología de reproducción y ponerla en cola en la sesión multimedia, como se describe en [crear topologías de reproducción](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="b1469-145">Next, create a playback topology and queue it on the Media Session, as described in [Creating Playback Topologies](creating-playback-topologies.md).</span></span>

## <a name="perform-rights-acquisition"></a><span data-ttu-id="b1469-146">Realizar la adquisición de derechos</span><span class="sxs-lookup"><span data-stu-id="b1469-146">Perform Rights Acquisition</span></span>

<span data-ttu-id="b1469-147">Si la reproducción requiere la adquisición de derechos, la sesión multimedia llama a [**IMFContentProtectionManager:: BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent).</span><span class="sxs-lookup"><span data-stu-id="b1469-147">If playback requires rights acquisition, the Media Session calls [**IMFContentProtectionManager::BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent).</span></span> <span data-ttu-id="b1469-148">El parámetro *pEnablerActivate* de este método es un puntero a la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="b1469-148">The *pEnablerActivate* parameter of this method is a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span> <span data-ttu-id="b1469-149">Use esta interfaz para crear el objeto de habilitador de contenido, que expone la interfaz [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) .</span><span class="sxs-lookup"><span data-stu-id="b1469-149">Use this interface to create the content enabler object, which exposes the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface.</span></span> <span data-ttu-id="b1469-150">A continuación, use el habilitador de contenido para realizar el paso de adquisición de derechos.</span><span class="sxs-lookup"><span data-stu-id="b1469-150">Then use the content enabler to perform the rights acquisition step.</span></span>

<span data-ttu-id="b1469-151">Para crear el habilitador de contenido, llame a [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject):</span><span class="sxs-lookup"><span data-stu-id="b1469-151">To create the content enabler, call [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject):</span></span>


```C++
IMFContentEnabler *pEnabler = NULL;
hr = pEnablerActivate->ActivateObject(
    IID_IMFContentEnabler, 
    (void**)&pEnabler
    );
```



<span data-ttu-id="b1469-152">Consulte el puntero [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) devuelto para la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="b1469-152">Query the returned [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) pointer for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="b1469-153">Use esta interfaz para obtener eventos del objeto de habilitador de contenido.</span><span class="sxs-lookup"><span data-stu-id="b1469-153">Use this interface to get events from the content enabler object.</span></span> <span data-ttu-id="b1469-154">Para obtener más información sobre los eventos, consulte [generadores de eventos multimedia](media-event-generators.md).</span><span class="sxs-lookup"><span data-stu-id="b1469-154">For more information about events, see [Media Event Generators](media-event-generators.md).</span></span>

<span data-ttu-id="b1469-155">Para averiguar si el habilitador de contenido admite la adquisición automática, llame a [**IMFContentEnabler:: IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported).</span><span class="sxs-lookup"><span data-stu-id="b1469-155">To find out whether the content enabler supports automatic acquisition, call [**IMFContentEnabler::IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported).</span></span> <span data-ttu-id="b1469-156">Si este método devuelve el valor **true**, la aplicación debe usar la adquisición automática.</span><span class="sxs-lookup"><span data-stu-id="b1469-156">If this method returns the value **TRUE**, the application should use automatic acquisition.</span></span> <span data-ttu-id="b1469-157">De lo contrario, use la adquisición no silenciosa.</span><span class="sxs-lookup"><span data-stu-id="b1469-157">Otherwise, use non-silent acquisition.</span></span>

<span data-ttu-id="b1469-158">El método [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) es asincrónico.</span><span class="sxs-lookup"><span data-stu-id="b1469-158">The [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) method is asynchronous.</span></span> <span data-ttu-id="b1469-159">La aplicación debe realizar el paso de adquisición en el subproceso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1469-159">The application should perform the acquisition step on the application's thread.</span></span> <span data-ttu-id="b1469-160">Un enfoque consiste en publicar un mensaje de ventana privada en la ventana principal de la aplicación, notificando al subproceso de la aplicación que realice la adquisición.</span><span class="sxs-lookup"><span data-stu-id="b1469-160">One approach is to post a private window message to the application's main window, notifying the application thread to perform the acquisition.</span></span> <span data-ttu-id="b1469-161">Mientras la operación está pendiente, la aplicación debe almacenar el puntero de devolución de llamada y el objeto de estado que recibió en los parámetros *pCallback* y *punkState* de **BeginEnableContent**.</span><span class="sxs-lookup"><span data-stu-id="b1469-161">While the operation is pending, the application must store the callback pointer and the state object that it received in the *pCallback* and *punkState* parameters of **BeginEnableContent**.</span></span> <span data-ttu-id="b1469-162">Se usarán para completar la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b1469-162">These will be used to complete the asynchronous operation.</span></span>

### <a name="automatic-acquisition"></a><span data-ttu-id="b1469-163">Adquisición automática</span><span class="sxs-lookup"><span data-stu-id="b1469-163">Automatic Acquisition</span></span>

<span data-ttu-id="b1469-164">Para realizar la adquisición automática, llame a [**IMFContentEnabler:: AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable).</span><span class="sxs-lookup"><span data-stu-id="b1469-164">To perform automatic acquisition, call [**IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable).</span></span> <span data-ttu-id="b1469-165">Este método es asincrónico.</span><span class="sxs-lookup"><span data-stu-id="b1469-165">This method is asynchronous.</span></span> <span data-ttu-id="b1469-166">Una vez completada la operación, el habilitador de contenido envía un evento [MEEnablerCompleted](meenablercompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="b1469-166">When the operation is completed, the content enabler sends an [MEEnablerCompleted](meenablercompleted.md) event.</span></span> <span data-ttu-id="b1469-167">El código de estado del evento indica si la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b1469-167">The event's status code indicates whether the operation was successful.</span></span> <span data-ttu-id="b1469-168">Si el código de estado del evento MEEnablerCompleted es NS \_ E \_ DRM \_ License \_ NOTACQUIRED, la aplicación debe intentar usar la adquisición no silenciosa.</span><span class="sxs-lookup"><span data-stu-id="b1469-168">If the status code from the MEEnablerCompleted event is NS\_E\_DRM\_LICENSE\_NOTACQUIRED, the application should try using non-silent acquisition.</span></span>

<span data-ttu-id="b1469-169">Mientras la operación de adquisición está en curso, el objeto Enabler podría enviar el evento [MEEnablerProgress](meenablerprogress.md) para indicar el progreso de la operación.</span><span class="sxs-lookup"><span data-stu-id="b1469-169">While the acquisition operation is in progress, the enabler object might send the [MEEnablerProgress](meenablerprogress.md) event to indicate the progress of the operation.</span></span> <span data-ttu-id="b1469-170">Para cancelar la operación, llame a [**IMFContentEnabler:: CANCEL**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-cancel).</span><span class="sxs-lookup"><span data-stu-id="b1469-170">To cancel the operation, call [**IMFContentEnabler::Cancel**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-cancel).</span></span>

### <a name="non-silent-acquisition"></a><span data-ttu-id="b1469-171">Adquisición no silenciosa</span><span class="sxs-lookup"><span data-stu-id="b1469-171">Non-Silent Acquisition</span></span>

<span data-ttu-id="b1469-172">Si el método [**IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported) devuelve **false** o se produce un error en el método [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) con el código de error NS \_ E \_ DRM \_ License \_ NOTACQUIRED, la aplicación debe realizar una adquisición no silenciosa como se describe en los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b1469-172">If the [**IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported) method returns **FALSE** or the [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) method fails with the error code NS\_E\_DRM\_LICENSE\_NOTACQUIRED, the application should perform non-silent acquisition as described in the following steps:</span></span>

1.  <span data-ttu-id="b1469-173">Llame a [**IMFContentEnabler:: GetEnableURL**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenableurl) para obtener la dirección URL de la adquisición de derechos.</span><span class="sxs-lookup"><span data-stu-id="b1469-173">Call [**IMFContentEnabler::GetEnableURL**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenableurl) to get the URL for the rights acquisition.</span></span> <span data-ttu-id="b1469-174">Este método también devuelve una marca que indica si la dirección URL es de confianza.</span><span class="sxs-lookup"><span data-stu-id="b1469-174">This method also returns a flag indicating whether the URL is trusted.</span></span>
2.  <span data-ttu-id="b1469-175">Llame a [**IMFContentEnabler:: GetEnableData**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabledata) para obtener los datos http post.</span><span class="sxs-lookup"><span data-stu-id="b1469-175">Call [**IMFContentEnabler::GetEnableData**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabledata) to get the HTTP POST data.</span></span>
3.  <span data-ttu-id="b1469-176">Llame a [**IMFContentEnabler:: MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable).</span><span class="sxs-lookup"><span data-stu-id="b1469-176">Call [**IMFContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable).</span></span> <span data-ttu-id="b1469-177">Este método hace que el habilitador de contenido supervise el progreso de la acción de adquisición de derechos.</span><span class="sxs-lookup"><span data-stu-id="b1469-177">This method causes the content enabler to monitor the progress of the rights acquisition action.</span></span>

4.  <span data-ttu-id="b1469-178">Envíe los datos a la dirección URL de adquisición de derechos mediante una acción HTTP POST.</span><span class="sxs-lookup"><span data-stu-id="b1469-178">Submit the data to the rights acquisition URL by using an HTTP POST action.</span></span> <span data-ttu-id="b1469-179">Puede usar el control de Internet Explorer o las API de Windows Internet (WinINet).</span><span class="sxs-lookup"><span data-stu-id="b1469-179">You can use the Internet Explorer control or the Windows Internet (WinINet) APIs.</span></span>

<span data-ttu-id="b1469-180">En el código siguiente se muestran los pasos 1 a 3.</span><span class="sxs-lookup"><span data-stu-id="b1469-180">The following code shows steps 1–3.</span></span> <span data-ttu-id="b1469-181">El paso 4 depende de los requisitos específicos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1469-181">Step 4 depends on your application's particular requirements.</span></span>


```C++
WCHAR   *sURL = NULL;  // URL.
DWORD   cchURL = 0;    // Size of the URL in characters.

// Trust status of the URL.
MF_URL_TRUST_STATUS  trustStatus = MF_LICENSE_URL_UNTRUSTED;

BYTE    *pPostData = NULL;  // Buffer to hold HTTP POST data.
DWORD   cbPostDataSize = 0; // Size of the buffer, in bytes.

HRESULT hr = S_OK;

// Get the URL. 
hr = m_pEnabler->GetEnableURL(&sURL, &cchURL, &trustStatus);

if (SUCCEEDED(hr))
{
    if (trustStatus != MF_LICENSE_URL_TRUSTED)
    {
        // The URL is not trusted. Do not proceed.
        hr = E_FAIL;
    }
}

// Monitor the rights acquisition. 
if (SUCCEEDED(hr))
{
    hr = m_pEnabler->MonitorEnable();
}

// Get the HTTP POST data.
if (SUCCEEDED(hr))
{
    hr = m_pEnabler->GetEnableData(&pPostData, &cbPostDataSize);
}

// Open the URL and send the HTTP POST data. (Not shown.)

// Release the buffers.
CoTaskMemFree(pPostData);
CoTaskMemFree(sURL);
```



<span data-ttu-id="b1469-182">Una vez completada la operación, el habilitador de contenido envía un evento [MEEnablerCompleted](meenablercompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="b1469-182">When the operation is completed, the content enabler sends an [MEEnablerCompleted](meenablercompleted.md) event.</span></span>

## <a name="complete-the-asynchronous-operation"></a><span data-ttu-id="b1469-183">Completar la operación asincrónica</span><span class="sxs-lookup"><span data-stu-id="b1469-183">Complete the Asynchronous Operation</span></span>

<span data-ttu-id="b1469-184">Una vez completada la adquisición de derechos, o de lo contrario, la aplicación debe notificar la sesión de medios mediante la invocación del puntero de devolución de llamada proporcionado en el método [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) .</span><span class="sxs-lookup"><span data-stu-id="b1469-184">When the rights acquisition is completed, successfully or otherwise, the application must notify the Media Session, by invoking the callback pointer given in the [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) method.</span></span>

1.  <span data-ttu-id="b1469-185">Cree un objeto de resultado asincrónico llamando a [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult).</span><span class="sxs-lookup"><span data-stu-id="b1469-185">Create an asynchronous result object by calling [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult).</span></span>
2.  <span data-ttu-id="b1469-186">Invocar la devolución de llamada de la sesión multimedia llamando a [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).</span><span class="sxs-lookup"><span data-stu-id="b1469-186">Invoke the Media Session's callback by calling [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).</span></span>
3.  <span data-ttu-id="b1469-187">La sesión multimedia llamará a [**IMFContentProtectionManager:: EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent).</span><span class="sxs-lookup"><span data-stu-id="b1469-187">The Media Session will call [**IMFContentProtectionManager::EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent).</span></span> <span data-ttu-id="b1469-188">En la implementación de este método, libere cualquier puntero o recurso que haya asignado dentro de [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent).</span><span class="sxs-lookup"><span data-stu-id="b1469-188">In your implementation of this method, release any pointers or resources that you allocated inside [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent).</span></span> <span data-ttu-id="b1469-189">Devuelve un **valor HRESULT** que indica el éxito global de la operación.</span><span class="sxs-lookup"><span data-stu-id="b1469-189">Return an **HRESULT** that indicates the overall success of the operation.</span></span> <span data-ttu-id="b1469-190">Si se produce un error en la adquisición de derechos o el usuario canceló antes de que se completara, devuelva un código de error.</span><span class="sxs-lookup"><span data-stu-id="b1469-190">If the rights acquisition failed or the user canceled before it was completed, return an error code.</span></span>

<span data-ttu-id="b1469-191">En el código siguiente se muestra cómo crear el resultado asincrónico e invocar la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b1469-191">The following code shows how to create the asynchronous result and invoke the callback.</span></span>


```C++
IMFAsyncResult  *pResult = NULL;

// Create the asynchronous result object.
hr = MFCreateAsyncResult(NULL, pCallback, punkState, &pResult);

// Invoke the callback.
if (SUCCEEDED(hr))
{
    pResult->SetStatus(hrStatus);
    hr = MFInvokeCallback(pResult);
}
SAFE_RELEASE(pResult);
```



## <a name="related-topics"></a><span data-ttu-id="b1469-192">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b1469-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1469-193">Sesión de medios</span><span class="sxs-lookup"><span data-stu-id="b1469-193">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="b1469-194">Reproducción de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="b1469-194">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



