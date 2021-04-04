---
description: Al tener acceso a los datos locales o remotos de WMI en una aplicación o un script, pueden producirse errores entre las clases que faltan y el acceso denegado. Los proveedores también tienen opciones de depuración y clases de solución de problemas disponibles.
ms.assetid: b0aecdf6-ec30-49be-af4e-7eac5d124057
ms.tgt_platform: multiple
title: Solución de problemas de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ccb8afa1af64e6eb80050c96973a9ad9456a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908669"
---
# <a name="wmi-troubleshooting"></a>Solución de problemas de WMI

Al tener acceso a los datos locales o remotos de WMI en una aplicación o un script, pueden producirse errores entre las clases que faltan y el acceso denegado. Los proveedores también tienen opciones de depuración y clases de solución de problemas disponibles.

> [!Note]  
> La siguiente documentación está dirigida a desarrolladores y administradores de ti. Si es un usuario final que ha experimentado un mensaje de error relacionado con WMI, debe ir a [soporte técnico de Microsoft](https://support.microsoft.com/) y buscar el código de error que aparece en el mensaje de error. Para obtener más información acerca de la solución de problemas con los scripts WMI y el servicio WMI, vea [WMI no funciona.](/previous-versions/tn-archive/ff406382(v=msdn.10))

 

## <a name="wmi-diagnosis-utility"></a>Utilidad de diagnóstico de WMI

La utilidad de diagnóstico de WMI (WMIDiag.exe) ya no se admite a partir de Windows 8 y Windows Server 2012.

* * Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008: * *

Si WMI devuelve mensajes de error, tenga en cuenta que es posible que no indiquen problemas en el servicio WMI o en los proveedores WMI. Los errores pueden originarse en otras partes del sistema operativo y surgir como errores a través de WMI. En cualquier circunstancia, no elimine el repositorio WMI como primera acción, ya que la eliminación del repositorio puede provocar daños en el sistema o en las aplicaciones instaladas.

Para obtener más información sobre el origen del problema, puede descargar y ejecutar la herramienta de línea de comandos de diagnóstico de [utilidad de diagnóstico de WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) . Esta herramienta genera un informe que normalmente puede aislar el origen del problema y proporcionar instrucciones sobre cómo corregirlo. El informe también ayuda a los servicios de soporte técnico de Microsoft para ayudarle. Puede descargar el Utilidad de diagnóstico de WMI en el [centro de descarga](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).

Los escritores de proveedores también pueden encontrar problemas de depuración, a menos que esté escribiendo un [*proveedor desacoplado*](gloss-d.md). Para obtener más información, vea [depuración de proveedores](debugging-providers.md).

## <a name="logging-and-tracing"></a>Registro y seguimiento

Los archivos de registro de WMI ya no existen; se reemplazaron por [seguimiento de eventos para Windows (ETW)](/windows/desktop/ETW/event-tracing-portal). Para obtener más información, vea seguimiento de la [actividad WMI](tracing-wmi-activity.md), registro de la [actividad WMI](logging-wmi-activity.md)y [archivos de registro WMI](wmi-log-files.md).

## <a name="troubleshooting-in-scripts-and-applications"></a>Solución de problemas en scripts y aplicaciones

WMI contiene un conjunto de clases para [solucionar problemas](wmi-troubleshooting-classes.md) de las aplicaciones cliente que utilizan proveedores WMI. Para obtener más información, consulte [solución de problemas de aplicaciones cliente WMI](troubleshooting-wmi-client-applications.md).

## <a name="how-provider-writers-can-prevent-wmi-problems"></a>Cómo los escritores de proveedores pueden evitar problemas de WMI

Los escritores de proveedores pueden impedir muchos problemas, que aparecen en los mensajes de error a través de WMI, mediante la realización de las siguientes acciones:

-   Registrando el proveedor correctamente. Para obtener más información, vea [registrar un proveedor](registering-a-provider.md).
-   Agregar la instrucción [**\# pragma de Autorrecuperación**](pragma-autorecover.md) al archivo Managed Object Format (MOF) que define las clases de proveedor.

Para obtener más información, vea [depuración de proveedores](debugging-providers.md), [proporcionar datos a WMI](providing-data-to-wmi.md)y [clases de solución de problemas y configuración del proveedor](provider-configuration-and-troubleshooting-classes.md).

## <a name="access-denied"></a>Acceso denegado

Los errores de acceso denegado que informan los scripts y las aplicaciones que tienen acceso a los espacios de nombres y datos de WMI generalmente se dividen en tres categorías. En la tabla siguiente se enumeran las tres categorías de errores junto con los problemas que pueden provocar los errores y las posibles soluciones.



| Error                                                                                                                        | Posibles problemas                                                                                                                                                                                                                                                                                                                                                                     | Solución                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x800706BA `HRESULT_FROM_WIN32(RPC_S_SERVER_UNAVAILABLE)`<br/> Problema de firewall o servidor no disponible.<br/>      | El equipo no existe realmente, el Firewall de Windows está bloqueando la conexión<br/>                                                                                                                                                                                                                                                                                        | Conexión a vista: **netsh advfirewall firewall set Rule Group = "instrumental de administración de Windows (WMI)" New enable = Yes** conectándose a Downlevel: permitir la regla "administración remota" en firewall de Windows.<br/>                                                                                                                                                                                                                                                                                                            |
| 0x80070005 **E \_ acceso \_ denegado**<br/> Acceso denegado por la seguridad de DCOM.<br/>                                       | El usuario no tiene acceso remoto al equipo a través de DCOM. Normalmente, se producen errores de DCOM al conectarse a un equipo remoto con una versión de sistema operativo diferente.<br/>                                                                                                                                                                                          | Conceda al usuario permisos de inicio remoto y activación remota en DCOMCNFG. Haga clic con el botón secundario en Mi PC > propiedades. En seguridad COM, haga clic en "editar límites" para ambas secciones. Conceda al usuario que desea acceso remoto, inicio remoto y activación remota. A continuación, vaya a configuración de DCOM, busque "Instrumental de administración de Windows" y proporcione al usuario el inicio remoto y la activación remota. Para obtener más información, consulte [conexión entre diferentes sistemas operativos](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)<br/> |
| 0x80041003 **WBEM \_ E \_ acceso \_ denegado**<br/> Acceso denegado por un [ *proveedor*](gloss-p.md)<br/> | El usuario no tiene permiso para realizar la operación en WMI. Esto puede ocurrir cuando se consultan determinadas clases como un usuario con derechos reducidos, pero suele ocurrir cuando se intenta invocar métodos o cambiar instancias de WMI como un usuario con derechos reducidos. El espacio de nombres al que se está conectando está cifrado y el usuario está intentando conectarse con una conexión sin cifrar<br/> | Conceda al usuario acceso con el control WMI (Asegúrese de que tiene \_ acceso remoto establecido en true) conectarse mediante un cliente que admita el cifrado.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |



 

-   Normalmente, se producen errores de DCOM al conectarse a un equipo remoto con una versión de sistema operativo diferente.

-   Los proveedores también pueden denegar el acceso a los datos de espacios de nombres específicos o pueden requerir ciertos niveles de seguridad de conexión. Para obtener más información, vea establecer la seguridad del proceso de la [aplicación cliente](setting-client-application-process-security.md) y el [hospedaje y la seguridad del proveedor](provider-hosting-and-security.md).

-   Errores de acceso denegado de los cambios de Firewall de conexión a Internet (ICF).

    Para obtener más información, consulte [conectarse a través de Firewall de Windows](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).

-   La seguridad de DCOM devuelve un error de acceso denegado cuando un cliente de baja integridad intenta tener acceso a WMI. Por ejemplo, un control ActiveX que se ejecuta en Internet Explorer, que tiene el nivel de seguridad establecido en Low, no tiene acceso para realizar operaciones WMI locales.

    **Windows 7:** Los usuarios de baja integridad tienen permisos de solo lectura para las operaciones WMI locales.

## <a name="information-on-errors"></a>Información sobre errores

Cuando recibe un mensaje de error de WMI, puede buscar el mensaje en [**constantes de error de WMI**](wmi-error-constants.md) o, para scripting, [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum). Sin embargo, la información proporcionada por el error por sí solo es insuficiente para determinar lo que está ocurriendo. Los daños en el repositorio WMI se pueden enmascarar como clases o instancias "no encontrado".

Para obtener más información acerca de los errores de WMI:

-   WMI registra los eventos de seguimiento desde dentro del núcleo de WMI y de los proveedores. Para obtener más información, vea [registrar la actividad WMI](logging-wmi-activity.md).
-   Utilice las [clases de solución de problemas de WMI](wmi-troubleshooting-classes.md) para comprobar el estado interno de WMI o recibir notificaciones de eventos del proveedor o del servicio WMI. Para obtener más información, vea [configuración del proveedor y solución de problemas](provider-configuration-and-troubleshooting-classes.md) de las [aplicaciones cliente WMI](troubleshooting-wmi-client-applications.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solución de problemas de WMI](wmi-troubleshooting.md)
</dt> <dt>

[Seguimiento de la actividad WMI](tracing-wmi-activity.md)
</dt> <dt>

[Registrar la actividad WMI](logging-wmi-activity.md)
</dt> </dl>

 

