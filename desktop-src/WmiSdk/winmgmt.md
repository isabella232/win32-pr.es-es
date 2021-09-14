---
description: Winmgmt es el servicio WMI dentro del proceso SVCHOST que se ejecuta en &\# 0034; LocalSystem&\# 0034; cuenta.
ms.assetid: 3923322a-3acb-407e-8a07-09c59d252e8b
ms.tgt_platform: multiple
title: Winmgmt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- winmgmt
api_type:
- NA
api_location: ''
ms.openlocfilehash: d28d37faf454accd91281034d0aeb8df5e10dddb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359212"
---
# <a name="winmgmt"></a>Winmgmt

Winmgmt es el servicio WMI dentro del proceso SVCHOST que se ejecuta en la cuenta "LocalSystem".

En todos los casos, el servicio WMI se inicia automáticamente cuando la primera aplicación de administración o script solicita la conexión a un espacio de nombres WMI. Para más información, vea [Inicio y detención del servicio WMI](starting-and-stopping-the-wmi-service.md).

> [!Note]  
> WMI es un componente básico del sistema operativo Windows que permite a los desarrolladores y administradores de TI escribir scripts y aplicaciones para automatizar ciertas tareas. Winmgmt.exe es el servicio que permite que WMI se ejecute en el equipo local. Para obtener más información sobre el uso de WMI, vea [Usar WMI.](using-wmi.md) Si ha recibido un mensaje de error relacionado con winmgmt.exe, vea [Solución de problemas de WMI.](wmi-troubleshooting.md) Para obtener más información sobre Winmgmt.exe, vea [Using WMI Management Tools](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).

 

Cuando se ejecuta desde el símbolo del sistema, el servicio WMI tiene los modificadores siguientes.

``` syntax
winmgmt 
  [/backup <filename>] 
  [/restore <filename> <mode>] 
  [/resyncperf <winmgmt service process id>] 
  [/standalonehost <level>]
  [/sharedhost]
  [/verifyrepository <path>]
  [/salvagerepository] 
  [/resetrepository]
```

## <a name="switches"></a>Conmutadores

<dl> <dt>

<span id="__________backup__filename_________"></span><span id="__________BACKUP__FILENAME_________"></span>**/backup** *&lt; filename &gt;* 
</dt> <dd>

Hace que WMI hace una copia de seguridad del repositorio en el nombre de archivo especificado. El *argumento filename* debe contener la ruta de acceso completa a la ubicación del archivo. Este proceso requiere un bloqueo de escritura en el repositorio para que las operaciones de escritura en el repositorio se suspendan hasta que se complete el proceso de copia de seguridad.

Si no especifica una ruta de acceso para el archivo, se coloca en el directorio %Windir% \\ System32.

</dd> <dt>

<span id="__________restore__filename____flag_____"></span><span id="__________RESTORE__FILENAME____FLAG_____"></span>**/restore** *&lt; filename &gt;* *&lt; flag &gt;* 
</dt> <dd>

Restaura manualmente el repositorio WMI desde el archivo de copia de seguridad especificado. El *argumento filename* debe contener la ruta de acceso completa a la ubicación del archivo de copia de seguridad. Para realizar la operación de restauración, WMI guarda el repositorio existente para que se reescriba si se produce un error en la operación. A continuación, el repositorio se restaura a partir del archivo de copia de seguridad especificado en el argumento *filename.* Si no se puede lograr el acceso exclusivo al repositorio, los clientes existentes se desconectan de WMI.

El *argumento de* marca debe ser 1 (forzar la desconexión de usuarios y restauración) o 0 (restauración predeterminada si no hay usuarios conectados) y especifica el modo de restauración.

</dd> <dt>

<span id="__________resyncperf__winmgmt-service-process-id_____"></span><span id="__________RESYNCPERF__WINMGMT-SERVICE-PROCESS-ID_____"></span>**/resyncperf** *&lt; winmgmt-service-process-id &gt;* 
</dt> <dd>

Registra las bibliotecas de rendimiento del equipo con WMI. EL PID de WMI es el identificador de proceso para el servicio WMI.

Solo es necesario si las clases del monitor de rendimiento no devuelven resultados confiables.

</dd> <dt>

<span id="_standalonehost__level_"></span><span id="_STANDALONEHOST__LEVEL_"></span>**/standalonehost** \[ *&lt; level &gt;*\]
</dt> <dd>

Mueve el servicio Winmgmt a un proceso Svchost independiente que tiene un punto de conexión DCOM fijo. El punto de conexión predeterminado es "ncacn \_ ip \_ tcp.0.24158". Sin embargo, el punto de conexión se puede cambiar mediante la ejecución Dcomcnfg.exe. Para obtener más información sobre cómo configurar un puerto fijo para WMI, vea [Configurar un puerto fijo para WMI.](setting-up-a-fixed-port-for-wmi.md)

El *argumento level* es el nivel de autenticación para el proceso svchost. WMI normalmente se ejecuta como parte de un host de servicio compartido y no se puede aumentar el nivel de autenticación solo para WMI. Si *no* se especifica level, el valor predeterminado es 4 **(RPC C \_ \_ AUTHN \_ LEVEL \_ PKT** o **WbemAuthenticationLevelPkt**).

Puede ejecutar WMI de forma más segura si aumenta el nivel de autenticación a Privacidad de paquetes **(RPC \_ C \_ \_ \_ AUTHN LEVEL PKT \_ PRIVACY** o **WbemAuthenticationLevelPktPrivacy).** Los niveles de autenticación para Visual Basic y scripting se describen [**en WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum). Para C++, vea [Establecer el nivel de seguridad de proceso predeterminado mediante C++.](setting-the-default-process-security-level-using-c-.md) Para obtener más información, vea [Mantenimiento de la seguridad WMI.](maintaining-wmi-security.md)

</dd> <dt>

<span id="_sharedhost"></span><span id="_SHAREDHOST"></span>**/sharedhost**
</dt> <dd>

Mueve el servicio Winmgmt al proceso svchost compartido.

</dd> <dt>

<span id="__________verifyrepository__path_____"></span><span id="__________VERIFYREPOSITORY__PATH_____"></span>**/verifyrepository** *&lt; path &gt;* 
</dt> <dd>

Realiza una comprobación de coherencia en el repositorio WMI. Al agregar el modificador *&lt; &gt;* **/verifyrepository** sin el argumento de ruta de acceso, se comprueba el repositorio en directo usado actualmente por WMI. Al especificar el argumento *de ruta* de acceso, puede comprobar cualquier copia guardada del repositorio. En este caso, el argumento path debe contener la ruta de acceso completa a la copia del repositorio guardada. El repositorio guardado debe ser una copia de toda la carpeta del repositorio. Para obtener más información sobre los errores devueltos por este comando, vea la sección Comentarios.

</dd> <dt>

<span id="_salvagerepository"></span><span id="_SALVAGEREPOSITORY"></span>**/salvagerepository**
</dt> <dd>

Realiza una comprobación de coherencia en el repositorio WMI y, si se detecta una incoherencia, vuelve a generar el repositorio. El contenido del repositorio incoherente se combina en el repositorio creado, si se puede leer. La operación de recuperación siempre funciona con el repositorio que el servicio WMI está usando actualmente. Para obtener más información sobre los errores devueltos por este comando, vea la sección Comentarios.

% de archivos MOF que contienen la instrucción de preprocesador [**\# pragma autorecover**](pragma-autorecover.md) se restauran en el repositorio.

</dd> <dt>

<span id="_resetrepository"></span><span id="_RESETREPOSITORY"></span>**/resetrepository**
</dt> <dd>

El repositorio se restablece al estado inicial cuando se instala por primera vez el sistema operativo. Los archivos MOF que contienen la instrucción de preprocesador [**\# pragma autorecover**](pragma-autorecover.md) se restauran en el repositorio.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta herramienta se encuentra en el directorio wbem %Windir% \\ \\ System32. Para obtener una lista de los modificadores disponibles, escriba `WinMgmt /?` en el símbolo del sistema.

El repositorio WMI, también conocido como repositorio CIM, no es solo un único archivo, sino una colección de archivos dentro de la carpeta Repositorio que funcionan conjuntamente como una base de datos. Cuando se usa el modificador **/backup** para realizar una copia de seguridad del repositorio, la copia de seguridad resultante es un único archivo comprimido.

WMI devuelve el error **ERROR \_ INTERNAL DB \_ \_ CORRUPTION** (net helpmsg 1358) si una operación de comprobación indica que el repositorio no está en un estado coherente. Este error se puede devolver desde cualquier comando que realice la comprobación del repositorio, como **/verifyrepository** o **/salvagerepository**.

> [!Note]
>
> Si WMI devuelve mensajes de error, tenga en cuenta que es posible que no indiquen problemas en el servicio WMI o en proveedores WMI. Los errores pueden originarse en otras partes del sistema operativo y surgir como errores a través de WMI. En cualquier caso, no elimine el repositorio WMI como primera acción porque la eliminación del repositorio puede causar daños en el sistema o en las aplicaciones instaladas.
>
> Para obtener más información sobre el origen del problema, descargue y ejecute la Utilidad de diagnóstico de WMI [línea](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) de comandos de diagnóstico. Esta herramienta genera un informe que normalmente puede aislar el origen del problema y proporcionar instrucciones sobre cómo corregirlo. El informe también ayuda a los servicios de soporte técnico de Microsoft a ayudarle. Puede descargar el [Utilidad de diagnóstico de WMI](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Solución de problemas de WMI](wmi-troubleshooting.md)
</dt> <dt>

[Conectarse a WMI de forma remota a partir de Vista](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> </dl>

 

