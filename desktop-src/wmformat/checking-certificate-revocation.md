---
title: Comprobación de la revocación de certificados
description: Comprobación de la revocación de certificados
ms.assetid: 498bd2a5-4336-4fc4-9718-6c5fe2db9066
keywords:
- Windows SDK de formato multimedia, importación de DRM
- Windows SDK de formato multimedia, importar
- Windows SDK de formato multimedia, revocación de certificados
- Windows SDK de formato multimedia, revocación de certificados
- administración de derechos digitales (DRM),importar
- DRM (administración de derechos digitales),importar
- administración de derechos digitales (DRM), revocación de certificados
- DRM (administración de derechos digitales), revocación de certificados
- administración de derechos digitales (DRM), revocación de certificados
- DRM (administración de derechos digitales), revocación de certificados
- API extendidas de cliente DRM, importar
- API extendidas de cliente, importar
- API extendidas de cliente DRM, revocación de certificados
- API extendidas de cliente, revocación de certificados
- API extendidas de cliente DRM, revocación de certificados
- API extendidas de cliente, revocación de certificados
- certificates,revocation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3d9f8aaa299873513f88a2be258cf2ddd96147934e461cbde49630542fd9b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028073"
---
# <a name="checking-certificate-revocation"></a>Comprobación de la revocación de certificados

Al importar contenido en Windows Media DRM, debe asegurarse de que no se ha revocado ningún certificado de una colección de certificados comprobando que ningún certificado de la colección está en la lista de revocación. La lista de revocación se extrae mediante el [**método IWMDRMSecurity::GetRevocationData.**](iwmdrmsecurity-getrevocationdata.md)

A continuación, use [**el método IWMDRMSecurity::CheckCertForRevocation**](iwmdrmsecurity-checkcertforrevocation.md) para comprobar que el certificado no se ha revocado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Importación de DRM**](drm-import.md)
</dt> </dl>

 

 




