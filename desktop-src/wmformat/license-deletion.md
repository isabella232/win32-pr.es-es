---
title: Eliminación de licencias
description: Eliminación de licencias
ms.assetid: f941efeb-145d-48a1-a3e2-d12f66b7fdcf
keywords:
- Windows SDK de formato multimedia, licencias
- Windows SDK de formato multimedia, eliminación de licencias
- administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- administración de derechos digitales (DRM), eliminación de licencias
- DRM (administración de derechos digitales), eliminación de licencias
- API extendidas de cliente DRM, licencias
- API extendidas de cliente, licencias
- API extendidas de cliente DRM, eliminar licencias
- API extendidas de cliente, eliminar licencias
- licenses,deleting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd1e20c0e98fd2129b807cf11f27f5975701d851d9301eda894ccb24015360a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808305"
---
# <a name="license-deletion"></a>Eliminación de licencias

Las licencias de terceros creadas localmente, por ejemplo a través de la importación de DRM, se pueden eliminar llamando al método [**IWMDRMLicenseManagement::P rocessLicenseDeletionMessage.**](iwmdrmlicensemanagement-processlicensedeletionmessage.md) La cadena que pase a este método será una licencia XMR similar a la siguiente:


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



El campo id. de usuario (UID) específico del propietario es opcional. Los campos opcionales no deben incluirse en la respuesta de licencia si no hay ningún dato asociado a ellos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de una licencia XMR**](building-an-xmr-license.md)
</dt> <dt>

[**Importación de DRM**](drm-import.md)
</dt> <dt>

[**Guía de programación**](drm-programming-guide.md)
</dt> </dl>

 

 




