---
description: Para conectarse a un equipo remoto mediante WMI, asegúrese de que la configuración DCOM correcta y la configuración de seguridad del espacio de nombres WMI están habilitadas para la conexión.
ms.assetid: 96ebaa9b-a062-4300-a637-8eb71cb80d1c
ms.tgt_platform: multiple
title: Protección de una conexión WMI remota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2a044e49fed5eaa27fbc246dca3306a6c29650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544686"
---
# <a name="securing-a-remote-wmi-connection"></a>Protección de una conexión WMI remota

Para conectarse a un equipo remoto mediante WMI, asegúrese de que la configuración DCOM correcta y la configuración de seguridad del espacio de nombres WMI están habilitadas para la conexión.

WMI tiene una configuración predeterminada de suplantación, autenticación y servicio de autenticación (NTLM o Kerberos) que requiere el equipo de destino en una conexión remota. El equipo local puede usar valores predeterminados diferentes que el sistema de destino no acepta. Puede cambiar esta configuración en la llamada de conexión.

En este tema se describen las siguientes secciones:

-   [Configuración de suplantación y autenticación de DCOM para WMI](#dcom-impersonation-and-authentication-settings-for-wmi)
-   [Configuración de la seguridad de DCOM para permitir que un usuario tenga acceso a un equipo de forma remota](#setting-dcom-security-to-allow-a-user-to-access-a-computer-remotely)
-   [Permitir el acceso de los usuarios a un espacio de nombres WMI específico](#allowing-users-access-to-a-specific-wmi-namespace)
-   [Establecer la seguridad del espacio de nombres para requerir el cifrado de datos para las conexiones remotas](#setting-namespace-security-to-require-data-encryption-for-remote-connections)
-   [Temas relacionados](#related-topics)

## <a name="dcom-impersonation-and-authentication-settings-for-wmi"></a>Configuración de suplantación y autenticación de DCOM para WMI

WMI tiene la configuración predeterminada de suplantación, autenticación y servicio de autenticación de DCOM (NTLM o Kerberos) que requiere el sistema remoto. El sistema local puede usar valores predeterminados diferentes que el sistema remoto de destino no acepta. Puede cambiar esta configuración en la llamada de conexión. Para obtener más información, vea [establecer la seguridad del proceso de aplicación cliente](setting-client-application-process-security.md). Sin embargo, para el servicio de autenticación, se recomienda especificar el **\_ \_ \_ valor predeterminado de autenticación de RPC C** y permitir que DCOM elija el servicio adecuado para el equipo de destino.

Puede proporcionar valores de configuración en los parámetros de las llamadas a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) en C++. En scripts, puede establecer la configuración de seguridad en las llamadas a [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md), en un objeto [**SWbemSecurity**](swbemsecurity.md) o en la cadena de [moniker](constructing-a-moniker-string.md) de scripting.

Para obtener una lista de todas las constantes de suplantación de C++, vea [establecer el nivel de seguridad de proceso predeterminado mediante C++](setting-the-default-process-security-level-using-c-.md). Para obtener las constantes de Visual Basic y las cadenas de scripting para usar la conexión de moniker, vea [establecer el nivel de seguridad de proceso predeterminado con VBScript](setting-the-default-process-security-level-using-vbscript.md).

En la tabla siguiente se enumeran los valores predeterminados de suplantación, autenticación y servicio de autenticación de DCOM requeridos por el equipo de destino (equipo B) en una conexión remota. Para obtener más información, consulte protección de una conexión WMI remota.



| Sistema operativo del equipo B | Cadena de scripting del nivel de suplantación | Cadena de scripting de nivel de autenticación | Servicio de autenticación |
|-----------------------------|--------------------------------------|---------------------------------------|------------------------|
| Windows Vista o posterior      | Impersonate                          | PKT                                   | Kerberos               |



 

Las conexiones remotas WMI se ven afectadas por el [control de cuentas de usuario (UAC)](/previous-versions/aa905108(v=msdn.10)) y el [firewall de Windows](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx). Para obtener más información, vea [conectarse a WMI de forma remota a partir de vista](connecting-to-wmi-remotely-starting-with-vista.md) y [conectarse a través de Firewall de Windows](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).

Tenga en cuenta que la conexión a WMI en el equipo local tiene un nivel de autenticación predeterminado de **PktPrivacy**.

## <a name="setting-dcom-security-to-allow-a-user-to-access-a-computer-remotely"></a>Configuración de la seguridad de DCOM para permitir que un usuario tenga acceso a un equipo de forma remota

La seguridad en WMI está relacionada con la conexión a un espacio de nombres WMI. WMI utiliza DCOM para controlar llamadas remotas. Una razón para que no se pueda conectar a un equipo remoto se debe a un error de DCOM (error "acceso a DCOM denegado" decimal-2147024891 o Hex 0x80070005). Para obtener más información sobre la seguridad de DCOM en WMI para aplicaciones de C++, vea [establecer la seguridad de procesos de aplicación cliente](setting-client-application-process-security.md).

Puede configurar DCOM para WMI mediante la utilidad de configuración DCOM (**DCOMCnfg.exe**) que se encuentra en **herramientas administrativas** del **Panel de control**. Esta utilidad expone la configuración que permite a determinados usuarios conectarse al equipo de forma remota a través de DCOM. Los miembros del grupo administradores pueden conectarse remotamente al equipo de forma predeterminada. Con esta utilidad puede establecer la seguridad para iniciar, tener acceso y configurar el servicio WMI.

En el procedimiento siguiente se describe cómo conceder permisos de inicio remoto y activación de DCOM para determinados usuarios y grupos. Si el equipo A se conecta de forma remota al equipo B, puede establecer estos permisos en el equipo B para permitir que un usuario o grupo que no forma parte del grupo administradores del equipo B ejecute llamadas de inicio y activación de DCOM en el equipo B.

**Para conceder permisos de inicio y activación remotos de DCOM para un usuario o grupo**

1.  Haga clic en **Inicio**, haga clic en **Ejecutar**, escriba **dcomcnfg** y, a continuación, haga clic en **Aceptar**.
2.  En el cuadro de diálogo **servicios de componentes** , expanda **servicios de componentes**, expanda **equipos** y, a continuación, haga clic con el botón secundario en **mi PC** y haga clic en **propiedades**.
3.  En el cuadro de diálogo **propiedades de mi PC** , haga clic en la pestaña **seguridad com** .
4.  En **Permisos de inicio y activación**, haga clic en **Editar límites**.
5.  En el cuadro de diálogo **permiso de inicio** , siga estos pasos si el nombre o el grupo no aparecen en la **lista nombres de grupos o usuarios**:

    1.  En el cuadro de diálogo **permiso de inicio** , haga clic en **Agregar**.
    2.  En el cuadro de diálogo **Seleccionar usuarios, equipos o grupos** , agregue el nombre y el grupo en el cuadro **Escriba los nombres de objeto que desea seleccionar** y, a continuación, haga clic en **Aceptar**.

6.  En el cuadro de diálogo **permiso de inicio** , seleccione el usuario y el grupo en el cuadro **nombres de grupos o usuarios** . En la columna **permitir** en **permisos para usuario**, seleccione **inicio remoto** y seleccione **activación remota** y, a continuación, haga clic en **Aceptar**.

En el procedimiento siguiente se describe cómo conceder permisos de acceso remoto DCOM para determinados usuarios y grupos. Si el equipo A se conecta de forma remota al equipo B, puede establecer estos permisos en el equipo B para permitir que un usuario o grupo que no forma parte del grupo administradores del equipo B se conecte al equipo B.

**Para conceder permisos de acceso remoto DCOM**

1.  Haga clic en **Inicio**, haga clic en **Ejecutar**, escriba **dcomcnfg** y, a continuación, haga clic en **Aceptar**.
2.  En el cuadro de diálogo **servicios de componentes** , expanda **servicios de componentes**, expanda **equipos** y, a continuación, haga clic con el botón secundario en **mi PC** y haga clic en **propiedades**.
3.  En el cuadro de diálogo **propiedades de mi PC** , haga clic en la pestaña **seguridad com** .
4.  En **Permisos de acceso**, haga clic en **Editar límites**.
5.  En el cuadro de diálogo **permiso de acceso** , seleccione nombre de **Inicio de sesión anónimo** en el cuadro **nombres de grupos o usuarios** . En la columna **permitir** en **permisos de usuario**, seleccione **acceso remoto** y, a continuación, haga clic en **Aceptar**.

## <a name="allowing-users-access-to-a-specific-wmi-namespace"></a>Permitir el acceso de los usuarios a un espacio de nombres WMI específico

Puede permitir o impedir el acceso de los usuarios a un espacio de nombres WMI específico estableciendo el permiso "acceso remoto habilitado" en el control WMI para un espacio de nombres. Si un usuario intenta conectarse a un espacio de nombres al que no se le permite el acceso, recibirá el error 0x80041003. De forma predeterminada, este permiso solo está habilitado para los administradores. Un administrador puede habilitar el acceso remoto a espacios de nombres WMI específicos para un usuario que no sea de administrador.

El siguiente procedimiento establece los permisos de habilitación remota para un usuario que no es administrador.

**Para establecer permisos de habilitación remota**

1.  Conéctese al equipo remoto mediante el control WMI.

    Para obtener más información sobre el control WMI, vea [establecer la seguridad de los espacios de nombres con el control WMI](setting-namespace-security-with-the-wmi-control.md).

2.  En la pestaña **seguridad** , seleccione el espacio de nombres y haga clic en **seguridad**.
3.  Busque la cuenta adecuada y Active **Habilitar remoto** en la lista de **permisos** .

## <a name="setting-namespace-security-to-require-data-encryption-for-remote-connections"></a>Establecer la seguridad del espacio de nombres para requerir el cifrado de datos para las conexiones remotas

Un administrador o un archivo MOF pueden configurar un espacio de nombres de WMI para que no se devuelvan datos a menos que se use la privacidad de paquetes (**\_ \_ \_ \_ \_ privacidad de nivel de autenticación de RPC C** o **PktPrivacy** como moniker en un script) en una conexión a ese espacio de nombres. Esto garantiza que los datos se cifren a medida que atraviesan la red. Si intenta establecer un nivel de autenticación inferior, recibirá un mensaje de acceso denegado. Para obtener más información, vea [requerir una conexión cifrada a un espacio de nombres](requiring-an-encrypted-connection-to-a-namespace.md).

En el ejemplo de código de VBScript siguiente se muestra cómo conectarse a un espacio de nombres cifrado mediante "pktPrivacy".


```VB
strComputer = "RemoteComputer"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktPrivacy}!\\" _
                              & strComputer & "\root\EncryptedNamespace")
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Delegación con WMI](connecting-to-a-3rd-computer-delegation.md)
</dt> <dt>

[Crear procesos de forma remota con WMI](creating-processes-remotely.md)
</dt> <dt>

[Protección de clientes y proveedores de C++](securing-c---clients-and-providers.md)
</dt> <dt>

[Protección de los clientes de scripting](securing-scripting-clients.md)
</dt> </dl>

 

 
