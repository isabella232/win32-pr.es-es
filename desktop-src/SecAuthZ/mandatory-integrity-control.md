---
description: Proporciona un mecanismo para controlar el acceso a objetos protegibles.
ms.assetid: 5923cb4c-f663-40d2-989a-07d71ac475db
title: Control de integridad de credenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac1a39cfc1d1ab819181e37c17328d6015a884f9ae1cce546643480351341b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117781498"
---
# <a name="mandatory-integrity-control"></a>Control de integridad de credenciales

Control de integridad de credenciales (MIC) proporciona un mecanismo para controlar el acceso a objetos protegibles. Este mecanismo se suma al control de acceso discrecional y evalúa el acceso antes de evaluar las comprobaciones de acceso en la lista de control de acceso [*discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) de un objeto.

MIC usa los niveles de integridad y la directiva obligatoria para evaluar el acceso. [*A las entidades de seguridad*](/windows/desktop/SecGloss/s-gly) y los objetos protegibles se les asignan niveles de integridad que determinan sus niveles de protección o acceso. Por ejemplo, una entidad de seguridad con un nivel de integridad bajo no puede escribir en un objeto con un nivel de integridad medio, incluso si la DACL de ese objeto permite el acceso de escritura a la entidad de seguridad.

Windows define cuatro niveles de integridad: bajo, medio, alto y sistema. Los usuarios estándar reciben usuarios medios y elevados que reciben un alto. Los procesos que se inician y los objetos que crea reciben el nivel de integridad (medio o alto) o bajo si el nivel del archivo ejecutable es bajo; los servicios del sistema reciben integridad del sistema. El sistema operativo trata los objetos que carecen de una etiqueta de integridad como medios. esto evita que el código de baja integridad modifique objetos sin etiquetar. Además, Windows garantiza que los procesos que se ejecutan con un nivel de integridad bajo no puedan obtener acceso a un proceso asociado a un contenedor de aplicaciones.

## <a name="integrity-labels"></a>Etiquetas de integridad

Las etiquetas de integridad especifican los niveles de integridad de los objetos protegibles y las entidades de seguridad. Las etiquetas de integridad se representan mediante [*SID de integridad.*](/windows/desktop/SecGloss/i-gly) El SID de integridad de un objeto protegible se almacena en su [*lista de control de acceso*](/windows/desktop/SecGloss/s-gly) del sistema (SACL). La SACL contiene una entrada de [*control*](/windows/desktop/SecGloss/a-gly) de acceso [**\_ \_ \_ (ACE)**](/windows/desktop/api/Winnt/ns-winnt-system_mandatory_label_ace) SYSTEM MANDATORY LABEL ACE que, a su vez, contiene el SID de integridad. Cualquier objeto sin un SID de integridad se trata como si tuviera integridad media.

El SID de integridad de una entidad de seguridad se almacena en su token de acceso. Un token de acceso puede contener uno o varios SID de integridad.

Para obtener información detallada sobre los SID de integridad definida, vea [SID conocidos.](well-known-sids.md)

## <a name="process-creation"></a>Creación de un proceso

Cuando un usuario intenta iniciar un archivo ejecutable, el nuevo proceso se crea con el nivel mínimo de integridad del usuario y el nivel de integridad del archivo. Esto significa que el nuevo proceso nunca se ejecutará con mayor integridad que el archivo ejecutable. Si el usuario administrador ejecuta un programa de baja integridad, el token del nuevo proceso funciona con el nivel de integridad bajo. Esto ayuda a proteger a un usuario que inicia código no confiable frente a acciones malintencionadas realizadas por ese código. Los datos de usuario, que se encuentra en el nivel de integridad de usuario típico, están protegidos por escritura en este nuevo proceso.

## <a name="mandatory-policy"></a>Directiva obligatoria

La ACE DE ETIQUETA OBLIGATORIA DEL SISTEMA en la SACL de un objeto protegible contiene una máscara de acceso que especifica el acceso al que se conceden las entidades de seguridad con niveles de integridad inferiores al objeto. [**\_ \_ \_**](/windows/desktop/api/Winnt/ns-winnt-system_mandatory_label_ace) Los valores definidos para esta máscara de acceso son **SYSTEM \_ MANDATORY \_ LABEL NO \_ WRITE \_ \_ UP**, **SYSTEM \_ MANDATORY LABEL NO READ \_ \_ \_ \_ UP** y **SYSTEM \_ MANDATORY LABEL NO EXECUTE \_ \_ \_ \_ UP**. De forma predeterminada, el sistema crea todos los objetos con una máscara de acceso **de SYSTEM \_ MANDATORY LABEL NO WRITE \_ \_ \_ \_ UP**.

Cada token de acceso también especifica una directiva obligatoria establecida por la autoridad de seguridad [*local*](/windows/desktop/SecGloss/l-gly) (LSA) cuando se crea el token. Esta directiva se especifica mediante una [**estructura DE DIRECTIVA OBLIGATORIA \_ \_ DE TOKEN**](/windows/desktop/api/Winnt/ns-winnt-token_mandatory_policy) asociada al token. Esta estructura se puede consultar llamando a la función [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) con el valor del *parámetro TokenInformationClass* establecido **en TokenMandatoryPolicy**.

 

 
