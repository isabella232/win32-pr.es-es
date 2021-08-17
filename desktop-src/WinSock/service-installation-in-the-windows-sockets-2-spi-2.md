---
description: Instalación del servicio en Windows Sockets 2 (Winsock) SPI.
ms.assetid: a303fbcf-9122-422a-9b12-d00a5df0fc0f
title: Instalación del servicio en Windows Sockets 2 SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faad2431add9b20ebd3358c48469f382596b658de1339525b147b094a7c3786c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740529"
---
# <a name="service-installation-in-the-windows-sockets-2-spi"></a>Instalación del servicio en Windows Sockets 2 SPI

-   [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass)
-   [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass)
-   [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice)

Cuando la clase de servicio necesaria aún no existe, un cliente SPI de espacio de nombres usa [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass) para instalar una nueva clase de servicio al proporcionar un nombre de clase de servicio, un GUID para el identificador de clase de servicio y una serie de estructuras [**WSANSCLASSINFO.**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) Estas estructuras son específicas de un espacio de nombres determinado y suministran valores comunes, como los números de puerto TCP recomendados o los identificadores sap de NetWare. Una clase de servicio se puede quitar llamando a [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass) y suministrando el GUID correspondiente al identificador de clase.

Una vez que existe una clase de servicio, se pueden instalar o quitar instancias específicas de un servicio a través [**de NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice). Esta función toma una [**estructura WSAQUERYSET como**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) parámetro de entrada junto con un código de operación y marcas de operación. El código de operación indica si el servicio se está instalando o quitando. La estructura **WSAQUERYSET** proporciona toda la información pertinente sobre el servicio, incluido el identificador de clase de servicio, el nombre de servicio (para esta instancia), el identificador de espacio de nombres aplicable y la información de protocolo, y un conjunto de direcciones de transporte en las que escucha el servicio.

 

 



