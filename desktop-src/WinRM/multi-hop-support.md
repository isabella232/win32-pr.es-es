---
title: Compatibilidad con varios saltos en WinRM
description: Windows Administración remota (WinRM) admite la delegación de credenciales de usuario en varios equipos remotos.
ms.assetid: 0e6c8966-bb05-4dfb-b154-300fa76e8d9c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76be3054fc9c0d624c206cf5a26d7788e763dfc81f1b2069f6abff8736be2388
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121765"
---
# <a name="multi-hop-support-in-winrm"></a>Compatibilidad con varios saltos en WinRM

Windows Administración remota (WinRM) admite la delegación de credenciales de usuario en varios equipos remotos. La funcionalidad de compatibilidad con varios saltos ahora puede usar el proveedor de servicios de seguridad de credenciales (CredSSP) para la autenticación. CredSSP permite que una aplicación delegue las credenciales del usuario desde el equipo cliente al servidor de destino.

La autenticación CredSSP está pensada para entornos en los que no se puede usar la delegación Kerberos. Se ha agregado compatibilidad con CredSSP para permitir que un usuario se conecte a un servidor remoto y tenga la capacidad de acceder a una máquina de segundo salto, como un recurso compartido de archivos.

Para obtener más información sobre CredSSP, vea [KB 951608](https://support.microsoft.com/kb/951608).

> [!Note]  
> Los clientes y servidores de WinRM solo admitirán la autenticación CredSSP con credenciales explícitas.

 

## <a name="multi-hop-support-configuration-setup-and-details"></a>Configuración y detalles de compatibilidad con varios saltos

Hay varios mecanismos para configurar las opciones de WinRM. En el procedimiento siguiente, se **usan la utilidad winrm** y directiva de grupo editor **(GPEdit.msc).** CredSSP también se puede habilitar para WinRM mediante Windows PowerShell. Consulte los cmdlets [enable-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Enable-WSManCredSSP?view=powershell-5.1&preserve-view=true), [Get-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Get-WSManCredSSP?view=powershell-5.1&preserve-view=true)y [Disable-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Disable-WSManCredSSP?view=powershell-5.1&preserve-view=true) Windows PowerShell para obtener información detallada de configuración y ejemplos de uso.

La delegación credSSP debe estar habilitada en la configuración del cliente y en la configuración del servicio en el equipo remoto. Además, el uso de CredSSP requiere configurar un agente de escucha HTTP [*o*](windows-remote-management-glossary.md) HTTPS en el servidor.

**Para configurar la compatibilidad con varios saltos mediante la autenticación CredSSP para WinRM**

1.  CredSSP debe estar habilitado en las opciones de configuración del cliente. Esta marca se puede habilitar manualmente o a través de directiva de grupo configuración. El valor predeterminado es **False**. La **directiva Permitir autenticación CredSSP** se encuentra en la siguiente ruta de acceso: Plantilla administrativa de configuración del equipo \\ Windows Components Windows Remote Management \\ \\ (WinRM) \\ WinRM Client.

    El siguiente comando muestra cómo usar la utilidad winrm para habilitar CredSSP en el cliente winRM:

    **winrm set winrm/config/client/auth @{CredSSP="true"}**

2.  CredSSP debe estar habilitado en los valores de configuración del servicio WinRM. Esta marca se puede habilitar manualmente o a través de directiva de grupo configuración. El valor predeterminado es **False**. La **directiva Permitir autenticación CredSSP** se encuentra en la siguiente ruta de acceso: Plantilla administrativa de configuración del equipo \\ Windows Components Windows Remote Management \\ \\ (WinRM) \\ WinRM Service.

    El siguiente comando muestra cómo usar la utilidad winrm para habilitar CredSSP en el servicio WinRM:

    **winrm set winrm/config/service/auth @{CredSSP="true"}**

3.  La configuración de directiva Allow Delegating Fresh **Credentials (AllowFreshCredentials)** debe estar habilitada en el cliente winRM y se debe agregar a la directiva un nombre principal de servicio (SPN) con el prefijo WSMAN. El SPN representa el equipo de destino en el que se pueden delegar las credenciales de usuario. El SPN se puede establecer en uno o varios equipos. La tabla siguiente contiene ejemplos de formatos válidos para SPN.

    

    | SPN                                       | Descripción                                                                         |
    |-------------------------------------------|-------------------------------------------------------------------------------------|
    | WSMAN/myComputer.myDomain.com<br/>  | Servidor WinRM que se ejecuta en myComputer.myDomain.com.<br/>                         |
    | WSMAN/ \* .myDomain.com<br/>          | Todos los servidores WinRM que se ejecutan en myDomain.com.<br/>                               |
    | WSMAN/ \* .fabrikam.myDomain.com<br/> | Todos los servidores WinRM que se ejecutan en en todos los equipos de .fabrikam.myDomain.com.<br/> |

    

     

    Para obtener más información sobre cómo establecer directivas de grupo, vea [Instalación y configuración para Windows administración remota.](installation-and-configuration-for-windows-remote-management.md)

    Para obtener más información sobre **la directiva AllowFreshCredentials,** vea la descripción de la directiva proporcionada por el editor de directiva de grupo y [kb 951608](https://support.microsoft.com/kb/951608). La **directiva AllowFreshCredentials** se encuentra en la siguiente ruta de acceso: Configuración del \\ equipo Plantillas administrativas delegación de credenciales del \\ \\ sistema.

4.  Se debe configurar un [*agente de escucha*](windows-remote-management-glossary.md) HTTPS o HTTP en el servidor. La huella digital del certificado que se usa para configurar el agente de escucha *HTTPS* también se usa para configurar la opción CertificateThumbprint en la configuración del servicio WinRM.

    El siguiente comando muestra cómo usar la utilidad winrm para configurar un agente [*de*](windows-remote-management-glossary.md)escucha HTTPS :

    **winrm quickconfig -transport:https**

Si no es posible la autenticación Kerberos entre el cliente y el servidor, el usuario debe configurar una de las siguientes opciones para la compatibilidad con varios saltos:

-   Para mejorar la seguridad, el usuario debe agregar el **atributo CertificateThumbprint** a la configuración del servicio WinRM. Si el servicio WinRM está configurado con un atributo **CertificateThumbprint,** el servicio intenta buscar el certificado correspondiente en el almacén de la máquina local y usa este certificado para la autenticación CredSSP. Si el servicio WinRM usa un certificado del almacén de la máquina local para autenticar el servidor, se debe permitir el acceso a la cuenta de servicio de red a la clave privada del certificado.

    > [!Note]  
    > Si la configuración del servicio no está configurada, el servidor WinRM usa un certificado autofirmado que se crea en memoria para cifrar los mensajes enviados al cliente. Sin embargo, este certificado no se usa para la autenticación.

     

-   Si no están disponibles la autenticación Kerberos ni las huellas digitales de certificado, el usuario puede habilitar la autenticación NTLM. Si se usa la autenticación NTLM, se debe habilitar la directiva Permitir nuevas credenciales con autenticación de servidor solo NTLM **(AllowFreshCredentialsWhenNTLMOnly)** y se debe agregar a la directiva un SPN con el prefijo WSMAN. Esta configuración es menos segura que la autenticación Kerberos y las huellas digitales de certificado, ya que las credenciales se envían a un servidor no autenticado.

    Para obtener más información sobre **la directiva AllowFreshCredentialsWhenNTLMOnly,** vea la descripción de la directiva proporcionada por el editor de directiva de grupo y [KB 951608](https://support.microsoft.com/kb/951608). La **directiva AllowFreshCredentialsWhenNTLMOnly** se encuentra en la siguiente ruta de acceso: Configuración del \\ equipo Plantillas administrativas delegación de credenciales del \\ \\ sistema.

## <a name="using-credssp-authentication-with-explicit-credentials"></a>Uso de la autenticación CredSSP con credenciales explícitas

Un usuario puede especificar credenciales explícitas a través de HTTP y HTTPS. El comando siguiente muestra cómo usar la utilidad winrm para realizar una operación remota mediante la autenticación CredSSP con credenciales explícitas a través de HTTPS:

**winrm OPERATION -remote: https://myMachine -authentication:CredSSP -username:myUsername -password:myPassword**

 

