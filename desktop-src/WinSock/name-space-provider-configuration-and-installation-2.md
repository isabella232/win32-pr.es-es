---
description: WSCEnableNSProviderWSCEnableNSProvider32WSCInstallNameSpaceWSCInstallNameSpace32WSCInstallNameSpaceExWSCInstallNameSpaceEx32WSCUnInstallNameSpaceWSCUnInstallNameSpace32WSCWriteNameSpaceOrderWSCWriteNameSpaceOrder32
ms.assetid: 3dd289fb-eebb-48b2-a887-eeb60322ab09
title: Configuración e instalación del proveedor de espacios de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c87de8fee4ccaea0fb6978037e1e41684b56267
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541547"
---
# <a name="namespace-provider-configuration-and-installation"></a>Configuración e instalación del proveedor de espacios de nombres

-   [**WSCEnableNSProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider)
-   [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32)
-   [**WSCInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace)
-   [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32)
-   [**WSCInstallNameSpaceEx**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex)
-   [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32)
-   [**WSCUnInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace)
-   [**WSCUnInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace32)
-   [**WSCWriteNameSpaceOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwritenamespaceorder)
-   [**WSCWriteNameSpaceOrder32**](/windows/desktop/api/Sporder/nf-sporder-wscwritenamespaceorder32)

Como se mencionó anteriormente, la aplicación de instalación de un proveedor de espacios de nombres debe llamar a [**WSCInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace) o [**WSCInstallNameSpaceEx**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex) para registrarse con Ws2 \_32.dll y proporcionar información de configuración estática. Para instalar en el catálogo de 32 bits en una plataforma de 64 bits, el proveedor de espacios de nombres debe llamar a [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) o [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32). El \_32.dll Ws2 usa esta información para realizar su función de enrutamiento y en su implementación de [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) y [**WSAEnumNameSpaceProvidersEx**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa). La función [**WSCUnInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace) se usa para quitar un proveedor de espacios de nombres del registro y la función [**WSCEnableNSProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider) se usa para alternar un proveedor entre los Estados activo e inactivo.

En una plataforma de 64 bits, [**WSCUnInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace32) y [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32) son funciones similares para tratar con el catálogo de 32 bits.

Los resultados de estas tres operaciones no son visibles para las aplicaciones que están actualmente cargadas y en ejecución. Solo las aplicaciones que empiecen a ejecutarse después de que se hayan producido estas operaciones se verán afectadas.

Esta arquitectura admite explícitamente la creación de instancias de varios proveedores de espacios de nombres dentro de un solo archivo DLL, sin embargo, cada uno de estos proveedores debe tener asignado un identificador de proveedor de espacio de nombres único (GUID) y se debe realizar una llamada independiente a [**WSCInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace) o [**WSCInstallNameSpaceEx**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex) para cada creación de instancias (en plataformas de 64 bits, las funciones para el catálogo de 32 bits son [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) [**y**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32) Dicho proveedor puede determinar la creación de instancias que se va a invocar porque el identificador del proveedor de espacio de nombres (NSP) aparece como un parámetro en cada función NSP.

 

 



