---
description: WMI usa un descriptor de seguridad Windows estándar para controlar el acceso a los espacios de nombres WMI.
ms.assetid: 5cf9886c-04fa-480e-889f-b64a6a70d053
ms.tgt_platform: multiple
title: Acceso a espacios de nombres WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b750c8dee2b95597636620dc54ad193cb762cd259b2bf7149c52996e85e09b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117926031"
---
# <a name="access-to-wmi-namespaces"></a>Acceso a espacios de nombres WMI

WMI usa un descriptor de seguridad Windows *estándar para* controlar el acceso a los espacios de nombres WMI. Al conectarse a WMI, ya sea mediante el moniker "winmgmts" de WMI o una llamada a [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) o [**SWbemLocator.ConnectServer,**](swbemlocator-connectserver.md)se conecta a un espacio de nombres específico.

En este tema se describe la siguiente información:

-   [Seguridad del espacio de nombres WMI](#wmi-namespace-security)
-   [Auditoría de espacios de nombres WMI](#wmi-namespace-auditing)
-   [Tipos de eventos de espacio de nombres](#types-of-namespace-events)
-   [Acceso al espacio de nombres Configuración](#namespace-access-settings)
-   [Permisos predeterminados en espacios de nombres WMI](#default-permissions-on-wmi-namespaces)
-   [Temas relacionados](#related-topics)

## <a name="wmi-namespace-security"></a>Seguridad del espacio de nombres WMI

WMI mantiene la seguridad del espacio de nombres comparando el [*token*](/windows/desktop/SecGloss/a-gly) de acceso del usuario que se conecta al espacio de nombres con el [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) del espacio de nombres. Para obtener más información sobre Windows seguridad, vea Acceso a [objetos protegibles WMI.](access-to-wmi-securable-objects.md)

Tenga en cuenta que, a partir de Windows Vista, el Control de cuentas de usuario [(UAC)](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) afecta al acceso a los datos WMI y a lo que se puede configurar con el [*control WMI*](gloss-w.md). Para obtener más información, vea [Permisos predeterminados en espacios de nombres WMI](#default-permissions-on-wmi-namespaces) y Control de cuentas de usuario y [WMI.](user-account-control-and-wmi.md)

El acceso a los espacios de nombres WMI también se ve afectado cuando la conexión es desde un equipo remoto. Para obtener más información, vea [Conectarse a WMI](connecting-to-wmi-on-a-remote-computer.md)en un equipo remoto , Proteger una conexión WMI remota y Conectarse [a](securing-a-remote-wmi-connection.md)través de [Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).

Los proveedores deben basarse en la configuración de suplantación para que la conexión determine si el script de cliente o la aplicación deben recibir datos. Para obtener más información sobre el script y las aplicaciones cliente, vea [Establecer la seguridad del proceso de aplicación cliente.](setting-client-application-process-security.md) Para obtener más información sobre [*la*](gloss-p.md) suplantación de proveedor, vea [Desarrollar un proveedor WMI.](developing-a-wmi-provider.md)

## <a name="wmi-namespace-auditing"></a>Auditoría de espacios de nombres WMI

WMI usa las listas de [*control de acceso del sistema (SACL)*](/windows/desktop/SecGloss/s-gly) del espacio de nombres para auditar la actividad del espacio de nombres. Para habilitar la auditoría de espacios  de nombres WMI, use la pestaña Seguridad del [*control WMI*](gloss-w.md) para cambiar la configuración de auditoría del espacio de nombres.

La auditoría no está habilitada durante la instalación del sistema operativo. Para habilitar la auditoría, haga clic en **la pestaña Auditoría** en la ventana **Seguridad** estándar. A continuación, puede agregar una entrada de auditoría.

directiva de grupo para el equipo local debe establecerse para permitir la auditoría. Puede habilitar la auditoría ejecutando el complemento MMC Gpedit.msc y estableciendo **Audit Object Access** en Computer **Configuration**  >  **Windows Configuración**  >  **Security Configuración** Local  >  **Policies**  >  **Audit Policy**.

Una entrada de auditoría edita la SACL del espacio de nombres. Al agregar una entrada de auditoría, es un usuario, un grupo, un equipo o una entidad de seguridad integrada. Después de agregar la entrada, puede establecer las operaciones de acceso que tienen como resultado eventos de registro de seguridad. Por ejemplo, para el grupo Usuarios autenticados, puede hacer clic en Ejecutar métodos. Esta configuración genera eventos de registro de seguridad cada vez que un miembro del grupo Usuarios autenticados ejecuta un método en ese espacio de nombres. El identificador de evento para los eventos WMI es 4662.

La cuenta debe estar en el grupo Administradores y ejecutarse con privilegios elevados para cambiar la configuración de auditoría. La cuenta de administrador integrada también puede cambiar la seguridad o la auditoría de un espacio de nombres. Para obtener más información sobre la ejecución en modo con privilegios elevados, vea [Control de cuentas de usuario y WMI.](user-account-control-and-wmi.md)

La auditoría de WMI genera eventos correctos o de error para los intentos de acceder a espacios de nombres WMI. El servicio no audita el éxito o error de las operaciones del proveedor. Por ejemplo, cuando un script se conecta a WMI y un espacio de nombres, puede producir un error porque la cuenta con la que se ejecuta el script no tiene acceso a ese espacio de nombres o puede intentar una operación, como editar la DACL, que no se concede.

Si está ejecutando con una cuenta en el grupo Administradores, puede ver los eventos de auditoría del espacio de nombres en la **Visor de eventos** de usuario.

## <a name="types-of-namespace-events"></a>Tipos de eventos de espacio de nombres

WMI hace un seguimiento de los siguientes tipos de eventos en el registro de eventos de seguridad:

-   Auditoría correcta

    La operación debe completar correctamente dos pasos para una auditoría correcta. En primer lugar, WMI concede acceso a la aplicación cliente o script basado en el SID del cliente y la DACL del espacio de nombres. En segundo lugar, la operación solicitada coincide con los derechos de acceso del espacio de nombres SACL para ese usuario o grupo.

-   Error de auditoría

    WMI deniega el acceso al espacio de nombres, pero la operación solicitada coincide con los derechos de acceso en la SACL del espacio de nombres para ese usuario o grupo.

## <a name="namespace-access-settings"></a>Acceso al espacio de nombres Configuración

Puede ver los derechos de acceso del espacio de nombres para varias cuentas en el control WMI. Estas constantes se describen en [**Constantes de derechos de acceso de**](namespace-access-rights-constants.md)espacio de nombres . Puede cambiar el acceso a un espacio de nombres WMI mediante el control WMI o mediante programación. Para obtener más información, vea [Cambiar la seguridad de acceso en objetos protegibles.](changing-access-security-on-securable-objects.md)

WMI audita los cambios en todos los permisos de acceso enumerados en la lista siguiente, excepto para el permiso De habilitación remota. Los cambios se registran como errores o aciertos de auditoría correspondientes al permiso Editar seguridad.

<dl> <dt>

<span id="Execute_Methods"></span><span id="execute_methods"></span><span id="EXECUTE_METHODS"></span>Ejecutar métodos
</dt> <dd>

Permite al usuario ejecutar métodos definidos en clases WMI. Corresponde a la constante de permiso de acceso **WBEM \_ METHOD \_ EXECUTE.**

</dd> <dt>

<span id="Full_Write"></span><span id="full_write"></span><span id="FULL_WRITE"></span>Escritura completa
</dt> <dd>

Permite el acceso completo de lectura, escritura y eliminación a clases WMI e instancias de clase, tanto estáticas como dinámicas. Corresponde a la constante **de permiso de acceso \_ WBEM FULL WRITE \_ \_ REP.**

</dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>Escritura parcial
</dt> <dd>

Permite el acceso de escritura a instancias de clase WMI estáticas. Corresponde a la constante **de permiso de acceso WBEM PARTIAL WRITE \_ \_ \_ REP.**

</dd> <dt>

<span id="Provider_Write"></span><span id="provider_write"></span><span id="PROVIDER_WRITE"></span>Escritura del proveedor
</dt> <dd>

Permite el acceso de escritura a instancias de clase WMI dinámicas. Corresponde a la constante **de permiso de acceso WBEM WRITE \_ \_ PROVIDER.**

</dd> <dt>

<span id="Enable_Account"></span><span id="enable_account"></span><span id="ENABLE_ACCOUNT"></span>Habilitar cuenta
</dt> <dd>

Permite el acceso de lectura a instancias de clase WMI. Corresponde a la constante de permiso de acceso **WBEM \_ ENABLE.**

</dd> <dt>

<span id="Remote_Enable"></span><span id="remote_enable"></span><span id="REMOTE_ENABLE"></span>Habilitación remota
</dt> <dd>

Permite el acceso al espacio de nombres por parte de equipos remotos. Corresponde a la constante **de permiso de acceso WBEM REMOTE \_ \_ ACCESS.**

</dd> <dt>

<span id="Read_Security"></span><span id="read_security"></span><span id="READ_SECURITY"></span>Leer seguridad
</dt> <dd>

Permite el acceso de solo lectura a la configuración de DACL. Corresponde a la constante de permiso de **acceso READ \_ CONTROL.**

</dd> <dt>

<span id="Edit_Security"></span><span id="edit_security"></span><span id="EDIT_SECURITY"></span>Editar seguridad
</dt> <dd>

Permite el acceso de escritura a la configuración de DACL. Corresponde a la constante **de permiso de acceso WRITE \_ DAC.**

</dd> </dl>

## <a name="default-permissions-on-wmi-namespaces"></a>Permisos predeterminados en espacios de nombres WMI

Los grupos de seguridad predeterminados son:

-   Usuarios autenticados
-   SERVICIO LOCAL
-   SERVICIO DE RED
-   Administradores (en el equipo local)

Los permisos de acceso predeterminados para los usuarios autenticados, el servicio local y el servicio de red son:

-   Ejecutar métodos
-   Escritura completa
-   Habilitar cuenta

Las cuentas del grupo Administradores tienen todos los derechos disponibles, incluida la edición de descriptores de seguridad. Sin embargo, debido al Control de cuentas de usuario (UAC), el control WMI o el script deben ejecutarse con seguridad elevada. Para obtener más información, vea [Control de cuentas de usuario y WMI.](user-account-control-and-wmi.md)

A veces, un script o aplicación debe habilitar un privilegio de administrador, **como SeSecurityPrivilege,** para llevar a cabo una operación. Por ejemplo, un script puede ejecutar el método [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) de la clase Printer de [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-printer) sin **SeSecurityPrivilege** y obtener la información de seguridad en la lista de control de acceso discrecional [*(DACL)*](/windows/desktop/SecGloss/d-gly) del descriptor de seguridad del objeto de [*impresora*](/windows/desktop/SecGloss/s-gly). Sin embargo, la información de SACL no se devuelve al script a menos que el privilegio **SeSecurityPrivilege** esté disponible y habilitado para la cuenta. Si la cuenta no tiene el privilegio disponible, no se puede habilitar. Para obtener más información, vea [Ejecutar operaciones con privilegios.](executing-privileged-operations.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de WMI](about-wmi.md)
</dt> </dl>

 

 
