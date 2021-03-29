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
# <a name="receiving-unsolicited-traffic-over-teredo"></a>Recibir tráfico no solicitado a través de Teredo

[Teredo](about-teredo.md) proporciona conectividad global mediante las funcionalidades de NAT transversales y IPv6. Sin embargo, muchas aplicaciones, incluido peer-to-peer, requerirán Teredo para recibir tráfico no solicitado de Internet. Una aplicación puede programarse para recibir tráfico a través de una única interfaz IPv6 o de todas las interfaces compatibles con IPv6. En esta documentación se describen los requisitos para las aplicaciones que usan la interfaz Teredo para recibir tráfico IPv6 no solicitado.

Una aplicación recibirá tráfico no solicitado a través de la interfaz Teredo solo si la aplicación está registrada en el [firewall de Windows](/previous-versions/windows/desktop/ics/windows-firewall-start-page). Para recibir tráfico no solicitado, debe producirse lo siguiente:

-   Se debe indicar a los usuarios que usen Microsoft Management Console (MMC) para habilitar la opción "cruce seguro del perímetro" para una aplicación. Esta opción está disponible en firewall de Windows Snap-In--> <application name> --> pestaña "Opciones avanzadas". La opción "cruce seguro del perímetro" debe estar habilitada individualmente para cada aplicación.

-   La aplicación habilita la opción "cruce seguro del perímetro". Es posible que las aplicaciones que pueden recibir tráfico no solicitado se registren en el Firewall de Windows para "cruce seguro del perímetro" y reciban tráfico no solicitado a través de la interfaz Teredo. Para ello, una aplicación debe llamar a la API [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) con la opción "cruce seguro del perímetro" establecida en Variant \_ true. El consentimiento del usuario es necesario para esta llamada API antes de que una aplicación pueda escuchar el tráfico.

-   La aplicación establece la opción de socket de [ \_ \_ nivel de protección IPv6](/windows/desktop/WinSock/ipv6-protection-level) de Winsock en el **nivel de protección no \_ \_ restringido** [**a través de**](/windows/desktop/api/winsock/nf-winsock-setsockopt)la Esto permitirá que la aplicación reciba tráfico de cruce seguro del perímetro.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recibir tráfico solicitado a través de Teredo](receiving-solicited-traffic-over-teredo.md)
</dt> </dl>

 

 