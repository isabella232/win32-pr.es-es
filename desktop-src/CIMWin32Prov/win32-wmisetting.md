---
description: La \_ clase WMI WMISetting singleton de Win32 contiene los parámetros operativos para el servicio WMI. Esta clase solo puede tener una instancia, que siempre existe para cada sistema de Windows y no se puede eliminar. No se pueden crear instancias adicionales.
ms.assetid: d33cd4f3-969b-46ce-baff-466f1a464906
ms.tgt_platform: multiple
title: Win32_WMISetting (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_WMISetting
- Win32_WMISetting.Caption
- Win32_WMISetting.Description
- Win32_WMISetting.SettingID
- Win32_WMISetting.ASPScriptDefaultNamespace
- Win32_WMISetting.ASPScriptEnabled
- Win32_WMISetting.AutorecoverMofs
- Win32_WMISetting.AutoStartWin9X
- Win32_WMISetting.BackupInterval
- Win32_WMISetting.BackupLastTime
- Win32_WMISetting.BuildVersion
- Win32_WMISetting.DatabaseDirectory
- Win32_WMISetting.DatabaseMaxSize
- Win32_WMISetting.EnableAnonWin9xConnections
- Win32_WMISetting.EnableEvents
- Win32_WMISetting.EnableStartupHeapPreallocation
- Win32_WMISetting.HighThresholdOnClientObjects
- Win32_WMISetting.HighThresholdOnEvents
- Win32_WMISetting.InstallationDirectory
- Win32_WMISetting.LastStartupHeapPreallocation
- Win32_WMISetting.LoggingDirectory
- Win32_WMISetting.LoggingLevel
- Win32_WMISetting.LowThresholdOnClientObjects
- Win32_WMISetting.LowThresholdOnEvents
- Win32_WMISetting.MaxLogFileSize
- Win32_WMISetting.MaxWaitOnClientObjects
- Win32_WMISetting.MaxWaitOnEvents
- Win32_WMISetting.MofSelfInstallDirectory
api_type:
- DllExport
api_location:
- Wbemcore.dll
ms.openlocfilehash: 8f94524d18074e3a35c7bcad09e9b9fba80e8470
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907007"
---
# <a name="win32_wmisetting-class"></a>\_Clase Win32 WMISetting

La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ WMISetting** singleton de Win32 contiene los parámetros operativos para el servicio WMI. Esta clase solo puede tener una instancia, que siempre existe para cada sistema de Windows y no se puede eliminar. No se pueden crear instancias adicionales.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Singleton, Dynamic, Provider("WBEMCORE"), UUID("{A83EF166-CA8D-11d2-B33D-00104BCC4B4A}"), AMENDMENT]
class Win32_WMISetting : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  string   ASPScriptDefaultNamespace = "\\\\root\\cimv2";
  boolean  ASPScriptEnabled;
  string   AutorecoverMofs[];
  uint32   AutoStartWin9X;
  uint32   BackupInterval;
  datetime BackupLastTime;
  string   BuildVersion;
  string   DatabaseDirectory;
  uint32   DatabaseMaxSize;
  boolean  EnableAnonWin9xConnections;
  boolean  EnableEvents;
  boolean  EnableStartupHeapPreallocation;
  uint32   HighThresholdOnClientObjects;
  uint32   HighThresholdOnEvents;
  string   InstallationDirectory;
  uint32   LastStartupHeapPreallocation;
  string   LoggingDirectory;
  uint32   LoggingLevel;
  uint32   LowThresholdOnClientObjects;
  uint32   LowThresholdOnEvents;
  uint32   MaxLogFileSize;
  uint32   MaxWaitOnClientObjects;
  uint32   MaxWaitOnEvents;
  string   MofSelfInstallDirectory;
};
```

## <a name="members"></a>Miembros

La **clase \_ WMISetting de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ WMISetting de Win32** tiene estas propiedades.

<dl> <dt>

**ASPScriptDefaultNamespace**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ scripting \| default namespace")
</dt> </dl>

Espacio de nombres de script predeterminado. Esta propiedad contiene el espacio de nombres utilizado por las llamadas de la API de scripting para WMI si no se especifica ninguno en el autor de la llamada.

Esta propiedad refleja el valor de la clave del registro.

**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **scripting \| default namespace**    

Ejemplo: raíz \\ cimv2

Para ver un script de ejemplo que usa esta propiedad, vea la sección Comentarios.

</dd> <dt>

**ASPScriptEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ scripting \| enable for ASP")
</dt> </dl>

Si **es true**, el scripting de WMI puede usarse en páginas de Active Server (ASP). Esta propiedad es válida en sistemas que solo ejecutan versiones no compatibles de Windows. En el caso de los sistemas Windows compatibles, el scripting de WMI siempre se permite en ASP.

</dd> <dt>

**AutorecoverMofs**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| software Win32Registry \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| autocover MOF")
</dt> </dl>

Lista de nombres de archivo MOF completos que se usan para inicializar o recuperar el repositorio WMI. La lista determina el orden en que se compilan los archivos MOF.

Esta propiedad refleja el valor de la clave del registro.

**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| autocover MOF**    

</dd> <dt>

**AutoStartWin9X**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| AutostartWin9X")
</dt> </dl>

No se admite.

<dt>

<span id="Don_t_start"></span><span id="don_t_start"></span><span id="DON_T_START"></span>

**No iniciar** (0)


</dt> <dd></dd> <dt>

<span id="Autostart"></span><span id="autostart"></span><span id="AUTOSTART"></span>

**Inicio automático** (1)


</dt> <dd></dd> <dt>

<span id="Start_on_reboot"></span><span id="start_on_reboot"></span><span id="START_ON_REBOOT"></span>

**Iniciar al reiniciar** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**BackupInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Backup Interval Threshold"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")
</dt> </dl>

No se admite. En su lugar, realice una copia de seguridad manual del repositorio WMI.

</dd> <dt>

**BackupLastTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Time Functions \| GetTimeZoneInformation")
</dt> </dl>

Fecha y hora en que se realizó la última copia de seguridad.

</dd> <dt>

**BuildVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \| Build")
</dt> </dl>

Información de versión para el servicio WMI instalado actualmente.

Período de tiempo que transcurre entre las copias de seguridad de la base de datos WMI.

Esta propiedad refleja el valor de la clave del registro.

**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM \| Build**

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descripción textual del objeto actual.

Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).

</dd> <dt>

**DatabaseDirectory**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| repository Directory")
</dt> </dl>

Ruta de acceso al directorio que contiene el repositorio WMI.

</dd> <dt>

**DatabaseMaxSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("software de Win32Registry \| \\ \\ \\ \\ de Microsoft WBEM \\ \\ CIMOM \| Max dB size"), [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")
</dt> </dl>

Tamaño máximo del repositorio WMI.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción textual del objeto actual.

Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).

</dd> <dt>

**EnableAnonWin9xConnections**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableAnonConnections")
</dt> </dl>

No se admite.

</dd> <dt>

**EnableEvents**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| software Win32Registry \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableEvents")
</dt> </dl>

Si **es true**, el subsistema de eventos WMI debe estar habilitado.

Esta propiedad refleja el valor de la clave del registro.

**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| EnableEvents**

</dd> <dt>

**EnableStartupHeapPreallocation**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableStartupHeapPreallocation")
</dt> </dl>

Si **es true**, WMI crea un montón previamente asignado con el tamaño del valor de **LastStartupHeapPreallocation** cuando se inicializa WMI.

</dd> <dt>

**HighThresholdOnClientObjects**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| software Win32Registry \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| High threshold en objetos de cliente"), [**unidades**](../wmisdk/standard-qualifiers.md) ("objetos por segundo")
</dt> </dl>

Velocidad máxima a la que los objetos creados por el proveedor se pueden entregar a los clientes. Para acomodar las diferencias de velocidad entre proveedores y clientes, WMI mantiene los objetos en las colas antes de entregarlos a los consumidores. Para mayor eficacia, los consumidores deben recopilar los objetos a un ritmo que coincida con el proveedor. Si la memoria mantenida por los objetos no recopilados alcanza el **LowThresholdOnObjects**, WMI ralentiza la adición de nuevos objetos a la cola. Si los eventos no recopilados continúan acumulados y se alcanza la espera máxima para la entrega de eventos en **MaxWaitOnClientObjects** mientras la memoria usada está en el valor de **HighThresholdOnClientObjects**, WMI no acepta más objetos de proveedores y **devuelve \_ WBEM \_ e \_ \_ memoria insuficiente** a los clientes.

</dd> <dt>

**HighThresholdOnEvents**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| software Win32Registry \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| High Threshold on Events"), [**unidades**](../wmisdk/standard-qualifiers.md) ("eventos por segundo")
</dt> </dl>

Velocidad máxima a la que se entregan los eventos a los clientes. Para acomodar las diferencias de velocidad entre proveedores y clientes, WMI pone en cola los eventos antes de entregarlos a los consumidores. Para mayor eficacia, los consumidores deben recopilar los eventos a un ritmo que coincida con el proveedor. Si la memoria mantenida por los eventos no recopilados alcanza **LowThresholdOnObjects**, WMI ralentiza la adición de nuevos eventos a la cola. Si los eventos no recopilados continúan acumulados y se alcanza la espera máxima de entrega de eventos en **MaxWaitOnEvents** mientras la memoria usada está en el valor de **HighThresholdOnEvents**, WMI no acepta más eventos de los proveedores y devuelve **WBEM \_ e \_ \_ \_ memoria insuficiente** a los clientes.

> [!Note]  
> La limitación solo se realiza para los consumidores de eventos permanentes, por lo que los consumidores temporales no deberían esperar la limitación cuando se realiza una copia de seguridad de eventos en la cola de eventos internos de WMI.

 

Esta propiedad refleja el valor de la clave del registro.

**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| alto umbral en objetos de cliente (B)**    

</dd> <dt>

**InstallationDirectory**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \| Installation Directory")
</dt> </dl>

Ruta de acceso al directorio donde se ha instalado el software WMI. La ubicación predeterminada es \\ system32 \\ WBEM.

Esta propiedad refleja el valor de la clave del registro.

**HKEY \_ Software de \_ equipo local** \\  \\ Directorio de instalación de **Microsoft** \\ **WBEM \|**

</dd> <dt>

**LastStartupHeapPreallocation**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| LastStartupHeapPreallocation"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Tamaño del montón asignado previamente creado por WMI durante la inicialización.

Esta propiedad refleja el valor de la clave del registro.

**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| LastStartupHeapPreallocation**

</dd> <dt>

**LoggingDirectory**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Logging Directory")
</dt> </dl>

Ruta de acceso al directorio que contiene la ubicación de los archivos de registro del sistema WMI.

Esta propiedad refleja el valor de la clave del registro.

**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| Logging Directory**

</dd> <dt>

**LoggingLevel**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("software Win32Registry de \| \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| logging")
</dt> </dl>

Habilitación del registro de eventos y el nivel de detalle del registro utilizado.

Esta propiedad refleja el valor de la clave del registro.

**HKEY \_ Software de \_ equipo local** \\  \\  \\ **\| \| registro CIMOM** de Microsoft WBEM

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

**Desactivado** (0)


</dt> <dd></dd> <dt>

<span id="Error_logging"></span><span id="error_logging"></span><span id="ERROR_LOGGING"></span>

**Registro de errores** (1)


</dt> <dd></dd> <dt>

<span id="Verbose_Error_logging"></span><span id="verbose_error_logging"></span><span id="VERBOSE_ERROR_LOGGING"></span>

**Registro de errores detallado** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**LowThresholdOnClientObjects**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| software Win32Registry \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Low threshold en objetos de cliente"), [**unidades**](../wmisdk/standard-qualifiers.md) ("objetos por segundo")
</dt> </dl>

Velocidad a la que WMI comienza a ralentizar la creación de nuevos objetos creados para clientes. Para acomodar las diferencias de velocidad entre proveedores y clientes, WMI mantiene los objetos en las colas antes de entregarlos a los consumidores. Para mayor eficacia, los consumidores deben recopilar los objetos a un ritmo que coincida con el proveedor. Si la tasa de solicitudes de objetos alcanza **LowThresholdOnClientObjects**, WMI reduce gradualmente la creación de objetos nuevos para que coincidan con la tasa de uso del cliente. Esta ralentización se inicia cuando la velocidad a la que se crean los objetos supera el valor de esta propiedad. Vea **HighThresholdOnClientObjects**.

Esta propiedad refleja el valor del registro.

**Clave \_ de Software de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| alto umbral en objetos de cliente (B)**    

</dd> <dt>

**LowThresholdOnEvents**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| software \\ \\ de Win32Registry \\ \\ de Microsoft WBEM \\ \\ CIMOM \| Low Threshold on Events"), [**unidades**](../wmisdk/standard-qualifiers.md) ("eventos por segundo")
</dt> </dl>

Velocidad a la que WMI comienza a ralentizar la entrega de eventos nuevos. Para acomodar las diferencias de velocidad entre proveedores y clientes, WMI pone en cola los eventos antes de entregarlos a los consumidores. Para mayor eficacia, los consumidores deben recopilar los objetos a un ritmo que coincida con el proveedor. Si la cola crece fuera del control, se reduce el nivel de rendimiento de WMI, lo que reduce la velocidad de los eventos para alinearlos con la tasa de clientes. Esta ralentización se inicia cuando la velocidad a la que se generan los eventos supera el valor de esta propiedad. Vea **HighThresholdOnEvents**.

> [!Note]  
> La limitación solo se realiza para los consumidores de eventos permanentes, por lo que los consumidores temporales no deberían esperar la limitación cuando se realiza una copia de seguridad de eventos en la cola de eventos internos de WMI.

 

Esta propiedad refleja el valor del registro.

**HKEY \_ Software de \_ máquina local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| alto umbral en objetos de cliente {B}**    

</dd> <dt>

**MaxLogFileSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Log File size Max size"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Tamaño máximo de los archivos de registro generados por el servicio WMI.

Esta propiedad refleja el valor de la clave del registro.

**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| tamaño máximo del archivo de registro**

</dd> <dt>

**MaxWaitOnClientObjects**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| software Win32Registry \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max wait on Events"), [**unidades**](../wmisdk/standard-qualifiers.md) ("milisegundos")
</dt> </dl>

Cantidad de tiempo que espera un objeto recién creado para que lo use el cliente antes de que se descarte y se devuelva un valor de error. Esta propiedad interactúa con las propiedades **LowThresholdOnClientObjects** y **HighThresholdOnClientObjects** para limitar, ralentizar, la entrega de objetos a los consumidores cuando el consumidor recibe los objetos demasiado lentamente.

</dd> <dt>

**MaxWaitOnEvents**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| software Win32Registry \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max wait on Events"), [**unidades**](../wmisdk/standard-qualifiers.md) ("milisegundos")
</dt> </dl>

Cantidad de tiempo durante el cual un evento enviado a un cliente se pone en cola antes de que se descarte. Esta propiedad interacts0 con **LowThresholdOnEvents** y **HighThresholdOnEvents** para limitar (ralentizar) la entrega de objetos a los consumidores cuando el consumidor recibe los objetos demasiado lentamente.

Esta propiedad refleja el valor del registro.

**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| Max wait on Events (MS)**    

</dd> <dt>

**MofSelfInstallDirectory**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \| MOF Self-Install Directory")
</dt> </dl>

Ruta de acceso del directorio para las aplicaciones que instalan archivos MOF en el repositorio WMI. WMI compila automáticamente cualquier archivo MOF colocado en este directorio y, dependiendo de si se ha realizado correctamente, mueve el MOF a un subdirectorio con la etiqueta Good o Bad. Si \# se incluye el comando [pragma autorecover](../wmisdk/pragma-autorecover.md) , se agrega el nombre de archivo completo a la lista **AutorecoverMofs** que se usa cuando WMI se inicializa o recupera el repositorio. La lista determina el orden en el que se compilan los MOF.

Esta propiedad refleja el valor de la clave del registro.

**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| MOF Self = directorio de instalación**

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificador por el que se conoce el objeto actual.

Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ WMISetting de Win32** se deriva de la [**\_ configuración de CIM**](cim-setting.md). Solo puede existir una instancia de esta clase en un equipo.

Saber cómo se configura WMI en un equipo puede ser muy útil al depurar scripts o solucionar problemas con el propio servicio WMI. Por ejemplo, muchos scripts de WMI se escriben bajo la suposición de que \\ la raíz cimv2 es el espacio de nombres predeterminado en el equipo de destino. Como resultado, \\ a menudo no se puede incluir el espacio de nombres en el moniker GetObject, como se muestra en el ejemplo de código siguiente:

`Set colServices = GetObject("winmgmts:").ExecQuery ("SELECT * FROM Win32_Service")`

Si \\ la raíz cimv2 no es el espacio de nombres predeterminado en el equipo de destino, se producirá un error en este script. Para evitar que esto suceda, el espacio de nombres root \\ cimv2 debe estar incluido en el moniker, tal y como se muestra en el siguiente ejemplo de código:

`Set colServices = GetObject("winmgmts:root\cimv2").ExecQuery("SELECT * FROM Win32_Service")`

Si el espacio de nombres predeterminado en el equipo de destino es diferente del espacio de nombres asumido por un script, se producirá un error en el script. Además de eso, se presentará al usuario el mensaje de error algo engañoso "clase no válida". En realidad, el error no se debe a que la clase no es válida, pero no se encuentra la clase en el espacio de nombres predeterminado. Se trata de un problema difícil de solucionar, porque es probable que investigue los posibles problemas con la clase en lugar de problemas con el espacio de nombres que se especificó (o, en este caso, no).

Puede usar la clase **Win32 \_ WMISetting** para determinar cómo se ha configurado WMI en un equipo. Los detalles de configuración como el espacio de nombres predeterminado o el número de compilación de WMI pueden ser útiles para solucionar problemas de scripts. Estas opciones también proporcionan información administrativa importante, como el modo en que se registran los errores de WMI en un equipo y los proveedores de WMI que se volverán a cargar automáticamente si es necesario volver a generar el repositorio WMI.

## <a name="examples"></a>Ejemplos

En el ejemplo de código de VBScript [Modify WMI Settings](https://Gallery.TechNet.Microsoft.Com/aa80d174-3592-4fed-9c50-11f34e541445) de la galería de TechNet se usa la clase **Win32 \_ WMISetting** para configurar el intervalo de copia de seguridad y el nivel de registro de WMI.

En el ejemplo de código VBScript [del espacio de nombres predeterminado](https://Gallery.TechNet.Microsoft.Com/3fc69acd-ead0-4dd1-9ea1-e15a7331cfa0) de la galería de TechNet se usa la clase **\_ WMISetting de Win32** para recuperar y mostrar el valor actual de "espacio de nombres predeterminado para scripting" de WMI.

En el ejemplo de código de VBScript del [espacio de nombres WMI](https://Gallery.TechNet.Microsoft.Com/6dbb20e6-036d-43a2-ad6d-58325ada6a19) de la galería de TechNet, se usa la propiedad **ASPScriptDefaultNamespace** para establecer el valor de "espacio de nombres predeterminado para scripting" en "root \\ cimv2".

La [lista de todos los valores de WMI](https://Gallery.TechNet.Microsoft.Com/29c04301-e9b2-46d1-8714-2dbb51014c92) ejemplo de código de VBScript utiliza un número de propiedades en **Win32 \_ WMISetting** para devolver una lista de las opciones de configuración de WMI configuradas en un equipo.

En el ejemplo de código JavaScript de la [información de configuración de WMI](https://Gallery.TechNet.Microsoft.Com/0427cfde-4cd9-4a3d-9140-3bb622a1df5d) se usa una serie de propiedades en **Win32 \_ WMISetting** para devolver una lista de las opciones de configuración de WMI configuradas en un equipo.

En el ejemplo de código de la [información de configuración de WMI](https://Gallery.TechNet.Microsoft.Com/370e7fbe-ea3c-4290-8a56-1e38519f518d) de la lista se usan varias propiedades de **Win32 \_ WMISetting** para devolver una lista de las opciones de configuración de WMI configuradas en un equipo.

En el ejemplo de código del objeto de [información de configuración de WMI](https://Gallery.TechNet.Microsoft.Com/9309e4c5-2ca6-4662-9451-f1342d5171d2) de la lista se usan varias propiedades de **Win32 \_ WMISetting** para devolver una lista de las opciones de configuración de WMI configuradas en un equipo.

En el ejemplo de código de VBScript siguiente se muestra cómo obtener la versión de WMI que se ejecuta en el equipo local. "Win32 \_ WMISetting = @" indica la instancia única de la clase. Para obtener más información, vea versiones de WMI.


```VB
set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!/Root/CIMv2")

set objWMISetting = objWMIService.Get("Win32_WMISetting=@")

WScript.Echo  objWMISetting.BuildVersion
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemcore.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Configuración de CIM \_**](cim-setting.md)
</dt> <dt>

[Clases de administración de servicios WMI](./wmi-service-management-classes.md)
</dt> </dl>

 

 
