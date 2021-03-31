---
title: Adquisición de licencias no silenciosa
description: Adquisición de licencias no silenciosa
ms.assetid: 3b3fce53-9202-4e55-82d5-7c70ea833087
keywords:
- SDK de Windows Media Format, adquisición de licencias no silenciosas
- SDK de Windows Media Format, licencias
- Administración de derechos digitales (DRM), adquisición de licencias no silenciosas
- DRM (administración de derechos digitales), adquisición de licencias no silenciosas
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- API extendidas del cliente DRM, adquisición de licencias no silenciosas
- API extendidas de cliente, adquisición de licencias no silenciosas
- adquisición de licencias no silenciosa
- licencias, adquisición de licencias no silenciosas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb8d7c4865e74fd5ce383cff8317de905828afe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532440"
---
# <a name="non-silent-license-acquisition"></a><span data-ttu-id="8af3f-113">Adquisición de licencias no silenciosa</span><span class="sxs-lookup"><span data-stu-id="8af3f-113">Non-Silent License Acquisition</span></span>

<span data-ttu-id="8af3f-114">La adquisición de licencias no silenciosa permite al proveedor de licencias interactuar con el usuario final a través de una página web, como un paso intermedio en el proceso de adquisición de licencias.</span><span class="sxs-lookup"><span data-stu-id="8af3f-114">Non-silent license acquisition enables the license provider to interact with the end user through a Web page, as an intermediate step in the license acquisition process.</span></span> <span data-ttu-id="8af3f-115">La adquisición de licencias no silenciosas se inicia en respuesta a un usuario que intenta tener acceso a contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="8af3f-115">Non-silent license acquisition is initiated in response to a user trying to access protected content.</span></span>

<span data-ttu-id="8af3f-116">Para realizar una adquisición de licencias no silenciosa, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="8af3f-116">To perform non-silent license acquisition, use the following steps:</span></span>

1.  <span data-ttu-id="8af3f-117">Llame al método [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="8af3f-117">Call the [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) method.</span></span> <span data-ttu-id="8af3f-118">Pase el encabezado DRM del archivo protegido como el parámetro *bstrHeaderData* .</span><span class="sxs-lookup"><span data-stu-id="8af3f-118">Pass in the DRM header from the protected file as the *bstrHeaderData* parameter.</span></span> <span data-ttu-id="8af3f-119">Especifique los derechos que desea conceder a la licencia en el parámetro *bstrActions* .</span><span class="sxs-lookup"><span data-stu-id="8af3f-119">Specify what rights you want the license to grant in the *bstrActions* parameter.</span></span> <span data-ttu-id="8af3f-120">Por último, establezca el parámetro *dwFlags* en la licencia de adquisición de WMDRM no es \_ \_ \_ silenciosa.</span><span class="sxs-lookup"><span data-stu-id="8af3f-120">Finally, set the *dwFlags* parameter to WMDRM\_ACQUIRE\_LICENSE\_NONSILENT.</span></span>
2.  <span data-ttu-id="8af3f-121">Eventos de captura para la interfaz **IWMDRMLicenseManagement** .</span><span class="sxs-lookup"><span data-stu-id="8af3f-121">Trap events for the **IWMDRMLicenseManagement** interface.</span></span> <span data-ttu-id="8af3f-122">Cuando reciba el evento **MEWMDRMLicenseAcquisitionCompleted** , obtenga su valor asociado llamando a **IMFMediaEvent:: GetValue**.</span><span class="sxs-lookup"><span data-stu-id="8af3f-122">When you receive the **MEWMDRMLicenseAcquisitionCompleted** event, get its associated value by calling **IMFMediaEvent::GetValue**.</span></span> <span data-ttu-id="8af3f-123">El valor debe ser de tipo VT \_ Unknown, un puntero a una interfaz **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="8af3f-123">The value should be of type VT\_UNKNOWN, a pointer to an **IUnknown** interface.</span></span>
3.  <span data-ttu-id="8af3f-124">Llame al método **QueryInterface** de la interfaz **IUnknown** recuperada en el paso 2 para obtener la interfaz [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) .</span><span class="sxs-lookup"><span data-stu-id="8af3f-124">Call the **QueryInterface** method of the **IUnknown** interface retrieved in step 2 to get the [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) interface.</span></span>
4.  <span data-ttu-id="8af3f-125">Llame a [**IWMDRMNonSilentLicenseAquisition:: GetChallenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) para recuperar el desafío de licencia.</span><span class="sxs-lookup"><span data-stu-id="8af3f-125">Call [**IWMDRMNonSilentLicenseAquisition::GetChallenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) to retrieve the license challenge.</span></span> <span data-ttu-id="8af3f-126">También debe llamar a [**IWMDRMNonSilentLicenseAquisition:: getURL**](iwmdrmnonsilentlicenseaquisition-geturl.md) si ya no tiene la dirección URL del servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="8af3f-126">Also call [**IWMDRMNonSilentLicenseAquisition::GetURL**](iwmdrmnonsilentlicenseaquisition-geturl.md) if you do not have the URL of the license server already.</span></span>
5.  <span data-ttu-id="8af3f-127">Envíe el desafío a la Página Web especificada por la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="8af3f-127">Send the challenge to the Web page specified by the URL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8af3f-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8af3f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8af3f-129">**Adquisición de licencias**</span><span class="sxs-lookup"><span data-stu-id="8af3f-129">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="8af3f-130">**Usar el modelo de eventos Media Foundation**</span><span class="sxs-lookup"><span data-stu-id="8af3f-130">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> </dl>

 

 




