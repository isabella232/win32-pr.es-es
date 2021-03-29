---
title: Recibir tráfico no solicitado a través de Teredo
description: Teredo proporciona conectividad global mediante las funcionalidades de NAT transversales y IPv6.
ms.assetid: 0c03d1bb-15f8-4e77-9a96-e182b1d190ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5c7ffe7b84cfa325b3ecd8c0858ad96445e629
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792933"
---
# <a name="receiving-unsolicited-traffic-over-teredo"></a><span data-ttu-id="05f43-103">Recibir tráfico no solicitado a través de Teredo</span><span class="sxs-lookup"><span data-stu-id="05f43-103">Receiving Unsolicited Traffic Over Teredo</span></span>

<span data-ttu-id="05f43-104">[Teredo](about-teredo.md) proporciona conectividad global mediante las funcionalidades de NAT transversales y IPv6.</span><span class="sxs-lookup"><span data-stu-id="05f43-104">[Teredo](about-teredo.md) provides global connectivity using IPv6 and NAT traversal capabilities.</span></span> <span data-ttu-id="05f43-105">Sin embargo, muchas aplicaciones, incluido peer-to-peer, requerirán Teredo para recibir tráfico no solicitado de Internet.</span><span class="sxs-lookup"><span data-stu-id="05f43-105">However, many applications, including peer-to-peer, will require Teredo to receive unsolicited traffic from the Internet.</span></span> <span data-ttu-id="05f43-106">Una aplicación puede programarse para recibir tráfico a través de una única interfaz IPv6 o de todas las interfaces compatibles con IPv6.</span><span class="sxs-lookup"><span data-stu-id="05f43-106">An application can be programmed to receive traffic over a single IPv6 interface or all IPv6-capable interfaces.</span></span> <span data-ttu-id="05f43-107">En esta documentación se describen los requisitos para las aplicaciones que usan la interfaz Teredo para recibir tráfico IPv6 no solicitado.</span><span class="sxs-lookup"><span data-stu-id="05f43-107">This documentation describes the requirements for applications that use the Teredo interface to receive unsolicited IPv6 traffic.</span></span>

<span data-ttu-id="05f43-108">Una aplicación recibirá tráfico no solicitado a través de la interfaz Teredo solo si la aplicación está registrada en el [firewall de Windows](/previous-versions/windows/desktop/ics/windows-firewall-start-page).</span><span class="sxs-lookup"><span data-stu-id="05f43-108">An application will receive unsolicited traffic over the Teredo interface only if the application is registered with [Windows Firewall](/previous-versions/windows/desktop/ics/windows-firewall-start-page).</span></span> <span data-ttu-id="05f43-109">Para recibir tráfico no solicitado, debe producirse lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="05f43-109">In order to receive unsolicited traffic the following must occur:</span></span>

-   <span data-ttu-id="05f43-110">Se debe indicar a los usuarios que usen Microsoft Management Console (MMC) para habilitar la opción "cruce seguro del perímetro" para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="05f43-110">Users must be instructed to use of the Microsoft Management Console (MMC) to enable the "Edge Traversal" option for an application.</span></span> <span data-ttu-id="05f43-111">Esta opción está disponible en firewall de Windows Snap-In--> <application name> --> pestaña "Opciones avanzadas". La opción "cruce seguro del perímetro" debe estar habilitada individualmente para cada aplicación.</span><span class="sxs-lookup"><span data-stu-id="05f43-111">This option is available under Windows Firewall Snap-In --> <application name> --> "Advanced" tab. The "Edge Traversal" option must be enabled individually for each application.</span></span>

-   <span data-ttu-id="05f43-112">La aplicación habilita la opción "cruce seguro del perímetro".</span><span class="sxs-lookup"><span data-stu-id="05f43-112">The "Edge Traversal" option is enabled by the application.</span></span> <span data-ttu-id="05f43-113">Es posible que las aplicaciones que pueden recibir tráfico no solicitado se registren en el Firewall de Windows para "cruce seguro del perímetro" y reciban tráfico no solicitado a través de la interfaz Teredo.</span><span class="sxs-lookup"><span data-stu-id="05f43-113">It is possible for applications capable of receiving unsolicited traffic to register with Windows Firewall for "Edge Traversal" and receive unsolicited traffic over the Teredo interface.</span></span> <span data-ttu-id="05f43-114">Para ello, una aplicación debe llamar a la API [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) con la opción "cruce seguro del perímetro" establecida en Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="05f43-114">To do this an application must call the [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) API with the "Edge Traversal" option set to VARIANT\_TRUE.</span></span> <span data-ttu-id="05f43-115">El consentimiento del usuario es necesario para esta llamada API antes de que una aplicación pueda escuchar el tráfico.</span><span class="sxs-lookup"><span data-stu-id="05f43-115">User consent is required for this API call before an application is permitted to listen for the traffic.</span></span>

-   <span data-ttu-id="05f43-116">La aplicación establece la opción de socket de [ \_ \_ nivel de protección IPv6](/windows/desktop/WinSock/ipv6-protection-level) de Winsock en el **nivel de protección no \_ \_ restringido** [**a través de**](/windows/desktop/api/winsock/nf-winsock-setsockopt)la</span><span class="sxs-lookup"><span data-stu-id="05f43-116">The application sets the Winsock [IPV6\_PROTECTION\_LEVEL](/windows/desktop/WinSock/ipv6-protection-level) socket option to **PROTECTION\_LEVEL\_UNRESTRICTED** via [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt).</span></span> <span data-ttu-id="05f43-117">Esto permitirá que la aplicación reciba tráfico de cruce seguro del perímetro.</span><span class="sxs-lookup"><span data-stu-id="05f43-117">This will allow the application to receive Edge Traversal traffic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05f43-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="05f43-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05f43-119">Recibir tráfico solicitado a través de Teredo</span><span class="sxs-lookup"><span data-stu-id="05f43-119">Receiving Solicited Traffic Over Teredo</span></span>](receiving-solicited-traffic-over-teredo.md)
</dt> </dl>

 

 