---
title: Acerca de la API de Network List Manager
description: Acerca de la API de Network List Manager
ms.assetid: 675cf7ed-9f57-4d62-8091-1f4e8812f2ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6230251e627671b7fd33adbf50b3904703bc9847
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779123"
---
# <a name="about-the-network-list-manager-api"></a>Acerca de la API de Network List Manager

El entorno de red de Microsoft Windows permite que los equipos de host múltiple se conecten a varias redes simultáneamente. Puede haber varias redes inalámbricas disponibles junto con las conexiones LAN y de acceso telefónico. Network List Manager identifica las redes disponibles y devuelve datos de atributos de red a la aplicación.

La API del administrador de lista de redes interactúa con el servicio Administrador de lista de redes para identificar y recuperar las propiedades de cada red a la que se conecta el equipo. Cada red se identifica de forma exclusiva con una firma de red basada en las propiedades de identificación única de esa red. Cuando una aplicación se registra para las notificaciones del administrador de la lista de redes, la aplicación recibe notificaciones sobre la disponibilidad de nuevas conexiones de red o cambios en las conexiones de red existentes. Las aplicaciones pueden ajustar su lógica según: la red a la que están conectadas. la conexión de red a la que están conectadas; o cuáles son las propiedades de red. Con esta información, las aplicaciones pueden ajustar sus acciones en función de las condiciones de la red actual.

Windows Vista presenta nuevas interfaces que se pueden usar para obtener información detallada sobre estas características de red y mucho más. Con la interfaz [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) es fácil enumerar todas las redes ([**inet**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)) que un equipo ha visto alguna vez, o simplemente las redes conectadas o simplemente las redes desconectadas. La interfaz **INetworkListManager** también facilita la enumeración de las interfaces de red en un equipo.

La interfaz [**inetss**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) se usa para determinar las propiedades de una conexión de red: nombre, descripción, identificador, administrado/autenticado, conectado/desconectado, etc. Es posible que una red única esté conectada a varias interfaces, por lo que a través de una interfaz de **inet** de usuario también puede enumerar las instancias de la interfaz de usuario de **inet** que se está usando.

La interfaz de [**inet**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) out le indica las propiedades pertinentes de una interfaz: identificador, GUID, tipo (administrado, autenticado) y estado (conectado, desconectado, V4 local, V4 Internet, V6 local, V6 Internet). V4 local significa acceso local del Protocolo de Internet versión 4 (IPv4). Internet v4 significa IPv4 con acceso a Internet. IPv6 local V6 y V6 de Internet: IPv6.

La raíz del árbol de objetos de la ubicación de red es la interfaz [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) . Esta interfaz se implementa en la coclase **CLSID \_ NetworkListManager** . Para usar esta interfaz, es necesario crear el objeto com NetworkListManager de **CLSID \_** como se muestra a continuación:


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



 

 




