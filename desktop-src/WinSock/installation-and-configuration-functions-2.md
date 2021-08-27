---
description: Las siguientes funciones se implementan en el32.dll Ws2 y están diseñadas para que las usen las aplicaciones que instalan proveedores de servicios de espacio de nombres y transporte de Windows Sockets en \_ un equipo.
ms.assetid: 3289737a-77b6-45d1-9c0a-3ed05b3475c2
title: Funciones de instalación y configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0731eff882c614c19c20d8323d012a7656fc2d8c15072aaafef3d7c91e46e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097865"
---
# <a name="installation-and-configuration-functions"></a>Funciones de instalación y configuración

Las siguientes funciones se implementan en el32.dll Ws2 y están diseñadas para que las usen las aplicaciones que instalan proveedores de servicios de espacio de nombres y transporte de Windows Sockets en \_ un equipo. Estas funciones no afectan a las aplicaciones que se están ejecutando actualmente ni a los cambios realizados por estas funciones visibles para las aplicaciones que se están ejecutando actualmente.

Para todos los proveedores, un identificador de proveedor es un GUID generado por el desarrollador del proveedor (mediante la utilidad Uuidgen.exe) y proporcionado a Ws2 \_32.dll.



| Función                                                                      | Descripción                                                                                                                                              |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSCDeinstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider)                        | Quita un proveedor de servicios de transporte del Registro.                                                                                                  |
| [**WSCDeinstallProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider32)                      | Quita el proveedor de servicios de transporte de 32 bits especificado del Registro en una plataforma de 64 bits.                                                          |
| [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)                                | Recupera información sobre los protocolos de transporte disponibles.                                                                                               |
| [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)                              | Recupera información sobre los protocolos de transporte disponibles en el catálogo de 32 bits en plataformas de 64 bits.                                                     |
| [**WSCInstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider)                            | Registra un nuevo proveedor de servicios de transporte.                                                                                                              |
| [**WSCInstallProvider64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider64_32)                   | Registra un nuevo proveedor de servicios de transporte en las bases de datos de configuración del sistema de 32 y 64 bits en una plataforma de 64 bits.                               |
| [**WSCInstallProviderAndChains**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains)            | Registra un nuevo proveedor de servicios de transporte de 32 bits, así como sus cadenas de protocolo específicas en la base de datos de configuración del sistema en una plataforma de 32 bits.   |
| [**WSCInstallProviderAndChains64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains64_32) | Registra un nuevo proveedor de transporte y sus cadenas de protocolo específicas en las bases de datos de configuración del sistema de 32 y 64 bits en una plataforma de 64 bits. |



 

 

 



