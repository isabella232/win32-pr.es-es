---
title: Valores predeterminados de seguridad COM
description: Puede usar los valores predeterminados de seguridad COM para la aplicación en lugar de especificar su propia configuración de seguridad.
ms.assetid: 6f1f6925-a6ab-4cfa-b0b4-b4b4012979f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cba607044d6e93c9f01243809feae6e5a600851
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060938"
---
# <a name="com-security-defaults"></a>Valores predeterminados de seguridad COM

Puede usar los valores predeterminados de seguridad COM para la aplicación en lugar de especificar su propia configuración de seguridad. En ese caso, COM inicializará y administrará la seguridad automáticamente. No es necesario configurar el registro ni llamar a ninguna función de seguridad del programa.

Sin embargo, si se han establecido o modificado ciertos valores con nombre del Registro, se verán afectados los valores predeterminados de seguridad que usa COM. En la lista siguiente se describen los valores predeterminados de seguridad COM y se explica cómo algunos valores se ven afectados por la configuración del Registro.

Estos son los valores de seguridad predeterminados que usa COM:

-   El proveedor de servicios de seguridad predeterminado es el que com determina que es el más compatible con el entorno. COM elige el protocolo Kerberos v5 o NTLMSSP, siendo el protocolo Kerberos la opción predeterminada. Ninguno de los protocolos proporcionados por Schannel se elige como valor predeterminado.
-   El sistema identifica a un llamador a través del nombre de usuario y la contraseña y crea automáticamente un token de identificación utilizado por el sistema de seguridad.
-   Si existe [el valor con nombre LegacyAuthenticationLevel](legacyauthenticationlevel.md) y si se ha establecido su valor, se usa ese valor. De lo contrario, el nivel de autenticación se establece en connect (RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT). Este nivel significa que, en la primera llamada que realiza un cliente al servidor, COM realiza una comprobación de autenticación. Si el cliente pasa la comprobación, no se realiza ninguna otra autenticación. El valor AuthenticationLevel también se puede establecer en la [clave AppID.](appid-key.md)
-   Si existe [el valor con nombre LegacyImpersonationLevel](legacyimpersonationlevel.md) y si se ha establecido su valor, se usa ese valor. De lo contrario, el nivel de suplantación se establece para identificar (RPC \_ C \_ IMP LEVEL \_ \_ IDENTIFY). El cliente concede derechos de suplantación al servidor. El nivel de identificación significa que el servidor puede obtener la identidad del cliente. El servidor puede suplantar al cliente para la comprobación de la lista de control de acceso (ACL), pero no puede acceder a los objetos del sistema como cliente. Para obtener más información, [vea Niveles de suplantación](impersonation-levels.md) [y Arroba.](cloaking.md)
-   Si el [valor con nombre AccessPermission](accesspermission.md) de **AppID** existe y se ha establecido, se usa ese valor. De lo contrario, COM comprueba si hay [una entrada DefaultAccessPermission.](defaultaccesspermission.md) Si está presente, se usa ese valor. Si este valor no está presente, COM crea una ACL que concede permisos a la identidad del servidor y al sistema local.
-   Si el [valor con nombre SRPTrustLevel](srptrustlevel.md) en **AppID** existe y se ha establecido, se usa ese valor. De lo contrario, el nivel de confianza de la directiva de restricción de software (SRP) se establece en No permitido (SAFER LEVELID NO PERMITIDO), lo que indica que la aplicación se ejecuta en un entorno restringido y no se permite el acceso a los privilegios de usuario que tienen en cuenta la seguridad del \_ \_ usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 




