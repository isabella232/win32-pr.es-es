---
description: Instalación del servicio en el SPI de Windows Sockets 2 (Winsock).
ms.assetid: a303fbcf-9122-422a-9b12-d00a5df0fc0f
title: Instalación del servicio en Windows Sockets 2 SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9028f35c21cc7055e8b8dde060c1c178dbf76715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696930"
---
# <a name="service-installation-in-the-windows-sockets-2-spi"></a>Instalación del servicio en Windows Sockets 2 SPI

-   [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass)
-   [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass)
-   [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice)

Cuando la clase de servicio necesaria todavía no existe, un cliente de espacio de nombres SPI usa [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass) para instalar una nueva clase de servicio proporcionando un nombre de clase de servicio, un GUID para el identificador de clase de servicio y una serie de estructuras [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) . Estas estructuras son específicas de un espacio de nombres determinado y proporcionan valores comunes, como los números de puerto TCP recomendados o los identificadores de SAP SAP. Se puede quitar una clase de servicio llamando a [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass) y proporcionando el GUID correspondiente al identificador de clase.

Una vez que existe una clase de servicio, se pueden instalar o quitar instancias específicas de un servicio a través de [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice). Esta función toma una estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) como parámetro de entrada junto con un código de operación y marcas de operación. El código de operación indica si el servicio se está instalando o quitando. La estructura **WSAQUERYSET** proporciona toda la información relevante sobre el servicio, incluido el identificador de clase de servicio, el nombre de servicio (para esta instancia), la información del protocolo y el identificador de espacio de nombres aplicable, y un conjunto de direcciones de transporte en el que el servicio realiza escuchas.

 

 



