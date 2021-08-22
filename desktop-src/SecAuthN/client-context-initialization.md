---
description: Inicialización de contexto de cliente
ms.assetid: 0c8aad3e-e726-49ce-8fc9-94dbd60cc5cb
title: Inicialización de contexto de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c0f2912de57487c1f30fdac1ef40740553947b993ef6f5179a028625f132af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141188"
---
# <a name="client-context-initialization"></a>Inicialización de contexto de cliente

Para establecer una conexión segura, el cliente adquiere un identificador de credenciales de [*salida*](/windows/desktop/SecGloss/c-gly) antes de enviar una solicitud de autenticación al servidor. El servidor crea un contexto de seguridad para el cliente a partir de la solicitud de autenticación. Hay dos funciones SSPI del lado cliente implicadas en la configuración de autenticación:

-   [**AcquireCredentialsHandle obtiene**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) una referencia a las credenciales de inicio de sesión [*obtenidas previamente.*](/windows/desktop/SecGloss/c-gly)
-   [**InitializeSecurityContext (General) crea los**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) tokens de seguridad de solicitud de autenticación inicial.

El código para este proceso se puede ver en la función **GenClientContext** en [Using SSPI with a Windows Sockets Client](using-sspi-with-a-windows-sockets-client.md).

Si un programa cliente necesita usar credenciales además de sus propias credenciales de inicio de sesión, como un nombre de usuario, un nombre de dominio y una contraseña diferentes, las proporciona en la llamada [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) con una estructura [**SEC \_ WINNT \_ AUTH \_ IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) que especifica las credenciales adicionales. Para obtener más información sobre las funciones de credenciales, vea [Administración de credenciales.](authentication-functions.md)

> [!Note]  
> El **miembro Flags** de la estructura [**SEC \_ WINNT \_ AUTH \_ IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) se puede establecer en SEC WINNT AUTH IDENTITY ANSI cuando las cadenas de la estructura \_ son \_ \_ \_ ASCI o OEM. Las cadenas ANSI se pueden usar con el miembro **Flags** de la estructura **SEC \_ WINNT \_ AUTH \_ IDENTITY** establecida en UNICODE SEC WINNT AUTH IDENTITY si primero se convierten a Unicode mediante la \_ función \_ \_ \_ [**MultiByteToWideChar.**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) [](/windows/desktop/SecGloss/u-gly)

 

Para iniciar el primer elemento de la autenticación, el cliente llama a [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) para obtener un token de seguridad inicial que se enviará en un mensaje de solicitud de conexión al servidor.

El cliente usa la información del token de seguridad recibida en el descriptor del búfer de salida para generar un mensaje que se enviará al servidor. La construcción del mensaje, en términos de colocación de varios [](/windows/desktop/SecGloss/a-gly) búferes, etc., forma parte del protocolo de aplicación y debe ser comprendida por ambas partes.

El cliente comprueba el estado de devolución [**de InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) para ver si la autenticación se completará en una sola llamada. Un estado de devolución de SEC I CONTINUE NEEDED indica \_ que el protocolo de seguridad requiere varios mensajes de \_ \_ autenticación. Para obtener más información sobre las funciones de contexto, vea [Context Management](authentication-functions.md).

 

 
