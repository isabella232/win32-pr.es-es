---
description: Al acceder a datos locales o remotos de WMI en una aplicación o script, puede encontrar errores que van desde las clases que faltan hasta el acceso denegado. Los proveedores también tienen disponibles opciones de depuración y clases de solución de problemas.
ms.assetid: b0aecdf6-ec30-49be-af4e-7eac5d124057
ms.tgt_platform: multiple
title: Solución de problemas de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58919617c663b52ffb840b3c3382b5707f0a305e
ms.sourcegitcommit: a3e96b6c9c6a3fb629e760dd6cc6327f9e4b62b6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/27/2021
ms.locfileid: "114714793"
---
# <a name="wmi-troubleshooting"></a>Solución de problemas de WMI

Al acceder a datos locales o remotos de WMI en una aplicación o script, puede encontrar errores que van desde las clases que faltan hasta el acceso denegado. Los proveedores también tienen disponibles opciones de depuración y clases de solución de problemas.

> [!Note]  
> La siguiente documentación está dirigida a desarrolladores y administradores de TI. Si es un usuario final que ha experimentado un mensaje de error relativo a WMI, debe ir [a Soporte técnico de Microsoft](https://support.microsoft.com/) y buscar el código de error que ve en el mensaje de error. Para obtener más información sobre cómo solucionar problemas con scripts WMI y el servicio WMI, vea [WMI isn't Working!](/previous-versions/tn-archive/ff406382(v=msdn.10))

 

## <a name="wmi-diagnosis-utility"></a>Utilidad de diagnóstico de WMI

La Utilidad de diagnóstico wmi (WMIDiag.exe) ya no se admite a partir de Windows 8 y Windows Server 2012.

**Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008: **

Si WMI devuelve mensajes de error, tenga en cuenta que es posible que no indiquen problemas en el servicio WMI o en proveedores WMI. Los errores pueden originarse en otras partes del sistema operativo y surgir como errores a través de WMI. En cualquier caso, no elimine el repositorio WMI como primera acción porque la eliminación del repositorio puede causar daños en el sistema o en las aplicaciones instaladas.

Para obtener más información sobre el origen del problema, puede descargar y ejecutar la herramienta Utilidad de diagnóstico de WMI [línea](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) de comandos de diagnóstico. Esta herramienta genera un informe que normalmente puede aislar el origen del problema y proporcionar instrucciones sobre cómo corregirlo. El informe también ayuda a los servicios de soporte técnico de Microsoft a ayudarle. Puede descargar el Utilidad de diagnóstico de WMI en el Centro [de descarga.](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d)

Los escritores de proveedores también pueden encontrar problemas de depuración a menos que esté escribiendo [*un proveedor desacoplado.*](gloss-d.md) Para obtener más información, vea [Proveedores de depuración.](debugging-providers.md)

## <a name="logging-and-tracing"></a>Registro y seguimiento

Los archivos de registro WMI ya no existen; Se reemplazaron por [seguimiento de eventos para Windows (ETW).](/windows/desktop/ETW/event-tracing-portal) Para obtener más información, vea [Actividad WMI de seguimiento](tracing-wmi-activity.md), Actividad WMI de [registro](logging-wmi-activity.md)y Archivos de [registro WMI](wmi-log-files.md).

## <a name="troubleshooting-in-scripts-and-applications"></a>Solución de problemas en scripts y aplicaciones

WMI contiene un conjunto de clases para solucionar problemas [de aplicaciones](wmi-troubleshooting-classes.md) cliente que usan proveedores WMI. Para obtener más información, vea [Solución de problemas de aplicaciones cliente WMI.](troubleshooting-wmi-client-applications.md)

## <a name="how-provider-writers-can-prevent-wmi-problems"></a>Cómo los escritores de proveedores pueden evitar problemas de WMI

Los escritores de proveedores pueden evitar muchos problemas, que aparecen en los mensajes de error a través de WMI, realizando las siguientes acciones:

-   Registrar el proveedor correctamente. Para obtener más información, [vea Registrar un proveedor.](registering-a-provider.md)
-   Agregar la [**\# instrucción pragma autorecover**](pragma-autorecover.md) al archivo Managed Object Format (MOF) que define las clases de proveedor.

Para obtener más información, vea [Proveedores de depuración](debugging-providers.md), Proporcionar datos [a WMI](providing-data-to-wmi.md)y Configuración del proveedor y Clases de solución [de problemas](provider-configuration-and-troubleshooting-classes.md).

## <a name="access-denied"></a>Acceso denegado

Los errores de acceso denegado que notifican los scripts y las aplicaciones que acceden a los espacios de nombres y los datos WMI generalmente se encuentran en tres categorías. En la tabla siguiente se enumeran las tres categorías de errores junto con los problemas que pueden provocar los errores y las posibles soluciones.



| Error                                                                                                                        | Posibles problemas                                                                                                                                                                                                                                                                                                                                                                     | Solución                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x800706BA `HRESULT_FROM_WIN32(RPC_S_SERVER_UNAVAILABLE)`<br/> Problema de firewall o servidor no disponible.<br/>      | El equipo realmente no existe o el firewall de Windows está bloqueando la conexión<br/>                                                                                                                                                                                                                                                                                        | Conectarse a Vista: **netsh advfirewall firewall set rule group="windows management instrumentation (wmi)" new enable=yes** Connecting to downlevel: Allow the "Remote Administration" rule in Windows Firewall.<br/>                                                                                                                                                                                                                                                                                                            |
| 0x80070005 **ACCESO DE E \_ \_ DENEGADO**<br/> Acceso denegado por la seguridad de DCOM.<br/>                                       | El usuario no tiene acceso remoto al equipo a través de DCOM. Normalmente, se producen errores DCOM al conectarse a un equipo remoto con una versión de sistema operativo diferente.<br/>                                                                                                                                                                                          | Conceder al usuario permisos de inicio remoto y activación remota en dcomcnfg. Haga clic con el botón Mi PC de > propiedades. En Seguridad COM, haga clic en "Editar límites" para ambas secciones. Dé al usuario que desea acceso remoto, inicio remoto y activación remota. A continuación, vaya a DCOM Config (Configuración de DCOM), busque "Windows Management Instrumentation" (Instrumentación de administración de recursos) y dé al usuario que desea que inicie y active de forma remota. Para obtener más información, vea [Conectarse entre diferentes sistemas operativos.](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)<br/> |
| 0x80041003 ACCESO **DE WBEM \_ E \_ \_ DENEGADO**<br/> Acceso denegado por un [ *proveedor*](gloss-p.md)<br/> | El usuario no tiene permiso para realizar la operación en WMI. Esto puede ocurrir cuando se consultan determinadas clases como un usuario con derechos bajos, pero lo más frecuente es que se intente invocar métodos o cambiar instancias de WMI como un usuario con derechos bajos. El espacio de nombres al que se conecta está cifrado y el usuario está intentando conectarse con una conexión sin cifrar.<br/> | Dé acceso al usuario con el control WMI (asegúrese de que el acceso remoto está establecido en true) Conectar un \_ cliente que admita el cifrado.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |



 

-   Normalmente, se producen errores DCOM al conectarse a un equipo remoto con una versión de sistema operativo diferente.

-   Los proveedores también pueden denegar el acceso a los datos en espacios de nombres específicos o pueden requerir ciertos niveles de seguridad de conexión. Para obtener más información, vea [Establecer la seguridad del proceso de aplicación cliente y](setting-client-application-process-security.md) el hospedaje y la seguridad del [proveedor.](provider-hosting-and-security.md)

-   Errores de acceso denegado desde los cambios del Firewall de conexión a Internet (ICF).

    Para obtener más información, vea [Conectarse a través de Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).

-   La seguridad de DCOM devuelve un error de acceso denegado cuando un cliente de baja integridad intenta acceder a WMI. Por ejemplo, un control ActiveX que se ejecuta en Internet Explorer, que tiene el nivel de seguridad establecido en bajo, no tiene acceso para realizar operaciones WMI locales.

    **Windows 7:** Los usuarios de baja integridad tienen permisos de solo lectura para las operaciones WMI locales.

## <a name="information-on-errors"></a>Información sobre errores

Cuando recibe un mensaje de error de WMI, puede encontrar el mensaje en Constantes de [**error wmi**](wmi-error-constants.md) o, para scripting, [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum). Sin embargo, la información proporcionada por el error por sí sola no suele ser suficiente para determinar lo que sucede. Los daños en el repositorio WMI pueden enmascarar como clases o instancias "no encontradas".

Para obtener más información sobre los errores de WMI:

-   Los registros WMI realiza un seguimiento de los eventos desde el núcleo wmi y desde los proveedores. Para obtener más información, vea [Registrar la actividad WMI](logging-wmi-activity.md).
-   Use las clases [de solución de problemas de WMI](wmi-troubleshooting-classes.md) para comprobar el estado interno de WMI o recibir notificaciones de eventos de proveedor o servicio WMI. Para obtener más información, vea [Clases de configuración y solución de](provider-configuration-and-troubleshooting-classes.md) problemas del proveedor y Solución de problemas de aplicaciones cliente [WMI.](troubleshooting-wmi-client-applications.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solución de problemas de WMI](wmi-troubleshooting.md)
</dt> <dt>

[Actividad WMI de seguimiento](tracing-wmi-activity.md)
</dt> <dt>

[Actividad WMI de registro](logging-wmi-activity.md)
</dt> </dl>

 

