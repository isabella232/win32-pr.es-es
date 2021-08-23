---
description: Las funciones de redirección de dispositivos redirigen los dispositivos MS-DOS estándar, las letras de unidad y los puertos LPT. Esto permite que las aplicaciones que se ejecutan en el sistema usen los dispositivos y accedan a la red de una manera totalmente transparente.
ms.assetid: a61ab1e6-dad9-4dc0-a908-f8440619f610
title: Device-Redirecting functions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4929052ed2691d6264791cac431e59faaacdb92f7f96bb610d99fdd4ded471
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008453"
---
# <a name="device-redirecting-functions"></a>Device-Redirecting functions

Las funciones de redirección de dispositivos redirigen los dispositivos MS-DOS estándar, las letras de unidad y los puertos LPT. Esto permite que las aplicaciones que se ejecutan en el sistema usen los dispositivos y accedan a la red de una manera totalmente transparente.



| Función                                                         | Descripción                                                                                                                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection)                       | Redirige o conecta un dispositivo local a un recurso de red.<br/>                                                                                                                              |
| [**NPAddConnection3**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection3)                     | Realiza la misma acción que [**NPAddConnection,**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection)pero permite al usuario especificar qué ventana debe ser propietaria de los cuadros de diálogo y cómo se debe establecer la conexión.<br/> |
| [**NPCancelConnection**](/windows/desktop/api/Npapi/nf-npapi-npcancelconnection)                 | Interrumpe una conexión de red. Los cambios se recordarán si un dispositivo está desconectado a menos que la conexión sea una conexión sin dispositivo.<br/>                                                    |
| [**NPGetConnection**](/windows/desktop/api/Npapi/nf-npapi-npgetconnection)                       | Devuelve información sobre una conexión.<br/>                                                                                                                                                  |
| [**NPGetConnection3**](/windows/desktop/api/Npapi/nf-npapi-npgetconnection3)                     | Devuelve información sobre una conexión, incluso si la conexión está desconectada actualmente.<br/>                                                                                                |
| [**NPGetConnectionPerformance**](/windows/desktop/api/Npapi/nf-npapi-npgetconnectionperformance) | Devuelve información de rendimiento sobre una conexión.<br/>                                                                                                                                      |
| [**NPGetUniversalName**](/windows/desktop/api/Npapi/nf-npapi-npgetuniversalname)                 | Devuelve el nombre universal local o remoto, en el formato especificado durante la llamada a la función.<br/>                                                                                            |



 

 

 




