---
description: En la lista siguiente se proporcionan descripciones concisas de cada estructura de ATM de Winsock. Para obtener información adicional sobre cualquier estructura, haga clic en el nombre de la estructura.
ms.assetid: ce80ef1f-9a76-4a6f-a7ce-f166bc46ca08
title: Estructuras de ATM de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaf28266de89e5346727a9ad42fdb90d9167bc9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715469"
---
# <a name="winsock-atm-structures"></a>Estructuras de ATM de Winsock

En la lista siguiente se proporcionan descripciones concisas de cada estructura de ATM de Winsock. Para obtener información adicional sobre cualquier estructura, haga clic en el nombre de la estructura.



| Estructura ATM                           | Descripción                                                |
|-----------------------------------------|------------------------------------------------------------|
| [**\_dirección ATM**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_address)   | Almacena datos de direcciones ATM para Sockets basados en ATM.             |
| [**\_BHLI ATM**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_bhli)         | Identifica la información de B-HLI para un socket ATM asociado. |
| [**\_BLLI ATM**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_blli)         | Identifica la información de B-LLI para un socket de ATM asociado. |
| [**\_ATM sockaddr**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) | Almacena la información de dirección de socket para Sockets ATM.         |



 

En el caso de los servicios ATM nativos, use AF \_ ATM para la familia de direcciones y la estructura de direcciones de socket [**\_ ATM sockaddr**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) . Para abrir un socket ATM nativo, pase AF \_ ATM, sock \_ raw y ATMPROTO \_ AAL5 o ATMPROTO \_ AALUSER a la función [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) , respectivamente.

 

 



