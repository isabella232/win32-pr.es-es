---
title: Acerca de la API de Network List Manager
description: Acerca de la API de Network List Manager
ms.assetid: 675cf7ed-9f57-4d62-8091-1f4e8812f2ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704bedb3a1029c2be3c123c65a896b1765f191b886af9b354d747abd5e1698e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065184"
---
# <a name="about-the-network-list-manager-api"></a>Acerca de la API de Network List Manager

El entorno Windows de red de Microsoft permite a los equipos de varios equipos conectarse a varias redes simultáneamente. Puede haber varias redes inalámbricas disponibles junto con la LAN y las conexiones de acceso telefónico. Network List Manager identifica las redes disponibles y devuelve datos de atributos de red a la aplicación.

La API de Network List Manager interactúa con el servicio Network List Manager para identificar y recuperar las propiedades de cada red a la que se conecta el equipo. Cada red se identifica de forma única con una firma de red en función de las propiedades de identificación única de esa red. Cuando una aplicación se registra para las notificaciones del Administrador de listas de redes, la aplicación recibe notificaciones sobre la disponibilidad de nuevas conexiones de red o cambios en las conexiones de red existentes. Las aplicaciones pueden ajustar su lógica en función de la red a la que están conectadas. a qué conexión de red están conectados; o cuáles son las propiedades de red. Con esta información, las aplicaciones pueden ajustar sus acciones en función de las condiciones de red actuales.

Windows Vista presenta nuevas interfaces que se pueden usar para obtener información detallada sobre estas características de red y mucho más. Con la [**interfaz INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) es fácil enumerar todas las redes [**(INetwork)**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)que un equipo ha visto alguna vez, o solo las redes conectadas, o simplemente las redes desconectadas. La **interfaz INetworkListManager** también facilita la enumeración de las interfaces de red en un equipo.

La [**interfaz INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) se usa para determinar las propiedades de una conexión de red: nombre, descripción, identificador, administrado/autenticado, conectado o desconectado, etc. Es posible que una sola red esté conectada a varias interfaces, por lo que a través de una interfaz **INetwork** también puede enumerar las instancias de la interfaz **INetwork** que se usa.

La [**interfaz INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) indica las propiedades pertinentes de una interfaz: ID, GUID, Type (administrado, autenticado) y State (conectado, desconectado, V4 Local, V4 Internet, V6 Local, V6 Internet). V4 Local significa acceso local de Protocolo de Internet versión 4 (IPv4). Internet V4 significa IPv4 con acceso a Internet. V6 Local e Internet V6 significan IPv6.

La raíz del árbol de objetos de Ubicación de red es [**la interfaz INetworkListManager.**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) Esta interfaz se implementa en la **coclase \_ NetworkListManager de CLSID.** Para usar esta interfaz, es necesario crear el objeto **COM \_ CLSID NetworkListManager** como se muestra a continuación:


```C++
#include <windows.h>
#include <netlistmgr.h>

#pragma comment(lib, "ole32.lib")

void main()
{
    INetworkListManager *pNetworkListManager = NULL; 
    HRESULT hr = CoCreateInstance(CLSID_NetworkListManager, NULL,
            CLSCTX_ALL, IID_INetworkListManager,
            (LPVOID *)&pNetworkListManager);
}
```



 

 




