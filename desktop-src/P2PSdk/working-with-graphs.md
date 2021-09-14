---
description: Al trabajar con gráficos del mismo nivel, se debe llamar a las funciones en un orden específico. El flujo de llamadas depende de si va a crear o abrir un gráfico del mismo nivel. En este tema se identifica el flujo de llamadas de función en una aplicación de grafo del mismo nivel simple.
ms.assetid: cb4f48d0-d1e2-4a4b-bd5a-6e8f66d03806
title: Trabajar con gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4328b7a0109139421cf03c72a7228a3dc17e375
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062902"
---
# <a name="working-with-graphs"></a>Trabajar con gráficos

Al trabajar con gráficos del mismo nivel, se debe llamar a las funciones en un orden específico. El flujo de llamadas depende de si va a crear o abrir un gráfico del mismo nivel. En este tema se identifica el flujo de llamadas de función en una aplicación de grafo del mismo nivel simple.

## <a name="starting-up-a-graph"></a>Iniciar una Graph

Antes de que una aplicación llame a una función en Peer Graphing API, se debe llamar a [**PeerGraphStartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup) para inicializar Peer Graphing API para una aplicación y, a continuación, establecer la versión admitida.

## <a name="creating-a-peer-graph"></a>Crear un punto de conexión Graph

El procedimiento siguiente identifica el flujo de llamadas para crear un gráfico del mismo nivel.

> [!IMPORTANT]
> Solo un par debe llamar a [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate). Todos los demás elementos del mismo nivel deben llamar [**a PeerGraphOpen.**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) Varias llamadas a **PeerGraphCreate** invalidan un gráfico.

 

-   Cree un gráfico del mismo nivel. Llame [**a PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate).
-   Regístrese para eventos del mismo nivel. Llame [**a PeerGraphRegisterEvent.**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)
    > [!Note]  
    > Para obtener más información sobre el registro de eventos del mismo nivel, vea [Infraestructura de eventos](peer-events-infrastructure.md).

     

-   Escuchar las conexiones a un gráfico del mismo nivel. Llame [**a PeerGraphListen.**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)
-   Realice funciones dependientes de la aplicación durante el resto del tiempo de ejecución, por ejemplo, procese eventos del mismo nivel y trabaje con conexiones.
-   Cierre la conexión a un gráfico del mismo nivel. Llame [**a PeerGraphClose.**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)

## <a name="opening-a-peer-graph"></a>Abrir un punto de conexión Graph

El flujo de llamadas de función para abrir un gráfico del mismo nivel depende del valor devuelto de la llamada a [**PeerGraphOpen.**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) Los valores más importantes son **S \_ OK y** PEER S DATA **\_ \_ \_ CREATED,** que se explican en las secciones siguientes de este tema.

> [!Note]  
> Si una llamada a [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) no devuelve **S \_ OK** o **PEER S DATA \_ \_ \_ CREATED,** controle el error.

 

## <a name="when-peergraphopen-returns-s_ok"></a>Cuando PeerGraphOpen devuelve S \_ OK

Cuando una llamada a [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) devuelve **S \_ OK**, se han abierto un gráfico del mismo nivel y una base de datos existente. El procedimiento siguiente identifica lo que puede hacer para abrir un gráfico del mismo nivel cuando una llamada a **PeerGraphOpen** devuelve **S \_ OK**

-   Regístrese para eventos del mismo nivel. Llame [**a PeerGraphRegisterEvent.**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)
    > [!Note]  
    > Para obtener más información sobre el registro de eventos, vea [Infraestructura de eventos](peer-events-infrastructure.md).

     

-   Busque un nodo. Se trata de un proceso que se realiza fuera de la infraestructura de grafos del mismo nivel, mediante un método o una aplicación que identifique. Peer Graphing API no proporciona un mecanismo específico para buscar un nodo de grafo inicial al que conectarse. Una aplicación debe usar otro mecanismo, como la API del Protocolo de resolución de nombres del mismo nivel [(PNRP),](pnrp-namespace-provider-api.md) para localizar el nodo inicial.
-   Si se encuentra un nodo, conéctese a él. Llame [**a PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect)y, a continuación, llame a [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) para escuchar las conexiones al gráfico del mismo nivel.
    > [!Note]  
    > Si no se encuentra un nodo, no llame a [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) y [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).

     

-   Realice funciones dependientes de la aplicación durante el resto del tiempo de ejecución, por ejemplo, procese eventos del mismo nivel y trabaje con conexiones, en función de si el nodo está conectado al gráfico del mismo nivel o no. Por ejemplo, la aplicación puede optar por agotar el tiempo de espera o realizar periódicamente la detección de un nodo activo en el gráfico.
-   Cierre la conexión al gráfico del mismo nivel. Llame [**a PeerGraphClose.**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)

## <a name="when-peergraphopen-returns-peer_s_data_created"></a>Cuando PeerGraphOpen devuelve PEER \_ S \_ DATA \_ CREATED

Cuando [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) devuelve **PEER S DATA \_ \_ \_ CREATED**, significa que no se encuentra una base de datos existente para un gráfico del mismo nivel, se crea una nueva base de datos y esta es la primera vez que se abre. Para usar o escuchar en un gráfico del mismo nivel, un mismo nivel debe estar conectado y sincronizado con un gráfico del mismo nivel.

El procedimiento siguiente identifica lo que puede hacer para abrir un gráfico del mismo nivel cuando una llamada a [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) devuelve **PEER S DATA \_ \_ \_ CREATED**.

-   Abra un gráfico del mismo nivel. Llame [**a PeerGraphOpen.**](/windows/desktop/api/P2P/nf-p2p-peergraphopen)
-   Regístrese para eventos del mismo nivel. Llame [**a PeerGraphRegisterEvent.**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)
    > [!Note]  
    > Para obtener más información sobre el registro de eventos del mismo nivel, vea [Infraestructura de eventos](peer-events-infrastructure.md).

     

-   Busque un nodo. Se trata de un proceso que se realiza fuera de la infraestructura de grafos del mismo nivel, mediante un método o una aplicación que identifique. Peer Graphing API no proporciona un mecanismo específico para buscar un nodo de grafo inicial al que conectarse. Una aplicación debe usar otro mecanismo, como la API del Protocolo de resolución de nombres del mismo nivel [(PNRP),](pnrp-namespace-provider-api.md) para localizar el nodo inicial.
-   Si se encuentra un nodo, conéctese a él. Llame [**a PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect)y, a continuación, llame a [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) para escuchar las conexiones al gráfico del mismo nivel.
    > [!Note]  
    > Si no se encuentra un nodo, no llame a [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) y [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).

     

-   Realice funciones dependientes de la aplicación durante el resto del tiempo de ejecución, por ejemplo, procese eventos del mismo nivel y trabaje con conexiones, en función de si el nodo está conectado al gráfico del mismo nivel o no. Por ejemplo, la aplicación puede optar por agotar el tiempo de espera o realizar periódicamente la detección de un nodo activo en el gráfico.
-   Cierre la conexión al gráfico del mismo nivel. Llame [**a PeerGraphClose.**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)

 

 



