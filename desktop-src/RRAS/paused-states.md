---
title: Estados en pausa
description: Durante una operación de conexión, puede haber ocasiones en las que el servidor remoto no pueda continuar sin información adicional del usuario local.
ms.assetid: a1a36b2a-33df-4cba-85a6-f4225779cd63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914acb85ccf74c92b4bd4119966a421faddeb011
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359369"
---
# <a name="paused-states"></a>Estados en pausa

Durante una operación de conexión, puede haber ocasiones en las que el servidor remoto no pueda continuar sin información adicional del usuario local. A partir de Windows NT 3,5, la función [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) admite Estados en pausa. Un estado pausado permite al administrador de conexiones de acceso remoto suspender una operación de conexión para que la aplicación cliente RAS pueda recopilar información del usuario.

Los Estados pausados son útiles en las situaciones siguientes:

-   Cuando el usuario debe proporcionar un número de [devolución de llamada](callback-connections.md) .
-   Cuando se produce un error en la autenticación del usuario, el usuario puede escribir un nombre de usuario y una contraseña diferentes.
-   Cuando la contraseña del usuario ha expirado, el usuario puede proporcionar una nueva contraseña.

De forma predeterminada, la compatibilidad con el estado en pausa está deshabilitada. Los clientes RAS que deseen admitir Estados en pausa deben establecer la \_ marca RDEOPTS PausedStates en la estructura [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) pasada como parámetro en [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala).

Cuando se produce un estado de pausa, el administrador de conexiones de acceso remoto invoca al controlador de notificaciones del cliente. Si se deshabilita la compatibilidad con el estado de pausa, el mensaje de notificación indica un error y se produce un error en la operación de conexión. Si está habilitada, el administrador de conexiones pausa la operación de conexión para esperar la respuesta del cliente RAS. El cliente RAS puede reanudar la operación de conexión mediante una segunda llamada [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) , o bien finalizarla llamando a la función [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) .

Después de obtener la entrada del usuario, el cliente RAS reinicia la operación de conexión mediante una llamada a [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) de nuevo. Esta segunda llamada **rasdial** debe especificar la siguiente información:

-   Identificador de conexión que devolvió la llamada [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) original.
-   El mismo controlador de notificación que la llamada [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) original.
-   La entrada del usuario en los miembros adecuados de la estructura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) . Otros miembros de la estructura **RASDIALPARAMS** deben tener la misma información que se especificó en la llamada [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) original.

No se puede realizar la segunda llamada [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) desde el controlador de notificación.

 

 