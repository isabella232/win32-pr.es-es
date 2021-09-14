---
title: Recepción de tráfico no solicitado a través de Teredo
description: Teredo proporciona conectividad global mediante funcionalidades de recorrido de IPv6 y NAT.
ms.assetid: 0c03d1bb-15f8-4e77-9a96-e182b1d190ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5c7ffe7b84cfa325b3ecd8c0858ad96445e629
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243543"
---
# <a name="receiving-unsolicited-traffic-over-teredo"></a>Recepción de tráfico no solicitado a través de Teredo

[Teredo proporciona](about-teredo.md) conectividad global mediante funcionalidades de recorrido de IPv6 y NAT. Sin embargo, muchas aplicaciones, incluido punto a punto, requerirán que Teredo reciba tráfico no solicitado de Internet. Una aplicación se puede programar para recibir tráfico a través de una única interfaz IPv6 o de todas las interfaces compatibles con IPv6. En esta documentación se describen los requisitos de las aplicaciones que usan la interfaz teredo para recibir tráfico IPv6 no solicitado.

Una aplicación recibirá tráfico no solicitado a través de la interfaz de Teredo solo si la aplicación está registrada con [Windows Firewall](/previous-versions/windows/desktop/ics/windows-firewall-start-page). Para recibir tráfico no solicitado, debe producirse lo siguiente:

-   Se debe indicar a los usuarios que usen el Microsoft Management Console (MMC) para habilitar la opción "Edge Traversal" para una aplicación. Esta opción está disponible en Windows Firewall Snap-In --> <application name> --> pestaña "Avanzado". La opción "Edge Traversal" debe habilitarse individualmente para cada aplicación.

-   La aplicación habilita la opción "Edge Traversal". Es posible que las aplicaciones capaces de recibir tráfico no solicitado se registren con Windows Firewall para "Edge Traversal" y reciban tráfico no solicitado a través de la interfaz teredo. Para ello, una aplicación debe llamar a la API [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) con la opción "Edge Traversal" establecida en VARIANT \_ TRUE. El consentimiento del usuario es necesario para esta llamada API antes de que se permita que una aplicación escuche el tráfico.

-   La aplicación establece la opción de socket Winsock [IPV6 \_ PROTECTION \_ LEVEL](/windows/desktop/WinSock/ipv6-protection-level) en **PROTECTION LEVEL \_ \_ UNRESTRICTED** mediante [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt). Esto permitirá que la aplicación reciba tráfico de Edge Traversal.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recepción de tráfico solicitado a través de Teredo](receiving-solicited-traffic-over-teredo.md)
</dt> </dl>

 

 