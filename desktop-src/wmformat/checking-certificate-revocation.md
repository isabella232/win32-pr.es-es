---
title: Comprobación de la revocación de certificados
description: Comprobación de la revocación de certificados
ms.assetid: 498bd2a5-4336-4fc4-9718-6c5fe2db9066
keywords:
- SDK de Windows Media Format, importación de DRM
- SDK de Windows Media Format, importar
- SDK de Windows Media Format, revocación de certificados
- SDK de Windows Media Format, revocación de certificados
- Administración de derechos digitales (DRM), importar
- DRM (administración de derechos digitales), importar
- Administración de derechos digitales (DRM), revocación de certificados
- DRM (administración de derechos digitales), revocación de certificados
- Administración de derechos digitales (DRM), revocación de certificados
- DRM (administración de derechos digitales), revocación de certificados
- API extendidas del cliente DRM, importar
- API extendidas de cliente, importar
- API extendidas del cliente DRM, revocación de certificados
- API extendidas de cliente, revocación de certificados
- API extendidas del cliente DRM, revocación de certificados
- API extendidas de cliente, revocación de certificados
- certificados, revocación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbb72dd52870437ef9b69b30cc36a57725abe09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775769"
---
# <a name="checking-certificate-revocation"></a>Comprobación de la revocación de certificados

Al importar contenido en DRM de Windows Media, debe asegurarse de que no se ha revocado ningún certificado de una colección de certificados comprobando que no haya ningún certificado en la colección en la lista de revocación. La lista de revocación se extrae mediante el método [**IWMDRMSecurity:: GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) .

A continuación, use el método [**IWMDRMSecurity:: CheckCertForRevocation**](iwmdrmsecurity-checkcertforrevocation.md) para comprobar que el certificado no se ha revocado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Importación de DRM**](drm-import.md)
</dt> </dl>

 

 




