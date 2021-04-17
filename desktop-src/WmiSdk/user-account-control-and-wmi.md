---
description: Control de cuentas de usuario (UAC) afecta a los datos de WMI que se devuelven desde una herramienta de línea de comandos, acceso remoto y cómo deben ejecutarse los scripts. Para obtener más información acerca de UAC, vea Introducción con control de cuentas de usuario.
ms.assetid: f6840aaa-834b-42c8-b641-01c570078fcb
ms.tgt_platform: multiple
title: Control de cuentas de usuario y WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 39d48abcffa537d886397092c6d4a7b558825021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706748"
---
# <a name="user-account-control-and-wmi"></a>Control de cuentas de usuario y WMI

Control de cuentas de usuario (UAC) afecta a los datos de WMI que se devuelven desde una herramienta de línea de comandos, acceso remoto y cómo deben ejecutarse los scripts. Para obtener más información acerca de UAC, vea [Introducción con control de cuentas de usuario](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).

En las secciones siguientes se describe la funcionalidad de UAC:

-   [Control de cuentas de usuario](#user-account-control-and-wmi)
-   [Cuenta necesaria para ejecutar herramientas de Command-Line de WMI](#account-needed-to-run-wmi-command-line-tools)
-   [Controlar conexiones remotas en UAC](#handling-remote-connections-under-uac)
-   [Efecto de UAC en los datos de WMI devueltos a scripts o aplicaciones](#uac-effect-on-wmi-data-returned-to-scripts-or-applications)
-   [Temas relacionados](#related-topics)

## <a name="user-account-control"></a>Control de cuentas de usuario

En UAC, las cuentas del grupo de administradores locales tienen dos [*tokens de acceso*](/windows/desktop/SecGloss/a-gly), uno con privilegios de usuario estándar y otro con privilegios de administrador. Debido al filtrado de tokens de acceso de UAC, un script se ejecuta normalmente en el token de usuario estándar, a menos que se ejecute "como administrador" en el modo de privilegios elevados. No todos los scripts requieren privilegios administrativos.

Los scripts no pueden determinar mediante programación si se ejecutan con un token de seguridad de usuario estándar o un token de administrador. El script puede producir un error de acceso denegado. Si el script requiere privilegios de administrador, se debe ejecutar en el modo con privilegios elevados. El acceso a los espacios de nombres de WMI difiere en función de si el script se ejecuta en modo con privilegios elevados. Algunas operaciones de WMI, como obtener datos o ejecutar la mayoría de los métodos, no requieren que la cuenta se ejecute como administrador. Para obtener más información sobre los permisos de acceso predeterminados, vea [acceso a espacios de nombres WMI](access-to-wmi-namespaces.md) y [ejecutar operaciones con privilegios](executing-privileged-operations.md).

Debido al control de cuentas de usuario, la cuenta que ejecuta el script debe estar en el grupo de administradores del equipo local para poder ejecutar con derechos elevados.

Puede ejecutar un script o una aplicación con permisos elevados mediante la realización de uno de los métodos siguientes:

**Para ejecutar un script en modo con privilegios elevados**

1.  Abra una ventana del símbolo del sistema haciendo clic con el botón secundario en símbolo del sistema en el menú Inicio y, a continuación, haciendo clic en **Ejecutar como administrador**.
2.  Programe el script para que se ejecute con privilegios elevados mediante Programador de tareas. Para obtener más información, vea [contextos de seguridad para ejecutar tareas](/windows/desktop/TaskSchd/security-contexts-for-running-tasks).
3.  Ejecute el script con la cuenta predefinida Administrador.

## <a name="account-needed-to-run-wmi-command-line-tools"></a>Cuenta necesaria para ejecutar herramientas de Command-Line de WMI

Para ejecutar las siguientes [herramientas de Command-Line WMI](wmi-command-line-tools.md), su cuenta debe estar en el grupo administradores y la herramienta debe ejecutarse desde un símbolo del sistema con privilegios elevados. La cuenta predefinida Administrador también puede ejecutar estas herramientas.

-   [**MOFCOMP**](mofcomp.md)

-   [**wmic**](wmic.md)

    La primera vez que ejecute WMIC después de la instalación del sistema, se debe ejecutar desde un símbolo del sistema con privilegios elevados. Es posible que el modo elevado no sea necesario para las ejecuciones posteriores de WMIC a menos que las operaciones de WMI requieran privilegios de administrador.

-   [**WinMgmt**](winmgmt.md)

-   [**wmiadap**](wmiadap.md)

Para ejecutar el [*control WMI*](gloss-w.md) (Wmimgmt. msc) y realizar cambios en la configuración de seguridad o auditoría del espacio de nombres WMI, la cuenta debe tener el derecho editar seguridad concedido explícitamente o estar en el grupo local Administradores. La cuenta predefinida Administrador también puede cambiar la seguridad o la auditoría de un espacio de nombres.

Wbemtest.exe, una herramienta de línea de comandos que no es compatible con los servicios de soporte al cliente de Microsoft, puede ser ejecutada por cuentas que no estén en el grupo de administradores locales, a menos que una operación específica requiera privilegios que normalmente se concedan a las cuentas de administrador.

## <a name="handling-remote-connections-under-uac"></a>Controlar conexiones remotas en UAC

Si se conecta a un equipo remoto en un dominio o en un grupo de trabajo, determina si se produce el filtrado de UAC.

Si el equipo forma parte de un dominio, conéctese al equipo de destino mediante una cuenta de dominio que esté en el grupo de administradores local del equipo remoto. Después, el filtrado de tokens de acceso de UAC no afectará a las cuentas de dominio del grupo de administradores locales. No use una cuenta local, que no sea de dominio, en el equipo remoto, incluso si la cuenta está en el grupo administradores.

En un grupo de trabajo, la cuenta que se conecta al equipo remoto es un usuario local del equipo. Incluso si la cuenta está en el grupo de administradores, el filtrado de UAC significa que un script se ejecuta como un usuario estándar. Un procedimiento recomendado es crear una cuenta de usuario o grupo de usuarios local dedicado en el equipo de destino específicamente para las conexiones remotas.

La seguridad debe ajustarse para poder usar esta cuenta porque la cuenta nunca tiene privilegios administrativos. Conceda al usuario local:

-   Derechos de inicio y activación remotos para tener acceso a DCOM. Para obtener más información, consulte [Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) (puede estar en inglés).
-   Derechos de acceso remoto al espacio de nombres WMI (habilitación remota). Para obtener más información, vea [acceso a los espacios de nombres WMI](access-to-wmi-namespaces.md).
-   Derecho para tener acceso al objeto protegible específico, en función de la seguridad que requiera el objeto.

Si usa una cuenta local, ya sea porque está en un grupo de trabajo o es una cuenta de equipo local, es posible que se le obligue a realizar tareas específicas a un usuario local. Por ejemplo, puede conceder al usuario el derecho a detener o iniciar un servicio específico a través del comando SC.exe, los métodos [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-service) y [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-service) del [**\_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service)o a través de directiva de grupo mediante gpedit. msc. Es posible que algunos objetos protegibles no permitan que un usuario estándar realice tareas y no ofrezca ningún medio para modificar la seguridad predeterminada. En este caso, es posible que deba deshabilitar UAC para que la cuenta de usuario local no se filtre y, en su lugar, se convierta en Administrador total. Tenga en cuenta que, por motivos de seguridad, la deshabilitación de UAC debe ser el último recurso.

No se recomienda deshabilitar UAC remoto cambiando la entrada del registro que controla UAC remoto, pero puede que sea necesario en un grupo de trabajo. La entrada del registro es **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Policies** \\ **System** \\ **LocalAccountTokenFilterPolicy**. Cuando el valor de esta entrada es cero (0), se habilita el filtrado remoto de tokens de acceso de UAC. Cuando el valor es 1, UAC remoto está deshabilitado.

## <a name="uac-effect-on-wmi-data-returned-to-scripts-or-applications"></a>Efecto de UAC en los datos de WMI devueltos a scripts o aplicaciones

Si un script o una aplicación se ejecuta en una cuenta del grupo administradores, pero no se ejecuta con privilegios elevados, es posible que no obtenga todos los datos devueltos porque esta cuenta se está ejecutando como usuario estándar. Los [*proveedores*](gloss-p.md) de WMI de algunas clases no devuelven todas las instancias a una cuenta de usuario estándar o a una cuenta de administrador que no se ejecuta como administrador total debido al filtrado de UAC.

Las siguientes clases no devuelven algunas instancias cuando UAC filtra la cuenta:

-   [**\_Bus Win32**](/windows/desktop/CIMWin32Prov/win32-bus)
-   [**\_Impresora Win32**](/windows/desktop/CIMWin32Prov/win32-printer)
-   [**Win32 \_ ComponentCategory**](/windows/desktop/CIMWin32Prov/win32-componentcategory)
-   [**Win32 \_ LogicalProgramGroupItem**](/windows/desktop/CIMWin32Prov/win32-logicalprogramgroupitem)
-   [**Win32 \_ LogicalProgramGroup**](/windows/desktop/CIMWin32Prov/win32-logicalprogramgroup)
-   [**Win32 \_ NetworkConnection**](/windows/desktop/CIMWin32Prov/win32-networkconnection)
-   [**Cuentadeusuario de Win32 \_**](/windows/desktop/CIMWin32Prov/win32-useraccount)
-   [**Win32 \_ PrinterDriver**](/windows/desktop/CIMWin32Prov/win32-printerdriver)
-   [**Win32 \_ PortResource**](/windows/desktop/CIMWin32Prov/win32-portresource)
-   [**Win32 \_ DeviceMemoryAddress**](/windows/desktop/CIMWin32Prov/win32-devicememoryaddress)

Las siguientes clases no devuelven algunas propiedades cuando UAC filtra la cuenta:

-   [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)
-   [**Win32 \_ DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)
-   [**Win32 \_ DCOMApplication**](/windows/desktop/CIMWin32Prov/win32-dcomapplication)
-   [**\_Placa base Win32**](/windows/desktop/CIMWin32Prov/win32-baseboard)
-   [**ComputerSystem de Win32 \_**](/windows/desktop/CIMWin32Prov/win32-computersystem)
-   [**Adaptador de Win32 \_**](/windows/desktop/CIMWin32Prov/win32-networkadapter)
-   [**Win32 \_ MotherboardDevice**](/windows/desktop/CIMWin32Prov/win32-motherboarddevice)
-   [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive)
-   [**Win32 \_ PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)
-   [**\_Videocontroladora Win32**](/windows/desktop/CIMWin32Prov/win32-videocontroller)
-   [**Win32 \_ ParallelPort**](/windows/desktop/CIMWin32Prov/win32-parallelport)
-   [**LogicalDisk de Win32 \_**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)
-   [**Win32 \_ SystemDriver**](/windows/desktop/CIMWin32Prov/win32-systemdriver)
-   [**Win32 \_ IRQResource**](/windows/desktop/CIMWin32Prov/win32-irqresource)
-   [**Win32 \_ NetworkProtocol**](/windows/desktop/CIMWin32Prov/win32-networkprotocol)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de WMI](about-wmi.md)
</dt> <dt>

[Acceso a objetos protegibles de WMI](access-to-wmi-securable-objects.md)
</dt> <dt>

[Cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 
