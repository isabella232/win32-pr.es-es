---
title: Compatibilidad con múltiples saltos en WinRM
description: Administración remota de Windows (WinRM) admite la delegación de las credenciales de usuario en varios equipos remotos.
ms.assetid: 0e6c8966-bb05-4dfb-b154-300fa76e8d9c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22c3d66e8605e932fe15b812f92d51350da2d69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495857"
---
# <a name="multi-hop-support-in-winrm"></a>Compatibilidad con múltiples saltos en WinRM

Administración remota de Windows (WinRM) admite la delegación de las credenciales de usuario en varios equipos remotos. La funcionalidad de compatibilidad con varios saltos ahora puede utilizar el proveedor de servicios de seguridad de credenciales (CredSSP) para la autenticación. CredSSP permite a una aplicación delegar las credenciales del usuario desde el equipo cliente al servidor de destino.

La autenticación CredSSP está pensada para entornos en los que no se puede usar la delegación Kerberos. Se ha agregado compatibilidad con CredSSP para permitir que un usuario se conecte a un servidor remoto y tenga la capacidad de obtener acceso a un equipo de segundo salto, como un recurso compartido de archivos.

Para obtener más información acerca de CredSSP, consulte [KB 951608](https://support.microsoft.com/kb/951608).

> [!Note]  
> Los clientes y servidores de WinRM solo admiten la autenticación CredSSP con credenciales explícitas.

 

## <a name="multi-hop-support-configuration-setup-and-details"></a>Configuración y detalles de la configuración de compatibilidad con múltiples saltos

Existen varios mecanismos para configurar las opciones de WinRM. En el procedimiento siguiente, se usan la utilidad **WinRM** y el editor de directiva de grupo (**gpedit. msc**). CredSSP también puede habilitarse para WinRM mediante Windows PowerShell. Consulte los cmdlets [enable-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Enable-WSManCredSSP?view=powershell-5.1&preserve-view=true), [Get-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Get-WSManCredSSP?view=powershell-5.1&preserve-view=true)y [Disable-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Disable-WSManCredSSP?view=powershell-5.1&preserve-view=true) de Windows PowerShell para obtener información detallada sobre la configuración y ejemplos de uso.

La delegación CredSSP debe estar habilitada en la configuración de cliente y en la configuración del servicio en el equipo remoto. Además, el uso de CredSSP requiere la configuración de un [*agente de escucha*](windows-remote-management-glossary.md) http o https en el servidor.

**Para configurar la compatibilidad con múltiples saltos mediante la autenticación CredSSP para WinRM**

1.  CredSSP debe estar habilitado en las opciones de configuración del cliente. Esta marca se puede habilitar manualmente o a través de un valor de directiva de grupo. El valor predeterminado es **False**. La Directiva de **autenticación CredSSP** se encuentra en la siguiente ruta de acceso: configuración del equipo \\ plantilla administrativa \\ componentes de Windows \\ administración remota de Windows (WinRM) \\ cliente WinRM.

    El siguiente comando muestra cómo usar la utilidad WinRM para habilitar CredSSP en el cliente WinRM:

    **WinRM Set WinRM/config/Client/auth @ {CredSSP = "true"}**

2.  CredSSP debe estar habilitado en la configuración del servicio WinRM. Esta marca se puede habilitar manualmente o a través de un valor de directiva de grupo. El valor predeterminado es **False**. La Directiva de **autenticación CredSSP** se encuentra en la siguiente ruta de acceso: configuración del equipo \\ plantillas administrativas \\ componentes de Windows \\ administración remota de Windows (WinRM) \\ WinRM.

    El siguiente comando muestra cómo usar la utilidad WinRM para habilitar CredSSP en el servicio WinRM:

    **WinRM Set WinRM/config/Service/auth @ {CredSSP = "true"}**

3.  La configuración de directiva permitir delegación de credenciales nuevas (**AllowFreshCredentials**) debe estar habilitada en el cliente WinRM y debe agregarse a la Directiva un nombre principal de servicio (SPN) con el prefijo WSMAN. El SPN representa el equipo de destino al que se pueden delegar las credenciales de usuario. El SPN se puede establecer en uno o varios equipos. En la tabla siguiente se incluyen ejemplos de formatos válidos para SPN.

    

    | SPN                                       | Descripción                                                                         |
    |-------------------------------------------|-------------------------------------------------------------------------------------|
    | WSMAN/mi. midominio. com<br/>  | Servidor WinRM que se ejecuta en myComputer.myDomain.com.<br/>                         |
    | WSMAN/ \* . mydomain.com<br/>          | Todos los servidores WinRM que se ejecutan en myDomain.com.<br/>                               |
    | WSMAN/ \* . fabrikam.mydomain.com<br/> | Todos los servidores WinRM que se ejecutan en en todos los equipos de. fabrikam.myDomain.com.<br/> |

    

     

    Para obtener más información sobre la configuración de directivas de grupo, consulte [instalación y configuración de administración remota de Windows](installation-and-configuration-for-windows-remote-management.md).

    Para obtener más información sobre la directiva **AllowFreshCredentials** , vea la descripción de la Directiva proporcionada por el editor de directiva de grupo y [KB 951608](https://support.microsoft.com/kb/951608). La directiva **AllowFreshCredentials** se encuentra en la siguiente ruta de acceso: configuración \\ del equipo Plantillas administrativas delegación de \\ \\ credenciales del sistema.

4.  Se debe configurar un [*agente de escucha*](windows-remote-management-glossary.md) https o http en el servidor. La huella digital del certificado que se usa para configurar el *agente de escucha* https también se usa para configurar el valor CertificateThumbprint en la configuración del servicio WinRM.

    El siguiente comando muestra cómo usar la utilidad WinRM para configurar un agente de [*escucha*](windows-remote-management-glossary.md)https:

    **WinRM quickconfig-Transport: https**

Si no es posible la autenticación Kerberos entre el cliente y el servidor, el usuario debe configurar una de las siguientes opciones para la compatibilidad con múltiples saltos:

-   Para mejorar la seguridad, el usuario debe agregar el atributo **CertificateThumbprint** a la configuración del servicio WinRM. Si el servicio WinRM está configurado con un atributo **CertificateThumbprint** , el servicio intenta buscar el certificado correspondiente en el almacén del equipo local y usa este certificado para la autenticación CredSSP. Si el servicio WinRM usa un certificado del almacén del equipo local para autenticar el servidor, se debe permitir el acceso a la cuenta de servicio de red a la clave privada del certificado.

    > [!Note]  
    > Si la configuración del servicio no está configurada, el servidor WinRM usa un certificado autofirmado que se crea en la memoria para cifrar los mensajes que se envían al cliente. Sin embargo, este certificado no se utiliza para la autenticación.

     

-   Si no hay disponible ninguna autenticación Kerberos ni huellas digitales de certificado, el usuario puede habilitar la autenticación NTLM. Si se usa la autenticación NTLM, la Directiva permitir credenciales nuevas con autenticación de servidor solo NTLM (**AllowFreshCredentialsWhenNTLMOnly**) debe estar habilitada y se debe agregar un SPN con el prefijo WSMAN a la Directiva. Esta opción es menos segura que la autenticación Kerberos y las huellas digitales de certificado, ya que las credenciales se envían a un servidor no autenticado.

    Para obtener más información sobre la directiva **AllowFreshCredentialsWhenNTLMOnly** , vea la descripción de la Directiva proporcionada por el editor de directiva de grupo y [KB 951608](https://support.microsoft.com/kb/951608). La directiva **AllowFreshCredentialsWhenNTLMOnly** se encuentra en la siguiente ruta de acceso: configuración \\ del equipo Plantillas administrativas delegación de \\ \\ credenciales del sistema.

## <a name="using-credssp-authentication-with-explicit-credentials"></a>Usar la autenticación CredSSP con credenciales explícitas

Un usuario puede especificar credenciales explícitas a través de HTTP y HTTPS. El siguiente comando muestra cómo usar la utilidad WinRM para realizar una operación remota mediante la autenticación CredSSP con credenciales explícitas a través de HTTPS:

**OPERACIÓN de WinRM-remoto: https://myMachine -autenticación: CredSSP-nombredeusuario: nombre de usuario-contraseña: contraseña**

 

