---
description: Las funciones de redirección de dispositivos redirigen los dispositivos MS-DOS estándar, las letras de unidad y los puertos LPT. Esto permite que las aplicaciones que se ejecutan en el sistema usen los dispositivos y accedan a la red de una manera totalmente transparente.
ms.assetid: a61ab1e6-dad9-4dc0-a908-f8440619f610
title: Device-Redirecting Functions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577f8d108b6bfdeb01f786478cd736e6c84cc83d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171261"
---
# <a name="device-redirecting-functions"></a>Device-Redirecting Functions

Las funciones de redirección de dispositivos redirigen los dispositivos MS-DOS estándar, las letras de unidad y los puertos LPT. Esto permite que las aplicaciones que se ejecutan en el sistema usen los dispositivos y accedan a la red de una manera totalmente transparente.



| Función                                                         | Descripción                                                                                                                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection)                       | Redirige o conecta un dispositivo local a un recurso de red.<br/>                                                                                                                              |
| [**NPAddConnection3**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection3)                     | Realiza la misma acción que [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection), pero permite al usuario especificar qué ventana debe poseer los cuadros de diálogo y cómo se debe establecer la conexión.<br/> |
| [**NPCancelConnection**](/windows/desktop/api/Npapi/nf-npapi-npcancelconnection)                 | Interrumpe una conexión de red. Los cambios se recordarán si un dispositivo está desconectado a menos que la conexión sea una conexión sin dispositivo.<br/>                                                    |
| [**NPGetConnection**](/windows/desktop/api/Npapi/nf-npapi-npgetconnection)                       | Devuelve información sobre una conexión.<br/>                                                                                                                                                  |
| [**NPGetConnection3**](/windows/desktop/api/Npapi/nf-npapi-npgetconnection3)                     | Devuelve información sobre una conexión, incluso si la conexión está desconectada actualmente.<br/>                                                                                                |
| [**NPGetConnectionPerformance**](/windows/desktop/api/Npapi/nf-npapi-npgetconnectionperformance) | Devuelve información de rendimiento sobre una conexión.<br/>                                                                                                                                      |
| [**NPGetUniversalName**](/windows/desktop/api/Npapi/nf-npapi-npgetuniversalname)                 | Devuelve el nombre universal local o remoto, en el formato especificado durante la llamada a la función.<br/>                                                                                            |



 

 

 




