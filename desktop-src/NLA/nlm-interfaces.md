---
title: Interfaces NLM
description: Interfaces NLM
ms.assetid: 57cc2a07-4551-428c-a303-9b1a4510f225
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322086a2860ff9bade47c9971662931f9ecada60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487062"
---
# <a name="nlm-interfaces"></a>Interfaces NLM

A continuación se muestran las interfaces de NLM.

| Interfaz                                                            | Descripción                                                                                                                                                                                                              |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumNetworkConnections**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-ienumnetworkconnections)           | Proporciona un enumerador estándar para las conexiones de red. Enumera las conexiones activas, desconectadas o de red en una red. Esta interfaz se puede obtener de la interfaz de [**inet**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) . |
| [**IEnumNetworks**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-ienumnetworks)                               | Enumera todas las redes disponibles en el servidor. Esta interfaz se puede obtener de la interfaz de [**inet**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) .                                                                                         |
| [**Inetd**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)                                         | Representa una red en el servidor. También puede representar una colección de conexiones de red con una firma de red similar.                                                                                          |
| [**INetworkConnection**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnection)                     | Representa una única conexión de red.                                                                                                                                                                                  |
| [**INetworkConnectionCost**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectioncost)                | Se usa para consultar el costo de red actual y el estado del plan de datos asociado a una conexión.                                                                                                                                    |
| [**INetworkConnectionCostEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectioncostevents) | Se usa para notificar a una aplicación los eventos de cambio de estado del plan de datos y de costos para una conexión.                                                                                                                               |
| [**INetworkConnectionEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectionevents)         | Una interfaz de receptor que un cliente implementa para recibir eventos relacionados con las conexiones de red. Las aplicaciones que están interesadas en eventos de nivel granular más bajos, como los cambios de autenticación, implementan esta interfaz.       |
| [**INetworkCostManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkcostmanager)                   | Se utiliza para consultar la información de estado del plan de datos y el costo del equipo asociada a una conexión utilizada para la conectividad a Internet de todo el equipo, o el primer salto de enrutamiento a un destino específico en una conexión. |
| [**INetworkCostManagerEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkcostmanagerevents)       | Se usa para notificar a una aplicación de eventos relacionados con el plan de datos y el costo de la máquina.                                                                                                                                         |
| [**INetworkEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkevents)                             | Una interfaz de receptor que un cliente implementa para recibir eventos relacionados con la red. Estas API son todas las funciones de devolución de llamada a las que se llama automáticamente cuando se generan los eventos respectivos.                                  |
| [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager)                   | Proporciona un conjunto de métodos para realizar funciones de administración de la lista de redes.                                                                                                                                                  |
| [**INetworkListManagerEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanagerevents)       | Una interfaz de receptor que un cliente implementa para recibir eventos relacionados con el administrador de lista de redes. Las aplicaciones que están interesadas en eventos de nivel granular más altos, como la conectividad a Internet, implementan la interfaz.   |



 

 

 




