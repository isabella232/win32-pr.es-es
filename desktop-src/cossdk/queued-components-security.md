---
description: Seguridad de componentes en cola
ms.assetid: 3fbeb81a-e3e4-495b-b891-896877fab92f
title: Seguridad de componentes en cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b51592f6216d7380e877f2cd582a277f1583b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153258"
---
# <a name="queued-components-security"></a>Seguridad de componentes en cola

Cuando un cliente realiza una llamada de método a un objeto en cola, la llamada se realiza realmente a la grabadora, que la empaqueta como parte de un mensaje en el servidor. El agente de escucha lee el mensaje de la cola y lo pasa al reproductor. El reproductor invoca el componente de servidor real y realiza la misma llamada de método. El componente de servidor debe observar el contexto de la llamada de seguridad del cliente (no el contexto de llamada de seguridad del reproductor) cuando el reproductor realiza la llamada al método. La grabadora calcula las referencias del contexto de la llamada de seguridad del cliente en el mensaje y el reproductor no las serializa en el servidor antes de efectuar la llamada al método. En lo que respecta al objeto de servidor, no hay ninguna diferencia en el contexto de seguridad entre una llamada directa desde el cliente y una llamada indirecta desde el reproductor. En concreto, los métodos invocados Execute con los privilegios del remitente.

Un componente en cola de COM+ admite la semántica de seguridad basada en roles, al igual que otros componentes creados para su uso con aplicaciones COM+. Por tanto, los componentes de una aplicación en cola pueden utilizar interfaces de programación para detectar la pertenencia a roles de su llamador ([**ISecurityCallContext:: IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole)) o un usuario específico ([**ISecurityCallContext:: IsUserInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-isuserinrole)). Se recomienda que cualquier componente en cola con un posible impacto en la seguridad Use estas interfaces para comprobar explícitamente las credenciales del remitente.

La identidad del autor de la llamada es la identidad asociada a una llamada al método. La seguridad basada en roles utiliza la identidad del autor de la llamada y está presente en el contexto de la llamada de seguridad. En los componentes en cola, la identidad del autor de la llamada se representa como datos en el mensaje de Message Queuing. Message Queue Server autentica la identidad del remitente del mensaje. Cuando la identidad del autor de la llamada y la identidad del remitente del mensaje son iguales, Message Queue Server autentica el mensaje y el autor de la llamada. Este es el caso habitual.

> [!Note]  
> Los componentes en cola de COM+ no admiten la seguridad de estilo de suplantación, que permite a un servidor obtener un token de acceso correspondiente a la identidad del cliente y usarlo para realizar comprobaciones de control de acceso o para actuar en el contexto de seguridad del cliente.

 

Cuando el autor de la llamada de un componente en cola está interactuando con el componente a través de una grabadora fuera de proceso, las identidades del autor de la llamada y del remitente del mensaje (grabador) pueden ser diferentes. En este caso, los componentes en cola de COM+ comprueban que el remitente del mensaje es miembro del rol de usuario de confianza QC en el servidor. Además, la grabadora fuera de proceso requiere un certificado de autenticación porque está siendo autenticado por Message Queuing.

Los miembros de la función Usuarios de confianza QC pueden especificar una identidad arbitraria, lo que significa que un miembro malintencionado podría ejecutar una llamada a un componente en cola con privilegios elevados. Por lo tanto, se recomienda que el número de estos usuarios se mantenga en el mínimo posible.

Debido al riesgo de un ataque complejo asociado a cualquier mecanismo que propague la identidad a través de una red, así como el riesgo de un ataque de denegación de servicio simple mediante la saturación de las colas con solicitudes no ejecutables, se recomienda implementar el servicio de componentes en cola de COM+ solo en una red de hosts de confianza, por ejemplo, en una red privada o una , o detrás de un firewall configurado correctamente.

Los componentes en cola de COM+ se ejecutan a través de DCOM, por lo que puede ayudar a proteger la integridad y la confidencialidad de las llamadas a métodos en cola seleccionando **privacidad de paquetes** como el **nivel de autenticación de la configuración de llamadas** en la pestaña **seguridad** de la hoja de **propiedades** de la aplicación en cola.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad de COM+](com--security.md)
</dt> <dt>

[Limitaciones de seguridad en el modo de grupo de trabajo](security-limitations-in-workgroup-mode.md)
</dt> <dt>

[Especificar el protocolo de autenticación](specifying-the-authentication-protocol.md)
</dt> </dl>

 

 



