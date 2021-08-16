---
description: El control de cuentas de usuario (UAC) afecta a los datos WMI que se devuelven desde una herramienta de línea de comandos, el acceso remoto y cómo se deben ejecutar los scripts. Para obtener más información sobre UAC, consulte Tareas iniciales control de cuentas de usuario.
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
ms.openlocfilehash: 2da001117fa75ccef737647038d3e58b942f666ba40e1fd14ec98cb4ebdd44af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553321"
---
# <a name="user-account-control-and-wmi"></a>Control de cuentas de usuario y WMI

El control de cuentas de usuario (UAC) afecta a los datos WMI que se devuelven desde una herramienta de línea de comandos, el acceso remoto y cómo se deben ejecutar los scripts. Para obtener más información sobre UAC, [vea Tareas iniciales con el control de cuentas de usuario](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).

En las secciones siguientes se describe la funcionalidad de UAC:

-   [Control de cuentas de usuario](#user-account-control-and-wmi)
-   [Cuenta necesaria para ejecutar herramientas de Command-Line WMI](#account-needed-to-run-wmi-command-line-tools)
-   [Control de conexiones remotas en UAC](#handling-remote-connections-under-uac)
-   [Efecto de UAC en los datos WMI devueltos a scripts o aplicaciones](#uac-effect-on-wmi-data-returned-to-scripts-or-applications)
-   [Temas relacionados](#related-topics)

## <a name="user-account-control"></a>Control de cuentas de usuario

En UAC, las cuentas del grupo administradores locales tienen dos [*tokens*](/windows/desktop/SecGloss/a-gly)de acceso, uno con privilegios de usuario estándar y otro con privilegios de administrador. Debido al filtrado de tokens de acceso de UAC, un script se ejecuta normalmente en el token de usuario estándar, a menos que se ejecute "como administrador" en modo con privilegios elevados. No todos los scripts requerían privilegios administrativos.

Los scripts no pueden determinar mediante programación si se ejecutan con un token de seguridad de usuario estándar o un token de administrador. El script puede producir un error de acceso denegado. Si el script requiere privilegios de administrador, debe ejecutarse en modo con privilegios elevados. El acceso a los espacios de nombres WMI difiere en función de si el script se ejecuta en modo con privilegios elevados. Algunas operaciones wmi, como obtener datos o ejecutar la mayoría de los métodos, no requieren que la cuenta se ejecute como administrador. Para obtener más información sobre los permisos de acceso predeterminados, vea Acceso a espacios [de nombres WMI](access-to-wmi-namespaces.md) y Ejecución de operaciones con [privilegios](executing-privileged-operations.md).

Debido al control de cuentas de usuario, la cuenta que ejecuta el script debe estar en el grupo Administradores del equipo local para poder ejecutarse con derechos elevados.

Puede ejecutar un script o una aplicación con derechos elevados mediante uno de los métodos siguientes:

**Para ejecutar un script en modo con privilegios elevados**

1.  Abra una ventana del símbolo del sistema haciendo clic con el botón derecho en Símbolo del sistema en la menú Inicio y, a continuación, haga clic **en Ejecutar como administrador.**
2.  Programe el script para que se ejecute con privilegios elevados Programador de tareas. Para obtener más información, vea [Contextos de seguridad para ejecutar tareas](/windows/desktop/TaskSchd/security-contexts-for-running-tasks).
3.  Ejecute el script con la cuenta de administrador integrada.

## <a name="account-needed-to-run-wmi-command-line-tools"></a>Cuenta necesaria para ejecutar herramientas de Command-Line WMI

Para ejecutar las siguientes herramientas [Command-Line WMI,](wmi-command-line-tools.md)la cuenta debe estar en el grupo Administradores y la herramienta debe ejecutarse desde un símbolo del sistema con privilegios elevados. La cuenta de administrador integrada también puede ejecutar estas herramientas.

-   [**mofcomp**](mofcomp.md)

-   [**wmic**](wmic.md)

    La primera vez que ejecute Wmic después de la instalación del sistema, debe ejecutarse desde un símbolo del sistema con privilegios elevados. Es posible que el modo con privilegios elevados no sea necesario para las ejecuciones posteriores de Wmic a menos que las operaciones WMI requieran privilegios de administrador.

-   [**Winmgmt**](winmgmt.md)

-   [**wmiadap**](wmiadap.md)

Para ejecutar el [*control WMI*](gloss-w.md) (Wmimgmt.msc) y realizar cambios en la configuración de seguridad o auditoría del espacio de nombres WMI, la cuenta debe tener el derecho Editar seguridad concedido explícitamente o estar en el grupo Administradores local. La cuenta de administrador integrada también puede cambiar la seguridad o la auditoría de un espacio de nombres.

Wbemtest.exe, una herramienta de línea de comandos que no es compatible con los servicios de soporte al cliente de Microsoft, se puede ejecutar mediante cuentas que no están en el grupo de administradores local, a menos que una operación específica requiera privilegios que normalmente se conceden a las cuentas de administrador.

## <a name="handling-remote-connections-under-uac"></a>Control de conexiones remotas en UAC

Si se conecta a un equipo remoto en un dominio o en un grupo de trabajo, determina si se produce el filtrado de UAC.

Si el equipo forma parte de un dominio, conéctese al equipo de destino mediante una cuenta de dominio que se encuentra en el grupo administradores local del equipo remoto. A continuación, el filtrado de tokens de acceso de UAC no afectará a las cuentas de dominio del grupo administradores local. No use una cuenta local que no sea de dominio en el equipo remoto, incluso si la cuenta está en el grupo Administradores.

En un grupo de trabajo, la cuenta que se conecta al equipo remoto es un usuario local en ese equipo. Incluso si la cuenta está en el grupo Administradores, el filtrado de UAC significa que un script se ejecuta como un usuario estándar. Un procedimiento recomendado es crear un grupo de usuarios local dedicado o una cuenta de usuario en el equipo de destino específicamente para las conexiones remotas.

La seguridad debe ajustarse para poder usar esta cuenta porque la cuenta nunca ha tenido privilegios administrativos. Proporcionar al usuario local:

-   Derechos de inicio y activación remotos para acceder a DCOM. Para obtener más información, consulte [Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) (puede estar en inglés).
-   Derechos para acceder al espacio de nombres WMI de forma remota (Habilitación remota). Para obtener más información, vea [Acceso a espacios de nombres WMI.](access-to-wmi-namespaces.md)
-   Derecho para acceder al objeto protegible específico, en función de la seguridad requerida por el objeto.

Si usa una cuenta local, ya sea porque está en un grupo de trabajo o es una cuenta de equipo local, es posible que se le fue forzada a proporcionar tareas específicas a un usuario local. Por ejemplo, puede conceder al usuario el derecho de detener o iniciar un servicio específico mediante el comando SC.exe, los métodos [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-service) y [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-service) del servicio [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-service)o a través de directiva de grupo mediante Gpedit.msc. Es posible que algunos objetos protegibles no permitan que un usuario estándar realice tareas y no ofrezca ningún medio para modificar la seguridad predeterminada. En este caso, es posible que tenga que deshabilitar UAC para que la cuenta de usuario local no se filtre y, en su lugar, se convierta en un administrador completo. Tenga en cuenta que, por motivos de seguridad, deshabilitar UAC debe ser un último recurso.

No se recomienda deshabilitar UAC remoto cambiando la entrada del Registro que controla UAC remoto, pero puede ser necesario en un grupo de trabajo. La entrada del Registro es **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **sistema de directivas CurrentVersion** \\  \\  \\ **LocalAccountTokenFilterPolicy**. Cuando el valor de esta entrada es cero (0), se habilita el filtrado de tokens de acceso remoto de UAC. Cuando el valor es 1, el UAC remoto está deshabilitado.

## <a name="uac-effect-on-wmi-data-returned-to-scripts-or-applications"></a>Efecto de UAC en los datos WMI devueltos a scripts o aplicaciones

Si un script o aplicación se ejecuta en una cuenta del grupo Administradores, pero no se ejecuta con privilegios elevados, es posible que no obtenga todos los datos devueltos porque esta cuenta se ejecuta como un usuario estándar. Los [*proveedores*](gloss-p.md) WMI de algunas clases no devuelven todas las instancias a una cuenta de usuario estándar o a una cuenta de administrador que no se ejecuta como administrador completo debido al filtrado de UAC.

Las clases siguientes no devuelven algunas instancias cuando UAC filtra la cuenta:

-   [**Win32 \_ Bus**](/windows/desktop/CIMWin32Prov/win32-bus)
-   [**Impresora \_ Win32**](/windows/desktop/CIMWin32Prov/win32-printer)
-   [**ComponentCategory de Win32 \_**](/windows/desktop/CIMWin32Prov/win32-componentcategory)
-   [**LogicalProgramGroupItem de Win32 \_**](/windows/desktop/CIMWin32Prov/win32-logicalprogramgroupitem)
-   [**LogicalProgramGroup de Win32 \_**](/windows/desktop/CIMWin32Prov/win32-logicalprogramgroup)
-   [**Win32 \_ NetworkConnection**](/windows/desktop/CIMWin32Prov/win32-networkconnection)
-   [**UserAccount de Win32 \_**](/windows/desktop/CIMWin32Prov/win32-useraccount)
-   [**Win32 \_ PrinterDriver**](/windows/desktop/CIMWin32Prov/win32-printerdriver)
-   [**Win32 \_ PortResource**](/windows/desktop/CIMWin32Prov/win32-portresource)
-   [**Win32 \_ DeviceMemoryAddress**](/windows/desktop/CIMWin32Prov/win32-devicememoryaddress)

Las clases siguientes no devuelven algunas propiedades cuando UAC filtra la cuenta:

-   [**NetworkAdapterConfiguration de Win32 \_**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)
-   [**Win32 \_ DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)
-   [**DCOMApplication de Win32 \_**](/windows/desktop/CIMWin32Prov/win32-dcomapplication)
-   [**\_Placa base win32**](/windows/desktop/CIMWin32Prov/win32-baseboard)
-   [**Equipo \_ Win32System**](/windows/desktop/CIMWin32Prov/win32-computersystem)
-   [**NetworkAdapter de Win32 \_**](/windows/desktop/CIMWin32Prov/win32-networkadapter)
-   [**Win32 \_ Placa baseDispositivo**](/windows/desktop/CIMWin32Prov/win32-motherboarddevice)
-   [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive)
-   [**Win32 \_ PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)
-   [**Win32 \_ VideoController**](/windows/desktop/CIMWin32Prov/win32-videocontroller)
-   [**Win32 \_ ParallelPort**](/windows/desktop/CIMWin32Prov/win32-parallelport)
-   [**Disco lógico \_ win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)
-   [**Win32 \_ SystemDriver**](/windows/desktop/CIMWin32Prov/win32-systemdriver)
-   [**Win32 \_ IRQResource**](/windows/desktop/CIMWin32Prov/win32-irqresource)
-   [**Win32 \_ NetworkProtocol**](/windows/desktop/CIMWin32Prov/win32-networkprotocol)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de WMI](about-wmi.md)
</dt> <dt>

[Acceso a objetos protegibles wmi](access-to-wmi-securable-objects.md)
</dt> <dt>

[Cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 
