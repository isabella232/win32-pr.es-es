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
- DRM (administración de derechos digitales), eliminar licencias
- API extendidas de cliente DRM, licencias
- API extendidas de cliente, licencias
- API extendidas de cliente DRM, eliminar licencias
- API extendidas de cliente, eliminar licencias
- licencias, eliminar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f297db679ac2c8afe2c836d032fa045d6955665
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267095"
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

 

 




