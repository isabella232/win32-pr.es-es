---
description: El32.dll Ws2 carga el archivo DLL de interfaz del proveedor de servicios en el sistema mediante los mecanismos de carga de biblioteca dinámica estándar de Microsoft Windows e inicializa mediante una llamada \_ a WSPStartup.
ms.assetid: 6df28d93-8757-45b3-8f05-86381c3be64e
title: Inicialización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76570fe401fb064047581a60a4340daf71b5a583034baf67b8e9b830ccae0dc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097875"
---
# <a name="initialization"></a>Inicialización

El *32.dll\_ Ws2* carga el archivo DLL de interfaz del proveedor de servicios en el sistema mediante los mecanismos de carga de biblioteca dinámica estándar de Microsoft Windows e inicializa mediante una llamada a [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup). Esto lo desencadena normalmente una aplicación que llama a [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) o [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) para crear un nuevo socket que se va a asociar a un proveedor de servicios cuyo archivo DLL de interfaz no está cargado actualmente en la memoria. Ws *\_32.dll2* almacena la ruta de acceso al archivo DLL de interfaz de cada proveedor de servicios en el momento en que se instala el proveedor de servicios. Consulte [Funciones de instalación y configuración](installation-and-configuration-functions-2.md) para obtener más información.

Con el tiempo, pueden existir versiones diferentes para los archivos DLL, las aplicaciones y los proveedores de servicios de Winsock. Las nuevas versiones pueden definir nuevas características y nuevos parámetros para estructuras de datos y parámetros de bits, etc. Por lo tanto, los números de versión indican cómo interpretar varias estructuras de datos.

Para permitir la combinación óptima y la coincidencia de diferentes versiones de aplicaciones, versiones del propio Ws232.dll y versiones de proveedores de servicios de distintos proveedores, el SPI proporciona un mecanismo de negociación de versiones para su uso entre el32.dll\_ *de Ws2 \_* y los proveedores de servicios. [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup)controla esta negociación de versión. Básicamente, el *32.dll\_ Ws2* pasa al proveedor de servicios los números de versión más altos con los que es compatible. El proveedor de servicios lo compara con su propio intervalo admitido de números de versión. Si estos intervalos se superponen, el proveedor de servicios devuelve un valor dentro de la parte superpuesta del intervalo como resultado de la negociación. Normalmente, debe ser el valor más alto posible. Si los intervalos no se superponen, las dos partes son incompatibles y la función devuelve un error.

[**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) debe ser llamado al menos una vez por cada proceso de cliente y Ws2 puede llamarlo varias veces32.dll \_ otras entidades. Se debe llamar a [**WSPCleanup correspondiente**](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) para cada llamada **de WSPStartup** correcta. El proveedor de servicios debe mantener un recuento de referencias por proceso. En cada **llamada de WSPStartup,** el autor de la llamada puede especificar cualquier número de versión compatible con el archivo DLL de SP.

Un proveedor de servicios debe almacenar el puntero a la tabla de distribución upcall del cliente que se recibe como un [**parámetro WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) por proceso. Si un proceso determinado llama a **WSPStartup** varias veces, el proveedor de servicios solo debe usar el puntero de tabla de distribución proporcionado más recientemente.

Como parte del proceso de inicialización del proveedor de servicios, Ws232.dll recupera la tabla de distribución del proveedor de servicios a través del parámetro lpProcTable para obtener puntos de entrada al resto de las funciones SPI especificadas en este \_ documento. 

El uso de una tabla de distribución (en lugar de los mecanismos dll habituales para acceder a los puntos de entrada) tiene dos propósitos:

-   Es más práctico para el32.dll Ws2, ya que se puede realizar una sola llamada para detectar todo el \_ conjunto de puntos de entrada.
-   Permite que los proveedores de servicios por capas formados en cadenas de protocolo funcionen de forma más eficaz.

## <a name="initializing-protocol-chains"></a>Inicialización de cadenas de protocolo

En el momento en que se instala la estructura INFO de [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para una cadena de protocolos, también se especifica la ruta de acceso al primer proveedor en capas de la cadena. Cuando se inicializa una cadena de protocolos, el32.dll Ws2 usa esta ruta de acceso para cargar el archivo DLL del proveedor y, a continuación, invoca \_ [**a WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup). Dado **que WSPStartup** incluye un puntero a la estructura INFO de **WSAPROTOCOL \_** de la cadena como uno de sus parámetros, los proveedores por capas pueden determinar en qué tipo de cadena se inicializan y la identidad de la siguiente capa inferior de la cadena. A su vez, un proveedor por capas cargaría el siguiente proveedor de protocolos en la cadena e inicializaría con una llamada a **WSPStartup,** etc. Siempre que la siguiente capa inferior sea otro proveedor por capas, se debe hacer referencia a la estructura INFO de **WSAPROTOCOL \_** de la cadena en la **llamada a WSPStartup.** Cuando la siguiente capa inferior es un protocolo base (que significa el final de la cadena), la estructura INFO de **WSAPROTOCOL \_** de la cadena ya no se propaga hacia abajo. En su lugar, la capa actual debe hacer referencia a una estructura **\_ INFO de WSAPROTOCOL** que se corresponda con el protocolo que debe usar el proveedor base. Por lo tanto, el proveedor base no tiene ninguna noción de estar implicado en una cadena de protocolo.

La tabla de distribución proporcionada por cualquier proveedor por capas determinado duplicará, en muchos casos, los puntos de entrada de un proveedor subyacente. El proveedor por capas solo insertaría sus propios puntos de entrada para las funciones en las que tenía que estar directamente implicado. Sin embargo, tenga en cuenta que es imperativo que un proveedor por capas no modifique el contenido de la tabla de llamada superior que recibió al llamar a [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) en la siguiente capa inferior de una cadena de protocolo. Estas llamadas de llamada se deben realizar directamente en la dll Windows Sockets 2.

 

 
