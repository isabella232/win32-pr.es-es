---
description: En Windows XP posterior, se proporciona una nueva herramienta de línea de comandos para configurar y administrar IPv4. Esta herramienta usa el &\# 0034;netsh interface ip&0034; para configurar y administrar \# IPv4.
ms.assetid: d27eb0c2-4ae0-42d1-b92e-055a1c232e1c
title: Usar IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f759d938ebebbc0ddfbb2326dfb10932c16310a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361306"
---
# <a name="using-ipv6"></a>Usar IPv6

En Windows XP posterior, se proporciona una nueva herramienta de línea de comandos para configurar y administrar IPv4. Esta herramienta usa el comando "netsh interface ip" para configurar y administrar IPv4.

En Windows XP con Service Pack 1 (SP1) y versiones posteriores, esta nueva herramienta de línea de comandos se mejoró para admitir la configuración y administración de IPv6. Esta herramienta mejorada es el comando "netsh interface ipv6". Los cambios de configuración realizados mediante Netsh.exe comandos son permanentes y no se pierden cuando se reinicia el equipo o el protocolo IPv6.

El siguiente comando está disponible en Windows XP con SP1 y versiones posteriores para consultar y configurar IPv6 en un equipo local:

-   [Netsh.exe](netsh-exe.md)

Antes de Windows XP con Service Pack 1 (SP1), la configuración y administración de IPv6 usaba varias herramientas de línea de comandos anteriores para configurar y administrar IPv6. Con estas herramientas anteriores, los cambios de IPv6 no son permanentes y se pierden cuando se reinicia el equipo o el protocolo IPv6.

Los siguientes comandos anteriores están disponibles en Windows XP

-   [Net.exe](net-exe-2.md)
-   [Ipv6.exe](ipv6-exe-2.md)
-   [Ipsec6.exe](ipsec6-exe-2.md)

Estas herramientas anteriores también se proporcionaron en IPv6 Technology Preview para Windows 2000

Los cambios de configuración que usan estas herramientas anteriores se pueden mantener si se colocan como líneas de comandos en un archivo de script de comandos (.cmd) que se ejecuta después de reiniciar el equipo o el protocolo IPv6. Para restablecer automáticamente los cambios de configuración después del reinicio, es posible usar Windows Scheduled Tasks para ejecutar el archivo .cmd cuando se inicia el equipo.

Estas herramientas anteriores no se proporcionan en Windows Server 2003 y versiones posteriores. La herramienta "netsh interface ipv6" se proporciona para configurar y administrar IPv6 desde la línea de comandos en Windows Server 2003 y versiones posteriores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Protocolo de Internet versión 6 (IPv6)](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[Guía de IPv6 para aplicaciones Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[IPv6 Technology Preview para Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> </dl>

 

 



