---
description: Para que un protocolo de transporte sea accesible a través de Windows Sockets, debe instalarse correctamente en el sistema y registrarse con Windows Sockets.
ms.assetid: 0f0b22e4-81b7-43a7-bc2f-7124fa32d925
title: Instalación y configuración de transporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1ec75810790df0d9373e8f3ee184f2dbd51d9bb5c37d7721097febe23a8aee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733245"
---
# <a name="transport-configuration-and-installation"></a>Instalación y configuración de transporte

Para que un protocolo de transporte sea accesible a través de Windows Sockets, debe instalarse correctamente en el sistema y registrarse con Windows Sockets. Cuando se instala un proveedor de servicios de transporte invocando el programa de instalación de un proveedor, se debe agregar información de configuración a una base de datos de configuración para proporcionar a Ws232.dll información necesaria sobre el proveedor de \_ servicios. El32.dll Ws2 exporta varias funciones de \_ instalación, [**WSCInstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider) y [**WSCInstallProviderAndChains,**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains)para que el programa de instalación del proveedor proporcione la información pertinente sobre el proveedor de servicios que se va a instalar. Esta información incluye, por ejemplo, el nombre y la ruta de acceso a la DLL del proveedor de servicios y una lista de estructuras info de [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) que este proveedor puede admitir. El32.dll Ws2 también proporciona una \_ función, [**WSCDeinstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider), para que el programa de desinstalación de un proveedor quite toda la información pertinente de la base de datos de configuración mantenida por el proveedor de \_ Ws232.dll. La ubicación y el formato exactos de esta información de configuración son privados para la32.dll Ws2 y solo se pueden manipular mediante las \_ funciones mencionadas anteriormente.

En las plataformas de 64 bits, hay funciones similares que funcionan en catálogos de 32 y 64 bits. Estas funciones incluyen [**WSCInstallProvider64 \_ 32,**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider64_32) [**WSCInstallProviderAndChains64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains64_32)y [**WSCDeinstallProvider32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider32)

El orden en que los proveedores de servicios de transporte se instalan inicialmente rige el orden en que se enumeran a través de [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) y [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) en la interfaz del proveedor de servicios, o a través de [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) en la interfaz de aplicación. Lo que es más importante, este orden también rige el orden en que se tienen en cuenta los protocolos y los proveedores de servicios cuando un cliente solicita la creación de un socket en función de su familia de direcciones, tipo e identificador de protocolo. Windows Sockets 2 incluye un applet denominado Sporder.exe que permite que el catálogo de protocolos instalados se reordene de forma interactiva después de que ya se hayan instalado los protocolos. Windows Sockets 2 también incluye un archivo DLL auxiliar, Sporder.dll, que exporta una interfaz de procedimientos para reordenar protocolos. Esta interfaz de procedimiento consta de un único procedimiento denominado [**WSCWriteProviderOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder).

## <a name="installing-layered-protocols-and-protocol-chains"></a>Instalación de protocolos por capas y cadenas de protocolo

La estructura INFO de [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) proporcionada con cada protocolo que se va a instalar indica si el protocolo es un protocolo base, un protocolo por capas o una cadena de protocolo. El valor del *parámetro ProtocolChain.ChainLen* se interpreta como se muestra en la tabla siguiente.

| Value | Significado                                           |
|-------|---------------------------------------------------|
| 0     | Protocolo por capas.                                 |
| 1     | Protocolo base (o cadena con un solo componente). |
| >1 | Cadena de protocolos.                                   |



 

La instalación de cadenas de protocolo solo puede producirse después de una instalación correcta de todos los componentes constituyentes (protocolos base y protocolos por capas). La estructura INFO de [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para una cadena de protocolo usa el parámetro *ProtocolChain* para describir la longitud de la cadena y la identidad de cada componente. Los protocolos individuales que son una cadena se enumeran en orden en la matriz ProtocolChain.ChainEntries, con el elemento cero de la matriz correspondiente al primer proveedor por capas. Los protocolos se identifican por sus valores *CatalogEntryID,* que se asignan mediante el32.dll de Ws2 en el momento de la instalación del protocolo, y se pueden encontrar en la estructura INFO de \_ **WSAPROTOCOL \_** para cada protocolo.

Se deben elegir los valores de los parámetros restantes de la estructura INFO de [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) de la cadena de protocolos para reflejar los atributos e identificadores que mejor caracterizan la cadena de protocolos en su conjunto. Al seleccionar estos valores, los desarrolladores deben tener en cuenta que las comunicaciones a través de cadenas de protocolo solo pueden producirse cuando ambos puntos de conexión tienen instaladas cadenas de protocolo compatibles y que las aplicaciones deben ser capaces de reconocer la estructura info de **WSAPROTOCOL correspondiente. \_**

Cuando se instala un protocolo base, no es necesario realizar ninguna entrada en la *matriz ProtocolChain.ChainEntries.* Se entiende implícitamente que el único componente de esta cadena ya está identificado en el parámetro *CatalogEntryID* de la misma estructura [**\_ INFO de WSAPROTOCOL.**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Tenga en cuenta también que es posible que las cadenas de protocolo no incluyan varias instancias del mismo protocolo en capas.

 

 
