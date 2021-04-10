---
title: Importación de la licencia y el material de clave
description: Importación de la licencia y el material de clave
ms.assetid: 72ce5901-3e5b-4339-b695-592895ac6bfe
keywords:
- SDK de Windows Media Format, importación de DRM
- SDK de Windows Media Format, importar
- SDK de Windows Media Format, licencias
- Administración de derechos digitales (DRM), importar
- DRM (administración de derechos digitales), importar
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- Administración de derechos digitales (DRM), material de clave
- DRM (administración de derechos digitales), material de clave
- API extendidas del cliente DRM, importar
- API extendidas de cliente, importar
- API extendidas del cliente DRM, licencias
- API extendidas del cliente, licencias
- API extendidas del cliente DRM, material de clave
- API extendidas de cliente, material de clave
- licencias, importar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a142d0087916a45b6dd8661b67f7e42eaed245c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269320"
---
# <a name="importing-license-and-key-material"></a>Importación de la licencia y el material de clave

Si tiene contenido multimedia que se cifró mediante un sistema de protección de contenido de terceros y desea importar la licencia y el material de clave en DRM de Windows Media, siga estos pasos:

1.  Recupere la colección de certificados de la máquina DRM de Windows Media llamando al método [**IWMDRMSecurity:: GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md) .
2.  Analice la colección de certificados, asegurándose de que se firmó correctamente y se valide a una clave pública raíz conocida de Microsoft. La colección de certificados se ajusta al esquema XMR. Para obtener más información, consulte [Building a XMR License](building-an-xmr-license.md).
3.  Opcional: Extraiga la lista de revocación llamando al método [**IWMDRMSecurity:: GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) .
4.  Opcional: Asegúrese de que no se revoca ningún certificado de la colección. Para obtener más información, consulte Comprobación de la [revocación de certificados](checking-certificate-revocation.md).
5.  Genere una licencia en el formato XMR que represente los requisitos de la Directiva para el contenido de importación y contenga el material de clave DRM de Windows Media adecuado. Para obtener más información, vea el tema [Building a XMR License](building-an-xmr-license.md).
6.  Pase la licencia de XMR al sistema DRM de Windows Media para su procesamiento, mediante el método [**IWMDRMLicenseManagement:: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) .

> [!Note]  
> Los detalles sobre el esquema XMR se le proporcionarán al conceder licencias de DRM de Windows Media.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Comprobación de la revocación de certificados**](checking-certificate-revocation.md)
</dt> <dt>

[**Creación de una licencia de XMR**](building-an-xmr-license.md)
</dt> <dt>

[**Importación de DRM**](drm-import.md)
</dt> </dl>

 

 




