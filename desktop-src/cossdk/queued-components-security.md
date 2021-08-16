---
description: Seguridad de componentes en cola
ms.assetid: 3fbeb81a-e3e4-495b-b891-896877fab92f
title: Seguridad de componentes en cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682a9b409df2f605c259a6af6741dcc6e59d9fc23852b950a13225b24386c010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547089"
---
# <a name="queued-components-security"></a>Seguridad de componentes en cola

Cuando un cliente realiza una llamada de método a un objeto en cola, la llamada se realiza realmente a la grabadora, que la empaqueta como parte de un mensaje al servidor. El agente de escucha lee el mensaje de la cola y lo pasa al reproductor. El reproductor invoca el componente de servidor real y realiza la misma llamada de método. El componente de servidor debe observar el contexto de llamada de seguridad del cliente (no el contexto de llamada de seguridad del reproductor) cuando el reproductor realiza la llamada al método. La grabadora serializa el contexto de llamada de seguridad del cliente en el mensaje y el reproductor lo desmarta en el servidor antes de realizar la llamada al método. En lo que respecta al objeto de servidor, no hay ninguna diferencia en el contexto de seguridad entre una llamada directa desde el cliente y una llamada indirecta desde el reproductor. En concreto, los métodos invocados se ejecutan con los privilegios del remitente.

Un componente en cola de COM+ admite la semántica de seguridad basada en roles, al igual que otros componentes creados para su uso con aplicaciones COM+. Por lo tanto, los componentes de una aplicación en cola pueden usar interfaces de programación para detectar la pertenencia a roles de su autor de la llamada ([**ISecurityCallContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole)) o un usuario específico ([**ISecurityCallContext::IsUserInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-isuserinrole)). Se recomienda que cualquier componente en cola con un posible impacto en la seguridad use estas interfaces para comprobar explícitamente las credenciales del remitente.

La identidad del autor de la llamada es la identidad asociada a una llamada de método. La seguridad basada en rol usa la identidad del llamador y está presente en el contexto de la llamada de seguridad. En los componentes en cola, la identidad del autor de la llamada se representa como datos en el mensaje de Message Queuing. Message Queuing autentica la identidad del remitente del mensaje. Cuando la identidad del autor de la llamada y la identidad del remitente del mensaje son iguales, Message Queuing autentica tanto el mensaje como el autor de la llamada. Este es el caso habitual.

> [!Note]  
> Los componentes en cola de COM+ no admiten la seguridad de estilo de suplantación, lo que permite a un servidor obtener un token de acceso correspondiente a la identidad del cliente y usarlo para realizar comprobaciones de control de acceso o para actuar en el contexto de seguridad del cliente.

 

Cuando el autor de la llamada de un componente en cola interactúa con el componente a través de una grabadora fuera de proceso, las identidades del autor de la llamada y del remitente del mensaje (grabadora) pueden ser diferentes. En este caso, los componentes en cola de COM+ comprueban que el remitente del mensaje es miembro del rol Usuario de confianza de QC en el servidor. Además, la grabadora fuera de proceso requiere un certificado de autenticación porque Message Queuing lo autentica.

Los miembros de la función Usuarios de confianza QC pueden especificar una identidad arbitraria, lo que significa que un miembro malintencionado podría ejecutar una llamada a un componente en cola con privilegios elevados. Por lo tanto, se recomienda que el número de estos usuarios se mantenga en el mínimo posible.

Debido al riesgo de un ataque sofisticado asociado a cualquier mecanismo que propague la identidad a través de una red, así como al riesgo de un ataque de denegación de servicio simple al desbordar las colas con solicitudes no ejecutables, se recomienda implementar el servicio de componentes en cola com+ solo en una red de hosts de confianza, por ejemplo,  en una red privada o una red privada virtual, o detrás de un firewall configurado correctamente.

Los componentes en cola de COM+ se ejecuta a través de DCOM, por  lo que  puede ayudar a  proteger la integridad y confidencialidad de las llamadas a métodos en cola seleccionando Privacidad de paquetes como la configuración Nivel de autenticación de llamadas en la pestaña Seguridad de la hoja Propiedades de la aplicación en cola. 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad de COM+](com--security.md)
</dt> <dt>

[Limitaciones de seguridad en el modo de grupo de trabajo](security-limitations-in-workgroup-mode.md)
</dt> <dt>

[Especificar el protocolo de autenticación](specifying-the-authentication-protocol.md)
</dt> </dl>

 

 



