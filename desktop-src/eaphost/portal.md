---
title: Host del Protocolo de autenticación extensible
description: Obtenga información sobre el host del Protocolo de autenticación extensible (EAP). Vea requisitos de tiempo de ejecución y ver recursos adicionales disponibles.
ms.assetid: caaef367-2952-44fc-ac4c-f0db6387850e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f007435c43969ad0f195b0a6a1e697ab817d9c4
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "104149750"
---
# <a name="extensible-authentication-protocol-host"></a>Host del Protocolo de autenticación extensible

## <a name="purpose"></a>Propósito


EAPHost es un componente de red de Microsoft Windows que proporciona una infraestructura de protocolo de autenticación extensible (EAP) para la autenticación de implementaciones de protocolo de "suplicante" como [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) y [punto a punto](https://go.microsoft.com/fwlink/p/?linkid=83919) (PPP). También permite la autenticación con tecnologías de "autenticador" como el servidor de directivas de redes (NPS) de Microsoft. A diferencia del servidor IAS anterior ([RADIUS](/windows/desktop/Nps/ias-about-internet-authentication-service)), NPS es compatible con la [protección de acceso a redes](/windows/desktop/NAP/network-access-protection-start-page) (NAP).


Las API de EAPHost permiten a las aplicaciones autenticarse mediante el servicio EAPHost y proporcionan una plantilla para el desarrollo de métodos de autenticación compatibles para su uso con EAPHost.

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

 

 