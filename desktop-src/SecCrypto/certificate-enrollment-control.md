---
description: El control de inscripción de certificados lo puede usar una aplicación que debe solicitar que se emita un certificado a un sujeto con nombre.
ms.assetid: ce6661b0-7ed2-452f-a54c-6705d14f3298
title: Control de inscripción de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f19499dad8c3d8b4d9720b285a4377c2f7b6b1903ca27f9e1cba17224fe1c857
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127134"
---
# <a name="certificate-enrollment-control"></a>Control de inscripción de certificados

El control de inscripción de certificados lo puede usar una aplicación que debe solicitar que se emita un certificado a un sujeto con nombre. Está diseñado para aceptar datos en forma de una cadena binaria (BSTR). Los datos pueden provienen de una página web o de la interfaz de usuario del Visual Basic o Visual C++ de desarrollo. El resultado del control de inscripción de certificados es una solicitud de certificado PKCS 10 que se puede enviar \# a una entidad de [*certificación*](../secgloss/c-gly.md) (CA).

![control de inscripción de certificados](images/xen-arch.png)

La información necesaria sobre el usuario, el sujeto del certificado, la recopila el Interfaz de usuario. Esta información se proporciona como entrada BSTR para el control de inscripción de certificados. El Control de inscripción de certificados genera la clave de firma, la clave de intercambio de claves o ambos pares de claves adecuados. A continuación, el control genera y firma una solicitud de certificado PKCS \# 10 mediante la [*clave privada generada.*](../secgloss/p-gly.md) [](../secgloss/c-gly.md) A continuación, el control de inscripción de certificados vincula el par de claves a un certificado ficticio temporal que se almacena en el almacén de solicitudes hasta que el certificado emitido se devuelve de una entidad de certificación. Por último, la aplicación envía la solicitud de certificado PKCS \# 10 a una entidad de certificación.

Si la ca aprueba la solicitud de certificado, la ca crea un certificado que contiene la clave pública. La CA también firma y devuelve el certificado.

Cuando se devuelve el certificado solicitado desde la ca, la aplicación devuelve el mensaje PKCS 7 al control de inscripción de certificados donde se extrae el certificado o la cadena de certificados del \# mensaje PKCS \# 7. El certificado y cualquier otro certificado de la cadena de confianza se almacenan en un almacén [*de certificados*](../secgloss/c-gly.md). El certificado devuelto no se modifica de ninguna manera. Cualquier aplicación que tenga en cuenta certificados ahora puede acceder a este certificado desde el almacén.

Un administrador usa el control de inscripción de tarjetas inteligentes para inscribirse en nombre de los usuarios de tarjetas inteligentes. El proceso de inscripción da como resultado la emisión de un certificado que se almacena en la tarjeta inteligente de un usuario.

El control de inscripción de tarjeta inteligente se encuentra en Scrdenrl.dll y consta de un objeto, **SCrdEnr**. No se incluyen otros objetos en Scrdenrl.dll. Este objeto de inscripción de tarjeta inteligente se puede usar con un lenguaje de script, como Visual Basic Scripting Edition (VBScript).

Se [*debe instalar un lector*](../secgloss/r-gly.md) de tarjetas inteligentes en el equipo que ejecuta el control de inscripción de tarjetas inteligentes.

Además, el emisor de tarjeta inteligente debe haber obtenido un certificado de firma basado en la plantilla de certificado "EnrollmentAgent". Este certificado de firma se usará para firmar la solicitud de certificado generada en nombre del destinatario de la tarjeta inteligente. De forma predeterminada, a los administradores de dominio se les concede permiso para solicitar un certificado basado en la plantilla "Agente de inscripción". Se puede conceder permiso a otro usuario para inscribirse para un certificado "EnrollmentAgent" (mediante el complemento MMC Active Directory Sites and Services); Sin embargo, esto permite a este usuario emitir una tarjeta inteligente con privilegios de administrador de dominio.

 

 
