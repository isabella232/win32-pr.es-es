---
description: Algunas aplicaciones necesitan recibir notificaciones de eventos de conexión, ya sea antes del evento, justo después de que se produzca, o ambos. Puede crear un archivo DLL para recibir una notificación anticipada y posterior de los eventos de conexión.
ms.assetid: 692eb8f2-1c53-4535-b44d-babb30eecd9c
title: Recepción de notificaciones de conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c054d4f7bb78f610afe6c1cbdf028416de7b5596
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069139"
---
# <a name="receiving-connection-notifications"></a>Recepción de notificaciones de conexión

Algunas aplicaciones necesitan recibir notificaciones de eventos de conexión, ya sea antes del evento, justo después de que se produzca, o ambos. Puede crear un archivo DLL para recibir una notificación anticipada y posterior de los eventos de conexión.

Un ejemplo de una aplicación que necesita recibir una notificación anticipada de un evento de conexión es el Servicio de acceso remoto (RAS). Es necesario informar a RAS antes de que se establezca una conexión, ya que puede ser necesario establecer una conexión de módem antes de realizar la conexión de red.

Del mismo modo, es posible que las aplicaciones necesiten limpiar los recursos después de realizar la conexión, por lo que requieren una notificación posterior a la conexión.

Las aplicaciones interesadas en recibir notificaciones avanzadas y adicionales de eventos de conexión deben proporcionar un archivo DLL que exporte dos funciones, [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) y [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify).

Después de implementar estas funciones, debe registrar el archivo DLL como se describe en [Registro para recibir notificaciones de conexión.](registering-to-receive-connection-notifications.md)

 

 



