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
# <a name="license-deletion"></a>Eliminación de licencias

Las licencias de terceros creadas localmente, por ejemplo a través de la importación de DRM, se pueden eliminar llamando al método [**IWMDRMLicenseManagement::P rocesslicensedeletionmessage**](iwmdrmlicensemanagement-processlicensedeletionmessage.md) . La cadena que se pasa a este método será una licencia XMR similar a la siguiente:


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



El campo ID. de usuario específico (UID) es opcional. Los campos opcionales no deben incluirse en la respuesta de la licencia si no hay ningún dato asociado a ellos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de una licencia de XMR**](building-an-xmr-license.md)
</dt> <dt>

[**Importación de DRM**](drm-import.md)
</dt> <dt>

[**Guía de programación**](drm-programming-guide.md)
</dt> </dl>

 

 




