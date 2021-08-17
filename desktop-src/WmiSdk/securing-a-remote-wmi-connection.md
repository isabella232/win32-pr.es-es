---
description: Para conectarse a un equipo remoto mediante WMI, asegúrese de que la configuración de DCOM correcta y la configuración de seguridad del espacio de nombres WMI están habilitadas para la conexión.
ms.assetid: 96ebaa9b-a062-4300-a637-8eb71cb80d1c
ms.tgt_platform: multiple
title: Protección de una conexión WMI remota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8650ee47c549121a51e5d131055a84c176da944c6146f0532ffc86f1d2f9e4c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739519"
---
# <a name="securing-a-remote-wmi-connection"></a>Protección de una conexión WMI remota

Para conectarse a un equipo remoto mediante WMI, asegúrese de que la configuración de DCOM correcta y la configuración de seguridad del espacio de nombres WMI están habilitadas para la conexión.

WMI tiene la configuración predeterminada del servicio de suplantación, autenticación y autenticación (NTLM o Kerberos) que requiere el equipo de destino en una conexión remota. La máquina local puede usar valores predeterminados diferentes que el sistema de destino no acepta. Puede cambiar esta configuración en la llamada de conexión.

En este tema se de abordan las secciones siguientes:

-   [Suplantación y autenticación de DCOM Configuración wmi](#dcom-impersonation-and-authentication-settings-for-wmi)
-   [Establecer la seguridad de DCOM para permitir que un usuario acceda a un equipo de forma remota](#setting-dcom-security-to-allow-a-user-to-access-a-computer-remotely)
-   [Permitir que los usuarios accedan a un espacio de nombres WMI específico](#allowing-users-access-to-a-specific-wmi-namespace)
-   [Establecer la seguridad del espacio de nombres para requerir cifrado de datos para conexiones remotas](#setting-namespace-security-to-require-data-encryption-for-remote-connections)
-   [Temas relacionados](#related-topics)

## <a name="dcom-impersonation-and-authentication-settings-for-wmi"></a>Suplantación y autenticación de DCOM Configuración para WMI

WMI tiene la configuración predeterminada del servicio de suplantación, autenticación y autenticación DCOM (NTLM o Kerberos) que requiere un sistema remoto. El sistema local puede usar valores predeterminados diferentes que el sistema remoto de destino no acepta. Puede cambiar esta configuración en la llamada de conexión. Para obtener más información, vea [Establecer la seguridad del proceso de aplicación cliente.](setting-client-application-process-security.md) Sin embargo, para el servicio de autenticación, se recomienda especificar **RPC \_ C \_ AUTHN \_ DEFAULT** y permitir que DCOM elija el servicio adecuado para el equipo de destino.

Puede proporcionar la configuración en parámetros para las llamadas a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) en C++. En los scripts, puede establecer la configuración de seguridad en las llamadas a [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md), en un [**objeto SWbemSecurity**](swbemsecurity.md) o en la cadena [de moniker de](constructing-a-moniker-string.md) scripting.

Para obtener una lista de todas las constantes de suplantación de C++, vea Establecer el nivel de seguridad [de proceso predeterminado mediante C++.](setting-the-default-process-security-level-using-c-.md) Para obtener Visual Basic constantes y cadenas de scripting para usar la conexión de moniker, vea Establecer el nivel de seguridad de proceso [predeterminado mediante VBScript.](setting-the-default-process-security-level-using-vbscript.md)

En la tabla siguiente se muestra la configuración predeterminada del servicio de suplantación, autenticación y autenticación de DCOM que requiere el equipo de destino (equipo B) en una conexión remota. Para obtener más información, vea Proteger una conexión WMI remota.



| Sistema operativo del equipo B | Cadena de scripting de nivel de suplantación | Cadena de scripting de nivel de autenticación | Servicio de autenticación |
|-----------------------------|--------------------------------------|---------------------------------------|------------------------|
| Windows Vista o posterior      | Impersonate                          | Pkt                                   | Kerberos               |



 

Las conexiones remotas WMI se ven afectadas por el Control de cuentas de [usuario (UAC)](/previous-versions/aa905108(v=msdn.10)) [y Windows firewall](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx). Para obtener más información, vea [Conectarse a WMI de forma remota a partir de Vista](connecting-to-wmi-remotely-starting-with-vista.md) y [Conectarse a través de Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).

Tenga en cuenta que la conexión a WMI en el equipo local tiene un nivel de autenticación predeterminado **de PktPrivacy**.

## <a name="setting-dcom-security-to-allow-a-user-to-access-a-computer-remotely"></a>Establecer la seguridad de DCOM para permitir que un usuario acceda a un equipo de forma remota

La seguridad de WMI está relacionada con la conexión a un espacio de nombres WMI. WMI usa DCOM para controlar las llamadas remotas. Uno de los motivos por los que no se puede conectar a un equipo remoto se debe a un error de DCOM (error "DCOM Access Denied" decimal -2147024891 or hex 0x80070005). Para obtener más información sobre la seguridad de DCOM en WMI para aplicaciones de C++, vea Establecer la seguridad del [proceso de aplicación cliente.](setting-client-application-process-security.md)

Puede configurar las opciones de DCOM para WMI mediante la utilidad de configuración de DCOM (**DCOMCnfg.exe**) que se encuentra en Herramientas **administrativas** **en Panel de control**. Esta utilidad expone la configuración que permite a determinados usuarios conectarse al equipo de forma remota a través de DCOM. Los miembros del grupo Administradores pueden conectarse de forma remota al equipo de forma predeterminada. Con esta utilidad puede establecer la seguridad para iniciar, acceder y configurar el servicio WMI.

En el procedimiento siguiente se describe cómo conceder permisos de activación y inicio remoto de DCOM para determinados usuarios y grupos. Si el equipo A se conecta de forma remota al equipo B, puede establecer estos permisos en el equipo B para permitir que un usuario o grupo que no forma parte del grupo Administradores del equipo B ejecute llamadas de inicio y activación DCOM en el equipo B.

**Para conceder permisos de inicio y activación remotos de DCOM para un usuario o grupo**

1.  Haga clic **en Inicio**, haga clic **en Ejecutar**, escriba **DCOMCNFG** y, a continuación, haga clic **en Aceptar.**
2.  En el cuadro **de diálogo** Servicios de componentes , expanda **Servicios** de componentes , expanda Equipos **y,** a **continuación, haga** clic con el botón Mi PC haga clic en **Propiedades**.
3.  En el cuadro **de Mi PC propiedades,** haga clic en la **pestaña Seguridad COM** .
4.  En **Permisos de inicio y activación**, haga clic en **Editar límites**.
5.  En el **cuadro de diálogo Permiso** de inicio , siga estos pasos si el nombre o el grupo no aparecen en la lista Grupos o nombres de **usuario**:

    1.  En el cuadro **de diálogo Permiso** de inicio , haga clic en **Agregar**.
    2.  En el cuadro de diálogo Seleccionar **usuarios, equipos** o grupos  , agregue su nombre y el grupo en el cuadro Escriba los nombres de objeto que desea seleccionar y, a continuación, haga clic **en Aceptar**.

6.  En el **cuadro de diálogo Permiso** de inicio , seleccione el usuario y el grupo en el cuadro Nombres de usuario **o** grupo . En la **columna Permitir** en Permisos para **el usuario**, seleccione **Inicio remoto,** activación **remota** y, a continuación, haga clic **en Aceptar.**

En el procedimiento siguiente se describe cómo conceder permisos de acceso remoto de DCOM para determinados usuarios y grupos. Si el equipo A se conecta de forma remota al equipo B, puede establecer estos permisos en el equipo B para permitir que un usuario o grupo que no forma parte del grupo Administradores del equipo B se conecte al equipo B.

**Para conceder permisos de acceso remoto de DCOM**

1.  Haga clic **en Inicio**, haga clic **en Ejecutar**, escriba **DCOMCNFG** y, a continuación, haga clic **en Aceptar.**
2.  En el cuadro **de diálogo** Servicios de componentes , expanda **Servicios** de componentes , expanda Equipos **y,** a **continuación, haga** clic con el botón Mi PC haga clic en **Propiedades**.
3.  En el cuadro **de Mi PC propiedades,** haga clic en la **pestaña Seguridad COM** .
4.  En **Permisos de acceso**, haga clic en **Editar límites**.
5.  En el cuadro **de diálogo Permiso** de acceso, seleccione Nombre DE INICIO DE **SESIÓN** ANÓNIMO en el cuadro Nombres de **usuario o** grupo. En la **columna Permitir** en Permisos para **el usuario**, seleccione Acceso **remoto** y, a continuación, haga clic **en Aceptar.**

## <a name="allowing-users-access-to-a-specific-wmi-namespace"></a>Permitir que los usuarios accedan a un espacio de nombres WMI específico

Puede permitir o no permitir que los usuarios accedan a un espacio de nombres WMI específico estableciendo el permiso "Habilitar remotamente" en el Control WMI para un espacio de nombres. Si un usuario intenta conectarse a un espacio de nombres al que no se le permite el acceso, recibirá un error 0x80041003. De forma predeterminada, este permiso solo está habilitado para los administradores. Un administrador puede habilitar el acceso remoto a espacios de nombres WMI específicos para un usuario que no es administrador.

El procedimiento siguiente establece permisos de habilitación remota para un usuario que no es administrador.

**Para establecer permisos de habilitación remota**

1.  Conectar al equipo remoto mediante el control WMI.

    Para obtener más información sobre el control WMI, vea [Establecer la seguridad del espacio de nombres con el control WMI](setting-namespace-security-with-the-wmi-control.md).

2.  En la pestaña **Seguridad,** seleccione el espacio de nombres y haga clic **en Seguridad.**
3.  Busque la cuenta adecuada y active **Habilitar remotamente en** la **lista Permisos.**

## <a name="setting-namespace-security-to-require-data-encryption-for-remote-connections"></a>Establecer la seguridad del espacio de nombres para requerir cifrado de datos para conexiones remotas

Un administrador o un archivo MOF puede configurar un espacio de nombres WMI para que no se devuelva ningún dato a menos que use la privacidad de paquetes **(RPC \_ C \_ \_ \_ AUTHN LEVEL PKT \_ PRIVACY** o **PktPrivacy** como moniker en un script) en una conexión a ese espacio de nombres. Esto garantiza que los datos se cifran a medida que cruzan la red. Si intenta establecer un nivel de autenticación inferior, recibirá un mensaje de acceso denegado. Para obtener más información, vea [Requerir una conexión cifrada a un espacio de nombres](requiring-an-encrypted-connection-to-a-namespace.md).

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

[Protección de clientes de scripting](securing-scripting-clients.md)
</dt> </dl>

 

 
