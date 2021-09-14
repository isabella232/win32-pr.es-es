---
title: Uso de Teredo en Windows XP
ms.assetid: 21590e3b-03de-48a4-b142-5d1934dacc38
description: 'Más información sobre: Uso de Teredo en Windows XP'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f29abb2b4056564be29708ceb00742b37d363d7a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160600"
---
# <a name="using-teredo-in-windows-xp"></a>Uso de Teredo en Windows XP

Para usar el cliente de Teredo o la retransmisión específica del host en equipos que ejecutan Windows XP con Service Pack 1 (SP1) con Advanced Networking Pack, Windows XP con Service Pack 2 (SP2), Windows Server 2003 con Service Pack 1 (SP1) o Windows Server 2003 con Service Pack 2 (SP2), un desarrollador de aplicaciones debe hacer lo siguiente:

-   Asegúrese de que la aplicación es compatible con IPv6 mediante nuevos elementos de programación de Windows Sockets 2 (funciones y estructuras) que admiten IPv4 e IPv6. Para obtener más información, vea la [Guía de IPv6 para Windows Sockets.](../winsock/ipv6-guide-for-windows-sockets-applications-2.md)
-   Habilite el uso de Teredo en la aplicación estableciendo la opción de socket IPV6 PROTECTION LEVEL Windows Sockets en el nivel \_ \_ PROTECTION LEVEL \_ \_ UNRESTRICTED. Para obtener más información, [vea Using IPV6 \_ PROTECTION \_ LEVEL](/previous-versions/aa916826(v=msdn.10)). También puede establecer esta opción a través de la [clase .NET Framework System.Net.Sockets.](/dotnet/api/system.net.sockets?view=netcore-3.1)
-   Cree una excepción para Windows Firewall para permitir el tráfico entrante no solicitado de Teredo. Use las [API Windows Firewall](/previous-versions/windows/desktop/ics/windows-firewall-start-page) para crear una excepción de puerto para el puerto UDP asignado para el tráfico de Teredo. Para obtener más información y ejemplos que detallan las consideraciones de seguridad y tráfico necesarias para Teredo, consulte [Uso de Teredo.](using-teredo.md)

Para asegurarse de que Teredo está disponible para su uso cuando se ejecuta la aplicación, los desarrolladores de aplicaciones deben hacer lo siguiente durante el proceso de instalación de la aplicación:

-   Instale IPv6 con el **comando netsh interface ipv6 install.** Windows El firewall protege el equipo del usuario frente al tráfico IPv6 entrante no solicitado de la misma manera que el tráfico IPv4.
-   Habilite Teredo con el **comando netsh interface ipv6 set teredo client.**

Opcionalmente, puede probar si IPv6 se instala cada vez que se ejecuta la aplicación e instalar IPv6 y habilitar Teredo según sea necesario. También debe informar al usuario de que se está instalando IPv6 y de que Teredo está habilitado.

 

 
