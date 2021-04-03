---
title: Adquisición de licencias silenciosa
description: Adquisición de licencias silenciosa
ms.assetid: bf88f1bb-0cbb-4c30-92e0-3d342977d67f
keywords:
- SDK de Windows Media Format, adquisición de licencias silenciosa
- SDK de Windows Media Format, licencias
- Administración de derechos digitales (DRM), adquisición de licencias silenciosa
- DRM (administración de derechos digitales), adquisición de licencias silenciosa
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- API extendidas del cliente DRM, adquisición de licencias silenciosa
- API extendidas de cliente, adquisición de licencias silenciosa
- adquisición de licencias silenciosa
- licencias, adquisición de licencias silenciosa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ef92eaf4e347e8eb30f56c1111ec5b27f1e62d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076010"
---
# <a name="silent-license-acquisition"></a><span data-ttu-id="3cd18-113">Adquisición de licencias silenciosa</span><span class="sxs-lookup"><span data-stu-id="3cd18-113">Silent License Acquisition</span></span>

<span data-ttu-id="3cd18-114">La adquisición de licencias silenciosa solo requiere una única llamada de método que controle todas las comunicaciones de red con el servidor de licencias de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="3cd18-114">Silent license acquisition requires only a single method call that handles all of the network communications with the license server asynchronously.</span></span>

<span data-ttu-id="3cd18-115">Este tipo de adquisición de licencias se usa normalmente como respuesta al usuario final que intenta tener acceso al contenido protegido, por ejemplo, intentando reproducir un archivo protegido en una aplicación del reproductor de media.</span><span class="sxs-lookup"><span data-stu-id="3cd18-115">This type of license acquisition is usually used as a response to the end user trying to access protected content—for example, trying to play a protected file in a media player application.</span></span> <span data-ttu-id="3cd18-116">Dado que la adquisición de licencia silenciosa obtiene la licencia con una sola llamada, no se puede usar si se requiere una entrada adicional del usuario, como el pago del contenido.</span><span class="sxs-lookup"><span data-stu-id="3cd18-116">Because silent license acquisition gets the license with a single call, it cannot be used if additional input from the user, such as payment for the content, is required.</span></span>

<span data-ttu-id="3cd18-117">Para realizar una adquisición de licencias silenciosa, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="3cd18-117">To perform silent license acquisition, use the following steps:</span></span>

1.  <span data-ttu-id="3cd18-118">Llame al método [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="3cd18-118">Call the [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) method.</span></span> <span data-ttu-id="3cd18-119">Pase el encabezado DRM del archivo protegido como el parámetro *bstrHeaderData* .</span><span class="sxs-lookup"><span data-stu-id="3cd18-119">Pass in the DRM header from the protected file as the *bstrHeaderData* parameter.</span></span> <span data-ttu-id="3cd18-120">Especifique los derechos que desea conceder a la licencia en el parámetro *bstrActions* .</span><span class="sxs-lookup"><span data-stu-id="3cd18-120">Specify what rights you want the license to grant in the *bstrActions* parameter.</span></span> <span data-ttu-id="3cd18-121">Por último, establezca el parámetro *dwFlags* en la licencia de adquisición de WMDRM en \_ \_ \_ modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="3cd18-121">Finally, set the *dwFlags* parameter to WMDRM\_ACQUIRE\_LICENSE\_SILENT.</span></span>
2.  <span data-ttu-id="3cd18-122">Eventos de captura para la interfaz [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) .</span><span class="sxs-lookup"><span data-stu-id="3cd18-122">Trap events for the [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) interface.</span></span> <span data-ttu-id="3cd18-123">Cuando reciba el evento **MEWMDRMLicenseAcquisitionCompleted** , compruebe su código de retorno llamando al método **IMFMediaEvent:: getStatus** , que se documenta en la documentación de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="3cd18-123">When you receive the **MEWMDRMLicenseAcquisitionCompleted** event, check its return code by calling the **IMFMediaEvent::GetStatus** method, which is documented in the Media Foundation documentation.</span></span> <span data-ttu-id="3cd18-124">Si el valor **HRESULT** recuperado es un código de éxito, la licencia se descargó correctamente y está en el almacén de licencias local listo para su uso.</span><span class="sxs-lookup"><span data-stu-id="3cd18-124">If the retrieved **HRESULT** value is a success code, then the license was successfully downloaded and is in the local license store ready for use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3cd18-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3cd18-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cd18-126">**Adquisición de licencias**</span><span class="sxs-lookup"><span data-stu-id="3cd18-126">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="3cd18-127">**Usar el modelo de eventos Media Foundation**</span><span class="sxs-lookup"><span data-stu-id="3cd18-127">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> </dl>

 

 




