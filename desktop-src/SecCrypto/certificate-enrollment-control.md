---
description: El control de inscripción de certificados se puede usar en una aplicación que debe solicitar la emisión de un certificado a un sujeto con nombre.
ms.assetid: ce6661b0-7ed2-452f-a54c-6705d14f3298
title: Control de inscripción de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e417a9db7984cbb58b7c2e3b51d828b6d61a97b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666455"
---
# <a name="certificate-enrollment-control"></a>Control de inscripción de certificados

El control de inscripción de certificados se puede usar en una aplicación que debe solicitar la emisión de un certificado a un sujeto con nombre. Está diseñado para aceptar datos en forma de cadena binaria (BSTR). Los datos pueden provienen de una página web o de la interfaz de usuario del sistema de desarrollo de Visual Basic o Visual C++. La salida del control de inscripción de certificados es una \# solicitud de certificado PKCS 10 que se puede enviar a una [*entidad de certificación*](../secgloss/c-gly.md) (CA).

![control de inscripción de certificados](images/xen-arch.png)

La interfaz de usuario recopila información necesaria sobre el usuario, el sujeto del certificado. Esta información se proporciona como una entrada BSTR para el control de inscripción de certificados. El control de inscripción de certificados genera la clave de firma adecuada, la clave de intercambio de claves o ambos pares de claves. A continuación, el control genera y firma \# una [*solicitud de certificado*](../secgloss/c-gly.md) PKCS 10 mediante la [*clave privada*](../secgloss/p-gly.md)generada. Después, el control de inscripción de certificados vincula el par de claves a un certificado ficticio temporal que se almacena en el almacén de solicitudes hasta que el certificado emitido se devuelve de una entidad de certificación. Por último, la aplicación envía la \# solicitud de certificado PKCS 10 a una CA.

Si la entidad de certificación aprueba la solicitud de certificado, la CA crea un certificado que contiene la clave pública. La CA también firma y devuelve el certificado.

Cuando el certificado solicitado se devuelve desde la entidad de certificación, la aplicación vuelve \# a pasar el mensaje PKCS 7 al control de inscripción de certificados donde se extrae el certificado o la cadena de certificados del \# mensaje PKCS 7. El certificado y los demás certificados de la cadena de confianza se almacenan en un [*almacén de certificados*](../secgloss/c-gly.md). El certificado devuelto no se modifica de ninguna manera. Cualquier aplicación compatible con certificados ahora puede tener acceso a este certificado desde el almacén.

Un administrador utiliza el control de inscripción de tarjetas inteligentes para inscribirse en nombre de los usuarios de tarjetas inteligentes. El proceso de inscripción da lugar a la emisión de un certificado que se almacena en la tarjeta inteligente de un usuario.

El control de inscripción de tarjetas inteligentes se incluye en Scrdenrl.dll y consta de un objeto, **SCrdEnr**. No se incluye ningún otro objeto en Scrdenrl.dll. Este objeto de inscripción de tarjeta inteligente se puede usar con un lenguaje de script, como Visual Basic Scripting Edition (VBScript).

Se debe instalar un [*lector de tarjeta inteligente*](../secgloss/r-gly.md) en el equipo que ejecuta el control de inscripción de tarjetas inteligentes.

Además, el emisor de la tarjeta inteligente debe haber obtenido un certificado de firma basado en la plantilla de certificado "EnrollmentAgent". Este certificado de firma se usará para firmar la solicitud de certificado generada en nombre del destinatario de la tarjeta inteligente. De forma predeterminada, se concede permiso a los administradores de dominio para solicitar un certificado basado en la plantilla "agente de inscripción". A otro usuario se le puede conceder permiso para inscribirse para un certificado "EnrollmentAgent" (por medio del complemento MMC sitios y servicios de Active Directory); de este modo, sin embargo, permite que este usuario emita automáticamente una tarjeta inteligente con privilegios de administrador de dominio.

 

 
