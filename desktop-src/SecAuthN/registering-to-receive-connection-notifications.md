---
description: Después de crear un archivo DLL para recibir notificaciones de conexión, debe registrarlo en el sistema.
ms.assetid: 1a389de1-367d-4b07-a420-4af431d48b7f
title: Registro para recibir notificaciones de conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3a25e26e290700b8f343d3d543af4fbd7b709ff8b099522e4cd4b02b3d587f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919478"
---
# <a name="registering-to-receive-connection-notifications"></a>Registro para recibir notificaciones de conexión

Después de crear un archivo DLL para recibir notificaciones de conexión, debe registrarlo en el sistema. Para ello, agregue un **valor \_ REG EXPAND \_ SZ** en

**HKEY \_ NOTIFICACIÓN \_ DE LOCAL MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Control** \\ **NetworkProvider** \\ **Notifyees**

. Este valor especifica la ruta de acceso al archivo DLL que implementa la conexión [API de notificación](connection-notification-api.md).

El valor puede tener cualquier nombre. Todos los valores de la **clave Notifyees** se tratan como rutas de acceso a los archivos DLL a los que se notifican eventos de conexión. Se recomienda usar un nombre que identifique el archivo DLL. Esto disminuirá la posibilidad de que un nombre entre en conflicto con otras aplicaciones de notificación de conexión.

Para obtener más información sobre cómo crear una aplicación que recibe notificaciones de conexión, vea [Recepción de notificaciones de conexión.](receiving-connection-notifications.md)

 

 



