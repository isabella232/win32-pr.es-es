---
description: El orden en que los proveedores de servicios de transporte se instalan inicialmente rige el orden en que se enumeran a través de WSCEnumProtocols y WSCEnumProtocols32 en la interfaz del proveedor de servicios, o a través de WSAEnumProtocols en la interfaz de aplicación. Lo que es más importante, este orden también rige el orden en que se tienen en cuenta los protocolos y los proveedores de servicios cuando un cliente solicita la creación de un socket en función de su familia de direcciones, tipo e identificador de protocolo.
ms.assetid: f76c63b3-9952-4aaf-813f-152f4838d3c4
title: Ordenación del proveedor de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 445fcc0cadafae8fd61ee2e34a872485b67466037c1dc71e34ab173156c8d9b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740586"
---
# <a name="service-provider-ordering"></a>Ordenación del proveedor de servicios

El orden en el que se instalan inicialmente los proveedores de servicios de transporte rige el orden en que se enumeran a través de [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) y [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) en la interfaz del proveedor de servicios, o a través de [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) en la interfaz de aplicación. Lo que es más importante, este orden también rige el orden en que se tienen en cuenta los protocolos y los proveedores de servicios cuando un cliente solicita la creación de un socket en función de su familia de direcciones, tipo e identificador de protocolo.

Windows Sockets 2 incluye un applet denominado Sporder.exe que permite que el catálogo de protocolos instalados se reordene de forma interactiva una vez instalados los protocolos. Winsock también incluye un archivo DLL auxiliar, Sporder.dll, que exporta una interfaz de procedimientos para reordenar protocolos. Esta interfaz de procedimiento consta de un único procedimiento denominado [**WSCWriteProviderOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder).

La definición de interfaz se puede importar en un programa de C o C++ mediante el archivo de incluir Sporder.h. El punto de entrada se puede vincular mediante el archivo lib Sporder.lib.

 

 



