---
title: Control de eventos de adquisición de licencias
description: Control de eventos de adquisición de licencias
ms.assetid: e118bf09-1fa6-41b6-a6bb-3e8cb6097994
keywords:
- SDK de Windows Media Format, control de eventos de adquisición de licencias
- SDK de Windows Media Format, eventos de adquisición de licencias
- Advanced Systems Format (ASF), control de eventos de adquisición de licencias
- ASF (Advanced Systems Format), control de eventos de adquisición de licencias
- Advanced Systems Format (ASF), eventos de adquisición de licencias
- ASF (formato de sistemas avanzados), eventos de adquisición de licencias
- Administración de derechos digitales (DRM), control de eventos de adquisición de licencias
- DRM (administración de derechos digitales), control de eventos de adquisición de licencias
- Administración de derechos digitales (DRM), eventos de adquisición de licencias
- DRM (administración de derechos digitales), eventos de adquisición de licencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e31fd5b108f41d5b0925918fdf1c83764bcf7e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420277"
---
# <a name="handling-license-acquisition-events"></a><span data-ttu-id="1eab4-113">Control de eventos de adquisición de licencias</span><span class="sxs-lookup"><span data-stu-id="1eab4-113">Handling License Acquisition Events</span></span>

<span data-ttu-id="1eab4-114">Una aplicación de lector habilitada para DRM, en su método de devolución de llamada [**IWMStatusCallback::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) en el estado, controla los cuatro eventos siguientes relacionados con el proceso de adquisición de licencias:</span><span class="sxs-lookup"><span data-stu-id="1eab4-114">A DRM-enabled reader application, in its [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method, handles the following four events related to the license acquisition process:</span></span>

-   <span data-ttu-id="1eab4-115">**\_Estado de \_ firma de LICENSEURL de WMT \_**</span><span class="sxs-lookup"><span data-stu-id="1eab4-115">**WMT\_LICENSEURL\_SIGNATURE\_STATE**</span></span>
-   <span data-ttu-id="1eab4-116">**\_sin \_ derechos de WMT**</span><span class="sxs-lookup"><span data-stu-id="1eab4-116">**WMT\_NO\_RIGHTS**</span></span>
-   <span data-ttu-id="1eab4-117">**\_no hay \_ derechos de WMT \_ ex**</span><span class="sxs-lookup"><span data-stu-id="1eab4-117">**WMT\_NO\_RIGHTS\_EX**</span></span>
-   <span data-ttu-id="1eab4-118">**\_licencia de adquisición de WMT \_**</span><span class="sxs-lookup"><span data-stu-id="1eab4-118">**WMT\_ACQUIRE\_LICENSE**</span></span>

<span data-ttu-id="1eab4-119">**\_Estado de \_ firma de LICENSEURL de WMT \_**</span><span class="sxs-lookup"><span data-stu-id="1eab4-119">**WMT\_LICENSEURL\_SIGNATURE\_STATE**</span></span>

<span data-ttu-id="1eab4-120">Cuando el componente DRM detecta contenido protegido por la versión 7 de DRM, primero busca una licencia válida en el sistema local.</span><span class="sxs-lookup"><span data-stu-id="1eab4-120">When the DRM component detects content protected by DRM version 7, it first looks for a valid license on the local system.</span></span> <span data-ttu-id="1eab4-121">Si no existe ninguno, evalúa la dirección URL de adquisición de licencias en el encabezado DRM del archivo y envía un evento de **\_ \_ \_ Estado de firma WMT LICENSEURL** con *pValue* establecido en uno de los valores de [**\_ \_ confianza de DRMLA WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust) , que indica si la dirección URL es de confianza, no es de confianza o se ha alterado.</span><span class="sxs-lookup"><span data-stu-id="1eab4-121">If none exists, it then evaluates the license acquisition URL in the file's DRM header and sends a **WMT\_LICENSEURL\_SIGNATURE\_STATE** event with *pValue* set to one of the [**WMT\_DRMLA\_TRUST**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust) values, indicating whether the URL is trusted, untrusted, or has been tampered with.</span></span> <span data-ttu-id="1eab4-122">Si la dirección URL no es de confianza, la aplicación debe advertir al usuario.</span><span class="sxs-lookup"><span data-stu-id="1eab4-122">If the URL is not trusted, then the application should warn the user.</span></span> <span data-ttu-id="1eab4-123">Si la dirección URL se ha alterado, el archivo debe considerarse dañado y la aplicación no debe navegar hasta la dirección URL sin emitir una advertencia segura al usuario.</span><span class="sxs-lookup"><span data-stu-id="1eab4-123">If the URL has been tampered with, then the file should be considered corrupted, and the application should not navigate to the URL without issuing a strong warning the user.</span></span>

<span data-ttu-id="1eab4-124">**\_sin \_ derechos de WMT**</span><span class="sxs-lookup"><span data-stu-id="1eab4-124">**WMT\_NO\_RIGHTS**</span></span>

<span data-ttu-id="1eab4-125">El evento **WMT \_ no \_ Rights** solo se envía para el contenido de la versión 1 de DRM, lo que significa que la licencia debe adquirirse de forma no silenciosa.</span><span class="sxs-lookup"><span data-stu-id="1eab4-125">The **WMT\_NO\_RIGHTS** event is sent only for DRM version 1 content, which means that the license must be acquired non-silently.</span></span> <span data-ttu-id="1eab4-126">En otras palabras, el usuario debe ir a una página web para adquirir una licencia.</span><span class="sxs-lookup"><span data-stu-id="1eab4-126">In other words, the user must navigate to a Web page to acquire a license.</span></span> <span data-ttu-id="1eab4-127">La dirección URL de la página se recupera como una cadena terminada en NULL de caracteres anchos del parámetro *pValue* en el método de **Estado** .</span><span class="sxs-lookup"><span data-stu-id="1eab4-127">The URL for the page is retrieved as a wide-character null-terminated string from the *pValue* parameter in the **OnStatus** method.</span></span>

<span data-ttu-id="1eab4-128">Si es necesario, una aplicación puede facilitar al usuario navegar a la página web, ya sea abriendo Internet Explorer en un proceso independiente o bien hospedando el control del explorador Web.</span><span class="sxs-lookup"><span data-stu-id="1eab4-128">If appropriate, an application can make it easier for the user to navigate to the Web page, either by opening up Internet Explorer in a separate process or else by hosting the Web Browser control.</span></span> <span data-ttu-id="1eab4-129">Sin embargo, esto no es necesario.</span><span class="sxs-lookup"><span data-stu-id="1eab4-129">This is not required, however.</span></span> <span data-ttu-id="1eab4-130">Como mínimo, una aplicación podría mostrar simplemente la dirección URL del usuario en un cuadro de mensaje y pedirles que la peguen en la barra de direcciones de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="1eab4-130">At the very least, an application could simply display the URL to the user in a message box and prompt them to paste it into the address bar of Internet Explorer.</span></span> <span data-ttu-id="1eab4-131">En el ejemplo AudioPlayer se muestra el control adecuado del evento **WMT \_ no \_ Rights** , incluido cómo dar formato a la cadena de dirección URL y cómo usar el método **CreateProcess** para abrir Internet Explorer y navegar a la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="1eab4-131">The Audioplayer sample demonstrates proper handling of the **WMT\_NO\_RIGHTS** event, including how to format the URL string, and how to use the **CreateProcess** method to open Internet Explorer and navigate to the specified URL.</span></span>

<span data-ttu-id="1eab4-132">Dado que la aplicación no tiene ninguna manera de saber cuándo se ha adquirido una licencia de DRM versión 1, es el usuario quien intenta volver a abrir el archivo después de adquirir la licencia.</span><span class="sxs-lookup"><span data-stu-id="1eab4-132">Because the application has no way of knowing when a DRM version 1 license has been acquired, it is up to the user to attempt to open the file again after acquiring the license.</span></span>

<span data-ttu-id="1eab4-133">Este mismo proceso de adquisición de licencias no silenciosa también puede usarse para las licencias de la versión 7, pero en este caso la aplicación puede llamar primero a [**IWMDRMReader:: MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition).</span><span class="sxs-lookup"><span data-stu-id="1eab4-133">This same non-silent license acquisition process can also be used for version 7 licenses, but in this case the application can first call [**IWMDRMReader::MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition).</span></span> <span data-ttu-id="1eab4-134">Este método hará que el almacén de licencias local se compruebe repetidamente hasta que se encuentre la licencia del nuevo archivo.</span><span class="sxs-lookup"><span data-stu-id="1eab4-134">This method will cause the local license store to be checked repeatedly until the license for the new file is found.</span></span> <span data-ttu-id="1eab4-135">En ese momento, la aplicación recibirá un evento de **\_ \_ licencia de adquisición de WMT** .</span><span class="sxs-lookup"><span data-stu-id="1eab4-135">At that point, the application will receive a **WMT\_ACQUIRE\_LICENSE** event.</span></span> <span data-ttu-id="1eab4-136">Para todas las licencias de la versión 7, se recomienda que las aplicaciones ofrezcan a los usuarios la opción de obtener licencias de forma silenciosa o no silenciosa.</span><span class="sxs-lookup"><span data-stu-id="1eab4-136">For all version 7 licenses, it is recommended that applications give users the option to obtain licenses silently or non-silently.</span></span>

<span data-ttu-id="1eab4-137">**\_no hay \_ derechos de WMT \_ ex**</span><span class="sxs-lookup"><span data-stu-id="1eab4-137">**WMT\_NO\_RIGHTS\_EX**</span></span>

<span data-ttu-id="1eab4-138">El evento **WMT \_ no \_ Rights \_ ex** indica que el contenido está protegido por la versión 7 de DRM y, por lo tanto, el proceso de adquisición de licencias puede continuar de forma silenciosa o no silenciosa.</span><span class="sxs-lookup"><span data-stu-id="1eab4-138">The **WMT\_NO\_RIGHTS\_EX** event indicates that the content is protected by DRM version 7, and therefore the license acquisition process can proceed either silently or non-silently.</span></span> <span data-ttu-id="1eab4-139">En general, la adquisición silenciosa de licencias es más cómoda para los usuarios finales, aunque algunas personas prefieren adquirir todas las licencias de forma no silenciosa.</span><span class="sxs-lookup"><span data-stu-id="1eab4-139">In general, silent license acquisition is more convenient for end users, although some people prefer to acquire all licenses non-silently.</span></span> <span data-ttu-id="1eab4-140">Cuando la adquisición de licencias requiere que el usuario envíe información personal o de pago, el proceso siempre debe realizarse de forma no silenciosa.</span><span class="sxs-lookup"><span data-stu-id="1eab4-140">When license acquisition requires the user to submit payment or personal information, the process should always be performed non-silently.</span></span> <span data-ttu-id="1eab4-141">La adquisición de licencias no silenciosas se ha descrito anteriormente en el encabezado **WMT \_ no \_ Rights** .</span><span class="sxs-lookup"><span data-stu-id="1eab4-141">Non-silent license acquisition is described above under the **WMT\_NO\_RIGHTS** heading.</span></span> <span data-ttu-id="1eab4-142">La adquisición silenciosa continúa como sigue:</span><span class="sxs-lookup"><span data-stu-id="1eab4-142">Silent acquisition proceeds as follows:</span></span>

1.  <span data-ttu-id="1eab4-143">Convierta el parámetro *pValue* a una estructura de [**datos de licencia de WM \_ Get \_ \_**](wm-get-license-data.md) y almacene la estructura en caso de que sea necesaria más adelante para la adquisición de licencias no silenciosa.</span><span class="sxs-lookup"><span data-stu-id="1eab4-143">Cast the *pValue* parameter to a [**WM\_GET\_LICENSE\_DATA**](wm-get-license-data.md) structure and store the structure in case it is needed later for non-silent license acquisition.</span></span>
2.  <span data-ttu-id="1eab4-144">Llame a **QueryInterface** en el objeto Reader para obtener la interfaz [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) .</span><span class="sxs-lookup"><span data-stu-id="1eab4-144">Call **QueryInterface** on the reader object to obtain the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface.</span></span>
3.  <span data-ttu-id="1eab4-145">Llame a [**IWMDRMReader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) y especifique 0x1 en el parámetro *dwFlags* para indicar la adquisición del lenguaje silencioso.</span><span class="sxs-lookup"><span data-stu-id="1eab4-145">Call [**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) and specify 0x1 in the *dwFlags* parameter to indicate silent language acquisition.</span></span> <span data-ttu-id="1eab4-146">Se trata de una llamada asincrónica que se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="1eab4-146">This is an asynchronous call that returns immediately.</span></span>
4.  <span data-ttu-id="1eab4-147">Espere al evento **de \_ \_ licencia de adquisición de WMT** .</span><span class="sxs-lookup"><span data-stu-id="1eab4-147">Wait for the **WMT\_ACQUIRE\_LICENSE** event.</span></span>

<span data-ttu-id="1eab4-148">**\_licencia de adquisición de WMT \_**</span><span class="sxs-lookup"><span data-stu-id="1eab4-148">**WMT\_ACQUIRE\_LICENSE**</span></span>

<span data-ttu-id="1eab4-149">El evento de **\_ \_ licencia de adquisición de WMT** se envía una vez completado el proceso de adquisición de licencias para una licencia de DRM versión 7.</span><span class="sxs-lookup"><span data-stu-id="1eab4-149">The **WMT\_ACQUIRE\_LICENSE** event is sent after the license acquisition process is completed for a DRM version 7 license.</span></span> <span data-ttu-id="1eab4-150">[**IWMDRMReader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) hace que este evento se envíe para la adquisición silenciosa, y [**MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition) hace que se envíe para la adquisición no silenciosa.</span><span class="sxs-lookup"><span data-stu-id="1eab4-150">[**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) causes this event to be sent for silent acquisition, and [**MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition) causes it to be sent for non-silent acquisition.</span></span> <span data-ttu-id="1eab4-151">En el controlador de eventos, convierta *pValue* en un puntero a una estructura de datos de licencia de Get de WM y examine el miembro de **recursos humanos** para determinar si la licencia se adquirió correctamente. [**\_ \_ \_**](wm-get-license-data.md)</span><span class="sxs-lookup"><span data-stu-id="1eab4-151">In your event handler, cast *pValue* to a pointer to a [**WM\_GET\_LICENSE\_DATA**](wm-get-license-data.md) structure and examine the **hr** member to determine whether the license was successfully acquired.</span></span> <span data-ttu-id="1eab4-152">Si **HR** es igual \_ a E DRM de NS E \_ \_ no tiene \_ derechos, indica que la licencia debe adquirirse de forma no silenciosa.</span><span class="sxs-lookup"><span data-stu-id="1eab4-152">If **hr** equals NS\_E\_DRM\_NO\_RIGHTS, it indicates that the license must be acquired non-silently.</span></span> <span data-ttu-id="1eab4-153">Las aplicaciones deben permitir que los usuarios cancelen el proceso de adquisición de licencias en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="1eab4-153">Applications should enable users to cancel the license acquisition process at any time.</span></span> <span data-ttu-id="1eab4-154">Esto se hace mediante una llamada a [**IWMDRMReader:: CancelLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancellicenseacquisition).</span><span class="sxs-lookup"><span data-stu-id="1eab4-154">This is done by calling [**IWMDRMReader::CancelLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancellicenseacquisition).</span></span> <span data-ttu-id="1eab4-155">Al llamar a este método, se enviará un evento de **\_ \_ licencia de adquisición WMT** con un valor **HRESULT** de la \_ adquisición de DRM S de NS \_ \_ \_ cancelada.</span><span class="sxs-lookup"><span data-stu-id="1eab4-155">Calling this method will send a **WMT\_ACQUIRE\_LICENSE** event with an **HRESULT** value of NS\_S\_DRM\_ACQUIRE\_CANCELLED.</span></span>

<span data-ttu-id="1eab4-156">Si **HR** es igual \_ a NS S \_ DRM \_ License \_ adquirida, se ha adquirido la licencia y la aplicación puede intentar reproducir el archivo o copiarlo en un dispositivo o realizar la acción para la que tenía derechos solicitados.</span><span class="sxs-lookup"><span data-stu-id="1eab4-156">If **hr** equals NS\_S\_DRM\_LICENSE\_ACQUIRED, then the license has been acquired and the application can attempt to play the file, or copy it to a device or perform whatever action it had requested rights for.</span></span>

<span data-ttu-id="1eab4-157">En Windows XP, se presentó un nuevo código de error: NS \_ E \_ DRM \_ License \_ NOTACQUIRED.</span><span class="sxs-lookup"><span data-stu-id="1eab4-157">On Windows XP, a new error code was introduced: NS\_E\_DRM\_LICENSE\_NOTACQUIRED.</span></span> <span data-ttu-id="1eab4-158">Este código de error se genera cuando los componentes en tiempo de ejecución de Windows Media Format en Windows XP no pueden adquirir una licencia durante la adquisición de licencias silenciosa o no silenciosa.</span><span class="sxs-lookup"><span data-stu-id="1eab4-158">This error code is generated whenever the Windows Media Format run-time components on Windows XP fail to acquire a license during silent or non-silent license acquisition.</span></span> <span data-ttu-id="1eab4-159">En otras plataformas, el \_ \_ error del almacén de licencias de DRM E DRM \_ \_ \_ se devuelve normalmente cuando se produce un error en la adquisición de licencias.</span><span class="sxs-lookup"><span data-stu-id="1eab4-159">On other platforms, NS\_E\_DRM\_LICENSE\_STORE\_ERROR is usually returned when license acquisition fails.</span></span> <span data-ttu-id="1eab4-160">El nuevo código de error se ha diseñado para distinguir los errores de adquisición de licencias de otras condiciones de error en las que \_ \_ se genera un error de almacén de licencias de DRM E DRM \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1eab4-160">The new error code is intended to distinguish license acquisition failure from other failure conditions where NS\_E\_DRM\_LICENSE\_STORE\_ERROR is generated.</span></span>

<span data-ttu-id="1eab4-161">La manera recomendada de controlar estos errores cuando se devuelven después de un intento de adquisición de licencias silenciosa se muestra en el siguiente fragmento de código:</span><span class="sxs-lookup"><span data-stu-id="1eab4-161">The recommended way to handle these errors when they are returned after a silent license acquisition attempt is shown in the following code snippet:</span></span>


```C++
if( hrStatus == NS_E_DRM_LICENSE_NOTACQUIRED || 
    hrStatus == NS_E_DRM_LICENSE_STORE_ERROR )
{
  // Attempt non-silent license acquisition.
}
else if( hrStatus == NS_E_DRM_NEEDS_INDIVIDUALIZATION )
{
  // Individualize and then retry.
}
else if( FAILED(hrStatus) )
{
  // Display a helpful error message.
}
else
{
  // Success. Play content.
}
```



> [!Note]  
> <span data-ttu-id="1eab4-162">DRM no es compatible con la versión basada en x64 de este SDK.</span><span class="sxs-lookup"><span data-stu-id="1eab4-162">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1eab4-163">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1eab4-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1eab4-164">**Leer archivos protegidos**</span><span class="sxs-lookup"><span data-stu-id="1eab4-164">**Reading Protected Files**</span></span>](reading-protected-files.md)
</dt> </dl>

 

 




