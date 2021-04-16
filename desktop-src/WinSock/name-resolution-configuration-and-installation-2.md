---
description: Para que un proveedor de espacios de nombres sea accesible a través de Windows Sockets, debe estar instalado correctamente en el sistema y registrarse con Windows Sockets.
ms.assetid: c73baf62-b862-476c-b381-be00699e78ca
title: Instalación y configuración de la resolución de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423e0ca7c9c5290a040a17e0f1ded2a97a1aed15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677369"
---
# <a name="name-resolution-configuration-and-installation"></a>Instalación y configuración de la resolución de nombres

Para que un proveedor de espacios de nombres sea accesible a través de Windows Sockets, debe estar instalado correctamente en el sistema y registrarse con Windows Sockets. Cuando se instala un proveedor de espacios de nombres mediante la invocación del programa de instalación de un proveedor, se debe agregar información de configuración a una base de datos de configuración para proporcionar a Ws2 \_32.dll información necesaria relacionada con el proveedor de servicios. El \_32.dll Ws2 exporta [**WSCInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace) para que lo use el programa de instalación del proveedor. Esta función se usa para proporcionar información relevante sobre el proveedor de servicios que se va a instalar. Esta información incluye lo siguiente:

-   Nombre del proveedor: una cadena que representa el proveedor que se va a mostrar en el panel de control.
-   Versión del proveedor: la versión de este proveedor.
-   Ruta de acceso del proveedor: un nombre de ruta de acceso al archivo DLL del proveedor.
-   Espacio de nombres: el espacio de nombres que admite el proveedor.
-   GUID de proveedor: un número único, proporcionado por el proveedor que representa esta combinación de proveedor/espacio de nombres. Se utiliza como clave para todas las referencias subsiguientes a este proveedor y para la desinstalación. Estos valores se crean mediante la utilidad Uuidgen.exe.
-   Almacena todas las marcas, una marca que indica si este proveedor de espacio de nombres será responsable de conservar toda la información de esquema de clase de servicio para todas las clases de servicio. Si existe un proveedor de este tipo, \_ no es necesario que la32.dll Ws2 tenga que consultar esta información en cada proveedor de espacio de nombres individual.

En Windows Vista y versiones posteriores, se proporciona una función [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32) mejorada que permite al proveedor de espacios de nombres pasar un BLOB adicional de datos específico al espacio de nombres.

En las plataformas de 64 bits, se proporcionan funciones similares [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) y [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32) para instalar un espacio de nombres en el catálogo de 32 bits.

El \_32.dll Ws2 también proporciona una función, [**WSCUnInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace), para que el programa de desinstalación de un proveedor Quite toda la información relevante de la base de datos de configuración. La ubicación y el formato exactos de esta información de configuración son privados para el \_32.dll Ws2 y solo las funciones mencionadas anteriormente pueden manipularlas.

En las plataformas de 64 bits, se proporciona una función [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) similar para desinstalar un espacio de nombres en el catálogo de 32 bits.

En cualquier momento, se considera que un proveedor de espacios de nombres está activo o inactivo, con esta configuración controlada a través de las funciones [**WSCEnableNSProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider) y [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32) . Los proveedores de espacios de nombres que están inactivos siguen apareciendo cuando se enumeran (mediante las funciones [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa), [**WSAEnumNameSpaceProvidersEx**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa), [**WSCEnumNameSpaceProviders32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceproviders32)y [**WSCEnumNameSpaceProvidersEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32) ), pero el \_32.dll Ws2 no enrutará ninguna operación de registro de servicio o consulta a estos proveedores. Esta capacidad puede ser útil en situaciones en las que más de uno de los proveedores de espacio de nombres instalados puede admitir un espacio de nombres determinado.

Cuando se hace referencia a varios proveedores de espacios de nombres en una sola función de la API, no se especifica el orden en el que se enrutan las operaciones de registro y las consultas a los proveedores de espacios de nombres. El orden no está relacionado con el orden en el que se instalan los proveedores de espacios de nombres. Hay dos formas de controlar qué proveedores de espacio de nombres se usan para resolver una consulta de nombre. En primer lugar, las funciones [**WSCEnableNSProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider) y [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32) se pueden usar para habilitar y deshabilitar los espacios de nombres de forma persistente en todo el equipo. En segundo lugar, las aplicaciones pueden dirigir una consulta individual a un proveedor determinado especificando el GUID de identificación del proveedor como parte de la consulta.

 

 



