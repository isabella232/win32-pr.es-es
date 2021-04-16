---
title: Eliminación de licencias
description: Eliminación de licencias
ms.assetid: f941efeb-145d-48a1-a3e2-d12f66b7fdcf
keywords:
- SDK de Windows Media Format, licencias
- Windows Media Format SDK, eliminar licencias
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- Administración de derechos digitales (DRM), eliminar licencias
- DRM (administración de derechos digitales), eliminar licencias
- API extendidas del cliente DRM, licencias
- API extendidas del cliente, licencias
- API extendidas del cliente DRM, eliminar licencias
- API extendidas de cliente, eliminar licencias
- licencias, eliminar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f297db679ac2c8afe2c836d032fa045d6955665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656285"
---
# <a name="license-deletion"></a><span data-ttu-id="3a181-114">Eliminación de licencias</span><span class="sxs-lookup"><span data-stu-id="3a181-114">License Deletion</span></span>

<span data-ttu-id="3a181-115">Las licencias de terceros creadas localmente, por ejemplo a través de la importación de DRM, se pueden eliminar llamando al método [**IWMDRMLicenseManagement::P rocesslicensedeletionmessage**](iwmdrmlicensemanagement-processlicensedeletionmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="3a181-115">Any third-party licenses created locally, for example through DRM import, can be deleted by calling the [**IWMDRMLicenseManagement::ProcessLicenseDeletionMessage**](iwmdrmlicensemanagement-processlicensedeletionmessage.md) method.</span></span> <span data-ttu-id="3a181-116">La cadena que se pasa a este método será una licencia XMR similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="3a181-116">The string you pass to this method will be an XMR license that resembles the following:</span></span>


```C++
<response type="LRB">
  <DATA>
    <LICENSEDATA>
      <DATA>
        <KID>include Key ID here to revoke certain keys</KID>
        <LID>rights ID</LID
        <META>
          <LGPUBKEY>
            <PublicKey>
              <Modulus>base64 encoded public key</Modulus>
              <Exponent>Exponent in network byte order</Exponent>
            </PublicKey>
          </LGPUBKEY>
          <UID>content-owner-specific user ID</UID>
        </META>
      </DATA>
    </LICENSEDATA>
  </DATA>
</response>
```



<span data-ttu-id="3a181-117">El campo ID. de usuario específico (UID) es opcional.</span><span class="sxs-lookup"><span data-stu-id="3a181-117">The owner specific user ID (UID) field is optional.</span></span> <span data-ttu-id="3a181-118">Los campos opcionales no deben incluirse en la respuesta de la licencia si no hay ningún dato asociado a ellos.</span><span class="sxs-lookup"><span data-stu-id="3a181-118">Optional fields must not be included in the license response if there is not any data associated with them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a181-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3a181-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a181-120">**Creación de una licencia de XMR**</span><span class="sxs-lookup"><span data-stu-id="3a181-120">**Building an XMR License**</span></span>](building-an-xmr-license.md)
</dt> <dt>

[<span data-ttu-id="3a181-121">**Importación de DRM**</span><span class="sxs-lookup"><span data-stu-id="3a181-121">**DRM Import**</span></span>](drm-import.md)
</dt> <dt>

[<span data-ttu-id="3a181-122">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="3a181-122">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




