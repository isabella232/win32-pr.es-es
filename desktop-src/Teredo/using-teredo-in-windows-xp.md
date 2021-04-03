---
title: Usar Teredo en Windows XP
ms.assetid: 21590e3b-03de-48a4-b142-5d1934dacc38
description: Más información acerca de cómo usar Teredo en Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f29abb2b4056564be29708ceb00742b37d363d7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083386"
---
# <a name="using-teredo-in-windows-xp"></a>Usar Teredo en Windows XP

Para usar el cliente Teredo o la retransmisión específica del host en equipos que ejecutan Windows XP con Service Pack 1 (SP1) con el paquete de redes avanzadas, Windows XP con Service Pack 2 (SP2), Windows Server 2003 con Service Pack 1 (SP1) o Windows Server 2003 con Service Pack 2 (SP2), un desarrollador de aplicaciones debe hacer lo siguiente:

-   Asegúrese de que la aplicación es compatible con IPv6 mediante el uso de nuevos elementos de programación de Windows Sockets 2 (funciones y estructuras) que admiten tanto IPv4 como IPv6. Para obtener más información, consulte la [Guía de IPv6 para aplicaciones de Windows Sockets](../winsock/ipv6-guide-for-windows-sockets-applications-2.md).
-   Habilite el uso de Teredo en la aplicación. para ello, establezca la \_ \_ opción de socket de Windows Sockets de nivel de protección IPv6 en el nivel de protección no \_ \_ restringido. Para obtener más información, vea [usar \_ el \_ nivel de protección de IPv6](/previous-versions/aa916826(v=msdn.10)). También puede establecer esta opción a través de la clase [System .net. sockets](/dotnet/api/system.net.sockets?view=netcore-3.1) .NET Framework.
-   Cree una excepción para que el Firewall de Windows permita el tráfico Teredo entrante no solicitado. Use las API de [firewall de Windows](/previous-versions/windows/desktop/ics/windows-firewall-start-page) para crear una excepción de puerto para el puerto UDP asignado para el tráfico Teredo. Para obtener más información y ejemplos que detallan la seguridad y las consideraciones de tráfico necesarias para Teredo, vea [usar Teredo](using-teredo.md).

Para asegurarse de que Teredo está disponible para su uso cuando se ejecuta la aplicación, los desarrolladores de aplicaciones deben realizar lo siguiente durante el proceso de instalación de la aplicación:

-   Instale IPv6 con el comando **netsh interface ipv6 install** . El Firewall de Windows protege el equipo del usuario del tráfico IPv6 entrante no solicitado de la misma manera que el tráfico IPv4.
-   Habilite Teredo con el comando **netsh interface ipv6 set teretor** .

Opcionalmente, puede probar si IPv6 se instala cada vez que se ejecuta la aplicación e instalar IPv6 y habilitar Teredo según sea necesario. También debe informar al usuario de que se está instalando IPv6 y que se está habilitando Teredo.

 

 
