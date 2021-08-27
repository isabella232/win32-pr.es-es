---
title: Autenticación para conexiones remotas
description: Windows La administración remota mantiene la seguridad para la comunicación entre equipos al admitir varios métodos estándar de autenticación y cifrado de mensajes.
ms.assetid: 97a13b07-ae7a-4d2f-8841-77a22c91b204
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9c9c0e98d884e09b9bbd52ef4f0e1cb53e782ea
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886996"
---
# <a name="authentication-for-remote-connections"></a>Autenticación para conexiones remotas

Windows La administración remota mantiene la seguridad para la comunicación entre equipos al admitir varios métodos estándar de autenticación y cifrado de mensajes.

## <a name="default-group-access"></a>Acceso de grupo predeterminado

Durante la instalación, WinRM crea el grupo local **\_ \_ WinRMRemoteWMIUsers**. A continuación, WinRM restringe el acceso remoto a cualquier usuario que no sea miembro del grupo de administración local o del grupo **\_ \_ WinRMRemoteWMIUsers.** Para agregar un usuario local, un usuario de dominio o un grupo de dominio a **\_ \_ WinRMRemoteWMIUsers,** escriba **net localgroup WinRMRemoteWMIUsers \_ \_ /add &lt; domain &gt; \\ &lt; username &gt;** en el símbolo del sistema. Opcionalmente, puede usar el directiva de grupo para agregar un usuario al grupo.

## <a name="default-authentication-settings"></a>Autenticación predeterminada Configuración

Las credenciales predeterminadas, el nombre de usuario y la contraseña son las credenciales de la cuenta de usuario que ha iniciado sesión y que ejecuta el script.

**Para cambiar a otra cuenta en un equipo remoto**

1.  Especifique las credenciales en un [**objeto ConnectionOptions**](connectionoptions.md) [**o IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) y proporcione las credenciales a la [**llamada CreateSession.**](wsman-createsession.md)
2.  Establezca **WSManFlagCredUserNamePassword** en el *parámetro flags* de la [**llamada a CreateSession.**](wsman-createsession.md)

La lista siguiente contiene una lista de lo que ocurre cuando se ejecuta un script o una aplicación con las credenciales predeterminadas:

-   [*Kerberos*](windows-remote-management-glossary.md) es el método predeterminado de autenticación cuando el cliente está en un dominio y la cadena de destino remoto no es una de las siguientes: localhost, 127.0.0.1 o \[ ::1 \] .
-   [*Negotiate*](windows-remote-management-glossary.md) es el método predeterminado cuando el cliente no está en un dominio, pero la cadena de destino remoto es una de las siguientes: localhost, 127.0.0.1 o \[ ::1 \] .

Si proporciona credenciales explícitas con un [**objeto ConnectionOptions,**](connectionoptions.md) Negotiate es el método predeterminado. Negociar la autenticación determina si el método de autenticación en curso es Kerberos o NTLM, en función de si los equipos están en un dominio o grupo de trabajo. Si se conecta a un equipo de destino remoto mediante una cuenta local, la cuenta debe tener como prefijo el nombre del equipo. Por ejemplo, myComputer \\ myUsername.

Si especifica la autenticación Negotiate, Digest o Basic y no proporciona un objeto [**ConnectionOptions,**](connectionoptions.md) recibirá un error que indica que se requieren credenciales explícitas. Si HTTPS no es el transporte, el equipo remoto de destino debe configurarse en la lista de equipos host de confianza.

Para obtener más información sobre los tipos de autenticación que están habilitados en las opciones de configuración predeterminadas, vea Instalación y configuración [de Windows Administración remota.](installation-and-configuration-for-windows-remote-management.md)

## <a name="basic-authentication"></a>Autenticación básica

Para establecer [](windows-remote-management-glossary.md) explícitamente la autenticación básica en la llamada a [**WSMan.CreateSession**](wsman-createsession.md), establezca las marcas **WSManFlagUseBasic** y **WSManFlagCredUserNamePassword** en el *parámetro flags.* La autenticación básica está deshabilitada en las opciones de configuración predeterminadas para el cliente de WinRM y el servidor WinRM.

## <a name="digest-authentication"></a>Autenticación implícita

Para establecer explícitamente la autenticación [*implícita*](windows-remote-management-glossary.md) en la llamada a [**WSMan.CreateSession**](wsman-createsession.md), establezca la marca **WSManFlagUseDigest** en el *parámetro flags.* No se admite la síntesis. No se puede configurar para el componente de servidor WinRM.

## <a name="negotiate-authentication"></a>Negociación de la autenticación

Para establecer explícitamente la autenticación [*negotiate,*](windows-remote-management-glossary.md) también conocida como autenticación integrada de Windows, en la llamada a [**WSMan.CreateSession**](wsman-createsession.md), establezca la marca **WSManFlagUseNegotiate** en el *parámetro flags.*

[El control de cuentas de usuario (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) afecta al acceso al servicio WinRM. Cuando se usa la autenticación Negotiate en un grupo de trabajo, solo la cuenta de administrador integrada puede acceder al servicio. Para permitir que todas las cuentas del grupo Administradores accedan al servicio, establezca el siguiente valor del Registro:

**HKEY \_ SOFTWARE \_ DE MÁQUINA** \\ **LOCAL** \\ **Microsoft** \\ **Windows** \\ **sistema de directivas CurrentVersion** \\  \\  \\ **LocalAccountTokenFilterPolicy** = 1

## <a name="kerberos-authentication"></a>Autenticación Kerberos

Para establecer explícitamente la [*autenticación Kerberos*](windows-remote-management-glossary.md) en la llamada a [**WSMan.CreateSession**](wsman-createsession.md), establezca la marca **WSManFlagUseKerberos** en el *parámetro flags.* Tanto el cliente como los equipos servidor deben estar unidos a un dominio. Si usa Kerberos como método de autenticación, no puede usar una dirección IP en la llamada a [**WSMan.CreateSession**](wsman-createsession.md) o [**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession).

## <a name="client-certificate-based-authentication"></a>Autenticación basada en certificados de cliente

Para establecer la autenticación basada en certificados de cliente en la llamada a [**WSMan.CreateSession**](wsman-createsession.md), establezca la marca **WSManFlagUseClientCertificate** en el *parámetro flags.*

Primero debe habilitar la autenticación de certificados en el cliente y el servicio mediante la herramienta de línea de comandos winrm. Para obtener más información, vea [Habilitar opciones de autenticación.](#enabling-or-disabling-authentication-options) También debe crear una entrada en la tabla CertMapping en el equipo del servidor WinRM. Esto establece una asignación entre uno o varios certificados y una cuenta local. Una vez que el certificado se ha usado para la autenticación y autorización, se usa la cuenta local correspondiente para las operaciones realizadas por el servicio WinRM.

La asignación se puede crear para un URI de recurso específico. Para obtener más información, incluido cómo crear una entrada de tabla CertMapping, escriba **winrm help certmapping** en el símbolo del sistema.

> [!Note]  
> El certificado de tamaño máximo utilizable por WinRM en este contexto es de 16 KB.

 

## <a name="enabling-or-disabling-authentication-options"></a>Habilitar o deshabilitar opciones de autenticación

La opción de autenticación predeterminada en la instalación del sistema es Kerberos. Para obtener más información, [vea Instalación y configuración de Windows Administración remota.](installation-and-configuration-for-windows-remote-management.md)

Si el script o la aplicación requiere un método de autenticación específico que no está habilitado, debe cambiar la configuración para habilitar este tipo de autenticación. Este cambio se puede realizar mediante la herramienta de línea de comandos **winrm** o a través de directiva de grupo para el Windows administración remota **directiva de grupo objeto**. También puede optar por deshabilitar determinados métodos de autenticación.

**Para habilitar o deshabilitar la autenticación con la herramienta Winrm**

1.  Para establecer la configuración del cliente WinRM, use el **comando Winrm Set** y especifique el cliente. Por ejemplo, el siguiente comando deshabilita la autenticación implícita para el cliente.

    **winrm set winrm/config/client/auth @{Digest="false"}**

2.  Para establecer la configuración del servidor WinRM, use el **comando Winrm Set** y especifique el servicio. Por ejemplo, el siguiente comando habilita la autenticación Kerberos para el servicio.

    **winrm set winrm/config/service/auth @{Kerberos="true"}**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca Windows administración remota](about-windows-remote-management.md)
</dt> <dt>

[**WSMan.CreateSession**](wsman-createsession.md)
</dt> <dt>

[Uso de Windows administración remota](using-windows-remote-management.md)
</dt> </dl>

 

 




