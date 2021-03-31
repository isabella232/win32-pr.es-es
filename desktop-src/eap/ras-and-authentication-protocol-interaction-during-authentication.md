---
title: Interacción del Protocolo de punto de acceso y autenticación durante la autenticación
description: La función RasEapMakeMessage controla la mayoría de la interacción entre el protocolo de autenticación y el punto de acceso (AP).
ms.assetid: edc128e0-3104-4df9-80f4-b2aebcfe1087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e486e3a10e323f28bc2f6fef4c131acfc095b48
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077592"
---
# <a name="access-point-and-authentication-protocol-interaction-during-authentication"></a>Interacción del Protocolo de punto de acceso y autenticación durante la autenticación

La función [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) controla la mayoría de la interacción entre el protocolo de autenticación y el punto de acceso (AP). **RasEapMakeMessage** procesa los paquetes EAP entrantes y crea paquetes EAP para la transmisión al equipo remoto del mismo nivel. También procesa eventos como los tiempos de espera y la finalización de la autenticación.

Si se recibe un mensaje desde el elemento remoto del mismo nivel, el servicio de autenticación de AP llama a [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)), pasando un puntero al mensaje recibido en el parámetro *pReceivePacket* .

Si el servicio llama a [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) con *PReceivePacket* establecido en **null**, el AP inicia el cuadro de diálogo con el protocolo de autenticación o solicita que el protocolo vuelva a enviar el último paquete. El protocolo de autenticación debe determinar qué acción está llevando a cabo el servicio en función de su estado y del contexto del mensaje.

En la devolución de [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)), el valor del miembro de **acción** de la estructura de [**\_ \_ salida EAP de PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) indica qué acción toma el servicio de autenticación. El miembro de **acción** toma valores del tipo enumerado de la [**\_ \_ acción EAP de PPP**](/windows/desktop/api/Raseapif/ne-raseapif-ppp_eap_action) .

Si **Action** es **EAPACTION \_ send**, **EAPACTION \_ SendAndDone**, **EAPACTION \_ SendWithTimeout** o **EAPACTION \_ SendWithTimeoutInteractive**, el servicio transmite el paquete al que apunta el parámetro *pSendPacket* al elemento remoto del mismo nivel.

El valor de **\_ SendWithTimeout de EAPACTION** permite un tiempo de espera, después del cual el servicio de autenticación asume que se perdió el vínculo y desconecta la sesión.

El valor de **EAPACTION \_ SendWithTimeoutInteractive** permite una cantidad infinita de tiempo de espera. El autenticador debe utilizar este valor cuando se espera la entrada del usuario en el cliente. Este tiempo de espera permite al usuario realizar una cantidad de tiempo no especificada para completar la entrada necesaria.

Si **Action** es **EAPACTION \_ SendWithTimeout** o **EAPACTION \_ SendWithTimeoutInteractive**, el protocolo de autenticación debe establecer el miembro **dwIdExpected** de la estructura de [**\_ \_ salida EAP de PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) en el identificador del siguiente paquete que se espera del elemento remoto del mismo nivel. Independientemente de si el siguiente paquete recibido del mismo nivel coincide con este valor, el servicio de autenticación pasa el paquete al Protocolo de autenticación en una llamada subsiguiente a [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)). El protocolo de autenticación puede descartar el paquete de forma silenciosa simplemente devolviendo un **paquete de error \_ PPP \_ no válido \_**. Si no se recibe un paquete con el identificador esperado en el período de tiempo de espera configurado, el servicio de autenticación todavía llama a **RasEapMakeMessage**. En este caso, la llamada se realiza con el parámetro *pReceivePacket* establecido en **null** para indicar que el paquete anterior debe volver a enviarse.

Si el miembro de **acción** es **EAPACTION \_ Done** o **EAPACTION \_ SendAndDone**, el servicio de autenticación examina el miembro **dwAuthResultCode** de la [**\_ \_ salida EAP de PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output). Si **dwAuthResultCode** NO es un \_ error, la autenticación se realizó correctamente. Si **dwAuthResultCode** es un valor distinto de \_ error, se produjo un error en la autenticación. El código de error devuelto para el caso de error debe proviene de Raserror. h, Mprerror. h o Winerror. h. Los códigos de retorno posibles incluyen, entre otros, lo siguiente:

-   ERROR \_ sin \_ permiso de marcado \_
-   ERROR \_ passwd \_ expiró
-   cuenta de ERROR \_ \_ deshabilitada
-   ERROR \_ de \_ horas de inicio de sesión restringidas \_
-   ERROR de \_ autenticación \_ interna

En el caso en el que la **acción** es **EAPACTION \_ Done** o **EAPACTION \_ SendAndDone**, el miembro **pUserAttributes** debe apuntar a atributos que invalidan los atributos del mismo tipo que se pasaron al servidor en la llamada a [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)).

El protocolo de autenticación en el servidor puede solicitar que el servicio de autenticación invoque el proveedor de autenticación actual devolviendo **EAPACTION \_ Authenticate** en el miembro de **acción** en la [**\_ \_ salida EAP de PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output). En este caso, el puntero **pUserAttributes** de **\_ \_ salida EAP de PPP** solo apunta a los atributos generados por el protocolo de autenticación en el servidor. No incluye ninguno de los atributos que se pasaron al servidor en la llamada a [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)). El proveedor de autenticación no requiere estos atributos iniciales, ya que las credenciales de autenticación se encuentran dentro del propio mensaje EAP, no en un atributo RADIUS independiente. Cuando el servicio de autenticación responde a la acción de **\_ autenticación EAPACTION** , **pUserAttributes** en [**\_ \_ entrada EAP de PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input), apunta a todos los atributos generados durante la autenticación. Estos atributos se devuelven al Protocolo de autenticación en el cliente.

Si el protocolo de autenticación usa **EAPACTION \_ Authenticate**, el proveedor de autenticación realiza una autenticación PAP o MD5-CHAP. Este método de autenticación solo se puede usar con clientes de Windows.

Si el protocolo de autenticación autentica al usuario sin depender de un proveedor de autenticación, no es necesario que el protocolo establezca la **acción** en **EAPACTION \_ Authenticate**. Un ejemplo de este caso es EAP-Transport Layer Security (TLS).

El paquete EAP Success es un paquete no confirmado. Por lo tanto, puede perderse y no reenviarse por el servidor. Si el servicio de autenticación en el cliente recibe un paquete NCP (Protocolo de control de red), el servicio de autenticación del lado servidor continúa como si la autenticación se realizara correctamente. Esto se debe a que el servidor ha pasado a la fase NCP de PPP. En consecuencia, el servicio de autenticación llama a [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) con el miembro **fSuccessPacketReceived** de la estructura de [**\_ \_ entrada EAP de PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) establecida en **true**.

Durante el transcurso de la sesión de autenticación, es posible que el protocolo de autenticación requiera interacción directa con el usuario en el cliente. El proveedor del Protocolo de autenticación puede proporcionar una interfaz de usuario interactiva para este fin. El protocolo de autenticación puede solicitar que el servicio muestre la interfaz de usuario interactiva estableciendo los miembros **fInvokeInteractiveUI**, **pUIContextData** y **dwSizeOfUIContextData** en la estructura de [**\_ \_ salida EAP de PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) . Para obtener más información sobre el uso de una interfaz de usuario interactiva, consulte [Interactive User Interface](interactive-user-interface.md).

El protocolo de autenticación debe mostrar una interfaz de usuario solo a través del mecanismo descrito en [interfaz de usuario interactiva](interactive-user-interface.md). Si el propio protocolo de autenticación muestra la interfaz de usuario, el subproceso PPP se bloquea hasta que se descarta la interfaz de usuario.

Si durante el proceso de autenticación, [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) devuelve cualquier valor distinto **de \_ error** o **error en el \_ \_ \_ paquete ppp no válido**, la sesión se desconecta y el error se registra (en el servidor) o se muestra al usuario (en el cliente).

 

 