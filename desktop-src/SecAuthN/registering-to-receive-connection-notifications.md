---
description: Después de crear un archivo DLL para recibir notificaciones de conexión, debe registrarlo en el sistema.
ms.assetid: 1a389de1-367d-4b07-a420-4af431d48b7f
title: Registro para recibir notificaciones de conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812c47ba43fe13e4908a1812f7c67f38a94bce5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813587"
---
# <a name="registering-to-receive-connection-notifications"></a>Registro para recibir notificaciones de conexión

Después de crear un archivo DLL para recibir notificaciones de conexión, debe registrarlo en el sistema. Para ello, agregue un valor **reg \_ Expand \_** en el

**HKEY \_ Sistema \_ del equipo local** NetworkProvider de los \\  \\  \\  \\  \\ **notificantes**

. Este valor especifica la ruta de acceso al archivo DLL que implementa la [API de notificación de conexión](connection-notification-api.md).

El valor puede tener cualquier nombre. Todos los valores de la clave **NotifyTo** se tratan como rutas de acceso a los archivos DLL a los que se notifican los eventos de conexión. Se recomienda usar un nombre que identifique el archivo DLL. Esto reduce la posibilidad de un conflicto de nombres con otras aplicaciones de notificación de conexión.

Para obtener más información sobre cómo crear una aplicación que reciba notificaciones de conexión, consulte [recibir notificaciones de conexión](receiving-connection-notifications.md).

 

 



