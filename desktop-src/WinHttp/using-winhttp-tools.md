---
description: Para los comandos que puede usar en Windows Vista y versiones posteriores para configurar el proxy y la traza para Windows HTTP, vea comandos Netsh para el protocolo de transferencia de hipertexto de Windows (WINHTTP).
ms.assetid: 81f6b25e-ea14-4dbd-a715-926db7cf90e7
title: Uso de las herramientas de WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e402962dc34cbf654fa8db49f96b86e7406a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715166"
---
# <a name="using-winhttp-tools"></a>Uso de las herramientas de WinHTTP

Para los comandos que puede usar en Windows Vista y versiones posteriores para configurar el proxy y la traza para Windows HTTP, vea [comandos Netsh para el protocolo de transferencia de hipertexto de Windows (WinHTTP)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731131(v=ws.10)).

**Windows Server 2003 y versiones anteriores:** Hay varias herramientas disponibles para ayudarle a escribir y depurar las aplicaciones. Se explican en los temas siguientes:

-   [WinHttpCfg.exe, una herramienta de configuración de certificados](winhttpcertcfg-exe--a-certificate-configuration-tool.md) permite a los administradores instalar y configurar certificados de cliente en cualquier [*almacén de certificados*](glossary.md) al que pueda tener acceso la cuenta del administrador de aplicaciones web (IWAM) de servidor de Internet. La herramienta también elimina la necesidad de hacer nada especial en cuentas como la cuenta IWAM para obtener acceso a los certificados cuando se utiliza Active Server páginas (ASP).
-   [Netsh.exe o ProxyCfg.exe Proxy herramientas de configuración](proxycfg-exe--a-proxy-configuration-tool.md) se pueden usar para configurar servidores proxy con los servicios http de Microsoft Windows (WinHTTP).
-   [WinHttpTraceCfg, una herramienta de configuración de seguimiento](winhttptracecfg-exe--a-trace-configuration-tool.md) proporciona la capacidad de supervisar las funciones WinHTTP y el tráfico de red correspondiente. La depuración de aplicaciones que usan protocolos de conexión cifrados, como Capa de sockets seguros (SSL), impide el examen de paquetes en la capa de transporte de red y requiere la capacidad de interceptar el tráfico entre el cliente y el servidor una vez descifrado. El servicio de seguimiento de WinHTTP tiene una serie de funciones para interceptar el flujo de tráfico entre el cliente y el servidor.

 

 
