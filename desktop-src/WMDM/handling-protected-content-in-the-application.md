---
title: Control del contenido protegido en la aplicación
description: Control del contenido protegido en la aplicación
ms.assetid: b59d4abc-e59d-47a7-8d91-825ac20ae2eb
keywords:
- Windows Media Administrador de dispositivos, certificados
- Administrador de dispositivos, certificados
- Guía de programación, certificados
- aplicaciones de escritorio, certificados
- crear aplicaciones de Windows Media Administrador de dispositivos, certificados
- certificates
- Windows Media Administrador de dispositivos, contenido protegido con DRM
- Administrador de dispositivos, contenido protegido con DRM
- Guía de programación, contenido protegido con DRM
- aplicaciones de escritorio, contenido protegido con DRM
- creación de aplicaciones de Windows Media Administrador de dispositivos, contenido protegido con DRM
- Contenido protegido con DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc354e78b9c937db339f5bf6a167f504986fbb64
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695701"
---
# <a name="handling-protected-content-in-the-application"></a><span data-ttu-id="73997-115">Control del contenido protegido en la aplicación</span><span class="sxs-lookup"><span data-stu-id="73997-115">Handling Protected Content in the Application</span></span>

<span data-ttu-id="73997-116">\[La característica Windows Media DRM está en desuso y no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="73997-116">\[The Windows Media DRM feature is deprecated and should not be used.</span></span> <span data-ttu-id="73997-117">En su lugar, use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]</span><span class="sxs-lookup"><span data-stu-id="73997-117">Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) instead.\]</span></span>

<span data-ttu-id="73997-118">Una aplicación debe tener un certificado de transferencia para poder controlar el contenido protegido con DRM.</span><span class="sxs-lookup"><span data-stu-id="73997-118">An application must have a transfer certificate to be able to handle DRM-protected content.</span></span> <span data-ttu-id="73997-119">Para obtener información sobre dónde obtener este certificado, vea [herramientas para el desarrollo](tools-for-development.md).</span><span class="sxs-lookup"><span data-stu-id="73997-119">To learn where to get this certificate, see [Tools for Development](tools-for-development.md).</span></span> <span data-ttu-id="73997-120">Para controlar el contenido no protegido, puede usar un certificado ficticio tal y como se describe en [autenticación de la aplicación](authenticating-the-application.md).</span><span class="sxs-lookup"><span data-stu-id="73997-120">For handling unprotected content, you can use a dummy certificate as described in [Authenticating the Application](authenticating-the-application.md).</span></span>

<span data-ttu-id="73997-121">Antes de usar un dispositivo, la aplicación debe determinar si el dispositivo es compatible con Windows Media DRM 10 para dispositivos portátiles y, en caso afirmativo, que los componentes de DRM estén actualizados.</span><span class="sxs-lookup"><span data-stu-id="73997-121">Before using a device, your application should determine whether the device supports Windows Media DRM 10 for Portable Devices, and if so, that the DRM components are current.</span></span> <span data-ttu-id="73997-122">(Actual significa que el reloj seguro es correcto y que el dispositivo se ha individualizado correctamente). Si el dispositivo no es compatible con esta versión de DRM, o si no se puede actualizar, todavía puede enviar archivos al dispositivo, pero es posible que no se puedan reproducir, dependiendo de la versión de licencia.</span><span class="sxs-lookup"><span data-stu-id="73997-122">(Current means that the secure clock is correct and that the device has been properly individualized.) If the device does not support this version of DRM, or if it cannot be updated, you can still send files to the device, but they might not be playable, depending on the license version.</span></span>

> [!Note]  
> <span data-ttu-id="73997-123">Actualmente no se admite la individualización de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="73997-123">Individualization of devices is not currently supported.</span></span>

 

<span data-ttu-id="73997-124">Si la aplicación va a vincularse a los métodos del SDK de Windows Media Format, deberá vincular a la biblioteca de formato de Windows Media WMStubDRM. lib.</span><span class="sxs-lookup"><span data-stu-id="73997-124">If your application will link to Windows Media Format SDK methods, it will need to link to the Windows Media Format library WMStubDRM.lib.</span></span> <span data-ttu-id="73997-125">Para obtener más información sobre cómo llamar a los métodos de formato de Windows Media en contenido protegido con DRM, vea "habilitar la compatibilidad con DRM" en la documentación del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="73997-125">For more information on calling Windows Media Format methods on DRM-protected content, see "Enabling DRM Support" in the Windows Media Format SDK documentation.</span></span> <span data-ttu-id="73997-126">Tenga en cuenta que hay un problema con la vinculación a Mssachlp. lib y WMStubDRM. lib.</span><span class="sxs-lookup"><span data-stu-id="73997-126">Note that there is a problem with linking to both Mssachlp.lib and WMStubDRM.lib.</span></span> <span data-ttu-id="73997-127">Esto se trata en el [artículo 890079 de Knowledge base en MSDN](https://support.microsoft.com/default.aspx?scid=kb;en-us;890079).</span><span class="sxs-lookup"><span data-stu-id="73997-127">This is covered in [KB article 890079 on MSDN](https://support.microsoft.com/default.aspx?scid=kb;en-us;890079).</span></span>

<span data-ttu-id="73997-128">En el siguiente ejemplo de código de C++ se determina si un dispositivo es un dispositivo DRM 10 de Windows Media y, en caso afirmativo, que su reloj está actualizado.</span><span class="sxs-lookup"><span data-stu-id="73997-128">The following C++ code example determines whether a device is a Windows Media DRM 10 device and, if so, that its clock is up to date.</span></span>

`HRESULT IsDRMClockUpToDate()`


```C++
{
    HRESULT hr = S_OK;

    // Create the DRM handler class.
    CComPtr<IWMDRMDeviceApp> pDRM;
    hr = pDRM.CoCreateInstance(CLSID_WMDRMDeviceApp, 0, CLSCTX_ALL);

    // Find out first if the device is a WMDRM 10 device, and if so,
    // whether it requires clock updates.
    DWORD status = 0;
    hr = pDRM->QueryDeviceStatus(pDevice, &status);

    if (FAILED(hr)
       || (!(WMDRM_DEVICE_ISWMDRM & status)) // Device is not WMDRM 10. 
       || (status & WMDRM_DEVICE_REVOKED))   // Device is revoked.
    {
        return E_FAIL;
    }
    else if (status & WMDRM_DEVICE_NEEDCLOCK || 
        status & WMDRM_DEVICE_REFRESHCLOCK)
    {
        // Attempt update. See following example.
        hr = UpdateDRM(status);
    }
    return hr;
}
```



<span data-ttu-id="73997-129">Si el dispositivo es compatible con Windows Media DRM 10 para dispositivos portátiles y debe actualizarse (es decir, si el valor de *status* en el ejemplo anterior no es simplemente \_ dispositivo WMDM \_ ISWMDRM), la aplicación debe llamar a [**IWMDRMDeviceApp:: AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) y pasar el valor de *status* para realizar las actualizaciones necesarias.</span><span class="sxs-lookup"><span data-stu-id="73997-129">If the device does support Windows Media DRM 10 for Portable Devices, and needs to be updated (that is, if the value of *status* in the previous example is not simply WMDM\_DEVICE\_ISWMDRM), the application should call [**IWMDRMDeviceApp::AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) and pass in the value of *status* to perform the required updates.</span></span> <span data-ttu-id="73997-130">El equipo de escritorio debe estar conectado a Internet.</span><span class="sxs-lookup"><span data-stu-id="73997-130">The desktop computer must be connected to the Internet.</span></span>

<span data-ttu-id="73997-131">La siguiente función de ejemplo de C++ intenta actualizar un dispositivo DRM.</span><span class="sxs-lookup"><span data-stu-id="73997-131">The following C++ example function attempts to update a DRM device.</span></span>


```C++
HRESULT UpdateDRM(DWORD status)
{
    HRESULT hr = S_OK;
    hr = pDRM->AcquireDeviceData(pDevice, this, status, &result);
    if (hr != S_OK || result != 0)
    {
            return E_FAIL;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="73997-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="73997-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73997-133">**Crear una aplicación de Windows Media Administrador de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="73997-133">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[<span data-ttu-id="73997-134">**Control de contenido protegido**</span><span class="sxs-lookup"><span data-stu-id="73997-134">**Handling Protected Content**</span></span>](handling-protected-content.md)
</dt> </dl>

 

 