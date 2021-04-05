---
description: WMI usa un descriptor de seguridad de Windows estándar para controlar el acceso a los espacios de nombres de WMI.
ms.assetid: 5cf9886c-04fa-480e-889f-b64a6a70d053
ms.tgt_platform: multiple
title: Acceso a los espacios de nombres WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6eaebe5370e97dcb42ddcf79018015ceff9147f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002835"
---
# <a name="access-to-wmi-namespaces"></a>Acceso a los espacios de nombres WMI

WMI usa un *descriptor de seguridad* de Windows estándar para controlar el acceso a los espacios de nombres de WMI. Cuando se conecta a WMI, mediante el moniker de WMI "winmgmts" o una llamada a [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) o [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md), se conecta a un espacio de nombres específico.

En este tema se describe la siguiente información:

-   [Seguridad del espacio de nombres WMI](#wmi-namespace-security)
-   [Auditoría de espacio de nombres WMI](#wmi-namespace-auditing)
-   [Tipos de eventos de espacio de nombres](#types-of-namespace-events)
-   [Configuración de acceso a espacios de nombres](#namespace-access-settings)
-   [Permisos predeterminados en espacios de nombres WMI](#default-permissions-on-wmi-namespaces)
-   [Temas relacionados](#related-topics)

## <a name="wmi-namespace-security"></a>Seguridad del espacio de nombres WMI

WMI mantiene la seguridad del espacio de nombres mediante la comparación del [*token de acceso*](/windows/desktop/SecGloss/a-gly) del usuario que se conecta al espacio de nombres con el [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) del espacio de nombres. Para obtener más información sobre la seguridad de Windows, consulte [acceso a objetos protegibles de WMI](access-to-wmi-securable-objects.md).

Tenga en cuenta que, a partir de Windows Vista, el [control de cuentas de usuario (UAC)](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) afecta al acceso a los datos WMI y a lo que se puede configurar con el [*control WMI*](gloss-w.md). Para obtener más información, vea [permisos predeterminados en espacios de nombres WMI](#default-permissions-on-wmi-namespaces) y [control de cuentas de usuario y WMI](user-account-control-and-wmi.md).

El acceso a los espacios de nombres WMI también se ve afectado cuando la conexión procede de un equipo remoto. Para obtener más información, vea [conectarse a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md), [proteger una conexión WMI remota](securing-a-remote-wmi-connection.md)y [conectarse a través de Firewall de Windows](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).

Los proveedores deben basarse en la configuración de suplantación de la conexión para determinar si la aplicación o el script de cliente deben recibir los datos. Para obtener más información sobre los scripts y las aplicaciones cliente, vea [establecer la seguridad de procesos de aplicación cliente](setting-client-application-process-security.md). Para obtener más información sobre la suplantación de [*proveedores*](gloss-p.md) , vea [desarrollar un proveedor WMI](developing-a-wmi-provider.md).

## <a name="wmi-namespace-auditing"></a>Auditoría de espacio de nombres WMI

WMI usa las [*listas de control de acceso de sistema (SACL) del*](/windows/desktop/SecGloss/s-gly) espacio de nombres para auditar la actividad del espacio de nombres. Para habilitar la auditoría de espacios de nombres de WMI, utilice la pestaña **seguridad** del [*control WMI*](gloss-w.md) para cambiar la configuración de auditoría del espacio de nombres.

La auditoría no se habilita durante la instalación del sistema operativo. Para habilitar la auditoría, haga clic en la pestaña **Auditoría** de la ventana **seguridad** estándar. Después, puede Agregar una entrada de auditoría.

Directiva de grupo para el equipo local debe estar establecido en permitir auditoría. Puede habilitar la auditoría ejecutando el complemento de MMC gpedit. msc y estableciendo **auditar el acceso a objetos** en **configuración del equipo** configuración de  >  **Windows**  >  **configuración de seguridad**  >  **Directivas locales**  >  **Directiva de auditoría**.

Una entrada de auditoría edita la SACL del espacio de nombres. Cuando se agrega una entrada de auditoría, se trata de un usuario, un grupo, un equipo o una entidad de seguridad integrada. Después de agregar la entrada, puede establecer las operaciones de acceso que dan como resultado eventos del registro de seguridad. Por ejemplo, para el grupo usuarios autenticados, puede hacer clic en ejecutar métodos. Esta configuración produce eventos de registro de seguridad cada vez que un miembro del grupo usuarios autenticados ejecuta un método en dicho espacio de nombres. El ID. de evento de los eventos WMI es 4662.

La cuenta debe estar en el grupo administradores y ejecutarse con privilegios elevados para cambiar la configuración de auditoría. La cuenta predefinida Administrador también puede cambiar la seguridad o la auditoría de un espacio de nombres. Para obtener más información acerca de la ejecución en modo elevado, vea [control de cuentas de usuario y WMI](user-account-control-and-wmi.md).

La auditoría de WMI genera eventos de éxito o error para los intentos de acceso a espacios de nombres WMI. El servicio no audita si las operaciones del proveedor se han realizado correctamente o no. Por ejemplo, cuando un script se conecta a WMI y a un espacio de nombres, puede producirse un error porque la cuenta con la que se está ejecutando el script no tiene acceso al espacio de nombres o puede intentar una operación, como editar la DACL, que no se concede.

Si está ejecutando en una cuenta del grupo administradores, puede ver los eventos de auditoría de espacio de nombres en la interfaz de usuario de **visor de eventos** .

## <a name="types-of-namespace-events"></a>Tipos de eventos de espacio de nombres

WMI realiza un seguimiento de los siguientes tipos de eventos en el registro de eventos de seguridad:

-   Auditoría correcta

    La operación debe completar correctamente dos pasos para una auditoría correcta. En primer lugar, WMI concede acceso a la aplicación cliente o script según el SID del cliente y la DACL del espacio de nombres. En segundo lugar, la operación solicitada coincide con los derechos de acceso en la SACL del espacio de nombres para ese usuario o grupo.

-   Error de auditoría

    WMI deniega el acceso al espacio de nombres, pero la operación solicitada coincide con los derechos de acceso de la SACL del espacio de nombres de ese usuario o grupo.

## <a name="namespace-access-settings"></a>Configuración de acceso a espacios de nombres

Puede ver los derechos de acceso del espacio de nombres de varias cuentas en el control WMI. Estas constantes se describen en [**constantes de derechos de acceso de espacio de nombres**](namespace-access-rights-constants.md). Puede cambiar el acceso a un espacio de nombres WMI mediante el control WMI o mediante programación. Para obtener más información, consulte [cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md).

WMI audita los cambios en todos los permisos de acceso que se muestran en la lista siguiente, salvo el permiso Remote enable. Los cambios se registran como auditoría de éxito o error correspondiente al permiso editar seguridad.

<dl> <dt>

<span id="Execute_Methods"></span><span id="execute_methods"></span><span id="EXECUTE_METHODS"></span>Ejecutar métodos
</dt> <dd>

Permite al usuario ejecutar los métodos definidos en las clases WMI. Corresponde a la constante de permiso de acceso de **\_ \_ ejecución del método WBEM** .

</dd> <dt>

<span id="Full_Write"></span><span id="full_write"></span><span id="FULL_WRITE"></span>Escritura completa
</dt> <dd>

Permite el acceso completo de lectura, escritura y eliminación a clases WMI e instancias de clase, tanto estáticas como dinámicas. Corresponde a la constante de permiso de acceso de **\_ rellenado de \_ escritura \_ completa de WBEM** .

</dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>Escritura parcial
</dt> <dd>

Permite el acceso de escritura a instancias de clase WMI estáticas. Corresponde a la constante de permiso de acceso de la **\_ \_ \_ representación parcial de escritura de WBEM** .

</dd> <dt>

<span id="Provider_Write"></span><span id="provider_write"></span><span id="PROVIDER_WRITE"></span>Escritura de proveedor
</dt> <dd>

Permite el acceso de escritura a instancias de clase WMI dinámicas. Corresponde a la constante de permiso de acceso de **\_ \_ proveedor de escritura WBEM** .

</dd> <dt>

<span id="Enable_Account"></span><span id="enable_account"></span><span id="ENABLE_ACCOUNT"></span>Habilitar cuenta
</dt> <dd>

Permite el acceso de lectura a las instancias de clase WMI. Corresponde a la constante de permiso **\_ Habilitar** acceso de WBEM.

</dd> <dt>

<span id="Remote_Enable"></span><span id="remote_enable"></span><span id="REMOTE_ENABLE"></span>Habilitación remota
</dt> <dd>

Permite el acceso al espacio de nombres de los equipos remotos. Corresponde a la constante de permiso de acceso **\_ \_ remoto de WBEM** .

</dd> <dt>

<span id="Read_Security"></span><span id="read_security"></span><span id="READ_SECURITY"></span>Seguridad de lectura
</dt> <dd>

Permite el acceso de solo lectura a la configuración de DACL. Corresponde a la constante de permiso de acceso de **\_ control de lectura** .

</dd> <dt>

<span id="Edit_Security"></span><span id="edit_security"></span><span id="EDIT_SECURITY"></span>Editar seguridad
</dt> <dd>

Permite el acceso de escritura a la configuración de DACL. Corresponde a la constante de permiso de acceso de **escritura de \_ DAC** .

</dd> </dl>

## <a name="default-permissions-on-wmi-namespaces"></a>Permisos predeterminados en espacios de nombres WMI

Los grupos de seguridad predeterminados son:

-   Usuarios autenticados
-   SERVICIO LOCAL
-   SERVICIO DE RED
-   Administradores (en el equipo local)

Los permisos de acceso predeterminados para los usuarios autenticados, el servicio LOCAL y el servicio de red son:

-   Ejecutar métodos
-   Escritura completa
-   Habilitar cuenta

Las cuentas del grupo administradores tienen todos los derechos disponibles, incluida la edición de descriptores de seguridad. Sin embargo, debido a un control de cuentas de usuario (UAC), el control WMI o el script deben ejecutarse con seguridad elevada. Para obtener más información, vea [control de cuentas de usuario y WMI](user-account-control-and-wmi.md).

A veces, un script o una aplicación debe habilitar un privilegio de administrador, como **SeSecurityPrivilege**, para llevar a cabo una operación. Por ejemplo, un script puede ejecutar el método [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) de la [**clase \_ Printer de Win32**](/windows/desktop/CIMWin32Prov/win32-printer) sin **SeSecurityPrivilege** y obtener la información de seguridad en la lista de [*control de acceso discrecional (DACL)*](/windows/desktop/SecGloss/d-gly) del [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly)del objeto Printer. Sin embargo, la información de SACL no se devuelve al script a menos que el privilegio **SeSecurityPrivilege** esté disponible y habilitado para la cuenta. Si la cuenta no tiene el privilegio disponible, no se puede habilitar. Para obtener más información, vea [ejecutar operaciones con privilegios](executing-privileged-operations.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de WMI](about-wmi.md)
</dt> </dl>

 

 
