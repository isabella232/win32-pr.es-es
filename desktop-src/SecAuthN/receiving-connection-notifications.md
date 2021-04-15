---
description: Algunas aplicaciones necesitan recibir notificaciones de eventos de conexión, antes del evento, justo después de que se produzca o ambos. Puede crear un archivo DLL para recibir notificaciones de eventos de conexión anticipados y posteriores a los hechos.
ms.assetid: 692eb8f2-1c53-4535-b44d-babb30eecd9c
title: Recepción de notificaciones de conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c054d4f7bb78f610afe6c1cbdf028416de7b5596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539859"
---
# <a name="receiving-connection-notifications"></a>Recepción de notificaciones de conexión

Algunas aplicaciones necesitan recibir notificaciones de eventos de conexión, antes del evento, justo después de que se produzca o ambos. Puede crear un archivo DLL para recibir notificaciones de eventos de conexión anticipados y posteriores a los hechos.

Un ejemplo de una aplicación que necesita recibir notificaciones previas de un evento de conexión es el servicio de acceso remoto (RAS). RAS debe ser informado antes de que se establezca una conexión, ya que puede ser necesario establecer una conexión de módem antes de realizar la conexión de red.

Del mismo modo, es posible que las aplicaciones necesiten limpiar los recursos una vez realizada la conexión, lo que requiere una notificación posterior a la conexión.

Las aplicaciones interesadas en recibir notificaciones anticipadas y posteriores a los eventos de conexión deben proporcionar un archivo DLL que exporte dos funciones, [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) y [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify).

Después de implementar estas funciones, debe registrar el archivo DLL tal y como se describe en [registrar para recibir notificaciones de conexión](registering-to-receive-connection-notifications.md).

 

 



