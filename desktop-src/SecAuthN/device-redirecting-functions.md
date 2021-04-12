---
description: Las funciones de redireccionamiento de dispositivos redirigen los dispositivos de MS-DOS estándar, las letras de unidad y los puertos LPT. Esto permite que las aplicaciones que se ejecutan en el sistema usen los dispositivos y tengan acceso a la red de forma totalmente transparente.
ms.assetid: a61ab1e6-dad9-4dc0-a908-f8440619f610
title: Funciones de Device-Redirecting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577f8d108b6bfdeb01f786478cd736e6c84cc83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275216"
---
# <a name="device-redirecting-functions"></a>Funciones de Device-Redirecting

Las funciones de redireccionamiento de dispositivos redirigen los dispositivos de MS-DOS estándar, las letras de unidad y los puertos LPT. Esto permite que las aplicaciones que se ejecutan en el sistema usen los dispositivos y tengan acceso a la red de forma totalmente transparente.



| Función                                                         | Descripción                                                                                                                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection)                       | Redirige o conecta un dispositivo local a un recurso de red.<br/>                                                                                                                              |
| [**NPAddConnection3**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection3)                     | Realiza la misma acción que [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection), pero permite al usuario especificar qué ventana debe ser propietaria de los cuadros de diálogo y cómo debe establecerse la conexión.<br/> |
| [**NPCancelConnection**](/windows/desktop/api/Npapi/nf-npapi-npcancelconnection)                 | Interrumpe una conexión de red. Los cambios se recuerdan si un dispositivo se desconecta a menos que la conexión sea una conexión sin dispositivo.<br/>                                                    |
| [**NPGetConnection**](/windows/desktop/api/Npapi/nf-npapi-npgetconnection)                       | Devuelve información sobre una conexión.<br/>                                                                                                                                                  |
| [**NPGetConnection3**](/windows/desktop/api/Npapi/nf-npapi-npgetconnection3)                     | Devuelve información sobre una conexión, incluso si la conexión está actualmente desconectada.<br/>                                                                                                |
| [**NPGetConnectionPerformance**](/windows/desktop/api/Npapi/nf-npapi-npgetconnectionperformance) | Devuelve información de rendimiento sobre una conexión.<br/>                                                                                                                                      |
| [**NPGetUniversalName**](/windows/desktop/api/Npapi/nf-npapi-npgetuniversalname)                 | Devuelve el nombre universal local o remoto, en el formato especificado durante la llamada de función.<br/>                                                                                            |



 

 

 




