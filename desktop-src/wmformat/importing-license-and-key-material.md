---
title: Importar material de clave y licencia
description: Importar material de clave y licencia
ms.assetid: 72ce5901-3e5b-4339-b695-592895ac6bfe
keywords:
- Windows SDK de formato multimedia, importación de DRM
- Windows SDK de formato multimedia, importación
- Windows SDK de formato multimedia, licencias
- digital rights management (DRM),import
- DRM (administración de derechos digitales),importar
- administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- digital rights management (DRM), material clave
- DRM (administración de derechos digitales), material clave
- API extendidas de cliente DRM, importar
- API extendidas de cliente, importar
- API extendidas de cliente DRM, licencias
- API extendidas de cliente, licencias
- API extendidas de cliente DRM, material clave
- API extendidas de cliente, material de clave
- licenses,importing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c9852102ab282c983488c2e5c35b7187bf0daccb62d347c312d1afb343b60f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118702509"
---
# <a name="importing-license-and-key-material"></a>Importar material de clave y licencia

Si tiene contenido multimedia cifrado mediante un sistema de protección de contenido de terceros y desea importar la licencia y el material de clave en Windows Media DRM, siga estos pasos:

1.  Recupere la Windows de certificados de máquina DRM multimedia mediante una llamada [**al método IWMDRMSecurity::GetMachineCertificate.**](iwmdrmsecurity-getmachinecertificate.md)
2.  Analice la colección de certificados, asegurándose de que está firmada correctamente y se valida con una clave pública raíz de Microsoft conocida. La colección de certificados se ajusta al esquema XMR. Para obtener más información, vea [Building an XMR License](building-an-xmr-license.md).
3.  Opcional: extraiga la lista de revocación llamando al [**método IWMDRMSecurity::GetRevocationData.**](iwmdrmsecurity-getrevocationdata.md)
4.  Opcional: se asegura de que no se revoca ningún certificado de la colección. Para obtener más información, vea [Comprobar la revocación de certificados.](checking-certificate-revocation.md)
5.  Genere una licencia en el formato XMR que represente los requisitos de directiva para el contenido de importación y contenga el material de clave DRM Windows multimedia adecuado. Para obtener más información, vea el tema [Building an XMR License](building-an-xmr-license.md).
6.  Pase la licencia XMR al sistema DRM de Windows Media para su procesamiento mediante el método [**IWMDRMLicenseManagement::StoreLicense.**](iwmdrmlicensemanagement-storelicense.md)

> [!Note]  
> Se le proporcionarán detalles sobre el esquema XMR cuando tenga licencia Windows DRM de media.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Comprobación de la revocación de certificados**](checking-certificate-revocation.md)
</dt> <dt>

[**Creación de una licencia XMR**](building-an-xmr-license.md)
</dt> <dt>

[**Importación de DRM**](drm-import.md)
</dt> </dl>

 

 




