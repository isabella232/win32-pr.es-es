---
description: Ya no se admiten los archivos de registro de WMI.
ms.assetid: 4ba80063-7aa6-42df-a620-1b366b795034
ms.tgt_platform: multiple
title: Registrar la actividad WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ced8645eb7ad9005e6ba751d011ae7f0ccb3dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697367"
---
# <a name="logging-wmi-activity"></a>Registrar la actividad WMI

Ya no se admiten los archivos de registro de WMI. A partir de Windows Vista, WMI utiliza el [seguimiento de eventos para Windows (ETW](/windows/desktop/ETW/event-tracing-portal)) y los eventos que están disponibles a través de la interfaz de usuario de **visor de eventos** o la herramienta de línea de comandos wevtutil. Para obtener más información, vea el proveedor ETW y la documentación de línea de comandos de [Wevutil](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732848(v=ws.11)) .

En este tema se describen las siguientes secciones:

-   [Archivos de registro de WMI antes de Windows Vista](#wmi-log-files-before-windows-vista)
-   [Actividades de registro para componentes principales de WMI antes de Windows Vista](#logging-activities-for-wmi-core-components-before-windows-vista)
-   [Actividades de registro para componentes de proveedor WMI antes de Windows Vista](#logging-activities-for-wmi-provider-components-before-windows-vista)
-   [Temas relacionados](#related-topics)

## <a name="wmi-log-files-before-windows-vista"></a>Archivos de registro de WMI antes de Windows Vista

Los archivos de registro creados por WMI y varios proveedores registran: eventos, datos de seguimiento o diagnósticos, errores y diversas actividades. Solo los administradores tienen acceso de lectura a la carpeta de registro de WMI que se encuentra en% WINDIR% \\ system32 \\ WBEM \\ logs.

Solo los componentes principales de WMI o los proveedores de WMI escriben en los archivos de registro. Solo puede leer o ver los datos de estos registros con fines de diagnóstico. Puede crear y almacenar sus propios archivos de registro en el directorio de registro de WMI.

## <a name="logging-activities-for-wmi-core-components-before-windows-vista"></a>Actividades de registro para componentes principales de WMI antes de Windows Vista

Estos archivos no contienen un formato coherente que sea adecuado para leer mediante programación. Para obtener más información acerca de registros específicos, consulte [archivos de registro de WMI](wmi-log-files.md).

Las actividades de registro de los componentes principales de WMI se producen cuando se establecen las siguientes claves del registro:

-   Nivel de registro

    Los cambios en el valor del registro del nivel de registro surten efecto inmediatamente. No es necesario reiniciar el servicio WMI.

    **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **Logging** = 2

    En la lista siguiente se enumeran los niveles de registro que se pueden definir en el registro.

    

    | Nivel de registro | Descripción               |
    |---------------|---------------------------|
    | 0             | Sin registro                |
    | 1             | Registrar solo errores           |
    | 2             | Registro detallado (predeterminado) |

    

     

-   Ubicación del archivo de registro

    Para que los cambios en la ubicación del archivo de registro surtan efecto, reinicie el servicio WMI.

    **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **Logging Directory** =% WINDIR% \\ system32 \\ WBEM \\ registros

-   Tamaño máximo del archivo de registro, en bytes

    **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **archivo de registro tamaño máximo** = 65536

Puede cambiar estos valores de clave del registro a través del editor del registro o mediante el complemento WMI de Microsoft Management Console.

**Para establecer el nivel de registro para WMI antes de Windows Vista**

1.  Haga clic en **Inicio** y, a continuación, haga clic en **Ejecutar**.
2.  Escriba **wmimgmt. msc**
3.  En el menú **Acción**, haga clic en **Propiedades**.
4.  En la pestaña **registro** , establezca el nivel de registro en **deshabilitado**, **habilitado** o **detallado**.
5.  En **Ubicación:**, escriba la ruta de acceso a la carpeta del archivo de registro y en **tamaño máximo (bytes):**, establezca el tamaño máximo, en bytes, del archivo de registro.

Para obtener más información acerca de cómo establecer las propiedades del archivo de registro, vea la ayuda en pantalla de la aplicación de control WMI.

## <a name="logging-activities-for-wmi-provider-components-before-windows-vista"></a>Actividades de registro para componentes de proveedor WMI antes de Windows Vista

Cuando está habilitado el registro de componentes principales de WMI, el registro también está habilitado para cualquier proveedor con capacidades de registro.

En la lista siguiente se enumeran los valores necesarios.

<dl> <dt>

<span id="File"></span><span id="file"></span><span id="FILE"></span>**Filesystem**
</dt> <dd>

Ruta de acceso completa y nombre de archivo del archivo de registro. El valor predeterminado es% WINDIR% \\ system32 \\ WBEM \\ logs. El **tipo** denominado Value debe establecerse en = file para que se use este valor con nombre.

</dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>**Dosis**
</dt> <dd>

Máscara lógica de 32 bits que define el tipo de resultado de depuración generado por el proveedor. Este valor depende del proveedor. El valor predeterminado es 0 (cero).

</dd> <dt>

<span id="MaxFileSize"></span><span id="maxfilesize"></span><span id="MAXFILESIZE"></span>**MaxFileSize**
</dt> <dd>

Tamaño máximo de archivo, en bytes, del archivo de registro. Este valor entero debe estar en el intervalo de 1024 a 2 ^ 32-1. Cuando el tamaño del archivo supera este valor, se cambia el nombre del archivo a **~ filename** y se crea un nuevo archivo de registro vacío. El espacio en disco necesario para el archivo de registro es dos veces el valor de **maxfilesize**. El valor predeterminado es 65.535.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Automáticamente**
</dt> <dd>

Se puede establecer en = File o = Debugger. Si se establece en = File, la información de seguimiento se escribe en el archivo de registro especificado en el **archivo** denominado Value. El valor predeterminado es = archivo.

</dd> </dl>

Por ejemplo, para registrar consultas y obtener llamadas de instancia desde el proveedor de vistas, use los siguientes valores de clave del registro. El registro se ubicará en la carpeta de registro y tendrá el tamaño de archivo predeterminado.

**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **providers** \\ **Logging** \\ **ViewProvider** \\ **File** = C: \\ Windows \\ system32 \\ WBEM \\ logs \\ ViewProvider. log

**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **providers** \\ **Logging** \\ **ViewProvider** \\ **LEVEL** = 2

**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **providers** \\ **Logging** \\ **ViewProvider** \\ **maxfilesize** = 65535

**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **providers** \\ **Logging** \\ **ViewProvider** \\ **Type** = File

> [!Note]  
> Para sus propios proveedores con capacidades de registro, debe escribir las claves y los valores del registro necesarios para habilitar el registro.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solución de problemas de WMI](wmi-troubleshooting.md)
</dt> <dt>

[Archivos de registro de WMI](wmi-log-files.md)
</dt> <dt>

[Clases de solución de problemas de WMI](wmi-troubleshooting-classes.md)
</dt> <dt>

[Seguimiento de la actividad WMI](tracing-wmi-activity.md)
</dt> </dl>

 

 
