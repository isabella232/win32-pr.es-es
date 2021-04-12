---
title: Registrar una devolución de llamada COM
description: En lugar de sondear los cambios en el estado de un trabajo, puede registrarse para recibir notificaciones cuando el estado del trabajo cambie.
ms.assetid: 29350ea4-f7a9-4a42-a531-2cf623fe247b
keywords:
- transferir BITS de trabajo, notificación de eventos
- registro para BITS de notificación de eventos
- BITS de notificación de eventos
- BITS de notificación de eventos, devoluciones de llamada
- BITS de eventos de notificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdcc52c772656c2168af9c10724ee43fac25aa80
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359160"
---
# <a name="registering-a-com-callback"></a><span data-ttu-id="1f056-108">Registrar una devolución de llamada COM</span><span class="sxs-lookup"><span data-stu-id="1f056-108">Registering a COM Callback</span></span>

<span data-ttu-id="1f056-109">En lugar de [sondear](polling-for-the-status-of-the-job.md) los cambios en el estado de un trabajo, puede registrarse para recibir notificaciones cuando el estado del trabajo cambie.</span><span class="sxs-lookup"><span data-stu-id="1f056-109">Instead of [polling](polling-for-the-status-of-the-job.md) for changes in the status of a job, you can register to receive notification when the job's status changes.</span></span> <span data-ttu-id="1f056-110">Para recibir la notificación, debe implementar la interfaz [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) .</span><span class="sxs-lookup"><span data-stu-id="1f056-110">To receive notification, you must implement the [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) interface.</span></span> <span data-ttu-id="1f056-111">La interfaz contiene los métodos siguientes que llama a BITS, en función del registro:</span><span class="sxs-lookup"><span data-stu-id="1f056-111">The interface contains the following methods that BITS calls, depending on your registration:</span></span>

-   [<span data-ttu-id="1f056-112">**JobTransferred**</span><span class="sxs-lookup"><span data-stu-id="1f056-112">**JobTransferred**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred)
-   [<span data-ttu-id="1f056-113">**JobError**</span><span class="sxs-lookup"><span data-stu-id="1f056-113">**JobError**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-joberror)
-   [<span data-ttu-id="1f056-114">**JobModification**</span><span class="sxs-lookup"><span data-stu-id="1f056-114">**JobModification**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobmodification)
-   [<span data-ttu-id="1f056-115">**FileTransferred**</span><span class="sxs-lookup"><span data-stu-id="1f056-115">**FileTransferred**</span></span>](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred)

<span data-ttu-id="1f056-116">Para obtener un ejemplo que implementa la interfaz [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) , vea el ejemplo de código en el tema de la interfaz [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .</span><span class="sxs-lookup"><span data-stu-id="1f056-116">For an example that implements the [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) interface, see the example code in the [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) interface topic.</span></span>

<span data-ttu-id="1f056-117">La interfaz [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) proporciona una notificación cuando se transfiere un archivo.</span><span class="sxs-lookup"><span data-stu-id="1f056-117">The [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) interface provides notification when a file is transferred.</span></span> <span data-ttu-id="1f056-118">Normalmente, este método se usa para validar el archivo, de modo que el archivo esté disponible para que los elementos del mismo nivel lo descarguen. de lo contrario, el archivo no estará disponible para los elementos del mismo nivel hasta que se llame al método [**IBackgroundCopyJob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) .</span><span class="sxs-lookup"><span data-stu-id="1f056-118">Typically, you use this method to validate the file, so that the file is available for peers to download; otherwise, the file is not available to peers until you call the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="1f056-119">Para validar el archivo, llame al método [**IBackgroundCopyFile3:: SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) .</span><span class="sxs-lookup"><span data-stu-id="1f056-119">To validate the file, call the [**IBackgroundCopyFile3::SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) method.</span></span>

<span data-ttu-id="1f056-120">Hay dos métodos para registrar una devolución de llamada COM: registrar un objeto de devolución de llamada o registrar un identificador de clase de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="1f056-120">There are two methods for registering a COM callback: registering a callback object, or registering a callback class ID.</span></span> <span data-ttu-id="1f056-121">El uso de un objeto de devolución de llamada es más sencillo y reduce la sobrecarga; el uso de un CLSID de devolución de llamada es más confiable, pero más complicado.</span><span class="sxs-lookup"><span data-stu-id="1f056-121">Using a callback object is simpler and lower overhead; using a callback CLSID is more reliable, but more complicated.</span></span> <span data-ttu-id="1f056-122">Puede registrar, ambos o ninguno: BITS usará un objeto de devolución de llamada si existe y todavía se puede llamar a, y volverá a crear instancias de un nuevo objeto basándose en un identificador de clase proporcionado si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="1f056-122">You can register either, both, or neither – BITS will use a callback object if one exists and can still be called, and will fall back to instantiating a new object based on a provided class ID if that fails.</span></span>

### <a name="registering-a-callback-object"></a><span data-ttu-id="1f056-123">Registrar un objeto de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="1f056-123">Registering a Callback Object</span></span>

<span data-ttu-id="1f056-124">Para registrar la implementación con BITS, llame al método [**IBackgroundCopyJob:: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) .</span><span class="sxs-lookup"><span data-stu-id="1f056-124">To register your implementation with BITS, call the [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) method.</span></span> <span data-ttu-id="1f056-125">Para especificar qué métodos llama a BITS, llame al método [**IBackgroundCopyJob:: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags).</span><span class="sxs-lookup"><span data-stu-id="1f056-125">To specify which methods BITS calls, call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)method.</span></span>

<span data-ttu-id="1f056-126">La interfaz de notificación deja de ser válida cuando finaliza la aplicación; BITS no conserva la interfaz de notificación.</span><span class="sxs-lookup"><span data-stu-id="1f056-126">The notification interface becomes invalid when your application terminates; BITS does not persist the notify interface.</span></span> <span data-ttu-id="1f056-127">Como resultado, el proceso de inicialización de la aplicación debe registrar los trabajos existentes para los que desea recibir la notificación.</span><span class="sxs-lookup"><span data-stu-id="1f056-127">As a result, your application's initialization process should register existing jobs for which you want to receive notification.</span></span> <span data-ttu-id="1f056-128">Si necesita capturar información sobre el estado y el progreso que se produjeron desde la última vez que se ejecutó la aplicación, sondee la información sobre el estado y el progreso durante la inicialización de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1f056-128">If you need to capture state and progress information that occurred since the last time your application was run, poll for state and progress information during application initialization.</span></span>

<span data-ttu-id="1f056-129">Antes de salir, la aplicación debe borrar el puntero de la interfaz de devolución de llamada (**SetNotifyInterface (NULL)**).</span><span class="sxs-lookup"><span data-stu-id="1f056-129">Before exiting, your application should clear the callback interface pointer (**SetNotifyInterface(NULL)**).</span></span> <span data-ttu-id="1f056-130">Es más eficaz borrar el puntero de devolución de llamada que para permitir que los BITS detecten que ya no es válido.</span><span class="sxs-lookup"><span data-stu-id="1f056-130">It is more efficient to clear the callback pointer than to let BITS discover that it is no longer valid.</span></span>

<span data-ttu-id="1f056-131">Tenga en cuenta que si más de una aplicación llama al método [**SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) para establecer la interfaz de notificación para el trabajo, la última aplicación que llama al método **SetNotifyInterface** es la que recibirá notificaciones; las demás aplicaciones no recibirán notificaciones.</span><span class="sxs-lookup"><span data-stu-id="1f056-131">Note that if more than one application calls the [**SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) method to set the notification interface for the job, the last application to call the **SetNotifyInterface** method is the one that will receive notifications—the other applications will not receive notifications.</span></span>

<span data-ttu-id="1f056-132">En el ejemplo siguiente se muestra cómo registrar las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="1f056-132">The following example shows how to register for notifications.</span></span> <span data-ttu-id="1f056-133">En el ejemplo se da por supuesto que el puntero de la interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) es válido.</span><span class="sxs-lookup"><span data-stu-id="1f056-133">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span> <span data-ttu-id="1f056-134">Para obtener más información sobre la clase de ejemplo CNotifyInterface que se usa en el ejemplo siguiente, vea la interfaz [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .</span><span class="sxs-lookup"><span data-stu-id="1f056-134">For details on the CNotifyInterface example class used in the following example, see the [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) interface.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
CNotifyInterface *pNotify = new CNotifyInterface();

if (pNotify)
{
    hr = pJob->SetNotifyInterface(pNotify);
    if (SUCCEEDED(hr))
    {
        hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
                                  BG_NOTIFY_JOB_ERROR );
    }
    pNotify->Release();
    pNotify = NULL;

    if (FAILED(hr))
    {
        //Handle error - unable to register callbacks.
    }
}
```



### <a name="registering-a-callback-clsid"></a><span data-ttu-id="1f056-135">Registrar un CLSID de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="1f056-135">Registering a Callback CLSID</span></span>

<span data-ttu-id="1f056-136">Para registrar un CLSID de devolución de llamada con BITS, llame al método [**IBackgroundCopyJob5:: SetProperty**](/windows/desktop/api/Bits5_0/nf-bits5_0-ibackgroundcopyjob5-setproperty) con el CLSID de notificación de la **\_ propiedad del trabajo de \_ \_ \_ bits** .</span><span class="sxs-lookup"><span data-stu-id="1f056-136">To register a callback CLSID with BITS, call the [**IBackgroundCopyJob5::SetProperty**](/windows/desktop/api/Bits5_0/nf-bits5_0-ibackgroundcopyjob5-setproperty) method with the **BITS\_JOB\_PROPERTY\_NOTIFICATION\_CLSID** PropertyId.</span></span> <span data-ttu-id="1f056-137">Para especificar qué métodos llama a BITS, llame al método [**IBackgroundCopyJob:: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) .</span><span class="sxs-lookup"><span data-stu-id="1f056-137">To specify which methods BITS calls, call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) method.</span></span>

<span data-ttu-id="1f056-138">Debe asegurarse de que el CLSID de notificación está registrado en un servidor COM fuera de proceso antes de registrar el CLSID con un trabajo de BITS.</span><span class="sxs-lookup"><span data-stu-id="1f056-138">You must ensure that the notification CLSID is registered to an out-of-process COM server prior to registering the CLSID with a BITS job.</span></span> <span data-ttu-id="1f056-139">La implementación de un [servidor com](/windows/desktop/com/com-server-responsibilities) es significativamente más complicada que definir y pasar un objeto de devolución de llamada, pero ofrece varias ventajas importantes.</span><span class="sxs-lookup"><span data-stu-id="1f056-139">Implementing a [COM server](/windows/desktop/com/com-server-responsibilities) is significantly more complicated than defining and passing a callback object, but offers several important advantages.</span></span> <span data-ttu-id="1f056-140">Un servidor COM permite que los BITS mantengan la asociación entre un trabajo de BITS y el código de la aplicación a través de reinicios del sistema, y para trabajos grandes o de larga duración.</span><span class="sxs-lookup"><span data-stu-id="1f056-140">A COM server allows BITS to maintain the association between a BITS job and your application’s code across system reboots, and for large or long-lived jobs.</span></span> <span data-ttu-id="1f056-141">Un servidor COM también permite que la aplicación se cierre completamente mientras BITS sigue ejecutando transferencias en segundo plano, lo que puede mejorar el uso de la batería, la CPU y la memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="1f056-141">A COM server also allows your application to shut down completely while BITS continues executing transfers in the background, which can improve battery, CPU, and memory usage of the system.</span></span>

<span data-ttu-id="1f056-142">Para proporcionar una notificación que se ha registrado para recibir, BITS primero intenta llamar al método correspondiente de cualquier objeto de devolución de llamada existente que se haya adjuntado.</span><span class="sxs-lookup"><span data-stu-id="1f056-142">To provide a notification you have registered to receive, BITS first attempts to call the corresponding method of any existing callback object you may have attached.</span></span> <span data-ttu-id="1f056-143">Si no hay ningún objeto existente, o si ese objeto existente se ha desconectado (normalmente, como resultado de la finalización de la aplicación), BITS llamará a CoCreateInstance mediante el CLSID de notificación para crear una instancia de un nuevo objeto de devolución de llamada y usará ese objeto para todas las devoluciones de llamada posteriores hasta que se desconecte o se reemplace por una nueva llamada a [**IBackgroundCopyJob:**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface)</span><span class="sxs-lookup"><span data-stu-id="1f056-143">If there is no existing object, or if that existing object has become disconnected (typically as a result of your application terminating), BITS will call CoCreateInstance using the notification CLSID to instantiate a new callback object, and will use that object for any further callbacks until it becomes disconnected or it is replaced by a new call to [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface).</span></span>

<span data-ttu-id="1f056-144">A diferencia de los objetos de devolución de llamada, el CLSID de devolución de llamada se conserva junto con sus trabajos de BITS correspondientes si el servicio BITS o el sistema se cierran y se reinician.</span><span class="sxs-lookup"><span data-stu-id="1f056-144">Unlike callback objects, callback CLSID are persisted alongside their corresponding BITS job(s) if the BITS service or the system are shut down and restarted.</span></span> <span data-ttu-id="1f056-145">La aplicación puede borrar cualquier CLSID de notificación de conjunto anterior antes de salir (o en cualquier otro momento) pasando un nuevo CLSID de notificación de GUID \_ null, pero es posible que la aplicación prefiera dejar el CLSID de notificación registrado si la aplicación se ha registrado para que com lo inicie en respuesta a las solicitudes de CoCreateInstance para su CLSID.</span><span class="sxs-lookup"><span data-stu-id="1f056-145">Your application may clear any previously-set notification CLSID before exiting (or at any other time) by passing a new notification CLSID of GUID\_NULL, but your application may prefer to leave the notification CLSID registered if your application has registered to have COM start it in response to CoCreateInstance requests for your CLSID.</span></span> <span data-ttu-id="1f056-146">Tenga en cuenta que si más de una aplicación establece la **propiedad \_ \_ CLSID de \_ notificación \_** de la propiedad del trabajo de bits, el último CLSID que se establecerá es el que bits usará para crear instancias de los objetos de devolución de llamada; no se crearán instancias de los otros CLSID.</span><span class="sxs-lookup"><span data-stu-id="1f056-146">Note that if more than one application sets the calls the **BITS\_JOB\_PROPERTY\_NOTIFICATION\_CLSID** property, the last CLSID to be set is the one that BITS will use to instantiate callback objects – the other CLSIDs will not be instantiated.</span></span> <span data-ttu-id="1f056-147">Del mismo modo, si una aplicación registra un CLSID y otro registra un objeto de devolución de llamada, se aplican las reglas habituales para el objeto de devolución de llamada, y el CLSID no se utilizará a menos que el objeto de devolución de llamada se borre o se desconecte.</span><span class="sxs-lookup"><span data-stu-id="1f056-147">Similarly, if one application registers a CLSID and another registers a callback object, the usual rules for the callback object taking precedence apply, and the CLSID will not be used unless the callback object is cleared or becomes disconnected.</span></span>

<span data-ttu-id="1f056-148">En el ejemplo siguiente se muestra cómo registrar las notificaciones CLSID.</span><span class="sxs-lookup"><span data-stu-id="1f056-148">The following example shows how to register for CLSID notifications.</span></span> <span data-ttu-id="1f056-149">En el ejemplo se da por supuesto que el puntero de la interfaz [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) es válido y que la aplicación ya se ha registrado como un servidor com fuera de proceso que implementa la clase CNotifyInterface.</span><span class="sxs-lookup"><span data-stu-id="1f056-149">The example assumes the [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) interface pointer is valid, and that your application has already registered as an out-of-process COM Server which implements the CNotifyInterface class.</span></span> <span data-ttu-id="1f056-150">Para obtener más información sobre la clase de ejemplo CNotifyInterface que se usa en el ejemplo siguiente, vea la interfaz [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .</span><span class="sxs-lookup"><span data-stu-id="1f056-150">For details on the CNotifyInterface example class used in the following example, see the [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) interface.</span></span>


```C++
HRESULT hr; 
IBackgroundCopyJob5* job; 
BITS_JOB_PROPERTY_VALUE propertyValue; 
propertyValue.ClsID = __uuidof(CNotifyInterface); 

hr = job->SetProperty(BITS_JOB_PROPERTY_NOTIFICATION_CLSID, propertyValue); 
if (SUCCEEDED(hr)) 
{ 
    hr = job->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED |  
                             BG_NOTIFY_JOB_ERROR); 
} 

if (FAILED(hr)) 
{ 
    // Handle error - unable to register callbacks. 
} 
```



 

 