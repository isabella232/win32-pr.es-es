---
description: La clase \_ WMI singleton WMI Win32 WMISetting contiene los parámetros operativos para el servicio WMI. Esta clase solo puede tener una instancia de , que siempre existe para cada Windows sistema y no se puede eliminar. No se pueden crear instancias adicionales.
ms.assetid: d33cd4f3-969b-46ce-baff-466f1a464906
ms.tgt_platform: multiple
title: Win32_WMISetting clase
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968775"
---
# <a name="win32_wmisetting-class"></a>Clase WMISetting de Win32 \_

La clase [WMI](../wmisdk/retrieving-a-class.md) singleton **WMI \_ Win32 WMISetting** contiene los parámetros operativos para el servicio WMI. Esta clase solo puede tener una instancia de , que siempre existe para cada Windows sistema y no se puede eliminar. No se pueden crear instancias adicionales.

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

## <a name="members"></a>Members

La **clase \_ WMISetting de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ WMISetting de Win32** tiene estas propiedades.

<dl> <dt>

**ASPScriptDefaultNamespace**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM scripting Default \\ \\ \| Namespace")
</dt> </dl>

Espacio de nombres de script predeterminado. Esta propiedad contiene el espacio de nombres utilizado por las llamadas desde scripting API para WMI si el autor de la llamada no especifica ninguno.

Esta propiedad refleja el valor de la clave del Registro.

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **scripting Default \| Namespace**    

Ejemplo: root \\ cimv2

Para obtener un script de ejemplo que usa esta propiedad, vea la sección Comentarios.

</dd> <dt>

**ASPScriptEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM scripting Enable for \\ \\ \| ASP")
</dt> </dl>

Si **es True,** el scripting WMI se puede usar en Active Server Pages (ASP). Esta propiedad es válida en sistemas que ejecutan versiones no admitidas de Windows solo. Para los sistemas Windows compatibles, el scripting WMI siempre se permite en ASP.

</dd> <dt>

**AutorecoverMofs**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| Autorecover MOFs")
</dt> </dl>

Lista de nombres de archivo MOF completos que se usan para inicializar o recuperar el repositorio WMI. La lista determina el orden en que se compilan los archivos MOF.

Esta propiedad refleja el valor de la clave del Registro.

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| Autorecover MOFs**    

</dd> <dt>

**AutoStartWin9X**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| AutostartWin9X")
</dt> </dl>

No compatible.

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

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM Backup Interval \| Threshold"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")
</dt> </dl>

No compatible. En su lugar, realice una copia de seguridad del repositorio WMI manualmente.

</dd> <dt>

**BackupLastTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funciones de tiempo de Win32API \| \| GetTimeZoneInformation")
</dt> </dl>

Fecha y hora en que se realizó la última copia de seguridad.

</dd> <dt>

**BuildVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \| Build")
</dt> </dl>

Información de versión del servicio WMI instalado actualmente.

Tiempo que transcurre entre las copias de seguridad de la base de datos WMI.

Esta propiedad refleja el valor de la clave del Registro.

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM \| Build**

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

Esta propiedad se hereda de la [**configuración de CIM \_**](cim-setting.md).

</dd> <dt>

**DatabaseDirectory**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| Repository Directory")
</dt> </dl>

Ruta de acceso del directorio que contiene el repositorio WMI.

</dd> <dt>

**DatabaseMaxSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM Max DB \| Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")
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

Esta propiedad se hereda de la [**configuración de CIM \_**](cim-setting.md).

</dd> <dt>

**EnableAnonWin9xConnections**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| EnableAnonConnections")
</dt> </dl>

No compatible.

</dd> <dt>

**EnableEvents**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| EnableEvents")
</dt> </dl>

Si **es True**, el subsistema de eventos WMI debe estar habilitado.

Esta propiedad refleja el valor de la clave del Registro.

**HKEY \_ SOFTWARE \_ DE MÁQUINA LOCAL** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| EnableEvents**

</dd> <dt>

**EnableStartupHeapPreallocation**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| EnableStartupHeapPreallocation")
</dt> </dl>

Si **es True,** WMI crea un montón asignado previamente con el tamaño del valor **LastStartupHeapPreallocation** cuando se inicializa WMI.

</dd> <dt>

**HighThresholdOnClientObjects**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM High Threshold On Client \| Objects"), [**Unidades**](../wmisdk/standard-qualifiers.md) ("objetos por segundo")
</dt> </dl>

Velocidad máxima a la que se pueden entregar los objetos creados por el proveedor a los clientes. Para dar cabida a las diferencias de velocidad entre proveedores y clientes, WMI contiene objetos en colas antes de entregarlos a los consumidores. Para obtener más eficacia, los consumidores deben recopilar los objetos a un ritmo que coincida con el proveedor. Si la memoria que mantienen los objetos no recopilados alcanza **LowThresholdOnObjects**, WMI ralentiza la adición de nuevos objetos a la cola. Si se siguen acumulando eventos no recopilados y se alcanza la espera máxima para entregar eventos en **MaxWaitOnClientObjects** mientras la memoria usada se encuentra en el valor de **HighThresholdOnClientObjects**, WMI no acepta más objetos de los proveedores y devuelve **WBEM \_ E OUT OF \_ \_ \_ MEMORY** a los clientes.

</dd> <dt>

**HighThresholdOnEvents**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM High Threshold On \| Events"), [**Unidades**](../wmisdk/standard-qualifiers.md) ("eventos por segundo")
</dt> </dl>

Velocidad máxima a la que se van a entregar los eventos a los clientes. Para dar cabida a las diferencias de velocidad entre proveedores y clientes, WMI pone en cola los eventos antes de entregarlos a los consumidores. Para obtener más eficacia, los consumidores deben recopilar los eventos a un ritmo que coincida con el proveedor. Si la memoria que mantienen los eventos no recopilados alcanza **LowThresholdOnObjects,** WMI ralentiza la adición de nuevos eventos a la cola. Si los eventos no recopilados se siguen acumulando y se alcanza la espera máxima para entregar eventos en **MaxWaitOnEvents** mientras la memoria usada se encuentra en el valor de **HighThresholdOnEvents,** WMI no acepta más eventos de los proveedores y devuelve **WBEM \_ E OUT OF \_ \_ \_ MEMORY** a los clientes.

> [!Note]  
> La limitación solo se realiza para los consumidores de eventos permanentes, por lo que los consumidores temporales no deben esperar limitación cuando se realiza una copia de seguridad de eventos en la cola de eventos interna de WMI.

 

Esta propiedad refleja el valor de la clave del Registro.

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| High Threshold On Client Objects (B)**    

</dd> <dt>

**InstallationDirectory**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM Installation \| Directory")
</dt> </dl>

Ruta de acceso del directorio donde se ha instalado el software WMI. La ubicación predeterminada es \\ System32 \\ Wbem.

Esta propiedad refleja el valor de la clave del Registro.

**HKEY \_ Directorio \_ de instalación** \\ **de** \\ **Microsoft** \\ **WBEM de \|** SOFTWARE LOCAL MACHINE

</dd> <dt>

**LastStartupHeapPreallocation**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| LastStartupHeapPreallocation"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Tamaño del montón preasignado creado por WMI durante la inicialización.

Esta propiedad refleja el valor de la clave del Registro.

**HKEY \_ SOFTWARE \_ DE MÁQUINA LOCAL** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| LastStartupHeapPreallocation**

</dd> <dt>

**LoggingDirectory**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| Logging Directory")
</dt> </dl>

Ruta de acceso del directorio que contiene la ubicación de los archivos de registro del sistema WMI.

Esta propiedad refleja el valor de la clave del Registro.

**HKEY \_ Directorio \_ de registro** DE \\  \\ **CIMOM** de Microsoft \\ **WBEM de \| \|** SOFTWARE LOCAL MACHINE

</dd> <dt>

**LoggingLevel**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| Logging")
</dt> </dl>

Habilitación del registro de eventos y el nivel de detalle del registro usado.

Esta propiedad refleja el valor de la clave del Registro.

**HKEY \_ Registro \_ CIMOM** de Microsoft \\  \\  \\ **WBEM de \| \|** SOFTWARE LOCAL MACHINE

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

**Desactivado** (0)


</dt> <dd></dd> <dt>

<span id="Error_logging"></span><span id="error_logging"></span><span id="ERROR_LOGGING"></span>

**Registro de errores** (1)


</dt> <dd></dd> <dt>

<span id="Verbose_Error_logging"></span><span id="verbose_error_logging"></span><span id="VERBOSE_ERROR_LOGGING"></span>

**Registro detallado de errores** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**LowThresholdOnClientObjects**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM Low Threshold On Client \| Objects"), [**Units**](../wmisdk/standard-qualifiers.md) ("objects per second")
</dt> </dl>

Velocidad a la que WMI comienza a ralentizar la creación de nuevos objetos creados para los clientes. Para dar cabida a las diferencias de velocidad entre proveedores y clientes, WMI contiene objetos en colas antes de entregarlos a los consumidores. Para obtener más eficacia, los consumidores deben recopilar los objetos a un ritmo que coincida con el proveedor. Si la tasa de solicitudes de objetos alcanza **LowThresholdOnClientObjects,** WMI ralentiza gradualmente la creación de nuevos objetos para que coincidan con la tasa de uso del cliente. Esta ralentización se inicia cuando la velocidad a la que se crean los objetos supera el valor de esta propiedad. Vea **HighThresholdOnClientObjects.**

Esta propiedad refleja el valor del Registro.

**KEY \_ Local \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| High Threshold On Client Objects (B)**    

</dd> <dt>

**LowThresholdOnEvents**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM Low Threshold On \| Events"), [**Unidades**](../wmisdk/standard-qualifiers.md) ("eventos por segundo")
</dt> </dl>

Velocidad a la que WMI comienza a ralentizar la entrega de nuevos eventos. Para dar cabida a las diferencias de velocidad entre proveedores y clientes, WMI pone en cola los eventos antes de entregarlos a los consumidores. Para obtener más eficacia, los consumidores deben recopilar los objetos a un ritmo que coincida con el proveedor. Si la cola crece fuera de control, WMI limita (ralentiza) la entrega de eventos gradualmente para alinearse con la velocidad del cliente. Esta ralentización se inicia cuando la velocidad a la que se generan los eventos supera el valor de esta propiedad. Vea **HighThresholdOnEvents.**

> [!Note]  
> La limitación solo se realiza para los consumidores de eventos permanentes, por lo que los consumidores temporales no deben esperar limitación cuando se realiza una copia de seguridad de eventos en la cola de eventos interna de WMI.

 

Esta propiedad refleja el valor del Registro.

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| High Threshold On Client Objects {B}**    

</dd> <dt>

**MaxLogFileSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM Log File Max \| Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Tamaño máximo de los archivos de registro generados por el servicio WMI.

Esta propiedad refleja el valor de la clave del Registro.

**HKEY \_ Tamaño \_ máximo del** archivo de registro \\  \\ CIMOM de **Microsoft** \\ **WBEM \| SOFTWARE LOCAL \| MACHINE** Software

</dd> <dt>

**MaxWaitOnClientObjects**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM Max Wait On \| Events"), [**Unidades**](../wmisdk/standard-qualifiers.md) ("milisegundos")
</dt> </dl>

Cantidad de tiempo que un objeto recién creado espera a ser utilizado por el cliente antes de que se descarte y se devuelva un valor de error. Esta propiedad interactúa con las propiedades **LowThresholdOnClientObjects** y **HighThresholdOnClientObjects** para limitar (ralentizar) la entrega de objetos a los consumidores cuando el consumidor recibe los objetos demasiado lentamente.

</dd> <dt>

**MaxWaitOnEvents**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM Max Wait On \| Events"), [**Unidades**](../wmisdk/standard-qualifiers.md) ("milisegundos")
</dt> </dl>

Cantidad de tiempo durante el que un evento enviado a un cliente se pone en cola antes de descartarse. Esta propiedad interactúa0 con **LowThresholdOnEvents** y **HighThresholdOnEvents** para limitar (ralentizar) la entrega de objetos a los consumidores cuando el consumidor recibe los objetos demasiado lentamente.

Esta propiedad refleja el valor del Registro.

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| Max Wait On Events (ms)**    

</dd> <dt>

**MofSelfInstallDirectory**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \| MOF Self-Install Directory")
</dt> </dl>

Ruta de acceso del directorio para las aplicaciones que instalan archivos MOF en el repositorio WMI. WMI compila automáticamente los archivos MOF colocados en este directorio y, en función de su éxito, mueve el MOF a un subdirectorio etiquetado como correcto o no correcto. Si se incluye el comando \# [pragma autorecover,](../wmisdk/pragma-autorecover.md) el nombre de archivo completo se agrega a la lista **AutorecoverMofs** que se usa cuando WMI inicializa o recupera el repositorio. La lista determina el orden en que se compilan los MOF.

Esta propiedad refleja el valor de la clave del Registro.

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM \| CIMOM \| MOF Self=Install Directory**

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

Esta propiedad se hereda de la [**configuración de CIM \_**](cim-setting.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ WMISetting de Win32** se deriva de [**cim \_ setting**](cim-setting.md). Solo puede existir una instancia de esta clase en un equipo.

Saber cómo se configura WMI en un equipo puede ser muy útil cuando se depuran scripts o se solucionan problemas con el propio servicio WMI. Por ejemplo, muchos scripts WMI se escriben bajo la suposición de que la raíz cimv2 es el espacio de nombres \\ predeterminado en el equipo de destino. Como resultado, los escritores de scripts que necesitan acceder a una clase en "ROOT CIMv2" suelen no incluir el espacio de nombres en el moniker GetObject, como se muestra en el ejemplo de código \\ siguiente:

`Set colServices = GetObject("winmgmts:").ExecQuery ("SELECT * FROM Win32_Service")`

Si root \\ cimv2 no es el espacio de nombres predeterminado en el equipo de destino, se producirá un error en este script. Para evitar que esto suceda, la raíz del espacio de nombres cimv2 debe incluirse en el moniker, como se muestra \\ en el ejemplo de código siguiente:

`Set colServices = GetObject("winmgmts:root\cimv2").ExecQuery("SELECT * FROM Win32_Service")`

Si el espacio de nombres predeterminado del equipo de destino es diferente del espacio de nombres asumido por un script, se producirá un error en el script. Además, se mostrará al usuario el mensaje de error algo engañoso "Clase no válida". En realidad, el error no se debe a que la clase no es válida, sino a que la clase no se encuentra en el espacio de nombres predeterminado. Se trata de un problema difícil de solucionar, ya que es probable que investigue posibles problemas con la clase en lugar de problemas con el espacio de nombres especificado (o, en este caso, no).

Puede usar la clase **\_ WMISetting de Win32** para determinar cómo se ha configurado WMI en un equipo. Los detalles de configuración, como el espacio de nombres predeterminado o el número de compilación wmi, pueden ser útiles para solucionar problemas de script. Esta configuración también proporciona información administrativa importante, como cómo o incluso si se registran errores de WMI en un equipo y qué proveedores WMI se volverán a cargar automáticamente si necesita volver a generar el repositorio WMI.

## <a name="examples"></a>Ejemplos

El [ejemplo de código Modify WMI Configuración](https://Gallery.TechNet.Microsoft.Com/aa80d174-3592-4fed-9c50-11f34e541445) VBScript de la Galería de TechNet usa la clase **\_ WMISetting de Win32** para configurar el intervalo de copia de seguridad de WMI y el nivel de registro.

El ejemplo [de](https://Gallery.TechNet.Microsoft.Com/3fc69acd-ead0-4dd1-9ea1-e15a7331cfa0) código DE VBScript Enumerar el espacio de nombres predeterminado de la Galería de TechNet usa la clase **\_ WMISetting de Win32** para recuperar y mostrar la configuración actual de WMI "Espacio de nombres predeterminado para scripting".

El ejemplo de código [VBScript](https://Gallery.TechNet.Microsoft.Com/6dbb20e6-036d-43a2-ad6d-58325ada6a19) Modificar el espacio de nombres WMI predeterminado de la Galería de TechNet usa la propiedad **ASPScriptDefaultNamespace** para establecer el valor "Espacio de nombres predeterminado para scripting" de WMI en "root \\ cimv2".

El ejemplo de código List [All the WMI Configuración](https://Gallery.TechNet.Microsoft.Com/29c04301-e9b2-46d1-8714-2dbb51014c92) VBSCript usa varias propiedades en **\_ WMISetting de Win32** para devolver una lista de la configuración de WMI configurada en un equipo.

El [ejemplo de código de](https://Gallery.TechNet.Microsoft.Com/0427cfde-4cd9-4a3d-9140-3bb622a1df5d) JavaScript List WMI Setting Information usa varias propiedades en **\_ WMISetting de Win32** para devolver una lista de la configuración de WMI configurada en un equipo.

El [ejemplo de código](https://Gallery.TechNet.Microsoft.Com/370e7fbe-ea3c-4290-8a56-1e38519f518d) de Python List WMI Setting Information usa varias propiedades en **\_ WMISetting de Win32** para devolver una lista de la configuración de WMI configurada en un equipo.

El [ejemplo de código](https://Gallery.TechNet.Microsoft.Com/9309e4c5-2ca6-4662-9451-f1342d5171d2) REXX Del objeto list WMI Setting Information usa varias propiedades en **\_ WMISetting de Win32** para devolver una lista de la configuración de WMI configurada en un equipo.

En el siguiente ejemplo de código de VBScript se muestra cómo obtener la versión de WMI que se ejecuta en el equipo local. "Win32 \_ WMISetting=@" indica la instancia única de la clase . Para obtener más información, vea Versiones de WMI.


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
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemcore.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Configuración de CIM \_**](cim-setting.md)
</dt> <dt>

[Clases de administración de servicios WMI](./wmi-service-management-classes.md)
</dt> </dl>

 

 
