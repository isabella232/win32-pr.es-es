---
description: El orden en que se instalan inicialmente los proveedores de servicios de transporte rige el orden en que se enumeran a través de WSCEnumProtocols y WSCEnumProtocols32 en la interfaz del proveedor de servicios o a través de WSAEnumProtocols en la interfaz de la aplicación. Lo que es más importante, este orden también rige el orden en el que se tienen en cuenta los protocolos y los proveedores de servicios cuando un cliente solicita la creación de un socket en función de su familia de direcciones, el tipo y el identificador de protocolo.
ms.assetid: f76c63b3-9952-4aaf-813f-152f4838d3c4
title: Ordenación del proveedor de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c23d9357d30c94b084bf6288013c38a2d46a4b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908571"
---
# <a name="service-provider-ordering"></a>Ordenación del proveedor de servicios

El orden en que se instalan inicialmente los proveedores de servicios de transporte rige el orden en que se enumeran a través de [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) y [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) en la interfaz del proveedor de servicios o a través de [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) en la interfaz de la aplicación. Lo que es más importante, este orden también rige el orden en el que se tienen en cuenta los protocolos y los proveedores de servicios cuando un cliente solicita la creación de un socket en función de su familia de direcciones, el tipo y el identificador de protocolo.

Windows Sockets 2 incluye un applet denominado Sporder.exe que permite que el catálogo de protocolos instalados se reordene de forma interactiva una vez que ya se hayan instalado los protocolos. Winsock también incluye un archivo DLL auxiliar, Sporder.dll, que exporta una interfaz de procedimientos para la reordenación de protocolos. Esta interfaz de procedimientos consta de un único procedimiento denominado [**WSCWriteProviderOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder).

La definición de la interfaz se puede importar en un programa de C o C++ por medio del archivo de inclusión sporder. h. El punto de entrada puede estar vinculado por medio del archivo lib sporder. lib.

 

 



