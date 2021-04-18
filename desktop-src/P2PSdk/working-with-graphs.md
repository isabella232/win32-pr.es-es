---
description: Al trabajar con gráficos del mismo nivel, se debe llamar a las funciones en un orden concreto. El flujo de llamadas depende de si se crea o se abre un grafo del mismo nivel. En este tema se identifica el flujo de llamadas a funciones en una aplicación sencilla de gráficos del mismo nivel.
ms.assetid: cb4f48d0-d1e2-4a4b-bd5a-6e8f66d03806
title: Trabajar con gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4328b7a0109139421cf03c72a7228a3dc17e375
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667358"
---
# <a name="working-with-graphs"></a>Trabajar con gráficos

Al trabajar con gráficos del mismo nivel, se debe llamar a las funciones en un orden concreto. El flujo de llamadas depende de si se crea o se abre un grafo del mismo nivel. En este tema se identifica el flujo de llamadas a funciones en una aplicación sencilla de gráficos del mismo nivel.

## <a name="starting-up-a-graph"></a>Inicio de un grafo

Antes de que una aplicación llame a una función de la API de gráficos del mismo nivel, se debe llamar a [**PeerGraphStartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup) para inicializar la API de gráficos del mismo nivel para una aplicación y, a continuación, establecer la versión compatible.

## <a name="creating-a-peer-graph"></a>Crear un grafo del mismo nivel

El procedimiento siguiente identifica el flujo de llamadas para crear un grafo del mismo nivel.

> [!IMPORTANT]
> Solo un elemento del mismo nivel debe llamar a [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate). Todos los demás elementos del mismo nivel deben llamar a [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen). Varias llamadas a **PeerGraphCreate** invalidan un grafo.

 

-   Cree un grafo del mismo nivel. Llame a [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate).
-   Registrar para eventos del mismo nivel. Llame a [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent).
    > [!Note]  
    > Para obtener más información sobre el registro de eventos del mismo nivel, vea [infraestructura de eventos](peer-events-infrastructure.md).

     

-   Escucha las conexiones a un grafo del mismo nivel. Llame a [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).
-   Realizar funciones dependientes de la aplicación para el resto del tiempo de ejecución, por ejemplo, procesar eventos del mismo nivel y trabajar con conexiones.
-   Cierre la conexión a un grafo del mismo nivel. Llame a [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose).

## <a name="opening-a-peer-graph"></a>Abrir un grafo del mismo nivel

El flujo de llamadas de función para abrir un grafo del mismo nivel depende del valor devuelto de la llamada a [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen). Los valores más importantes son **s \_ OK** y **datos del mismo nivel \_ \_ \_ creados**, que se explican en las siguientes secciones de este tema.

> [!Note]  
> Si una llamada a [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) no devuelve los **datos \_ correctos** o **del mismo nivel que se \_ \_ \_ han creado**, controle el error.

 

## <a name="when-peergraphopen-returns-s_ok"></a>Cuando PeerGraphOpen devuelve S \_ OK

Cuando una llamada a [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) devuelve **S \_ correcto**, se han abierto un grafo del mismo nivel y una base de datos existente. El siguiente procedimiento identifica lo que puede hacer para abrir un grafo del mismo nivel cuando una llamada a **PeerGraphOpen** devuelve **S \_ correctos** .

-   Registrar para eventos del mismo nivel. Llame a [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent).
    > [!Note]  
    > Para obtener más información sobre el registro de eventos, vea [infraestructura de eventos](peer-events-infrastructure.md).

     

-   Busque un nodo. Se trata de un proceso realizado fuera de la infraestructura de gráficos del mismo nivel, mediante el uso de un método o una aplicación que se identifican. La API de gráficos del mismo nivel no proporciona un mecanismo específico para encontrar un nodo de gráfico inicial al que conectarse. Una aplicación debe usar otro mecanismo, como la API del [Protocolo de resolución de nombres de mismo nivel (PNRP)](pnrp-namespace-provider-api.md) , para buscar el nodo inicial.
-   Si se encuentra un nodo, conéctese a él. Llame a [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect)y, a continuación, llame a [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) para escuchar las conexiones al grafo del mismo nivel.
    > [!Note]  
    > Si no se encuentra un nodo, no llame a [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) y [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).

     

-   Realizar funciones dependientes de la aplicación durante el resto del tiempo de ejecución, por ejemplo, procesar eventos del mismo nivel y trabajar con conexiones, dependiendo de si el nodo está conectado al grafo del mismo nivel o no. Por ejemplo, la aplicación puede elegir el tiempo de espera o realizar la detección periódicamente para un nodo activo en el gráfico.
-   Cierre la conexión al grafo del mismo nivel. Llame a [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose).

## <a name="when-peergraphopen-returns-peer_s_data_created"></a>Cuando PeerGraphOpen devuelve datos del mismo nivel \_ \_ \_ creados

Cuando [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) devuelve **datos del mismo nivel \_ \_ \_ creados**, significa que no se encuentra una base de datos existente para un grafo del mismo nivel, se crea una nueva base de datos y es la primera vez que se abre. Para usar o escuchar en un grafo del mismo nivel, un elemento del mismo nivel debe estar conectado y sincronizado con un grafo del mismo nivel.

El siguiente procedimiento identifica lo que puede hacer para abrir un grafo del mismo nivel cuando una llamada a [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) devuelve los **datos del mismo nivel \_ \_ \_ creados**.

-   Abra un grafo del mismo nivel. Llame a [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen).
-   Registrar para eventos del mismo nivel. Llame a [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent).
    > [!Note]  
    > Para obtener más información sobre el registro de eventos del mismo nivel, vea [infraestructura de eventos](peer-events-infrastructure.md).

     

-   Busque un nodo. Se trata de un proceso realizado fuera de la infraestructura de gráficos del mismo nivel, mediante el uso de un método o una aplicación que se identifican. La API de gráficos del mismo nivel no proporciona un mecanismo específico para encontrar un nodo de gráfico inicial al que conectarse. Una aplicación debe usar otro mecanismo, como la API del [Protocolo de resolución de nombres de mismo nivel (PNRP)](pnrp-namespace-provider-api.md) , para buscar el nodo inicial.
-   Si se encuentra un nodo, conéctese a él. Llame a [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect)y, a continuación, llame a [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) para escuchar las conexiones al grafo del mismo nivel.
    > [!Note]  
    > Si no se encuentra un nodo, no llame a [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) y [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).

     

-   Realizar funciones dependientes de la aplicación durante el resto del tiempo de ejecución, por ejemplo, procesar eventos del mismo nivel y trabajar con conexiones, dependiendo de si el nodo está conectado al grafo del mismo nivel o no. Por ejemplo, la aplicación puede elegir el tiempo de espera o realizar la detección periódicamente para un nodo activo en el gráfico.
-   Cierre la conexión al grafo del mismo nivel. Llame a [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose).

 

 



