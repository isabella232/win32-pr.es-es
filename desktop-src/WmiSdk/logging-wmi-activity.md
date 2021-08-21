---
description: Ya no se admiten los archivos de registro WMI.
ms.assetid: 4ba80063-7aa6-42df-a620-1b366b795034
ms.tgt_platform: multiple
title: Actividad WMI de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f578702636f68959f2ca1bc03a00c39d3234d5b3136099226cfe98013409a15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992935"
---
# <a name="logging-wmi-activity"></a>Actividad WMI de registro

Ya no se admiten los archivos de registro WMI. A partir de Windows Vista, WMI usa seguimiento de eventos para [Windows (ETW)](/windows/desktop/ETW/event-tracing-portal)y eventos que están disponibles a través de la interfaz de usuario de **Visor de eventos** o la herramienta de línea de comandos Wevtutil. Para obtener más información, vea el proveedor ETW y la documentación de la línea de comandos de [Wevutil.](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732848(v=ws.11))

En este tema se de abordan las secciones siguientes:

-   [Archivos de registro WMI antes de Windows Vista](#wmi-log-files-before-windows-vista)
-   [Registrar actividades para los componentes principales de WMI antes de Windows Vista](#logging-activities-for-wmi-core-components-before-windows-vista)
-   [Registrar actividades para componentes del proveedor WMI antes de Windows Vista](#logging-activities-for-wmi-provider-components-before-windows-vista)
-   [Temas relacionados](#related-topics)

## <a name="wmi-log-files-before-windows-vista"></a>Archivos de registro WMI antes de Windows Vista

Los archivos de registro creados por WMI y varios proveedores registran: eventos, datos de seguimiento o diagnóstico, errores y diversas actividades. Solo los administradores tienen acceso de lectura a la carpeta de registro wmi que se encuentra en %windir% \\ system32 \\ wbem \\ logs.

Solo los componentes principales de WMI o los proveedores WMI escriben en los archivos de registro. Solo puede leer o ver los datos de estos registros con fines de diagnóstico. Puede crear y almacenar sus propios archivos de registro en el directorio de registro wmi.

## <a name="logging-activities-for-wmi-core-components-before-windows-vista"></a>Registrar actividades para componentes principales de WMI antes de Windows Vista

Estos archivos no contienen un formato coherente que sea adecuado para leer mediante programación. Para obtener más información sobre registros específicos, vea [Archivos de registro WMI.](wmi-log-files.md)

Las actividades de registro de los componentes principales de WMI se producen cuando se establecen las siguientes claves del Registro:

-   Nivel de registro

    Los cambios en el valor del Registro de nivel de registro se a vigor inmediatamente. No es necesario reiniciar el servicio WMI.

    **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **Logging** = 2

    En la lista siguiente se enumeran los niveles de registro que se pueden definir en el Registro.

    

    | Nivel de registro | Descripción               |
    |---------------|---------------------------|
    | 0             | Sin registro                |
    | 1             | Errores de solo registro           |
    | 2             | Registro detallado (valor predeterminado) |

    

     

-   Ubicación del archivo de registro

    Para que los cambios en la ubicación del archivo de registro sumen efecto, reinicie el servicio WMI.

    **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **Logging Directory** = %windir% \\ system32 \\ wbem \\ logs

-   Tamaño máximo del archivo de registro, en bytes

    **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** Log File Max \\ **Size** = 65536

Puede cambiar estos valores de clave del Registro a través del Editor del Registro o del complemento WMI para el Microsoft Management Console.

**Para establecer el nivel de registro de WMI antes de Windows Vista**

1.  Haga clic en **Inicio** y, a continuación, haga clic en **Ejecutar**.
2.  Escriba **wmimgmt.msc.**
3.  En el menú **Acción**, haga clic en **Propiedades**.
4.  En la **pestaña Registro,** establezca el nivel de registro en **Deshabilitado,** **Habilitado** o **Detallado.**
5.  En **Ubicación:**, escriba la ruta de acceso a la carpeta del archivo de registro y, en Tamaño máximo **(bytes):**, establezca el tamaño máximo, en bytes, del archivo de registro.

Para obtener más información sobre cómo establecer las propiedades del archivo de registro, vea la Ayuda en línea de la aplicación control WMI.

## <a name="logging-activities-for-wmi-provider-components-before-windows-vista"></a>Registrar actividades para componentes del proveedor WMI antes de Windows Vista

Cuando el registro de los componentes principales de WMI está habilitado, también se habilita el registro para cualquier proveedor con funcionalidades de registro.

En la lista siguiente se enumeran los valores necesarios.

<dl> <dt>

<span id="File"></span><span id="file"></span><span id="FILE"></span>**Archivo**
</dt> <dd>

Ruta de acceso completa y nombre de archivo del archivo de registro. El valor predeterminado es %windir% \\ system32 \\ wbem \\ logs. El **valor** type con nombre debe establecerse en = File para que se utilice este valor con nombre.

</dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>**Nivel**
</dt> <dd>

Máscara lógica de 32 bits que define el tipo de salida de depuración generado por el proveedor. Este valor depende del proveedor. El valor predeterminado es 0 (cero).

</dd> <dt>

<span id="MaxFileSize"></span><span id="maxfilesize"></span><span id="MAXFILESIZE"></span>**MaxFileSize**
</dt> <dd>

Tamaño máximo del archivo, en bytes, del archivo de registro. Este valor entero debe estar entre 1024 y 2^32-1. Cuando el tamaño del archivo supera este valor, se cambia el nombre del archivo a **~filename** y se crea un nuevo archivo de registro vacío. El espacio en disco necesario para el archivo de registro es el doble del valor de **MaxFileSize.** El valor predeterminado es 65 535.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Tipo**
</dt> <dd>

Se puede establecer en = Archivo o = Depurador. Si se establece en = Archivo, la información de seguimiento se escribe en el archivo de registro especificado en **el valor De** archivo con nombre. El valor predeterminado es = Archivo.

</dd> </dl>

Por ejemplo, para registrar la consulta y obtener llamadas de instancia del proveedor de vistas, use los siguientes valores de clave del Registro. El registro se ubicará en la carpeta de registro y será el tamaño de archivo predeterminado.

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **PROVIDERS** \\ **Logging** \\ **ViewProvider** \\ **File** = C: Windows \\ \\ system32 \\ WBEM Logs \\ \\ ViewProvider.log

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **PROVIDERS** \\ **Logging** \\ **View** \\ **Level** = 2

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **PROVIDERS** \\ **Logging** \\ **ViewProvider** \\ **MaxFileSize** = 65535

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **PROVIDERS** \\ **Logging** \\ **View Tipo de** \\ **proveedor** = Archivo

> [!Note]  
> Para sus propios proveedores con funcionalidades de registro, debe escribir los valores y las claves del Registro necesarios para habilitar el registro.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solución de problemas de WMI](wmi-troubleshooting.md)
</dt> <dt>

[Archivos de registro WMI](wmi-log-files.md)
</dt> <dt>

[Clases de solución de problemas de WMI](wmi-troubleshooting-classes.md)
</dt> <dt>

[Actividad WMI de seguimiento](tracing-wmi-activity.md)
</dt> </dl>

 

 
