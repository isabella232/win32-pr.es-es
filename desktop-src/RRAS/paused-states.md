---
title: Estados en pausa
description: Durante una operación de conexión, puede haber ocasiones en las que el servidor remoto no pueda continuar sin información adicional del usuario local.
ms.assetid: a1a36b2a-33df-4cba-85a6-f4225779cd63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec66a63adbee524ec231b5c9dd9b0b410c8f4fbc73746ae9b924294c680b4a9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029145"
---
# <a name="paused-states"></a>Estados en pausa

Durante una operación de conexión, puede haber ocasiones en las que el servidor remoto no pueda continuar sin información adicional del usuario local. A partir Windows NT 3.5, la [**función RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) admite estados en pausa. Un estado en pausa permite que el Connection Manager remoto suspenda una operación de conexión para que la aplicación cliente ras pueda recopilar información del usuario.

Los estados en pausa son útiles en las situaciones siguientes:

-   Cuando el usuario necesita proporcionar un número [de devolución de](callback-connections.md) llamada.
-   Cuando se produce un error en la autenticación del usuario, el usuario puede escribir un nombre de usuario y una contraseña diferentes.
-   Cuando la contraseña del usuario ha expirado, el usuario puede proporcionar una nueva contraseña.

De forma predeterminada, la compatibilidad con el estado en pausa está deshabilitada. Los clientes RAS que quieran admitir estados en pausa deben establecer la marca PausedStates de RDEOPTS en la estructura \_ [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) que se pasa como parámetro a [**RasDial.**](/windows/desktop/api/Ras/nf-ras-rasdiala)

Cuando se produce un estado en pausa, el Connection Manager remoto invoca el controlador de notificaciones del cliente. Si la compatibilidad con el estado en pausa está deshabilitada, el mensaje de notificación indica un error y se produce un error en la operación de conexión. Si está habilitada, el Connection Manager pausa la operación de conexión para esperar la respuesta del cliente RAS. El cliente RAS puede reanudar la operación de conexión mediante una segunda llamada a [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) o finalizarla mediante una llamada a la [**función RasHangUp.**](/windows/desktop/api/Ras/nf-ras-rashangupa)

Después de obtener la entrada del usuario, el cliente RAS reinicia la operación de conexión llamando de nuevo [**a RasDial.**](/windows/desktop/api/Ras/nf-ras-rasdiala) Esta segunda **llamada RasDial** debe especificar la siguiente información:

-   Identificador de conexión devuelto por la llamada [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) original.
-   El mismo controlador de notificaciones que la llamada [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) original.
-   Entrada del usuario en los miembros adecuados de la [**estructura RASDIALPARAMS.**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) Otros miembros de la **estructura RASDIALPARAMS** deben tener la misma información que se especificó en la llamada [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) original.

La segunda [**llamada RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) no se puede realizar desde dentro del controlador de notificaciones.

 

 