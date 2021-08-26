---
description: El enrutador de varios proveedores (MPR) llama a las funciones de notificación de conexión cuando se conecta o desconecta un recurso de red. Para recibir estas notificaciones, puede implementar estas funciones en un archivo DLL.
ms.assetid: 62559eab-dd2f-43fa-9b09-5e4d82efc879
title: Conexión API de notificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0afaa2e08e6a88f101e8914d9d98a40d6024bdf942ed4bcb0fd1924bc5800213
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883315"
---
# <a name="connection-notification-api"></a>Conexión API de notificación

El [*enrutador de varios proveedores*](/windows/desktop/SecGloss/m-gly) (MPR) llama a las funciones de notificación de conexión cuando se conecta o desconecta un recurso de red. Para recibir estas notificaciones, puede implementar estas funciones en un archivo DLL.

MpR llama a la [**función AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) antes y después de intentar cada operación de conexión de complemento ([**WNetAddConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona), [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a)o [**WNetAddConnection3**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a)). No se llama a esta función cuando mpr restaura automáticamente las conexiones de red.

El MPR llama a la [**función CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify) antes y después de intentar cada operación de cancelación de conexión ([**WNetCancelConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) o [**WNetCancelConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)).

Para obtener más información sobre las funciones de WNet, [vea Windows Networking](/windows/desktop/WNet/windows-networking-wnet-).

Para obtener más información sobre cómo crear y registrar una aplicación que recibe notificaciones de conexión de red, vea [Recepción](receiving-connection-notifications.md) de notificaciones de conexión y Registro para recibir notificaciones [de conexión.](registering-to-receive-connection-notifications.md)

 

 
