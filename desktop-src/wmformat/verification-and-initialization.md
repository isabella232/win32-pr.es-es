---
title: Comprobación e inicialización
description: Comprobación e inicialización
ms.assetid: e92abaa2-0bac-4c78-bda7-d118c4f5b332
keywords:
- Windows Media Format SDK, comprobación
- SDK de Windows Media Format, inicialización
- Administración de derechos digitales (DRM), comprobación
- DRM (administración de derechos digitales), comprobación
- Administración de derechos digitales (DRM), inicialización
- DRM (administración de derechos digitales), inicialización
- API extendidas del cliente DRM, comprobación
- API extendidas del cliente, comprobación
- API extendidas del cliente DRM, inicialización
- API extendidas de cliente, inicialización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59c54b56e0622fb65a1a57ae1909e0e6e64aaca6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358698"
---
# <a name="verification-and-initialization"></a><span data-ttu-id="342d4-113">Comprobación e inicialización</span><span class="sxs-lookup"><span data-stu-id="342d4-113">Verification and Initialization</span></span>

<span data-ttu-id="342d4-114">Debe realizar los pasos siguientes para comprobar que se permite el descifrado e inicializar un objeto que descifrará el contenido:</span><span class="sxs-lookup"><span data-stu-id="342d4-114">You should perform the following steps to verify that transcryption is allowed and to initialize an object that will decrypt the content:</span></span>

1.  <span data-ttu-id="342d4-115">Si ya tiene el identificador de clave para el contenido, vaya al paso 5.</span><span class="sxs-lookup"><span data-stu-id="342d4-115">If you already have the Key ID for the content, skip to step 5.</span></span>
2.  <span data-ttu-id="342d4-116">Llame a la función [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor) para crear un objeto de editor de metadatos y obtener una instancia de la interfaz [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor) de ese objeto.</span><span class="sxs-lookup"><span data-stu-id="342d4-116">Call the [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor) function to create a metadata editor object and get an instance of that object's [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor) interface.</span></span>
3.  <span data-ttu-id="342d4-117">Llame a **IWMMetadataEditor:: QueryInterface** para obtener una instancia de la interfaz [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) .</span><span class="sxs-lookup"><span data-stu-id="342d4-117">Call **IWMMetadataEditor::QueryInterface** to get an instance of the [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) interface.</span></span>
4.  <span data-ttu-id="342d4-118">Llame a [**IWMDRMEditor:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) para obtener la propiedad de ID. de la **\_ DRMHeader \_ de DRM** .</span><span class="sxs-lookup"><span data-stu-id="342d4-118">Call [**IWMDRMEditor::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) to get the **DRM\_DRMHeader\_KeyID** property.</span></span>
5.  <span data-ttu-id="342d4-119">Inicialice las API extendidas del cliente DRM de Windows Media mediante una llamada a la función [**WMDRMStartup**](wmdrmstartup.md) .</span><span class="sxs-lookup"><span data-stu-id="342d4-119">Initialize the Windows Media DRM Client Extended APIs by calling the [**WMDRMStartup**](wmdrmstartup.md) function.</span></span>
6.  <span data-ttu-id="342d4-120">Llame a la función [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) para crear un objeto de proveedor seguro y obtener una instancia de la interfaz [**IWMDRMProvider**](iwmdrmprovider.md) de ese objeto.</span><span class="sxs-lookup"><span data-stu-id="342d4-120">Call the [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) function to create a secure provider object and get an instance of that object's [**IWMDRMProvider**](iwmdrmprovider.md) interface.</span></span>
7.  <span data-ttu-id="342d4-121">Llame a [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md) para crear un objeto de administración de licencias y obtener una instancia de su interfaz [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) .</span><span class="sxs-lookup"><span data-stu-id="342d4-121">Call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md) to create a license management object and get an instance of its [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) interface.</span></span>
8.  <span data-ttu-id="342d4-122">Llame a [**IWMDRMLicenseManagement:: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), pasando el identificador de clave y el derecho que rige las acciones que se van a llevar a cabo con el contenido después de que se haya transcifrado.</span><span class="sxs-lookup"><span data-stu-id="342d4-122">Call [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), passing in the Key ID and the right that governs the actions to be taken with the content after it is transcrypted.</span></span> <span data-ttu-id="342d4-123">Esta llamada recuperará una instancia de la interfaz [**IWMDRMLicense**](iwmdrmlicense.md) que se puede usar para enumerar a través de las licencias coincidentes.</span><span class="sxs-lookup"><span data-stu-id="342d4-123">This call will retrieve an instance of the [**IWMDRMLicense**](iwmdrmlicense.md) interface that can be used to enumerate through any matching licenses.</span></span>
9.  <span data-ttu-id="342d4-124">Llame a [**IWMDRMLicense:: GetInclusionList**](iwmdrmlicense-getinclusionlist.md) para recuperar la lista de sistemas de protección de contenido (CPS) autorizados según lo especificado por el emisor de la licencia.</span><span class="sxs-lookup"><span data-stu-id="342d4-124">Call [**IWMDRMLicense::GetInclusionList**](iwmdrmlicense-getinclusionlist.md) to retrieve the list of authorized content protection systems (CPS) as specified by the license issuer.</span></span>
10. <span data-ttu-id="342d4-125">Analice la lista de inclusión para confirmar que la licencia permite el GUID de la CPS de salida.</span><span class="sxs-lookup"><span data-stu-id="342d4-125">Parse the inclusion list to confirm that the GUID of the output CPS is allowed by the license.</span></span>
11. <span data-ttu-id="342d4-126">Si el GUID de exportación deseado no está en la lista de inclusión, llame a [**IWMDRMLicense:: Getnext**](iwmdrmlicense-getnext.md) para obtener la siguiente licencia aplicable (si existe) y repita los pasos 9 y 10.</span><span class="sxs-lookup"><span data-stu-id="342d4-126">If the desired export GUID is not in the inclusion list, call [**IWMDRMLicense::GetNext**](iwmdrmlicense-getnext.md) to get the next applicable license (if any) and repeat steps 9 and 10.</span></span> <span data-ttu-id="342d4-127">Si ninguna licencia tiene el GUID deseado en su lista de inclusión, no se puede realizar la exportación.</span><span class="sxs-lookup"><span data-stu-id="342d4-127">If no license has the desired GUID in its inclusion list, the export cannot be performed.</span></span>
12. <span data-ttu-id="342d4-128">Llame a [**IWMDRMLicense:: CreateSecureDecryptor**](iwmdrmlicense-createsecuredecryptor.md) para crear un objeto descifrador.</span><span class="sxs-lookup"><span data-stu-id="342d4-128">Call [**IWMDRMLicense::CreateSecureDecryptor**](iwmdrmlicense-createsecuredecryptor.md) to create a decryptor object.</span></span> <span data-ttu-id="342d4-129">Pase el certificado de la aplicación de exportación.</span><span class="sxs-lookup"><span data-stu-id="342d4-129">Pass in the export application certificate.</span></span> <span data-ttu-id="342d4-130">Esta llamada proporcionará un puntero a una instancia de la interfaz [**IWMDRMDecrypt**](iwmdrmdecrypt.md) del objeto descifrador y un objeto binario que contiene el valor de inicialización.</span><span class="sxs-lookup"><span data-stu-id="342d4-130">This call will provide a pointer to an instance of the decryptor object's [**IWMDRMDecrypt**](iwmdrmdecrypt.md) interface and a binary object containing the seed.</span></span> <span data-ttu-id="342d4-131">En este momento solo se admite la constante **RC4 del \_ tipo de protección \_ \_ DRM** de Windows Media como argumento para el parámetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="342d4-131">Only the Windows Media **DRM\_PROTECTION\_TYPE\_RC4** constant is supported as an argument to the *dwFlags* parameter at this time.</span></span>
13. <span data-ttu-id="342d4-132">Use el esquema de cifrado RSA OAEP para descifrar el vector de inicialización.</span><span class="sxs-lookup"><span data-stu-id="342d4-132">Use the RSA OAEP encryption scheme to decrypt the initialization vector.</span></span>
14. <span data-ttu-id="342d4-133">Use la biblioteca de análisis de ASF proporcionada por Microsoft al entrar en el contrato de exportación de DRM de Windows Media para buscar el desplazamiento en bytes para cada carga.</span><span class="sxs-lookup"><span data-stu-id="342d4-133">Use the ASF parsing library provided by Microsoft when you enter into the Windows Media DRM export agreement, to locate the offset in bytes for each payload.</span></span>

## <a name="related-topics"></a><span data-ttu-id="342d4-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="342d4-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="342d4-135">**Exportar contenido comprimido**</span><span class="sxs-lookup"><span data-stu-id="342d4-135">**Exporting Compressed Content**</span></span>](exporting-compressed-content.md)
</dt> </dl>

 

 




