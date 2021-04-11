---
description: Las siguientes funciones se implementan en el \_32.dll Ws2 y están pensadas para que las usen las aplicaciones que instalan los proveedores de transporte y servicio de espacio de nombres de Windows Sockets en un equipo.
ms.assetid: 3289737a-77b6-45d1-9c0a-3ed05b3475c2
title: Funciones de instalación y configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c72bb3ddaedb0b1d97c52d961293c161fe63c7ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275398"
---
# <a name="installation-and-configuration-functions"></a>Funciones de instalación y configuración

Las siguientes funciones se implementan en el \_32.dll Ws2 y están pensadas para que las usen las aplicaciones que instalan los proveedores de transporte y servicio de espacio de nombres de Windows Sockets en un equipo. Estas funciones no afectan a las aplicaciones que se están ejecutando actualmente, ni a los cambios realizados por estas funciones visibles para las aplicaciones que se están ejecutando actualmente.

Para todos los proveedores, un identificador de proveedor es un GUID generado por el desarrollador del proveedor (mediante la utilidad Uuidgen.exe) y proporcionado a Ws2 \_32.dll.



| Función                                                                      | Descripción                                                                                                                                              |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSCDeinstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider)                        | Quita un proveedor de servicios de transporte del registro.                                                                                                  |
| [**WSCDeinstallProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider32)                      | Quita el proveedor de servicios de transporte de 32 bits especificado del registro en una plataforma de 64 bits.                                                          |
| [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)                                | Recupera información acerca de los protocolos de transporte disponibles.                                                                                               |
| [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)                              | Recupera información acerca de los protocolos de transporte disponibles en el catálogo de 32 bits en plataformas de 64 bits.                                                     |
| [**WSCInstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider)                            | Registra un nuevo proveedor de servicios de transporte.                                                                                                              |
| [**WSCInstallProvider64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider64_32)                   | Registra un nuevo proveedor de servicios de transporte en las bases de datos de configuración del sistema de 32 bits y 64 bits en una plataforma de 64 bits.                               |
| [**WSCInstallProviderAndChains**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains)            | Registra un nuevo proveedor de servicios de transporte de 32 bits, así como su cadena de protocolo específica en la base de datos de configuración del sistema en una plataforma de 32 bits.   |
| [**WSCInstallProviderAndChains64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains64_32) | Registra un nuevo proveedor de transporte y su cadena de protocolo específica en las bases de datos de configuración del sistema de 32 bits y 64 bits en una plataforma de 64 bits. |



 

 

 



