---
title: Creación de una licencia de XMR
description: Creación de una licencia de XMR
ms.assetid: c43e4913-82a6-4dd0-9d1f-1fb237ecbb30
keywords:
- SDK de Windows Media Format, importación de DRM
- SDK de Windows Media Format, importar
- SDK de Windows Media Format, licencias de XMR
- SDK de Windows Media Format, licencias
- SDK de Windows Media Format, derechos de medios extensibles (XMR)
- Administración de derechos digitales (DRM), importar
- DRM (administración de derechos digitales), importar
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- Administración de derechos digitales (DRM), licencias de XMR
- DRM (administración de derechos digitales), licencias de XMR
- Administración de derechos digitales (DRM), derechos de medios extensibles (XMR)
- DRM (administración de derechos digitales), derechos multimedia extensibles (XMR)
- API extendidas del cliente DRM, importar
- API extendidas de cliente, importar
- API extendidas del cliente DRM, licencias de XMR
- API extendidas de cliente, licencias de XMR
- API extendidas del cliente DRM, licencias
- API extendidas del cliente, licencias
- API extendidas del cliente DRM, derechos multimedia extensibles (XMR)
- API extendidas de cliente, derechos multimedia extensibles (XMR)
- licencias, XMR
- Derechos de medios extensibles (XMR)
- XMR (derechos multimedia extensible)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc275419116362c08cabe4dc70aa227687705fdb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418372"
---
# <a name="building-an-xmr-license"></a><span data-ttu-id="2cd76-127">Creación de una licencia de XMR</span><span class="sxs-lookup"><span data-stu-id="2cd76-127">Building an XMR License</span></span>

<span data-ttu-id="2cd76-128">Para generar una licencia para el procesamiento de DRM de Windows Media, debe usar el esquema binario de manextensible Media Rights (XMR).</span><span class="sxs-lookup"><span data-stu-id="2cd76-128">To generate a license for Windows Media DRM to process, you must use the Extensible Media Rights (XMR) binary schema.</span></span> <span data-ttu-id="2cd76-129">XMR es un esquema para transmitir derechos y restricciones de uso de medios y debe tener licencia por separado.</span><span class="sxs-lookup"><span data-stu-id="2cd76-129">XMR is a schema for conveying media usage rights and restrictions and needs to be licensed separately.</span></span>

<span data-ttu-id="2cd76-130">El material importante de una licencia se cifra mediante la clave pública de la colección de certificados DRM de Windows Media, por lo que solo es visible para el subsistema de API extendida del cliente DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2cd76-130">The important material in a license is encrypted using the public key in the Windows Media DRM certificate collection, so it is visible only to the Windows Media DRM Client Extended API subsystem.</span></span> <span data-ttu-id="2cd76-131">.</span><span class="sxs-lookup"><span data-stu-id="2cd76-131">.</span></span>

<span data-ttu-id="2cd76-132">Es responsabilidad suya asegurarse de que la configuración de la Directiva y la estructura de licencias son válidas y coherentes con la intención del emisor de la licencia y que se ajustan a las reglas de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="2cd76-132">It is your responsibility to ensure that the license structure and policy settings are valid and consistent with the license issuer's intent, and that they conform to the compliance rules.</span></span>

<span data-ttu-id="2cd76-133">Debe leer las reglas de cumplimiento de importación de DRM de Windows Media para obtener información sobre el conjunto completo de objetos XMR que deben estar presentes en la licencia.</span><span class="sxs-lookup"><span data-stu-id="2cd76-133">You should read the Windows Media DRM import compliance rules to learn the complete set of XMR objects that must be present in the license.</span></span>

<span data-ttu-id="2cd76-134">Para pasar la licencia de XMR al subsistema DRM, llame al método [**IWMDRMLicenseManagement:: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="2cd76-134">To pass the XMR license to the DRM subsystem, call the [**IWMDRMLicenseManagement::StoreLicense**](iwmdrmlicensemanagement-storelicense.md) method.</span></span> <span data-ttu-id="2cd76-135">Use el formato siguiente para pasar la licencia en el parámetro *bstrLicenseResponse* :</span><span class="sxs-lookup"><span data-stu-id="2cd76-135">Use the following format to pass the license in the *bstrLicenseResponse* parameter:</span></span>


```C++
<LICENSERESPONSE>
    <LICENSE version="3.0.0.0">insert base64-encoded XMR license here</LICENSE>
</LICENSERESPONSE>
```



<span data-ttu-id="2cd76-136">Esta cadena debe tener el formato Unicode (UTF-16).</span><span class="sxs-lookup"><span data-stu-id="2cd76-136">This string must be in Unicode format (UTF-16).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2cd76-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2cd76-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cd76-138">**Importación de DRM**</span><span class="sxs-lookup"><span data-stu-id="2cd76-138">**DRM Import**</span></span>](drm-import.md)
</dt> </dl>

 

 




