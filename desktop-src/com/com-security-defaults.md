---
title: Valores predeterminados de seguridad COM
description: Puede usar los valores predeterminados de seguridad COM para la aplicación en lugar de especificar su propia configuración de seguridad.
ms.assetid: 6f1f6925-a6ab-4cfa-b0b4-b4b4012979f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cba607044d6e93c9f01243809feae6e5a600851
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356729"
---
# <a name="com-security-defaults"></a>Valores predeterminados de seguridad COM

Puede usar los valores predeterminados de seguridad COM para la aplicación en lugar de especificar su propia configuración de seguridad. En ese caso, COM inicializará y administrará la seguridad. No es necesario configurar el registro ni llamar a ninguna función de seguridad del programa.

Sin embargo, si ciertos valores con nombre del registro se han establecido o modificado, se verán afectados los valores predeterminados de seguridad que usa COM. La siguiente lista describe los valores predeterminados de seguridad de COM y explica cómo afectan algunos valores a la configuración del registro.

A continuación se muestran los valores de seguridad predeterminados que usa COM:

-   El proveedor de servicios de seguridad predeterminado es el que determina COM como el más compatible con el entorno. COM elige el protocolo Kerberos V5 o NTLMSSP, con el protocolo Kerberos como opción predeterminada. Ninguno de los protocolos proporcionados por Schannel se eligen nunca como valor predeterminado.
-   El sistema identifica un llamador a través de su nombre de usuario y contraseña, y crea automáticamente un token de identificación utilizado por el sistema de seguridad.
-   Si el valor con nombre [LegacyAuthenticationLevel](legacyauthenticationlevel.md) existe y se ha establecido su valor, se utiliza ese valor. De lo contrario, el nivel de autenticación se establece en Connect (RPC \_ C \_ authn \_ LEVEL \_ Connect). Este nivel significa que en la primera llamada que realiza un cliente al servidor, COM realiza una comprobación de autenticación. Si el cliente pasa la comprobación, no se realiza ninguna autenticación adicional. El valor de AuthenticationLevel también se puede establecer en la clave [AppID](appid-key.md) .
-   Si el valor con nombre [LegacyImpersonationLevel](legacyimpersonationlevel.md) existe y se ha establecido su valor, se utiliza ese valor. De lo contrario, el nivel de suplantación se establece para identificar (el \_ nivel Imp de RPC C \_ \_ \_ ). El cliente concede los derechos de suplantación al servidor. El nivel de identificación significa que el servidor puede obtener la identidad del cliente. El servidor puede suplantar al cliente para la comprobación de la lista de control de acceso (ACL), pero no puede tener acceso a los objetos del sistema como el cliente. Para obtener más información, vea [niveles de suplantación](impersonation-levels.md) y [Cloaking](cloaking.md).
-   Si el valor con nombre [AccessPermission](accesspermission.md) en **AppID** existe y se ha establecido, se utiliza ese valor. De lo contrario, COM comprueba una entrada [DefaultAccessPermission](defaultaccesspermission.md) . Si está presente, se utiliza ese valor. Si este valor no está presente, COM construye una ACL que concede permisos a la identidad del servidor y al sistema local.
-   Si el valor con nombre [SRPTrustLevel](srptrustlevel.md) en **AppID** existe y se ha establecido, se utiliza ese valor. De lo contrario, el nivel de confianza de la Directiva de restricción de software (SRP) se establece en no permitido (LEVELID seguro no \_ \_ permitido), lo que indica que la aplicación se ejecuta en un entorno restringido y no se permite el acceso a los privilegios de usuario confidenciales de seguridad del usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 




