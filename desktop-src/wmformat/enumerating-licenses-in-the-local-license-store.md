---
title: Enumerar licencias en el almacén de licencias local
description: Enumerar licencias en el almacén de licencias local
ms.assetid: 1f380b9e-85e4-4190-a809-65dfd4658b7c
keywords:
- Windows Media Format SDK, enumerar licencias
- SDK de Windows Media Format, licencias
- SDK de Windows Media Format, almacén de licencias local
- Administración de derechos digitales (DRM), enumerar licencias
- DRM (administración de derechos digitales), enumerar licencias
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- Administración de derechos digitales (DRM), almacén de licencias local
- DRM (administración de derechos digitales), almacén de licencias local
- API extendidas del cliente DRM, enumerar licencias
- API extendidas del cliente, enumerar licencias
- API extendidas del cliente DRM, licencias
- API extendidas del cliente, licencias
- API extendidas del cliente DRM, almacén de licencias local
- API extendidas de cliente, almacén de licencias local
- licencias, enumeración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b1384e08a6789fedca9704f36ad8da1e31b4ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418520"
---
# <a name="enumerating-licenses-in-the-local-license-store"></a><span data-ttu-id="e329a-119">Enumerar licencias en el almacén de licencias local</span><span class="sxs-lookup"><span data-stu-id="e329a-119">Enumerating Licenses in the Local License Store</span></span>

<span data-ttu-id="e329a-120">La enumeración es un proceso que consiste en obtener información acerca de las licencias en el almacén de licencias local, ya que se recorren una por una.</span><span class="sxs-lookup"><span data-stu-id="e329a-120">Enumeration is a process of getting information about the licenses in the local license store, by stepping through them one by one.</span></span> <span data-ttu-id="e329a-121">Puede crear una enumeración de licencias mediante una llamada a [**IWMDRMLicenseManagement:: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md).</span><span class="sxs-lookup"><span data-stu-id="e329a-121">You can create a license enumeration by calling the [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md).</span></span>

<span data-ttu-id="e329a-122">La razón más común para enumerar licencias en el almacén es encontrar una licencia concreta para el descifrado de algún contenido.</span><span class="sxs-lookup"><span data-stu-id="e329a-122">The most common reason for enumerating through licenses in the store is to find a particular license for decryption of some content.</span></span>

<span data-ttu-id="e329a-123">La interfaz [**IWMDRMLicense**](iwmdrmlicense.md) sirve como portal para los resultados de licencia individuales y como enumerador.</span><span class="sxs-lookup"><span data-stu-id="e329a-123">The [**IWMDRMLicense**](iwmdrmlicense.md) interface serves as both a portal to the individual license results and as the enumerator.</span></span> <span data-ttu-id="e329a-124">Cuando se crea la enumeración de licencias, la primera licencia de la lista se carga en la interfaz **IWMDRMLicense** .</span><span class="sxs-lookup"><span data-stu-id="e329a-124">When the license enumeration is created, the first license in the list is loaded into the **IWMDRMLicense** interface.</span></span> <span data-ttu-id="e329a-125">La mayoría de los métodos de **IWMDRMLicense** permiten obtener información sobre la licencia o crear objetos para cifrar o descifrar el contenido en función de la licencia.</span><span class="sxs-lookup"><span data-stu-id="e329a-125">Most of the methods of **IWMDRMLicense** enable you to get information about the license or to create objects to encrypt or decrypt content based on the license.</span></span> <span data-ttu-id="e329a-126">Sin embargo, hay dos métodos que controlan la enumeración: [**Getnext**](iwmdrmlicense-getnext.md) y [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md).</span><span class="sxs-lookup"><span data-stu-id="e329a-126">However, there are two methods that control the enumeration: [**GetNext**](iwmdrmlicense-getnext.md) and [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md).</span></span> <span data-ttu-id="e329a-127">**Getnext** carga la siguiente licencia de la lista en la interfaz.</span><span class="sxs-lookup"><span data-stu-id="e329a-127">**GetNext** loads the next license in the list into the interface.</span></span> <span data-ttu-id="e329a-128">**ResetEnumeration** devuelve la enumeración al estado en que se encontraba cuando se creó por primera vez.</span><span class="sxs-lookup"><span data-stu-id="e329a-128">**ResetEnumeration** returns the enumeration to the state it was in when it was first created.</span></span> <span data-ttu-id="e329a-129">Cuando se restablece la enumeración, la primera licencia de la lista se vuelve a cargar en la interfaz **IWMDRMLicense** .</span><span class="sxs-lookup"><span data-stu-id="e329a-129">When the enumeration is reset, the first license in the list is loaded back into the **IWMDRMLicense** interface.</span></span>

<span data-ttu-id="e329a-130">Cuando se ha alcanzado la última licencia de la lista, la siguiente llamada a **Getnext** devuelve el error \_ no hay \_ más \_ elementos.</span><span class="sxs-lookup"><span data-stu-id="e329a-130">When you have reached the last license in the list, the next call to **GetNext** returns ERROR\_NO\_MORE\_ITEMS.</span></span>

<span data-ttu-id="e329a-131">Si la aplicación realiza una acción con el contenido que está incluido en DRM, debe comprobar las licencias en el almacén de licencias local para los derechos y otros factores de limitación, como los niveles de protección de salida (OPLs).</span><span class="sxs-lookup"><span data-stu-id="e329a-131">If your application performs an action with the content that is covered by DRM, you should check the licenses in the local license store for the rights and for other limiting factors, such as output protection levels (OPLs).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e329a-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e329a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e329a-133">**Obtención de información de licencias en el almacén de licencias local**</span><span class="sxs-lookup"><span data-stu-id="e329a-133">**Getting Information from Licenses in the Local License Store**</span></span>](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




