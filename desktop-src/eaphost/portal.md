---
title: Host de protocolo de autenticación extensible
description: Obtenga información sobre el host del Protocolo de autenticación extensible (EAP). Consulte los requisitos en tiempo de ejecución y vea los recursos disponibles adicionales.
ms.assetid: caaef367-2952-44fc-ac4c-f0db6387850e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bd43feec10cfadf4aee071ff5f7fe98da5d579878231b9ba3e86287bf4dbab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117719820"
---
# <a name="extensible-authentication-protocol-host"></a>Host de protocolo de autenticación extensible

## <a name="purpose"></a>Propósito


EAPHost es un componente de redes de Microsoft Windows que proporciona una infraestructura de Protocolo de autenticación extensible (EAP) para [](https://go.microsoft.com/fwlink/p/?linkid=83919) la autenticación de implementaciones de protocolo "suplicante", como [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) y punto a punto (PPP). También permite la autenticación con tecnologías de "autenticación", como el servidor de directivas de red (NPS) de Microsoft. A diferencia del servidor IAS anterior[(RADIUS),](/windows/desktop/Nps/ias-about-internet-authentication-service)NPS admite [la protección de acceso a redes](/windows/desktop/NAP/network-access-protection-start-page) (NAP).


Las API de EAPHost permiten que las aplicaciones se autentiquen mediante el servicio EAPHost y proporcionan una plantilla para el desarrollo de métodos de autenticación compatibles para su uso con EAPHost.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Las API de EAPHost solo se admiten en Windows Vista y sistemas operativos posteriores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de EAPHost](about-eap-host.md)
</dt> <dt>

[Uso de EAPHost](using-eap-host.md)
</dt> <dt>

[Referencia de API de EAPHost](eaphost-api-reference.md)
</dt> </dl>

 

 