---
title: Instrucciones de seguridad
description: Es importante mantener al usuario informado sobre los posibles problemas de seguridad.
ms.assetid: f0c041fd-3cc5-491e-b088-6c93fcd61def
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3d4214ba4582394ed555bafd58551e8b047493
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149508"
---
# <a name="security-guideline"></a>Instrucciones de seguridad

Es importante mantener al usuario informado sobre los posibles problemas de seguridad.

## <a name="notify-the-user-of-security-related-events"></a>Notificar al usuario de Security-Related eventos

Notifique siempre al usuario cualquier cambio en la seguridad, si se trata de un error relacionado con la seguridad, como un error en el certificado o un cambio en la seguridad del protocolo subyacente, como el cambio de un sitio HTTPS a un sitio HTTP.

## <a name="notify-the-user-of-security-related-errors"></a>Notificar al usuario de Security-Related errores

Cuando la aplicación recibe un mensaje de error que puede indicar un problema de seguridad, la función **InternetErrorDlg** proporciona una interfaz estándar y familiar para notificar al usuario en la mayoría de los casos.

Entre los errores que se encuentran en esta categoría se encuentran:

**ERROR \_ de Internet de \_ http \_ a \_ https \_ en \_ redir**

**ERROR \_ de \_ CA no válida de Internet \_**

**ERROR: la \_ publicación en Internet \_ \_ \_ no es \_ segura**

**errores de certificado de ERROR de \_ Internet \_ s \_ \_**

**ERROR \_ de \_ \_ certificado CN de Internet \_ \_ no válido**

**ERROR la \_ fecha de certificado de Internet \_ s \_ \_ \_ no es válida**

Un error al notificar al usuario de errores como estos puede exponer al usuario a diferentes tipos de infracciones de seguridad, incluidos los ataques de suplantación de identidad o la divulgación de información involuntaria.

## <a name="notify-the-user-when-connection-security-changes"></a>Notificar al usuario cuando cambie la seguridad de la conexión

Notifique siempre al usuario cuando cambie la seguridad de la conexión, por ejemplo, de HTTPS a HTTP. De lo contrario, a menos que el usuario haya elegido explícitamente no recibir notificaciones de estos cambios, está ocultando los riesgos de la divulgación de información involuntaria.

Entre las funciones que informan de este cambio en la seguridad de la conexión se encuentran la función de devolución de llamada **InternetStatusCallback** y la función **InternetConfirmZoneCrossing** .

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 