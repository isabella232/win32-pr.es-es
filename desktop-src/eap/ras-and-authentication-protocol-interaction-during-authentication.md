---
title: Interacción del punto de acceso y el protocolo de autenticación durante la autenticación
description: La función RasEapMakeMessage controla la mayor parte de la interacción entre el protocolo de autenticación y el punto de acceso (AP).
ms.assetid: edc128e0-3104-4df9-80f4-b2aebcfe1087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aea18883225a2a34e592b73e0cdc93b019c1bf466124976f01851febb2a17d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117775"
---
# <a name="access-point-and-authentication-protocol-interaction-during-authentication"></a>Interacción del punto de acceso y el protocolo de autenticación durante la autenticación

La [**función RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) controla la mayoría de la interacción entre el protocolo de autenticación y el punto de acceso (AP). **RasEapMakeMessage procesa** los paquetes EAP entrantes y crea paquetes EAP para su transmisión al par remoto. También procesa eventos como tiempos de espera y finalización de autenticación.

Si se recibe un mensaje del elemento remoto del mismo nivel, el servicio de autenticación de AP llama a [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)), pasando un puntero al mensaje recibido en el *parámetro pReceivePacket.*

Si el servicio llama a [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) con *pReceivePacket* establecido en **NULL,** la AP inicia el diálogo con el protocolo de autenticación o solicita que el protocolo vuelva a enviar el último paquete. El protocolo de autenticación debe determinar qué acción está tomando el servicio en función de su estado y del contexto del mensaje.

En la devolución de [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)), el valor del miembro **Action** de la estructura [**PPP EAP \_ \_ OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) indica qué acción, si la hay, realiza el servicio de autenticación. El **miembro Action** toma valores del tipo enumerado PPP EAP [**\_ \_ ACTION.**](/windows/desktop/api/Raseapif/ne-raseapif-ppp_eap_action)

Si **Action** es **EAPACTION \_ Send**, **EAPACTION \_ SendAndDone,** **EAPACTION \_ SendWithTimeout** o **EAPACTION \_ SendWithTimeoutInteractive,** el servicio transmite el paquete al que apunta el parámetro *pSendPacket* al par remoto.

El **valor \_ sendWithTimeout** de EAPACTION permite un tiempo de espera, después del cual el servicio de autenticación asume que se perdió el vínculo y desconecta la sesión.

El **valor \_ sendWithTimeoutInteractive** de EAPACTION permite que se produzca una cantidad infinita de tiempo de espera. El autenticador debe usar este valor cuando se espera la entrada del usuario en el cliente. Este tiempo de espera permite al usuario una cantidad de tiempo no especificada para completar la entrada necesaria.

Si **Action** es **EAPACTION \_ SendWithTimeout** o **EAPACTION \_ SendWithTimeoutInteractive,** el protocolo de autenticación debe establecer el miembro **dwIdExpected** de la estructura [**PPP EAP \_ \_ OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) en el identificador del siguiente paquete que se espera del par remoto. Independientemente de si el siguiente paquete recibido del mismo nivel coincide con este valor, el servicio de autenticación pasa el paquete al protocolo de autenticación en una llamada posterior a [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)). El protocolo de autenticación puede descartar silenciosamente el paquete simplemente devolviendo **ERROR \_ PPP INVALID \_ \_ PACKET**. Si no se recibe un paquete con el identificador esperado dentro del período de tiempo de espera configurado, el servicio de autenticación todavía llama a **RasEapMakeMessage**. En este caso, la llamada se realiza con el parámetro *pReceivePacket* establecido en **NULL** para indicar que el paquete anterior debe enviarse de nuevo.

Si el **miembro Action** es **EAPACTION \_ Done** o **EAPACTION \_ SendAndDone,** el servicio de autenticación examina el **miembro dwAuthResultCode** de [**PPP EAP \_ \_ OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output). Si **dwAuthResultCode** es NO \_ ERROR, la autenticación se ha hecho correctamente. Si **dwAuthResultCode** es un valor distinto de NO \_ ERROR, se produjo un error en la autenticación. El código de error devuelto para el caso de error debe ser Raserror.h, Mprerror.h o Winerror.h. Los códigos de retorno posibles incluyen, entre otros, los siguientes:

-   ERROR \_ SIN PERMISO DE ACCESO \_ \_ TELEFÓNICO
-   ERROR \_ PASSWD \_ EXPIRED
-   ERROR \_ ACCT \_ DISABLED
-   ERROR \_ RESTRICTED \_ LOGON \_ HOURS
-   ERROR \_ AUTH \_ INTERNAL

En el caso de que **Action** sea **EAPACTION \_ Done** o **EAPACTION \_ SendAndDone,** el miembro **pUserAttributes** debe apuntar a atributos que invalide atributos del mismo tipo que se pasaron al servidor en la llamada a [**RasEapBegin.**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))

El protocolo de autenticación en el servidor puede solicitar que el servicio de autenticación invoque el proveedor de autenticación actual devolviendo **EAPACTION \_ Authenticate** en el miembro **Action** en [**PPP EAP \_ \_ OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output). En este caso, el **puntero pUserAttributes** en **PPP EAP \_ \_ OUTPUT** solo apunta a los atributos generados por el protocolo de autenticación en el servidor. No incluye ninguno de los atributos que se pasaron al servidor en la llamada a [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)). El proveedor de autenticación no requiere estos atributos iniciales porque las credenciales de autenticación están dentro del propio mensaje EAP, no en un atributo RADIUS independiente. Cuando el servicio de autenticación responde a la acción **AUTENTICACIÓN EAPACTION, \_** **pUserAttributes** en [**PPP EAP \_ \_ INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)apunta a todos los atributos generados durante la autenticación. Estos atributos se devuelven al protocolo de autenticación en el cliente.

Si el protocolo de autenticación **usa AUTENTICACIÓN \_ EAPACTION,** el proveedor de autenticación realiza LAN o MD5-CHAP. Este método de autenticación solo se puede usar con Windows clientes.

Si el protocolo de autenticación autentica al usuario sin depender de un proveedor de autenticación, no es necesario que el protocolo establezca alguna vez **Acción** en **EAPACTION \_ Authenticate**. Un ejemplo de este caso es EAP-Transport seguridad de capa de seguridad (TLS).

El paquete eap correcto es un paquete no reconocido. Por lo tanto, el servidor puede perderlo y no reenviarse. Si el servicio de autenticación del cliente recibe un paquete del Protocolo de control de red (NCP), el servicio de autenticación del lado servidor continúa como si la autenticación se realizara correctamente. Esto se debe a que el servidor ha pasado a la fase NCP de PPP. En consecuencia, el servicio de autenticación llama a [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) con el **miembro fSuccessPacketReceived** de la estructura [**PPP EAP \_ \_ INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) establecida en **TRUE.**

Durante el transcurso de la sesión de autenticación, el protocolo de autenticación puede requerir interacción directa con el usuario en el cliente. El proveedor del protocolo de autenticación puede proporcionar una interfaz de usuario interactiva para este propósito. El protocolo de autenticación puede solicitar que el servicio muestre la interfaz de usuario interactiva estableciendo los miembros **fInvokeInteractiveUI**, **pUIContextData** y **dwSizeOfUIContextData** en la estructura [**PPP EAP \_ \_ OUTPUT.**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) Para obtener más información sobre el uso de una interfaz de usuario interactiva, vea [Interactive Interfaz de usuario](interactive-user-interface.md).

El protocolo de autenticación solo debe mostrar una interfaz de usuario a través del mecanismo descrito en [Interactive Interfaz de usuario](interactive-user-interface.md). Si el propio protocolo de autenticación muestra la interfaz de usuario, el subproceso PPP se bloquea hasta que se descarta la interfaz de usuario.

Si durante el proceso de autenticación, [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) devuelve cualquier valor distinto de **NO \_ ERROR** o **ERROR PPP INVALID \_ \_ \_ PACKET**, la sesión se desconecta y el error se registra (en el servidor) o se muestra al usuario (en el cliente).

 

 