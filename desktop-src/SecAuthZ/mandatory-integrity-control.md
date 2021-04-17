---
description: Proporciona un mecanismo para controlar el acceso a los objetos protegibles.
ms.assetid: 5923cb4c-f663-40d2-989a-07d71ac475db
title: Control de integridad de credenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c184ba01da0a55309fcb27ace9b0fe156edd6425
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "105654028"
---
# <a name="mandatory-integrity-control"></a>Control de integridad de credenciales

Control de integridad de credenciales (MIC) proporciona un mecanismo para controlar el acceso a los objetos protegibles. Este mecanismo se suma al control de acceso discrecional y evalúa el acceso antes de que se evalúen las comprobaciones de acceso de la [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) de un objeto.

MIC usa niveles de integridad y directivas obligatorias para evaluar el acceso. Las [*entidades de seguridad*](/windows/desktop/SecGloss/s-gly) y los objetos protegibles tienen asignados niveles de integridad que determinan sus niveles de protección o acceso. Por ejemplo, una entidad de seguridad con un nivel de integridad bajo no puede escribir en un objeto con un nivel de integridad medio, aunque la DACL de ese objeto permita el acceso de escritura a la entidad de seguridad.

Windows define cuatro niveles de integridad: baja, media, alta y sistema. Los usuarios estándar reciben un nivel alto de usuarios con privilegios elevados. Los procesos que se inician y los objetos que se crean reciben el nivel de integridad (medio o alto) o bajo si el nivel del archivo ejecutable es bajo; los servicios del sistema reciben la integridad del sistema. Los objetos que carecen de una etiqueta de integridad se tratan como medios del sistema operativo; Esto evita que el código de baja integridad modifique los objetos sin etiquetar. Además, Windows garantiza que los procesos que se ejecutan con un nivel de integridad bajo no pueden obtener acceso a un proceso asociado a un contenedor de la aplicación.

## <a name="integrity-labels"></a>Etiquetas de integridad

Las etiquetas de integridad especifican los niveles de integridad de los objetos protegibles y las entidades de seguridad. Las etiquetas de integridad se representan mediante [*SID de integridad*](/windows/desktop/SecGloss/i-gly). El SID de integridad de un objeto protegible se almacena en su [*lista de control de acceso de sistema*](/windows/desktop/SecGloss/s-gly) (SACL). La SACL contiene una [*entrada de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) [**\_ \_ \_ ACE de etiqueta obligatoria del sistema**](/windows/desktop/api/Winnt/ns-winnt-system_mandatory_label_ace) que a su vez contiene el SID de integridad. Cualquier objeto sin SID de integridad se trata como si tuviera integridad media.

El SID de integridad de una entidad de seguridad se almacena en su token de acceso. Un token de acceso puede contener uno o más SID de integridad.

Para obtener información detallada sobre los SID de integridad definidos, consulte [SID conocidos](well-known-sids.md).

## <a name="process-creation"></a>Creación de un proceso

Cuando un usuario intenta iniciar un archivo ejecutable, el nuevo proceso se crea con el nivel de integridad del usuario mínimo y el nivel de integridad de los archivos. Esto significa que el nuevo proceso nunca se ejecutará con una mayor integridad que el archivo ejecutable. Si el usuario administrador ejecuta un programa de baja integridad, el token del nuevo proceso funciona con el nivel de integridad baja. Esto ayuda a proteger a un usuario que inicia código no confiable de actos malintencionados realizados por ese código. Los datos de usuario, que se encuentra en el nivel de integridad de usuario típico, están protegidos contra escritura contra este nuevo proceso.

## <a name="mandatory-policy"></a>Directiva obligatoria

La ACE de [**\_ \_ \_ ACE de etiqueta obligatoria del sistema**](/windows/desktop/api/Winnt/ns-winnt-system_mandatory_label_ace) en la SACL de un objeto protegible contiene una máscara de acceso que especifica el acceso a las entidades de seguridad con niveles de integridad inferiores al objeto que se conceden. Los valores definidos para esta máscara de acceso son la **\_ etiqueta obligatoria del sistema no se \_ \_ \_ escribe \_**, la **\_ etiqueta obligatoria del sistema no se \_ \_ \_ Lee \_** y la **\_ etiqueta obligatoria del sistema no se \_ \_ \_ ejecuta \_**. De forma predeterminada, el sistema crea cada objeto con una máscara de acceso de **\_ etiqueta obligatoria del sistema no se \_ \_ \_ escribe \_**.

Cada token de acceso también especifica una directiva obligatoria establecida por la [*autoridad de seguridad local*](/windows/desktop/SecGloss/l-gly) (LSA) cuando se crea el token. Esta Directiva se especifica mediante una estructura de [**\_ \_ Directiva obligatoria de token**](/windows/desktop/api/Winnt/ns-winnt-token_mandatory_policy) asociada al token. Esta estructura se puede consultar mediante una llamada a la función [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) con el valor del parámetro *TokenInformationClass* establecido en **TokenMandatoryPolicy**.

 

 
