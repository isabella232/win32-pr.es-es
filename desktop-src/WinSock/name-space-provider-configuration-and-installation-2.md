---
description: WSCEnableNSProviderWSCEnableNSProvider32WSCInstallNameSpaceWSCInstallNameSpace32WSCInstallNameSpaceExWSCInstallNameSpaceEx32WSCUnInstallNameSpaceWSCUnInstallNameSpace32WSCWriteNameSpaceOrderWSCWriteNameSpaceOrder32
ms.assetid: 3dd289fb-eebb-48b2-a887-eeb60322ab09
title: Instalación y configuración del proveedor de espacios de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d420e9322d1d39816cdb9b3812b23b1e7e72e945c3d0f2ef95e7edff77f12276
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121375"
---
# <a name="namespace-provider-configuration-and-installation"></a>Instalación y configuración del proveedor de espacios de nombres

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

Como se mencionó anteriormente, la aplicación de instalación de un proveedor de espacios de nombres debe llamar a [**WSCInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace) o [**WSCInstallNameSpaceEx**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex) para registrarse con el32.dll Ws2 y proporcionar información de configuración \_ estática. Para instalar en el catálogo de 32 bits en una plataforma de 64 bits, el proveedor de espacios de nombres debe llamar a [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) o [**WSCInstallNameSpaceEx32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32) El32.dll Ws2 usa esta información para realizar su función de enrutamiento y en su implementación de \_ [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) y [**WSAEnumNameSpaceProvidersEx**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa). La función [**WSCUnInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace) se usa para quitar un proveedor de espacios de nombres del Registro y la función [**WSCEnableNSProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider) se usa para alternar un proveedor entre los estados activo e inactivo.

En una plataforma de 64 bits, [**WSCUnInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace32) y [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32) son funciones similares para tratar con el catálogo de 32 bits.

Los resultados de estas tres operaciones no son visibles para las aplicaciones que se cargan y ejecutan actualmente. Solo las aplicaciones que comienzan a ejecutarse después de que se han producido estas operaciones se verán afectadas por ellas.

Esta arquitectura admite explícitamente la creación de instancias de varios proveedores de espacios de nombres dentro de un único archivo DLL, pero cada uno de estos proveedores debe tener asignado un identificador de proveedor de espacio de nombres único (GUID) y debe producirse una llamada independiente a [**WSCInstallNameSpace o**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace) [**WSCInstallNameSpaceEx**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex) para cada creación de instancias (en plataformas de 64 bits, las funciones del catálogo de 32 bits son [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) y [**WSCInstallNameSpaceEx32).**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32) Este tipo de proveedor puede determinar qué creación de instancias se invoca porque el identificador del proveedor de espacios de nombres (NSP) aparece como un parámetro en cada función de NSP.

 

 



