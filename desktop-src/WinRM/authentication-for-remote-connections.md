---
title: Autenticación para conexiones remotas
description: Administración remota de Windows mantiene la seguridad para la comunicación entre equipos al admitir varios métodos estándar de autenticación y cifrado de mensajes.
ms.assetid: 97a13b07-ae7a-4d2f-8841-77a22c91b204
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0e9aa125f2ccf5d8c224eee645a6dba1ec2fd96e
ms.sourcegitcommit: 25c6d442ab55cbf0e065398a006b1d409349fffd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2020
ms.locfileid: "104077455"
---
# <a name="authentication-for-remote-connections"></a>Autenticación para conexiones remotas

Administración remota de Windows mantiene la seguridad para la comunicación entre equipos al admitir varios métodos estándar de autenticación y cifrado de mensajes.

## <a name="default-group-access"></a>Acceso al grupo predeterminado

Durante la instalación, WinRM crea el grupo **local \_ \_ WinRMRemoteWMIUsers**. WinRM restringe el acceso remoto a cualquier usuario que no sea miembro del grupo de administración local o del grupo **WinRMRemoteWMIUsers \_ \_** . Puede Agregar un usuario local, un usuario de dominio o un grupo de dominio a **WinRMRemoteWMIUsers \_ \_** escribiendo **net localgroup WinRMRemoteWMIUsers \_ \_ /Add <domain> \\ <username>** en el símbolo del sistema. Opcionalmente, puede usar el directiva de grupo para agregar un usuario al grupo.

## <a name="default-authentication-settings"></a>Configuración de autenticación predeterminada

Las credenciales predeterminadas, el nombre de usuario y la contraseña son las credenciales de la cuenta de usuario que ha iniciado la sesión que ejecuta el script.

**Para cambiar a otra cuenta en un equipo remoto**

1.  Especifique las credenciales en un objeto [**ConnectionOptions**](connectionoptions.md) o [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) y proporcione esto a la llamada [**createSession**](wsman-createsession.md) .
2.  Establezca **WSManFlagCredUserNamePassword** en el parámetro *Flags* de la llamada a [**createSession**](wsman-createsession.md) .

La lista siguiente contiene una lista de lo que ocurre cuando un script o una aplicación se ejecuta con las credenciales predeterminadas:

-   [*Kerberos*](windows-remote-management-glossary.md) es el método predeterminado de autenticación cuando el cliente está en un dominio y la cadena de destino remoto no es una de las siguientes: localhost, 127.0.0.1 o \[ :: 1 \] .
-   [*Negotiate*](windows-remote-management-glossary.md) es el método predeterminado cuando el cliente no está en un dominio, pero la cadena de destino remoto es uno de los siguientes: localhost, 127.0.0.1 o \[ :: 1 \] .

Si proporciona credenciales explícitas con un objeto [**ConnectionOptions**](connectionoptions.md) , Negotiate es el método predeterminado. Negociar autenticación determina si el método de autenticación en curso es Kerberos o NTLM, en función de si los equipos están en un dominio o grupo de trabajo. Si se conecta a un equipo de destino remoto mediante una cuenta local, la cuenta debe tener como prefijo el nombre del equipo. Por ejemplo, mi \\ nombreDeUsuario.

Si especifica la autenticación Negotiate, Digest o Basic y no proporciona un objeto [**ConnectionOptions**](connectionoptions.md) , recibirá un error que indica que se requieren credenciales explícitas. Si HTTPS no es el transporte, el equipo remoto de destino debe configurarse en la lista de equipos host de confianza.

Para obtener más información sobre los tipos de autenticación que están habilitados en los valores de configuración predeterminados, vea [instalación y configuración de administración remota de Windows](installation-and-configuration-for-windows-remote-management.md).

## <a name="basic-authentication"></a>Autenticación básica

Para establecer explícitamente la autenticación [*básica*](windows-remote-management-glossary.md) en la llamada a [**WSMan. createSession**](wsman-createsession.md), establezca las marcas **WSManFlagUseBasic** y **WSManFlagCredUserNamePassword** en el parámetro *Flags* . La autenticación básica está deshabilitada en los valores de configuración predeterminados para el cliente WinRM y el servidor WinRM.

## <a name="digest-authentication"></a>Autenticación implícita

Para establecer explícitamente la autenticación [*implícita*](windows-remote-management-glossary.md) en la llamada a [**WSMan. createSession**](wsman-createsession.md), establezca la marca **WSManFlagUseDigest** en el parámetro *Flags* . No se admite la síntesis. No se puede configurar para el componente de servidor WinRM.

## <a name="negotiate-authentication"></a>Negociar la autenticación

Para establecer explícitamente la autenticación [*Negotiate*](windows-remote-management-glossary.md) , también conocida como autenticación integrada de Windows, en la llamada a [**WSMan. createSession**](wsman-createsession.md), establezca la marca **WSManFlagUseNegotiate** en el parámetro *Flags* .

[Control de cuentas de usuario (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) afecta al acceso al servicio WinRM. Cuando se usa Negotiate Authentication en un grupo de trabajo, solo la cuenta de administrador integrada puede tener acceso al servicio. Para permitir que todas las cuentas del grupo administradores tengan acceso al servicio, establezca el siguiente valor del registro:

**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Policies** \\ **System** \\ **LocalAccountTokenFilterPolicy** = 1

## <a name="kerberos-authentication"></a>Autenticación Kerberos

Para establecer explícitamente la autenticación [*Kerberos*](windows-remote-management-glossary.md) en la llamada a [**WSMan. createSession**](wsman-createsession.md), establezca la marca **WSManFlagUseKerberos** en el parámetro *Flags* . Los equipos cliente y servidor deben estar Unidos a un dominio. Si usa Kerberos como método de autenticación, no puede usar una dirección IP en la llamada a [**WSMan. createSession**](wsman-createsession.md) o [**IWSMan:: createSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession).

## <a name="client-certificate-based-authentication"></a>Autenticación basada en certificado de cliente

Para establecer la autenticación basada en certificados de cliente en la llamada a [**WSMan. createSession**](wsman-createsession.md), establezca la marca **WSManFlagUseClientCertificate** en el parámetro *Flags* .

En primer lugar, debe habilitar la autenticación de certificados en el cliente y el servicio mediante la herramienta de línea de comandos de WinRM. Para obtener más información, vea [Habilitar opciones de autenticación](#enabling-or-disabling-authentication-options). También debe crear una entrada en la tabla CertMapping en el equipo del servidor WinRM. Esto establece una asignación entre uno o varios certificados y una cuenta local. Una vez que se ha utilizado el certificado para la autenticación y la autorización, se usa la cuenta local correspondiente para las operaciones realizadas por el servicio WinRM.

La asignación se puede crear para un URI de recurso específico. Para obtener más información, incluido cómo crear una entrada de la tabla CertMapping, escriba **WinRM Help CertMapping** en el símbolo del sistema.

> [!Note]  
> El certificado de tamaño máximo que WinRM puede usar en este contexto es 16 KB.

 

## <a name="enabling-or-disabling-authentication-options"></a>Habilitar o deshabilitar las opciones de autenticación

La opción de autenticación predeterminada en la instalación del sistema es Kerberos. Para obtener más información, vea [instalación y configuración de administración remota de Windows](installation-and-configuration-for-windows-remote-management.md).

Si el script o la aplicación requieren un método de autenticación específico que no está habilitado, debe cambiar la configuración para habilitar este tipo de autenticación. Este cambio se puede realizar mediante la herramienta de línea de comandos **WinRM** o a través de directiva de grupo para el **objeto Directiva de Grupo administración remota de Windows**. También puede optar por deshabilitar ciertos métodos de autenticación.

**Para habilitar o deshabilitar la autenticación con la herramienta WinRM**

1.  Para establecer la configuración del cliente WinRM, use el comando **WinRM Set** y especifique el cliente. Por ejemplo, el siguiente comando deshabilita la autenticación implícita para el cliente.

    **WinRM Set WinRM/config/Client/auth @ {Digest = "false"}**

2.  Para establecer la configuración del servidor WinRM, use el comando **WinRM Set** y especifique el servicio. Por ejemplo, el siguiente comando habilita la autenticación Kerberos para el servicio.

    **WinRM Set WinRM/config/Service/auth @ {Kerberos = "true"}**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Administración remota de Windows](about-windows-remote-management.md)
</dt> <dt>

[**WSMan. CreateSession**](wsman-createsession.md)
</dt> <dt>

[Usar Administración remota de Windows](using-windows-remote-management.md)
</dt> </dl>

 

 




