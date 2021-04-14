---
description: El establecimiento de una sesión PGM es similar a la rutina de establecimiento de conexión asociada a una sesión TCP.
ms.assetid: 777e0106-0314-4ec8-b064-88ceb694614b
title: Receptores y remitentes de PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e300a0c9de199e1f836e71407caf6487812cf7b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541518"
---
# <a name="pgm-senders-and-receivers"></a>Receptores y remitentes de PGM

El establecimiento de una sesión PGM es similar a la rutina de establecimiento de conexión asociada a una sesión TCP. La salida importante de una sesión TCP, sin embargo, es que se invierte la semántica del cliente y del servidor. el servidor (el remitente PGM) se conecta a un grupo de multidifusión, mientras que el cliente (el receptor PGM) espera a aceptar una conexión. En los párrafos siguientes se detallan los pasos de programación necesarios para crear un remitente PGM y un receptor PGM. En esta página también se describen los modos de datos disponibles para las sesiones de PGM.

## <a name="pgm-sender"></a>Remitente PGM

**Para crear un remitente PGM, realice los pasos siguientes:**

1.  Cree un socket PGM.
2.  [**enlazar**](/windows/desktop/api/winsock/nf-winsock-bind) el socket para la indirección \_ .
3.  [**Conéctese**](/windows/desktop/api/Winsock2/nf-winsock2-connect) a la dirección de transmisión del grupo de multidifusión.

No se realiza ningún protocolo de enlace de sesión formal con ningún cliente. El proceso de conexión es similar a una [**conexión**](/windows/desktop/api/Winsock2/nf-winsock2-connect)UDP, ya que asocia una dirección de extremo (el grupo de multidifusión) con el socket. Una vez completado, se pueden enviar datos en el socket.

Cuando un remitente crea un socket PGM y lo conecta a una dirección de multidifusión, se crea una sesión PGM. Una sesión de multidifusión confiable se define mediante una combinación del identificador único global (GUID) y el puerto de origen. El transporte genera el GUID. El transporte especifica el puerto sSource y no se proporciona ningún control sobre el que se utiliza el puerto de origen.

> [!Note]  
> No se permite recibir datos en un socket de remitente y se produce un error.

 

En el fragmento de código siguiente se muestra cómo configurar un remitente PGM:


```C++

SOCKET        s;
SOCKADDR_IN   salocal, sasession;
int           dwSessionPort;

s = socket (AF_INET, SOCK_RDM, IPPROTO_RM);

salocal.sin_family = AF_INET;
salocal.sin_port   = htons (0);    // Port is ignored here
salocal.sin_addr.s_addr = htonl (INADDR_ANY);

bind (s, (SOCKADDR *)&salocal, sizeof(salocal));

//
// Set all relevant sender socket options here
//

//
// Now, connect <entity type="hellip"/>
// Setting the connection port (dwSessionPort) has relevance, and
// can be used to multiplex multiple sessions to the same
// multicast group address over different ports
//
dwSessionPort = 0;
sasession.sin_family = AF_INET;
sasession.sin_port   = htons (dwSessionPort);
sasession.sin_addr.s_addr = inet_addr ("234.5.6.7");

connect (s, (SOCKADDR *)&sasession, sizeof(sasession));

//
// We're now ready to send data!
//



```



## <a name="pgm-receiver"></a>Receptor PGM

**Para crear un receptor PGM, realice los pasos siguientes:**

1.  Cree un socket PGM.
2.  [**enlazar**](/windows/desktop/api/winsock/nf-winsock-bind) el socket a la dirección del grupo de multidifusión en la que el remitente está transmitiendo.
3.  Llame a la función [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) en el socket para poner el socket en modo de escucha. La función Listen devuelve cuando se detecta una sesión PGM en la dirección y el puerto del grupo de multidifusión especificado.
4.  Llame a la función [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) para obtener un nuevo identificador de socket correspondiente a la sesión.

Solo los datos PGM originales (ODATA) desencadenan la aceptación de una nueva sesión. Como tal, el transporte puede recibir otro tráfico PGM (como paquetes SPM o RDATA), pero no se devuelve la función [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) .

Una vez aceptada una sesión, el identificador de socket devuelto se usa para recibir los datos.

> [!Note]  
> No se permite el envío de datos en un socket de recepción y se produce un error.

 

En el fragmento de código siguiente se muestra la configuración de un receptor PGM:


```C++

SOCKET        s,
              sclient;
SOCKADDR_IN   salocal,
              sasession;
int           sasessionsz, dwSessionPort;

s = socket (AF_INET, SOCK_RDM, IPPROTO_RM);

//
// The bind port (dwSessionPort) specified should match that
// which the sender specified in the connect call
//
dwSessionPort = 0;
salocal.sin_family = AF_INET;
salocal.sin_port   = htons (dwSessionPort);    
salocal.sin_addr.s_addr = inet_addr ("234.5.6.7");

bind (s, (SOCKADDR *)&salocal, sizeof(salocal));

//
// Set all relevant receiver socket options here
//

listen (s, 10);

sasessionsz = sizeof(sasession);
sclient = accept (s, (SOCKADDR *)&sasession, &sasessionsz);

//
// accept will return the client socket and we are now ready
// to receive data on the new socket!
//



```



## <a name="data-modes"></a>Modos de datos

Las sesiones PGM tienen dos opciones para los modos de datos: modo de mensaje y modo de flujo.

El modo de mensaje es adecuado para las aplicaciones que necesitan enviar mensajes discretos, y se especifica mediante un tipo de socket de SOCK \_ RDM. El modo de secuencia es adecuado para las aplicaciones que necesitan enviar datos de streaming a receptores, como aplicaciones de vídeo o de voz, y se especifica mediante un tipo de socket de \_ flujo sock. La elección de modo afecta a la forma en que Winsock procesa los datos.

Considere el ejemplo siguiente: un remitente PGM del modo de mensaje realiza tres llamadas a la función [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) , cada una con un búfer de 100 bytes. Esta operación aparece en la conexión como tres paquetes PGM discretos. En el lado del receptor, cada llamada a la función [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) devuelve solo 100 bytes, incluso si se proporciona un búfer de recepción mayor. Por el contrario, con un remitente PGM en modo de transmisión, esas transmisiones de 3 100 bytes podrían fusionarse en menos de tres paquetes físicos en la conexión (o fusionarse en un BLOB de datos en el lado del receptor). Como tal, cuando el receptor llama a una de las funciones de recepción de Windows Sockets, cualquier cantidad de datos que haya recibido el transporte PGM se puede devolver a la aplicación sin tener en cuenta cómo se han transmitido o recibido físicamente los datos.

 

 



