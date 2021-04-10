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
# <a name="extensible-authentication-protocol-host"></a><span data-ttu-id="ec732-104">Host del Protocolo de autenticación extensible</span><span class="sxs-lookup"><span data-stu-id="ec732-104">Extensible Authentication Protocol Host</span></span>

## <a name="purpose"></a><span data-ttu-id="ec732-105">Propósito</span><span class="sxs-lookup"><span data-stu-id="ec732-105">Purpose</span></span>


<span data-ttu-id="ec732-106">EAPHost es un componente de red de Microsoft Windows que proporciona una infraestructura de protocolo de autenticación extensible (EAP) para la autenticación de implementaciones de protocolo de "suplicante" como [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) y [punto a punto](https://go.microsoft.com/fwlink/p/?linkid=83919) (PPP).</span><span class="sxs-lookup"><span data-stu-id="ec732-106">EAPHost is a Microsoft Windows Networking component that provides an Extensible Authentication Protocol (EAP) infrastructure for the authentication of "supplicant" protocol implementations such as [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) and [Point-to-Point](https://go.microsoft.com/fwlink/p/?linkid=83919) (PPP).</span></span> <span data-ttu-id="ec732-107">También permite la autenticación con tecnologías de "autenticador" como el servidor de directivas de redes (NPS) de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ec732-107">It also allows for authentication with "authenticator" technologies such as the Microsoft network policy server (NPS).</span></span> <span data-ttu-id="ec732-108">A diferencia del servidor IAS anterior ([RADIUS](/windows/desktop/Nps/ias-about-internet-authentication-service)), NPS es compatible con la [protección de acceso a redes](/windows/desktop/NAP/network-access-protection-start-page) (NAP).</span><span class="sxs-lookup"><span data-stu-id="ec732-108">Unlike the previous IAS Server ([RADIUS](/windows/desktop/Nps/ias-about-internet-authentication-service)), NPS supports [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP).</span></span>


<span data-ttu-id="ec732-109">Las API de EAPHost permiten a las aplicaciones autenticarse mediante el servicio EAPHost y proporcionan una plantilla para el desarrollo de métodos de autenticación compatibles para su uso con EAPHost.</span><span class="sxs-lookup"><span data-stu-id="ec732-109">The EAPHost APIs enable applications to authenticate using the EAPHost service, and provide a template for the development of conformant authentication methods for use with EAPHost.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="ec732-110">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="ec732-110">Run-time requirements</span></span>

<span data-ttu-id="ec732-111">Las API de EAPHost solo se admiten en Windows Vista y sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="ec732-111">The EAPHost APIs are supported only in Windows Vista and later operating systems.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ec732-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ec732-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec732-113">Acerca de EAPHost</span><span class="sxs-lookup"><span data-stu-id="ec732-113">About EAPHost</span></span>](about-eap-host.md)
</dt> <dt>

[<span data-ttu-id="ec732-114">Uso de EAPHost</span><span class="sxs-lookup"><span data-stu-id="ec732-114">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="ec732-115">Referencia de API de EAPHost</span><span class="sxs-lookup"><span data-stu-id="ec732-115">EAPHost API Reference</span></span>](eaphost-api-reference.md)
</dt> </dl>

 

 