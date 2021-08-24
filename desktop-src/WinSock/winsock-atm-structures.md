---
description: En la lista siguiente se proporcionan descripciones concisas de cada estructura de Winsock ATM. Para obtener información adicional sobre cualquier estructura, haga clic en el nombre de la estructura.
ms.assetid: ce80ef1f-9a76-4a6f-a7ce-f166bc46ca08
title: Estructuras de cajero automático de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f45cafef8bcf628f9172f2ad7ce3323d0d5b0c3e2c3912d195615ea2471501
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612805"
---
# <a name="winsock-atm-structures"></a>Estructuras de cajero automático de Winsock

En la lista siguiente se proporcionan descripciones concisas de cada estructura de Winsock ATM. Para obtener información adicional sobre cualquier estructura, haga clic en el nombre de la estructura.



| Estructura de ATM                           | Descripción                                                |
|-----------------------------------------|------------------------------------------------------------|
| [**DIRECCIÓN DE \_ CAJERO AUTOMÁTICO**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_address)   | Almacena datos de direcciones ATM para sockets basados en ATM.             |
| [**ATM \_ ATM ATMLI**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_bhli)         | Identifica la información de B-HLI para un socket de ATM asociado. |
| [**ATM \_ BLLI**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_blli)         | Identifica la información de B-LLI para un socket de ATM asociado. |
| [**sockaddr \_ atm**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) | Almacena información de dirección de socket para sockets DE ATM.         |



 

Para los servicios de ATM nativos, use AF ATM para la familia de direcciones y la estructura de direcciones de socket de cajero automático \_ [**sockaddr. \_**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) Para abrir un socket de ATM nativo, pase AF \_ ATM, SOCK RAW y \_ ATMPROTO AAL5 o ATMPROTO AALUSER a la función \_ \_ [**socket,**](/windows/desktop/api/Winsock2/nf-winsock2-socket) respectivamente.

 

 



