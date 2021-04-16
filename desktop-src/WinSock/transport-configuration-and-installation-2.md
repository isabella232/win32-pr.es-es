---
description: Para que un protocolo de transporte sea accesible a través de Windows Sockets, debe estar instalado correctamente en el sistema y estar registrado en Windows Sockets.
ms.assetid: 0f0b22e4-81b7-43a7-bc2f-7124fa32d925
title: Instalación y configuración de transporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea980740f727e39338c7568f4cc30a961b5484df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705590"
---
# <a name="transport-configuration-and-installation"></a>Instalación y configuración de transporte

Para que un protocolo de transporte sea accesible a través de Windows Sockets, debe estar instalado correctamente en el sistema y estar registrado en Windows Sockets. Cuando un proveedor de servicios de transporte se instala mediante la invocación del programa de instalación de un proveedor, se debe agregar información de configuración a una base de datos de configuración para proporcionar a Ws2 \_32.dll información necesaria relacionada con el proveedor de servicios. El \_32.dll Ws2 exporta varias funciones de instalación, [**WSCInstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider) y [**WSCInstallProviderAndChains**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains), para que el programa de instalación del proveedor proporcione la información pertinente sobre el proveedor de servicios que se va a instalar. Esta información incluye, por ejemplo, el nombre y la ruta de acceso al archivo DLL del proveedor de servicios y una lista de estructuras de [**\_ información WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) que este proveedor puede admitir. El \_32.dll Ws2 también proporciona una función, [**WSCDeinstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider), para que el programa de desinstalación de un proveedor Quite toda la información relevante de la base de datos de configuración que mantiene el32.dll de Ws2 \_ . La ubicación y el formato exactos de esta información de configuración son privados para el \_32.dll Ws2 y solo las funciones mencionadas anteriormente pueden manipularlas.

En las plataformas de 64 bits, existen funciones similares que operan en catálogos de 32 y 64 bits. Estas funciones incluyen [**WSCInstallProvider64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider64_32), [**WSCInstallProviderAndChains64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains64_32)y [**WSCDeinstallProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider32).

El orden en que se instalan inicialmente los proveedores de servicios de transporte rige el orden en que se enumeran a través de [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) y [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) en la interfaz del proveedor de servicios o a través de [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) en la interfaz de la aplicación. Lo que es más importante, este orden también rige el orden en el que se tienen en cuenta los protocolos y los proveedores de servicios cuando un cliente solicita la creación de un socket en función de su familia de direcciones, el tipo y el identificador de protocolo. Windows Sockets 2 incluye un applet denominado Sporder.exe que permite que el catálogo de protocolos instalados se reordene de forma interactiva una vez que ya se hayan instalado los protocolos. Windows Sockets 2 también incluye un archivo DLL auxiliar, Sporder.dll, que exporta una interfaz de procedimientos para la reordenación de protocolos. Esta interfaz de procedimientos consta de un único procedimiento denominado [**WSCWriteProviderOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder).

## <a name="installing-layered-protocols-and-protocol-chains"></a>Instalación de protocolos en capas y cadenas de protocolo

La estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) proporcionada con cada protocolo que se va a instalar indica si el protocolo es un protocolo base, un protocolo en capas o una cadena de protocolos. El valor del parámetro *ProtocolChain. ChainLen* se interpreta como se muestra en la tabla siguiente.

| Value | Significado                                           |
|-------|---------------------------------------------------|
| 0     | Protocolo superpuesto.                                 |
| 1     | Protocolo base (o cadena con un solo componente). |
| >1 | Cadena de protocolos.                                   |



 

La instalación de cadenas de protocolo solo puede producirse después de una instalación correcta de todos los componentes constituyentes (protocolos base y protocolos en capas). La estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para una cadena de protocolos usa el parámetro *ProtocolChain* para describir la longitud de la cadena y la identidad de cada componente. Los protocolos individuales que componen una cadena se enumeran en orden en la matriz ProtocolChain. ChainEntries, con el elemento inicial de la matriz correspondiente al primer proveedor superpuesto. Los protocolos se identifican por sus valores de *CatalogEntryID* , que son asignados por el32.dll de Ws2 en el momento de la \_ instalación del protocolo y se pueden encontrar en la estructura de **\_ información de WSAPROTOCOL** para cada protocolo.

Los valores de los parámetros restantes en la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) de la cadena de protocolos deben elegirse para reflejar los atributos y los identificadores que mejor caracterizan la cadena de protocolos en conjunto. Al seleccionar estos valores, los desarrolladores deben tener en cuenta que las comunicaciones a través de cadenas de protocolo solo se pueden producir cuando ambos extremos tienen cadenas de protocolo compatibles instaladas y las aplicaciones deben ser capaces de reconocer la estructura de **\_ información de WSAPROTOCOL** correspondiente.

Cuando se instala un protocolo base, no es necesario realizar ninguna entrada en la matriz *ProtocolChain. ChainEntries* . Se entiende implícitamente que el componente único de esta cadena ya está identificado en el parámetro *CatalogEntryID* de la misma estructura [**de \_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) . Tenga en cuenta también que las cadenas de protocolos no pueden incluir varias instancias del mismo protocolo en capas.

 

 
