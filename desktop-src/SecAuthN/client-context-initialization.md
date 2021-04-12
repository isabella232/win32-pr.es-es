---
description: Inicialización de contexto de cliente
ms.assetid: 0c8aad3e-e726-49ce-8fc9-94dbd60cc5cb
title: Inicialización de contexto de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 615ce5c157371f1ebfec685d6227bd11a1d76531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155909"
---
# <a name="client-context-initialization"></a>Inicialización de contexto de cliente

Para establecer una conexión segura, el cliente adquiere un identificador de [*credenciales*](/windows/desktop/SecGloss/c-gly) de salida antes de enviar una solicitud de autenticación al servidor. El servidor crea un contexto de seguridad para el cliente desde la solicitud de autenticación. Hay dos funciones SSPI del lado cliente implicadas en la configuración de la autenticación:

-   [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) obtiene una referencia a [*las credenciales*](/windows/desktop/SecGloss/c-gly)de inicio de sesión obtenidas previamente.
-   [**InitializeSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) crea los tokens de seguridad de la solicitud de autenticación inicial.

El código de este proceso puede verse en la función **GenClientContext** en el [uso de SSPI con un cliente de Windows Sockets](using-sspi-with-a-windows-sockets-client.md).

Si un programa cliente necesita usar credenciales además de sus propias credenciales de inicio de sesión, como un nombre de usuario, un nombre de dominio y una contraseña diferentes, las proporciona en la llamada [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) con una estructura de [**identidad de \_ \_ autenticación \_ de WinNT**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) de la SEC que especifica las credenciales adicionales. Para obtener más información sobre las funciones de credenciales, vea [Administración de credenciales](authentication-functions.md).

> [!Note]  
> El miembro **Flags** de la estructura de [**identidad de \_ \_ autenticación \_ de WinNT**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) de la SEC se puede establecer en sec \_ autenticación de \_ autenticación \_ \_ ANSI ANSI cuando las cadenas de la estructura son ASCI o OEM. Las cadenas ANSI se pueden usar con el miembro **Flags** de la estructura de **\_ identidad de \_ autenticación \_ de WinNT** de la SEC establecida en sec \_ WinNT \_ Authentication \_ Identity \_ Unicode si primero se convierten a [*Unicode*](/windows/desktop/SecGloss/u-gly) mediante la función [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) .

 

Para iniciar el primer segmento de la autenticación, el cliente llama a [**InitializeSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) para obtener un token de seguridad inicial que se va a enviar en un mensaje de solicitud de conexión al servidor.

El cliente utiliza la información del token de seguridad recibida en el descriptor del búfer de salida para generar un mensaje que se enviará al servidor. La construcción del mensaje, en lo que se refiere a la ubicación de varios búferes, etc., forma parte del [*Protocolo de aplicación*](/windows/desktop/SecGloss/a-gly) y debe ser entendida por ambas partes.

El cliente comprueba el estado de devolución de [**InitializeSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) para ver si la autenticación se completará en una sola llamada. Un estado de devolución de los segundos \_ que se \_ siguen siendo \_ necesarios indica que el protocolo de seguridad requiere varios mensajes de autenticación. Para obtener más información sobre las funciones de contexto, consulte [Administración de contexto](authentication-functions.md).

 

 
