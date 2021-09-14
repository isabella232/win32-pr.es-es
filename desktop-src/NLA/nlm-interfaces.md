---
title: NLM Interfaces
description: NLM Interfaces
ms.assetid: 57cc2a07-4551-428c-a303-9b1a4510f225
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322086a2860ff9bade47c9971662931f9ecada60
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169466"
---
# <a name="nlm-interfaces"></a>NLM Interfaces

Las siguientes son las interfaces NLM.

| Interfaz                                                            | Descripción                                                                                                                                                                                                              |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumNetworkConnections**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-ienumnetworkconnections)           | Proporciona un enumerador estándar para las conexiones de red. Enumera las conexiones de red activas, desconectadas o todas dentro de una red. Esta interfaz se puede obtener de la [**interfaz INetwork.**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) |
| [**IEnumNetworks**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-ienumnetworks)                               | Enumera todas las redes disponibles en el servidor. Esta interfaz se puede obtener de la [**interfaz INetwork.**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)                                                                                         |
| [**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)                                         | Representa una red en el servidor. También puede representar una colección de conexiones de red con una firma de red similar.                                                                                          |
| [**INetworkConnection**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnection)                     | Representa una única conexión de red.                                                                                                                                                                                  |
| [**INetworkConnectionCost**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectioncost)                | Se usa para consultar el costo de red actual y el estado del plan de datos asociado a una conexión.                                                                                                                                    |
| [**INetworkConnectionCostEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectioncostevents) | Se usa para notificar a una aplicación los eventos de cambio de estado del plan de datos y de costos para una conexión.                                                                                                                               |
| [**INetworkConnectionEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectionevents)         | Interfaz de receptor que un cliente implementa para recibir eventos relacionados con las conexiones de red. Las aplicaciones que están interesadas en eventos de nivel inferior, como los cambios de autenticación, implementan esta interfaz.       |
| [**INetworkCostManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkcostmanager)                   | Se usa para consultar la información de estado del plan de datos y costo de todo el equipo asociada a una conexión que se usa para la conectividad a Internet en toda la máquina o al primer salto de enrutamiento a un destino específico de una conexión. |
| [**INetworkCostManagerEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkcostmanagerevents)       | Se usa para notificar a una aplicación los eventos relacionados con el costo de todo el equipo y el plan de datos.                                                                                                                                         |
| [**INetworkEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkevents)                             | Interfaz de receptor que un cliente implementa para recibir eventos relacionados con la red. Estas API son todas las funciones de devolución de llamada a las que se llama automáticamente cuando se inician los eventos respectivos.                                  |
| [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager)                   | Proporciona un conjunto de métodos para realizar funciones de administración de listas de redes.                                                                                                                                                  |
| [**INetworkListManagerEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanagerevents)       | Interfaz de receptor que un cliente implementa para recibir eventos relacionados con el Administrador de listas de redes. Las aplicaciones que están interesadas en eventos de nivel más pormenorizados, como la conectividad a Internet, implementan la interfaz .   |



 

 

 




