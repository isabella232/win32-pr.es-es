---
description: El enrutador de proveedor múltiple (MPR) llama a las funciones de notificación de conexión cuando se conecta o desconecta un recurso de red. Para recibir estas notificaciones, puede implementar estas funciones en un archivo DLL.
ms.assetid: 62559eab-dd2f-43fa-9b09-5e4d82efc879
title: API de notificación de conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 352d5cb09923a666e3fe1474e9fd2ebe033f05be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155904"
---
# <a name="connection-notification-api"></a>API de notificación de conexión

El [*enrutador de proveedor múltiple*](/windows/desktop/SecGloss/m-gly) (MPR) llama a las funciones de notificación de conexión cuando se conecta o desconecta un recurso de red. Para recibir estas notificaciones, puede implementar estas funciones en un archivo DLL.

El MPR llama a la función [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) antes y después de intentar cada operación Add-Connection ([**WNetAddConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona), [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a)o [**WNetAddConnection3**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a)). No se llama a esta función cuando el MPR está restaurando automáticamente las conexiones de red.

El MPR llama a la función [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify) antes y después de intentar cada operación de cancelación de conexión ([**WNetCancelConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) o [**WNetCancelConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)).

Para obtener más información acerca de las funciones de WNet, consulte [redes de Windows](/windows/desktop/WNet/windows-networking-wnet-).

Para obtener más información acerca de cómo crear y registrar una aplicación que recibe notificaciones de conexión de red, consulte recepción de notificaciones de [conexión](receiving-connection-notifications.md) y [registro para recibir notificaciones de conexión](registering-to-receive-connection-notifications.md).

 

 
