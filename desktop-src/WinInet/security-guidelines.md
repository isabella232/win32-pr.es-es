---
title: Guía de seguridad
description: Es importante mantener informado al usuario sobre posibles problemas de seguridad.
ms.assetid: f0c041fd-3cc5-491e-b088-6c93fcd61def
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3d4214ba4582394ed555bafd58551e8b047493
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249380"
---
# <a name="security-guideline"></a>Guía de seguridad

Es importante mantener informado al usuario sobre posibles problemas de seguridad.

## <a name="notify-the-user-of-security-related-events"></a>Notificar al usuario de Security-Related eventos

Notifique siempre al usuario cualquier cambio en la seguridad, ya sea un error relacionado con la seguridad, como un error de certificado, o un cambio en la seguridad del protocolo subyacente, como el cambio de un sitio HTTPS a un sitio HTTP.

## <a name="notify-the-user-of-security-related-errors"></a>Notificación al usuario de Security-Related errores

Cuando la aplicación recibe un mensaje de error que puede indicar un problema de seguridad, la función **InternetErrorDlg** proporciona una interfaz estándar y familiar para notificar al usuario en la mayoría de los casos.

Entre los errores que se encuentran en esta categoría se encuentran:

**ERROR \_ HTTP DE INTERNET A HTTPS EN \_ \_ \_ \_ \_ REDIR**

**ERROR \_ INTERNET \_ INVALID \_ CA**

**ERROR \_ INTERNET \_ POST \_ IS \_ NON \_ SECURE**

**ERROR \_ ERRORES DE CERTIFICADO DE INTERNET \_ SEC \_ \_**

**ERROR \_ INTERNET \_ SEC \_ CERT \_ CN \_ INVALID**

**ERROR \_ INTERNET \_ SEC \_ CERT \_ DATE \_ INVALID**

Un error al notificar al usuario errores como estos puede exponer al usuario a diversos tipos de infracciones de seguridad, incluidos ataques de suplantación de información o divulgación involuntaria de información.

## <a name="notify-the-user-when-connection-security-changes"></a>Notificar al usuario cuándo cambia la seguridad de la conexión

Notifique siempre al usuario cuándo cambia la seguridad de la conexión, por ejemplo de HTTPS a HTTP. De lo contrario, a menos que el usuario haya decidido explícitamente no recibir notificaciones de dichos cambios, oculta los riesgos de divulgación involuntaria de información.

Entre las funciones que informan de este cambio en la seguridad de conexión se encuentran la función de devolución de llamada **InternetStatusCallback** y la **función InternetConfirmZoneCrossing.**

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para implementaciones de servidor o servicios, use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 