---
description: El \_32.dll Ws2 carga el archivo dll de la interfaz del proveedor de servicios en el sistema mediante el uso de los mecanismos estándar de carga de biblioteca dinámica de Microsoft Windows y lo inicializa llamando a WSPStartup.
ms.assetid: 6df28d93-8757-45b3-8f05-86381c3be64e
title: Inicialización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d6ef10db421ef15f2bb94eb67e96fc2cfc5924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705608"
---
# <a name="initialization"></a>Inicialización

El *\_32.dllWs2* carga el archivo dll de la interfaz del proveedor de servicios en el sistema mediante el uso de los mecanismos estándar de carga de biblioteca dinámica de Microsoft Windows y lo inicializa llamando a [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup). Normalmente, esto lo desencadena una aplicación que llama a [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) o [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) para crear un nuevo socket que se va a asociar a un proveedor de servicios cuya dll de interfaz no está cargada actualmente en la memoria. La ruta de acceso a la DLL de interfaz de cada proveedor de servicios se almacena mediante el *\_32.dllWs2* en el momento en que se instala el proveedor de servicios. Consulte [funciones de instalación y configuración](installation-and-configuration-functions-2.md) para obtener más información.

Con el tiempo, pueden existir diferentes versiones de los archivos dll, las aplicaciones y los proveedores de servicios de Winsock. Las nuevas versiones pueden definir nuevas características y nuevos parámetros para estructuras de datos y parámetros de bits, etc. Por lo tanto, los números de versión indican cómo interpretar varias estructuras de datos.

Para permitir la combinación y coincidencia óptimas de distintas versiones de aplicaciones, las versiones de Ws2 \_32.dll y las versiones de los proveedores de servicios de diferentes proveedores, el SPI proporciona un mecanismo de negociación de la versión para su uso entre el *\_32.dllWs2* y los proveedores de servicios. Esta negociación de versión se controla mediante [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup). Básicamente, el *\_32.dllWs2* pasa al proveedor de servicios los números de versión más altos con los que es compatible. El proveedor de servicios lo compara con su propio intervalo de versión compatible. Si estos intervalos se superponen, el proveedor de servicios devuelve un valor dentro de la parte que se superpone del intervalo como resultado de la negociación. Normalmente, debe ser el valor más alto posible. Si los intervalos no se superponen, las dos partes son incompatibles y la función devuelve un error.

Se debe llamar a [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) al menos una vez por cada proceso de cliente y se le puede llamar varias veces por parte de Ws2 \_32.dll u otras entidades. Se debe llamar a un [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) coincidente para cada llamada **WSPStartup** correcta. El proveedor de servicios debe mantener un recuento de referencias por proceso. En cada llamada a **WSPStartup** , el autor de la llamada puede especificar cualquier número de versión compatible con la dll del SP.

Un proveedor de servicios debe almacenar el puntero en la tabla de envío de llamadas de llamada del cliente que se recibe como parámetro [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) por proceso. Si un proceso determinado llama a **WSPStartup** varias veces, el proveedor de servicios solo debe usar el puntero de tabla de envío proporcionado más recientemente.

Como parte del proceso de inicialización del proveedor de servicios, Ws2 \_32.dll recupera la tabla de envío del proveedor de servicios a través del parámetro *lpProcTable* para obtener los puntos de entrada al resto de las funciones SPI especificadas en este documento.

El uso de una tabla de distribución (en contraposición a los mecanismos de DLL habituales para tener acceso a los puntos de entrada) sirve para dos propósitos:

-   Es más conveniente para el32.dll Ws2 \_ , ya que se puede realizar una única llamada para detectar todo el conjunto de puntos de entrada.
-   Permite que los proveedores de servicios en capas formados en cadenas de protocolo funcionen de forma más eficaz.

## <a name="initializing-protocol-chains"></a>Inicializando cadenas de protocolo

En el momento en que se instala la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para una cadena de protocolos, también se especifica la ruta de acceso al primer proveedor en capas de la cadena. Cuando se inicializa una cadena de protocolos, el \_32.dll Ws2 usa esta ruta de acceso para cargar la dll del proveedor y, a continuación, invoca [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup). Dado que **WSPStartup** incluye un puntero a la estructura **de \_ información de WSAPROTOCOL** de la cadena como uno de sus parámetros, los proveedores superpuestos pueden determinar el tipo de cadena en el que se están inicializando y la identidad de la siguiente capa inferior de la cadena. A su vez, un proveedor superpuesto carga el siguiente proveedor de protocolo en la cadena y lo inicializa con una llamada a **WSPStartup**, y así sucesivamente. Siempre que la capa inferior siguiente sea otro proveedor superpuesto, se debe hacer referencia a la estructura de **\_ información de WSAPROTOCOL** de la cadena en la llamada a **WSPStartup** . Cuando la siguiente capa inferior es un protocolo base (que indica el final de la cadena), la estructura de **\_ información de WSAPROTOCOL** de la cadena deja de propagarse hacia abajo. En su lugar, la capa actual debe hacer referencia a una estructura de **\_ información WSAPROTOCOL** que se corresponda con el protocolo que debe usar el proveedor base. Por lo tanto, el proveedor base no tiene ninguna noción de estar implicado en una cadena de protocolos.

La tabla de distribución proporcionada por cualquier proveedor en capas determinado, en muchos casos, duplica los puntos de entrada de un proveedor subyacente. El proveedor en capas solo insertaría sus propios puntos de entrada para las funciones de las que necesitaba estar implicado directamente. Sin embargo, tenga en cuenta que es imperativo que un proveedor superpuesto no modifique el contenido de la tabla de llamadas que recibió al llamar a [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) en la siguiente capa inferior en una cadena de protocolos. Estas llamadas se deben realizar directamente en el archivo DLL de Windows Sockets 2.

 

 
