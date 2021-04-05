---
title: Revocación y renovación de componentes automatizados
description: Revocación y renovación de componentes automatizados
ms.assetid: be4899d7-1d87-4450-8c0e-75cf112ca66a
keywords:
- SDK de Windows Media Format, revocación automatizada y renovación
- SDK de Windows Media Format, revocación
- SDK de Windows Media Format, renovación
- Administración de derechos digitales (DRM), revocación automatizada y renovación
- DRM (administración de derechos digitales), revocación automatizada y renovación
- Administración de derechos digitales (DRM), revocación
- DRM (administración de derechos digitales), revocación
- Administración de derechos digitales (DRM), renovación
- DRM (administración de derechos digitales), renovación
- API extendidas del cliente DRM, revocación automatizada y renovación
- API extendidas de cliente, revocación automatizada y renovación
- API extendidas del cliente DRM, revocación
- API extendidas de cliente, revocación
- API extendidas del cliente DRM, renovación
- API extendidas de cliente, renovación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9046d04d8ca7a138a06cba4d26cd82bc5a12b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359262"
---
# <a name="automated-component-revocation-and-renewal"></a><span data-ttu-id="12adb-118">Revocación y renovación de componentes automatizados</span><span class="sxs-lookup"><span data-stu-id="12adb-118">Automated Component Revocation and Renewal</span></span>

<span data-ttu-id="12adb-119">Microsoft puede revocar las aplicaciones o los componentes de software considerados en peligro.</span><span class="sxs-lookup"><span data-stu-id="12adb-119">Software applications or components that are considered compromised can be revoked by Microsoft.</span></span> <span data-ttu-id="12adb-120">La API extendida cliente de Windows Media Format proporciona un mecanismo para la revocación automatizada y la renovación de componentes.</span><span class="sxs-lookup"><span data-stu-id="12adb-120">The Windows Media Format Client Extended API provides a mechanism for the automated revocation and renewal of components.</span></span>

<span data-ttu-id="12adb-121">Los componentes revocados se enumeran en una lista de revocación de certificados, publicada por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="12adb-121">Revoked components are listed in a certificate revocation list, which is published by Microsoft.</span></span> <span data-ttu-id="12adb-122">Cuando se revoca un componente, su certificado se agrega a la lista de revocación de certificados y se actualiza el BLOB de información de revocación ( \_ información de revisión) en los servidores de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="12adb-122">When a component is revoked, its certificate is added to the certificate revocation list, and the revocation information BLOB (REV\_INFO) is updated on the Microsoft servers.</span></span>

<span data-ttu-id="12adb-123">Para realizar la revocación y renovación automatizadas cuando un usuario intenta procesar contenido protegido con DRM de Windows Media, la aplicación debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="12adb-123">To perform automated revocation and renewal when a user attempts to process Windows Media DRM protected content, your application must do the following:</span></span>

1.  <span data-ttu-id="12adb-124">Extraiga la \_ versión de la información de Rev de la licencia.</span><span class="sxs-lookup"><span data-stu-id="12adb-124">Extract the REV\_INFO version from the license.</span></span> <span data-ttu-id="12adb-125">El número de versión de la información de REV \_ se encuentra en la siguiente ubicación en una licencia de XMR:</span><span class="sxs-lookup"><span data-stu-id="12adb-125">The REV\_INFO version number is located in the following location in an XMR license:</span></span>
    ```C++
    <LICENSE version="2.0.0.0">
        <LICENSORINFO/>
        <DATA>
            <LID>...</LID>
            <KID>...</KID>
            <RevInfoVersion>42</RevInfoVersion>
            ...
         </DATA>
    ....
    </LICENSE>
    ```

    

2.  <span data-ttu-id="12adb-126">Compare el \_ número de versión de la información de revisión de la licencia con el \_ número de versión de la información de revisión en el almacén local llamando al método [**IWMDRMSecurity:: GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md) .</span><span class="sxs-lookup"><span data-stu-id="12adb-126">Compare the REV\_INFO version number of the license with the REV\_INFO version number in the local store by calling the [**IWMDRMSecurity::GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md) method.</span></span>
3.  <span data-ttu-id="12adb-127">Si la versión de la información de REV \_ no está actualizada, llame al método [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) , pasando la \_ \_ \_ \_ marca de actualización de revocación de la ejecución de WMDRM Security en el parámetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="12adb-127">If the REV\_INFO version is not up to date, call the [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) method, passing the WMDRM\_SECURITY\_PERFORM\_REVOCATION\_REFRESH flag in the *dwFlags* parameter.</span></span>
4.  <span data-ttu-id="12adb-128">Recupere la lista de revocación de certificados del almacén local llamando al método [**IWMDRMSecurity:: GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) .</span><span class="sxs-lookup"><span data-stu-id="12adb-128">Retrieve the certificate revocation list from the local store by calling the [**IWMDRMSecurity::GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) method.</span></span>
5.  <span data-ttu-id="12adb-129">Analice la lista de revocación y compruebe si hay revocación de DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="12adb-129">Parse the revocation list, and check for Windows Media DRM revocations.</span></span> <span data-ttu-id="12adb-130">Para obtener más información, consulte Comprobación de la [revocación de certificados](checking-certificate-revocation.md).</span><span class="sxs-lookup"><span data-stu-id="12adb-130">For more information, see [Checking Certificate Revocation](checking-certificate-revocation.md).</span></span>
6.  <span data-ttu-id="12adb-131">Si hay alguna revocación de DRM de Windows Media:</span><span class="sxs-lookup"><span data-stu-id="12adb-131">If there are any Windows Media DRM revocations:</span></span>
    1.  <span data-ttu-id="12adb-132">Cree un habilitador de contenido para renovar los componentes revocados llamando al método [**IWMDRMSecurity:: GetContentEnablersForRevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) .</span><span class="sxs-lookup"><span data-stu-id="12adb-132">Create a content enabler to renew the revoked components by calling the [**IWMDRMSecurity::GetContentEnablersForRevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) method.</span></span>
    2.  <span data-ttu-id="12adb-133">Llame a **IMFContentEnabler:: AutomaticEnable** , que dirige al usuario a una dirección URL que contiene información sobre la renovación de componentes.</span><span class="sxs-lookup"><span data-stu-id="12adb-133">Call **IMFContentEnabler::AutomaticEnable** which directs the user to a URL that contains component renewal information.</span></span> <span data-ttu-id="12adb-134">Este método se documenta en el [SDK de Media Foundation](../medfound/microsoft-media-foundation-sdk.md) ( https://msdn.microsoft.com/library/ms694197(VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="12adb-134">This method is documented in the [Media Foundation SDK](../medfound/microsoft-media-foundation-sdk.md) (https://msdn.microsoft.com/library/ms694197(VS.85).aspx).</span></span>
        > [!Note]  
        > <span data-ttu-id="12adb-135">Debe aclarar este proceso al usuario mediante el uso de una declaración de privacidad, ya que el proceso de actualización envía información desde el equipo cliente a un sitio web de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="12adb-135">You must clarify this process to the user through the use of a privacy statement because the update process sends information from the client computer to a Microsoft Web site.</span></span>

         

    3.  <span data-ttu-id="12adb-136">Si es posible, el usuario renovará el componente desde la dirección URL, ya sea de forma automática o mediante instrucciones específicas.</span><span class="sxs-lookup"><span data-stu-id="12adb-136">If possible, the user will renew the component from the URL, either automatically or by following specific instructions.</span></span> <span data-ttu-id="12adb-137">Habrá algunas situaciones en las que el componente no se puede renovar.</span><span class="sxs-lookup"><span data-stu-id="12adb-137">There will be some situations in which the component cannot be renewed.</span></span>
    4.  <span data-ttu-id="12adb-138">Intente obtener acceso al contenido de nuevo hasta que no haya más revocación o se detenga el proceso por alguna razón.</span><span class="sxs-lookup"><span data-stu-id="12adb-138">Try to access the content again until there are no more revocations, or the process is halted for some reason.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12adb-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="12adb-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12adb-140">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="12adb-140">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 