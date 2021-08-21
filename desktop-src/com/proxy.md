---
title: Proxy
description: Un proxy reside en el espacio de direcciones del proceso de llamada y actúa como suplente para el objeto remoto.
ms.assetid: 6c82f655-ac46-4ed9-992b-0387b324a8f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0478ce9ad1e08d343f1536fcd4bba63e59ae0fd229390be31c978bd20f737b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130016"
---
# <a name="proxy"></a>Proxy

Un proxy reside en el espacio de direcciones del proceso de llamada y actúa como suplente para el objeto remoto. Desde la perspectiva del objeto que realiza la llamada, el proxy es el objeto . Normalmente, el rol del proxy es empaquetar los parámetros de interfaz para las llamadas a métodos en sus interfaces de objeto. El proxy empaqueta los parámetros en un búfer de mensajes y pasa el búfer al canal, que controla el transporte entre procesos. El proxy se implementa como un objeto agregado o compuesto. Contiene una pieza de administrador proporcionada por el sistema denominada administrador de proxy y uno o varios componentes específicos de la interfaz denominados servidores proxy de interfaz. El número de servidores proxy de interfaz es igual al número de interfaces de objeto que se han expuesto a ese cliente determinado. Para el cliente que cumple con el modelo de objetos de componente, el proxy parece ser el objeto real.

> [!Note]  
> Con la serialización personalizada, el proxy se puede implementar de forma similar o puede comunicarse directamente con el objeto sin usar un código auxiliar.

 

Cada proxy de interfaz es un objeto de componente que implementa el código de serialización para una de las interfaces del objeto. El proxy representa el objeto para el que proporciona código de serialización. Cada proxy también implementa la [**interfaz IRpcProxyBuffer.**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) Aunque la interfaz de objeto representada por el proxy es pública, la implementación **de IRpcProxyBuffer** es privada y se usa internamente dentro del proxy. El administrador de proxy realiza un seguimiento de los servidores proxy de interfaz y también contiene la implementación pública de la interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) de control para el agregado. Cada proxy de interfaz puede existir en un archivo DLL independiente que se carga cuando la interfaz que admite se materializa al cliente.

## <a name="structure-of-the-proxy"></a>Estructura del proxy

En el diagrama siguiente se muestra la estructura de un proxy que admite la serialización estándar de los parámetros que pertenecen a dos interfaces: IA1 e IA2. Cada proxy de interfaz implementa [**IRpcProxyBuffer para**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) la comunicación interna entre las partes agregadas. Cuando el proxy está listo para pasar sus parámetros serializados a través del límite del proceso, llama a los métodos de la interfaz [**IRpcChannelBuffer,**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) que se implementa mediante el canal. A su vez, el canal reenvía la llamada a la biblioteca en tiempo de ejecución de RPC para que pueda alcanzar su destino en el objeto .

![Diagrama que muestra la estructura del proxy.](images/4432d8d3-dfab-4635-90f8-408aecf70134.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canal](channel.md)
</dt> <dt>

[Comunicación entre objetos](inter-object-communication.md)
</dt> <dt>

[Detalles de serialización](marshaling-details.md)
</dt> <dt>

[Microsoft RPC](microsoft-rpc.md)
</dt> <dt>

[Stub](stub.md)
</dt> </dl>

 

 