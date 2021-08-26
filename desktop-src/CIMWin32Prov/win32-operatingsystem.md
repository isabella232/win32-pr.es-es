---
description: Representa un Windows operativo basado en datos instalado en un equipo.
ms.assetid: eb6a8cff-20a0-4211-b46a-3084e9c39246
ms.tgt_platform: multiple
title: Clase Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem
- Win32_OperatingSystem.BootDevice
- Win32_OperatingSystem.BuildNumber
- Win32_OperatingSystem.BuildType
- Win32_OperatingSystem.Caption
- Win32_OperatingSystem.CodeSet
- Win32_OperatingSystem.CountryCode
- Win32_OperatingSystem.CreationClassName
- Win32_OperatingSystem.CSCreationClassName
- Win32_OperatingSystem.CSDVersion
- Win32_OperatingSystem.CSName
- Win32_OperatingSystem.CurrentTimeZone
- Win32_OperatingSystem.DataExecutionPrevention_Available
- Win32_OperatingSystem.DataExecutionPrevention_32BitApplications
- Win32_OperatingSystem.DataExecutionPrevention_Drivers
- Win32_OperatingSystem.DataExecutionPrevention_SupportPolicy
- Win32_OperatingSystem.Debug
- Win32_OperatingSystem.Description
- Win32_OperatingSystem.Distributed
- Win32_OperatingSystem.EncryptionLevel
- Win32_OperatingSystem.ForegroundApplicationBoost
- Win32_OperatingSystem.FreePhysicalMemory
- Win32_OperatingSystem.FreeSpaceInPagingFiles
- Win32_OperatingSystem.FreeVirtualMemory
- Win32_OperatingSystem.InstallDate
- Win32_OperatingSystem.LargeSystemCache
- Win32_OperatingSystem.LastBootUpTime
- Win32_OperatingSystem.LocalDateTime
- Win32_OperatingSystem.Locale
- Win32_OperatingSystem.Manufacturer
- Win32_OperatingSystem.MaxNumberOfProcesses
- Win32_OperatingSystem.MaxProcessMemorySize
- Win32_OperatingSystem.MUILanguages
- Win32_OperatingSystem.Name
- Win32_OperatingSystem.NumberOfLicensedUsers
- Win32_OperatingSystem.NumberOfProcesses
- Win32_OperatingSystem.NumberOfUsers
- Win32_OperatingSystem.OperatingSystemSKU
- Win32_OperatingSystem.Organization
- Win32_OperatingSystem.OSArchitecture
- Win32_OperatingSystem.OSLanguage
- Win32_OperatingSystem.OSProductSuite
- Win32_OperatingSystem.OSType
- Win32_OperatingSystem.OtherTypeDescription
- Win32_OperatingSystem.PAEEnabled
- Win32_OperatingSystem.PlusProductID
- Win32_OperatingSystem.PlusVersionNumber
- Win32_OperatingSystem.PortableOperatingSystem
- Win32_OperatingSystem.Primary
- Win32_OperatingSystem.ProductType
- Win32_OperatingSystem.RegisteredUser
- Win32_OperatingSystem.SerialNumber
- Win32_OperatingSystem.ServicePackMajorVersion
- Win32_OperatingSystem.ServicePackMinorVersion
- Win32_OperatingSystem.SizeStoredInPagingFiles
- Win32_OperatingSystem.Status
- Win32_OperatingSystem.SuiteMask
- Win32_OperatingSystem.SystemDevice
- Win32_OperatingSystem.SystemDirectory
- Win32_OperatingSystem.SystemDrive
- Win32_OperatingSystem.TotalSwapSpaceSize
- Win32_OperatingSystem.TotalVirtualMemorySize
- Win32_OperatingSystem.TotalVisibleMemorySize
- Win32_OperatingSystem.Version
- Win32_OperatingSystem.WindowsDirectory
- Win32_OperatingSystem.QuantumLength
- Win32_OperatingSystem.QuantumType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a1df0da4cadf0cd610803b2f456f22049471b28bc5653bc400f4c730cb0c47de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972535"
---
# <a name="win32_operatingsystem-class"></a>Clase OperatingSystem de Win32 \_

La clase [WMI](../wmisdk/retrieving-a-class.md) **\_ Win32 OperatingSystem** representa un Windows operativo basado en el sistema operativo instalado en un equipo.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Singleton, Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4DE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_OperatingSystem : CIM_OperatingSystem
{
  string   BootDevice;
  string   BuildNumber;
  string   BuildType;
  string   Caption;
  string   CodeSet;
  string   CountryCode;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSDVersion;
  string   CSName;
  sint16   CurrentTimeZone;
  boolean  DataExecutionPrevention_Available;
  boolean  DataExecutionPrevention_32BitApplications;
  boolean  DataExecutionPrevention_Drivers;
  uint8    DataExecutionPrevention_SupportPolicy;
  boolean  Debug;
  string   Description;
  boolean  Distributed;
  uint32   EncryptionLevel;
  uint8    ForegroundApplicationBoost = 2;
  uint64   FreePhysicalMemory;
  uint64   FreeSpaceInPagingFiles;
  uint64   FreeVirtualMemory;
  datetime InstallDate;
  uint32   LargeSystemCache;
  datetime LastBootUpTime;
  datetime LocalDateTime;
  string   Locale;
  string   Manufacturer;
  uint32   MaxNumberOfProcesses;
  uint64   MaxProcessMemorySize;
  string   MUILanguages[];
  string   Name;
  uint32   NumberOfLicensedUsers;
  uint32   NumberOfProcesses;
  uint32   NumberOfUsers;
  uint32   OperatingSystemSKU;
  string   Organization;
  string   OSArchitecture;
  uint32   OSLanguage;
  uint32   OSProductSuite;
  uint16   OSType;
  string   OtherTypeDescription;
  Boolean  PAEEnabled;
  string   PlusProductID;
  string   PlusVersionNumber;
  boolean  PortableOperatingSystem;
  boolean  Primary;
  uint32   ProductType;
  string   RegisteredUser;
  string   SerialNumber;
  uint16   ServicePackMajorVersion;
  uint16   ServicePackMinorVersion;
  uint64   SizeStoredInPagingFiles;
  string   Status;
  uint32   SuiteMask;
  string   SystemDevice;
  string   SystemDirectory;
  string   SystemDrive;
  uint64   TotalSwapSpaceSize;
  uint64   TotalVirtualMemorySize;
  uint64   TotalVisibleMemorySize;
  string   Version;
  string   WindowsDirectory;
  uint8    QuantumLength;
  uint8    QuantumType;
};
```

## <a name="members"></a>Miembros

La **clase \_ OperatingSystem de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ OperatingSystem de Win32** tiene estos métodos.



| Método                                                                                     | Descripción                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Reboot**](reboot-method-in-class-win32-operatingsystem.md)                             | Se apaga y, a continuación, se reinicia el sistema del equipo.<br/>                                                                                                                                                                                                           |
| [**SetDateTime**](setdatetime-method-in-class-win32-operatingsystem.md)                   | Permite establecer la fecha y hora del equipo.<br/>                                                                                                                                                                                                                |
| [**Apagado**](shutdown-method-in-class-win32-operatingsystem.md)                         | Descarga programas y archivos DLL hasta el punto en el que es seguro desactivar el equipo.<br/>                                                                                                                                                                           |
| [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md)               | Proporciona el conjunto completo de opciones de apagado admitidas por Windows sistemas operativos.<br/>                                                                                                                                                                           |
| [**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) | Proporciona el mismo conjunto de opciones de apagado compatibles con el método [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) en **Win32 \_ OperatingSystem,** pero también permite especificar comentarios, un motivo para el apagado o un tiempo de espera.<br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ OperatingSystem de Win32** tiene estas propiedades.

<dl> <dt>

**BootDevice**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| DRIVE MAP INFO \_ \_ \| btInt13Unit")
</dt> </dl>

Nombre de la unidad de disco desde la que se inicia Windows sistema operativo.

Ejemplo: \\ \\ "Disco \\ duro del dispositivo0"

</dd> <dt>

**BuildNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Información del sistema Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| dwBuildNumber")
</dt> </dl>

Número de compilación de un sistema operativo. Se puede usar para obtener información de versión más precisa que los números de versión de lanzamiento del producto.

Ejemplo: "1381"

</dd> <dt>

**BuildType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows \\ \\ \\ \\ \\ \\ CurrentVersion \| CurrentType")
</dt> </dl>

Tipo de compilación que se usa para un sistema operativo.

Ejemplos: ""retail build"", ""checked build""

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descripción del objeto: una cadena de una línea. La cadena incluye la versión del sistema operativo. Por ejemplo, "Microsoft Windows 7 Enterprise". Esta propiedad se puede localizar.

**Windows Vista y Windows 7:** Esta propiedad puede contener caracteres finales. Por ejemplo, la cadena "Microsoft Windows 7 Enterprise" (espacio final incluido) puede ser necesaria para recuperar información mediante esta propiedad.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**CodeSet**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (6), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| National Language Support Functions \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| LOCALE \_ IDEFAULTANSICODEPAGE")
</dt> </dl>

Valor de página de códigos que usa un sistema operativo. Una página de códigos contiene una tabla de caracteres que un sistema operativo usa para traducir cadenas para distintos idiomas. El American National Standards Institute (ANSI) enumera los valores que representan páginas de códigos definidas. Si un sistema operativo no usa una página de códigos ANSI, este miembro se establece en 0 (cero). La **cadena CodeSet** puede usar un máximo de seis caracteres para definir el valor de la página de códigos.

Ejemplo: "1255"

</dd> <dt>

**CountryCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| National Language Support Functions \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| LOCALE \_ ICOUNTRY")
</dt> </dl>

Código para el país o región que usa un sistema operativo. Los valores se basan en prefijos de marcación telefónica internacionales, también denominados códigos de país o región de IBM. Esta propiedad puede usar un máximo de seis caracteres para definir el valor de código de país o región.

Ejemplo: "1" (Estados Unidos)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**\_ Clave CIM,**](../wmisdk/standard-wmi-qualifiers.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nombre de la primera clase concreta que aparece en la cadena de herencia utilizada en la creación de una instancia de . Cuando se usa con otras propiedades clave de la clase , esta propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.

Esta propiedad se hereda de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**Cim \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nombre de clase de creación del sistema de equipo de ámbito.

Esta propiedad se hereda de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**CSDVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Información del sistema Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **szCSDVersion**")
</dt> </dl>

**Cadena** terminada en NULL que indica el Service Pack más reciente instalado en un equipo. Si no hay ningún Service Pack instalado, la cadena es **NULL.**

Ejemplo: "Service Pack 3"

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nombre del sistema de equipo de ámbito.

Esta propiedad se hereda de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**CurrentTimeZone**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("minutos")
</dt> </dl>

Número, en minutos, un sistema operativo se desplaza con respecto a la hora media de Greenwich (GMT). El número es positivo, negativo o cero.

Esta propiedad se hereda de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**DataExecutionPrevention \_ 32BitApplications**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Cuando la característica de hardware de prevención de ejecución de datos está disponible, esta propiedad indica que la característica está establecida para funcionar con aplicaciones de 32 bits si **es True.** En equipos de 64 bits, la característica de prevención de ejecución de datos se configura en el almacén [de datos de la configuración de arranque (BCD) (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) y las propiedades de **Win32 \_ OperatingSystem** se establecen en consecuencia.

</dd> <dt>

**DataExecutionPrevention \_ Disponible**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

La prevención de ejecución de datos es una característica de hardware para evitar ataques de saturación del búfer al detener la ejecución de código en páginas de memoria de tipo de datos. Si **es True**, esta característica está disponible. En equipos de 64 bits, la característica de prevención de ejecución de datos se configura en el almacén BCD y las propiedades de **Win32 \_ OperatingSystem** se establecen en consecuencia.

</dd> <dt>

**Controladores DataExecutionPrevention \_**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Cuando la característica de hardware de prevención de ejecución de datos está disponible, esta propiedad indica que la característica está establecida para funcionar para los controladores si es **True.** En equipos de 64 bits, la característica de prevención de ejecución de datos se configura en el almacén BCD y las propiedades de **Win32 \_ OperatingSystem** se establecen en consecuencia.

</dd> <dt>

**DataExecutionPrevention \_ SupportPolicy**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Indica qué configuración de Prevención de ejecución de datos (DEP) se aplica. La configuración de DEP especifica la medida en que DEP se aplica a las aplicaciones de 32 bits en el sistema. DEP siempre se aplica al Windows kernel.

<dt>

<span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>

<span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>**Always Off** (0)


</dt> <dd>

DEP está desactivado para todas las aplicaciones de 32 bits del equipo sin excepciones. Esta configuración no está disponible para la interfaz de usuario.

</dd> <dt>

<span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>

<span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>**Always On** (1)


</dt> <dd>

DEP está habilitado para todas las aplicaciones de 32 bits del equipo. Esta configuración no está disponible para la interfaz de usuario.

</dd> <dt>

<span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>

<span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>**Participar** (2)


</dt> <dd>

DEP está habilitado para un número limitado de archivos binarios, el kernel y todos los Windows basados en datos. Sin embargo, está desactivada de forma predeterminada para todas las aplicaciones de 32 bits. Un usuario o administrador debe elegir explícitamente  la configuración **Always On** o no participar antes de que DEP se pueda aplicar a aplicaciones de 32 bits.

</dd> <dt>

<span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>

<span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>**No participar** (3)


</dt> <dd>

DEP está habilitado de forma predeterminada para todas las aplicaciones de 32 bits. Un usuario o administrador puede quitar explícitamente la compatibilidad con una aplicación de 32 bits agregando la aplicación a una lista de excepciones.

</dd> </dl>

</dd> <dt>

**Depurar**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ DEBUG")
</dt> </dl>

El sistema operativo es una compilación activada (depuración). Si **es True**, se instala la versión de depuración. Las compilaciones comprobadas proporcionan comprobación de errores, comprobación de argumentos y código de depuración del sistema. El código adicional de un binario activado genera un mensaje de error del depurador del kernel y se interrumpe en el depurador. Esto ayuda a determinar inmediatamente la causa y la ubicación del error. El rendimiento puede verse afectado en una compilación comprobada debido al código adicional que se ejecuta.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("Description"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Descripción de la Windows operativo. Algunas interfaces de usuario, por ejemplo, las que permiten editar esta descripción, limitan su longitud a 48 caracteres.

</dd> <dt>

**Distribuido**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es True**, el sistema operativo se distribuye entre varios nodos del sistema del equipo. Si es así, estos nodos deben agruparse como un clúster.

Esta propiedad se hereda de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**EncryptionLevel**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nivel de cifrado para transacciones seguras: 40 bits, 128 bits o *n* bits.

<dt>

<span id="40-bit"></span><span id="40-BIT"></span>

**40 bits** (0)


</dt> <dd></dd> <dt>

<span id="128-bit"></span><span id="128-BIT"></span>

**128 bits** (1)


</dt> <dd></dd> <dt>

<span id="n-bit"></span><span id="N-BIT"></span>

**n bits** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**ForegroundApplicationBoost**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ PriorityControl \| Win32PrioritySeparation")
</dt> </dl>

El aumento de prioridad se da a la aplicación en primer plano. La potenciación de la aplicación se implementa al proporcionar a una aplicación más segmentos de tiempo de ejecución (longitudes cuánticas).

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Ninguno** (0)


</dt> <dd>

El sistema aumenta la longitud cuántica en 6.

</dd> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Mínimo** (1)


</dt> <dd>

El sistema aumenta la longitud cuántica en 12.

</dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Máximo** (2)


</dt> <dd>

El sistema aumenta la longitud cuántica en 18.

</dd> </dl>

</dd> <dt>

**FreePhysicalMemory**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")
</dt> </dl>

Número, en kilobytes, de memoria física actualmente sin usar y disponible.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/previous-versions//aa393262(v=vs.85))

Esta propiedad se hereda de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**FreeSpaceInPagingFiles**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| System Memory Configuración \| 001.4"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")
</dt> </dl>

Número, en kilobytes, que se puede asignar a los archivos de paginación del sistema operativo sin provocar que se intercambien otras páginas.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/previous-versions//aa393262(v=vs.85))

Esta propiedad se hereda de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**FreeVirtualMemory**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")
</dt> </dl>

Número, en kilobytes, de memoria virtual actualmente sin usar y disponible.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/previous-versions//aa393262(v=vs.85))

Esta propiedad se hereda de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Fecha de instalación")
</dt> </dl>

Se instaló el objeto Date. Esta propiedad no requiere un valor para indicar que el objeto está instalado.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**LargeSystemCache**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **EN DESUSO**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Esta propiedad está obsoleta y no se admite.

<dt>

<span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>

<span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>**Optimizar para aplicaciones** (0)


</dt> <dd>

Optimice la memoria de las aplicaciones.

</dd> <dt>

<span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>

<span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>**Optimizar el rendimiento del sistema** (1)


</dt> <dd>

Optimice la memoria para el rendimiento del sistema.

</dd> </dl>

</dd> <dt>

**LastBootUpTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se reinició por última vez el sistema operativo.

Esta propiedad se hereda de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**LocalDateTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| HOST-RESOURCES-MIB.hrSystemDate", "MIF. Información general de DMTF \| \| 001.6")
</dt> </dl>

Versión del sistema operativo de la fecha y hora del día locales.

Esta propiedad se hereda de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**Configuración regional**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| National Language Support Functions \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| LOCALE \_ ILANGUAGE")
</dt> </dl>

Identificador de idioma utilizado por el sistema operativo. Un identificador de idioma es una abreviatura numérica internacional estándar para un país o región. Cada idioma tiene un identificador de idioma único (LANGID), un valor de 16 bits que consta de un identificador de idioma principal y un identificador de idioma secundario.

</dd> <dt>

**Fabricante**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Nombre del fabricante del sistema operativo. Para Windows basados en datos, este valor es "Microsoft Corporation".

</dd> <dt>

**MaxNumberOfProcesses**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| HOST-RESOURCES-MIB.hrSystemMaxProcesses")
</dt> </dl>

Número máximo de contextos de proceso que el sistema operativo puede admitir. El valor predeterminado establecido por el proveedor es 4294967295 (0xFFFFFFFF). Si no hay ningún máximo fijo, el valor debe ser 0 (cero). En los sistemas que tienen un máximo fijo, este objeto puede ayudar a diagnosticar errores que se producen cuando se alcanza el máximo( si se desconoce, escriba 4294967295 (0xFFFFFFFF).

Esta propiedad se hereda de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**MaxProcessMemorySize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")
</dt> </dl>

Número máximo, en kilobytes, de memoria que se puede asignar a un proceso. Para los sistemas operativos sin memoria virtual, normalmente este valor es igual a la cantidad total de memoria física menos la memoria usada por el BIOS y el sistema operativo. Para algunos sistemas operativos, este valor puede ser infinito, en cuyo caso se debe especificar 0 (cero). En otros casos, este valor podría ser una constante, por ejemplo, 2G o 4G.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/previous-versions//aa393262(v=vs.85))

Esta propiedad se hereda de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**LOS IDIOMAS DE LOS IDIOMAS DE LA COLA**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Interfaz de usuario multilingüe Idiomas pack (PACK) instalados en el equipo. Por ejemplo, "en-us". Los idiomas de PACK son archivos de recursos que se pueden instalar en la versión en inglés del sistema operativo. Cuando se instala un paquete DE EXTENSIÓN, puede cambiar el idioma de la interfaz de usuario a uno de los 33 idiomas admitidos.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Instancia de sistema operativo dentro de un sistema informático.

Esta propiedad se hereda de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**NumberOfLicensedUsers**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de licencias de usuario para el sistema operativo. Si es ilimitado, escriba 0 (cero). Si es desconocido, escriba -1.

Esta propiedad se hereda de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**NumberOfProcesses**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| HOST-RESOURCES-MIB.hrSystemProcesses")
</dt> </dl>

Número de contextos de proceso cargados o en ejecución actualmente en el sistema operativo.

Esta propiedad se hereda de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**NumberOfUsers**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| HOST-RESOURCES-MIB.hrSystemNumUsers")
</dt> </dl>

Número de sesiones de usuario para las que el sistema operativo almacena actualmente información de estado.

Esta propiedad se hereda de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**OperatingSystemSKU**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Número de unidad de almacenamiento de existencias (SKU) para el sistema operativo. Estos valores son los mismos que las constantes **PRODUCT \_ \** _ definidas en WinNT.h que se usan con la [función _ *GetProductInfo.* *](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getproductinfo)

En la lista siguiente se enumeran los posibles valores de SKU.

<dt>

<span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>

<span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>**PRODUCT \_ UNDEFINED** (0)


</dt> <dd>

No definido

</dd> <dt>

<span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>

<span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>**PRODUCT \_ ULTIMATE** (1)


</dt> <dd>

Ultimate Edition, por ejemplo, Windows Vista Ultimate.

</dd> <dt>

<span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>

<span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>**PRODUCT \_ HOME \_ BASIC** (2)


</dt> <dd>

Home Basic Edition

</dd> <dt>

<span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>

<span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>**PRODUCT \_ HOME \_ PREMIUM** (3)


</dt> <dd>

Home Premium Edition

</dd> <dt>

<span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>

<span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>**PRODUCT \_ ENTERPRISE** (4)


</dt> <dd>

Enterprise Edition

</dd> <dt>

<span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>

<span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>**PRODUCT \_ BUSINESS** (6)


</dt> <dd>

Business Edition

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>

<span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>**PRODUCT \_ SERVIDOR \_ ESTÁNDAR** (7)


</dt> <dd>

Windows Servidor Standard Edition (instalación de experiencia de escritorio)

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>

<span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>**PRODUCT \_ DATACENTER \_ SERVER** (8)


</dt> <dd>

Windows Server Datacenter Edition (instalación de experiencia de escritorio)

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>

<span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>**PRODUCT \_ SMALLBUSINESS \_ SERVER** (9)


</dt> <dd>

Small Business Server Edition

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>

<span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>**PRODUCT \_ ENTERPRISE \_ SERVER** (10)


</dt> <dd>

Enterprise Server Edition

</dd> <dt>

<span id="PRODUCT_STARTER"></span><span id="product_starter"></span>

<span id="PRODUCT_STARTER"></span><span id="product_starter"></span>**PRODUCT \_ STARTER** (11)


</dt> <dd>

 Starter Edition

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>

<span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>**PRODUCT \_ DATACENTER \_ SERVER \_ CORE** (12)


</dt> <dd>

Datacenter Server Core Edition

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>

<span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>**PRODUCT \_ STANDARD \_ SERVER \_ CORE** (13)


</dt> <dd>

Standard Server Core Edition

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>**PRODUCT \_ ENTERPRISE \_ SERVER \_ CORE** (14)


</dt> <dd>

Enterprise Server Core Edition

</dd> <dt>

<span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>

<span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>**PRODUCT \_ SERVIDOR \_ WEB** (17)


</dt> <dd>

Web Server Edition

</dd> <dt>

<span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>

<span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>**PRODUCT \_ SERVIDOR \_ PRINCIPAL** (19)


</dt> <dd>

Home Server Edition

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>**PRODUCT \_ STORAGE \_ EXPRESS \_ SERVER** (20)


</dt> <dd>

Storage Express Server Edition

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>

<span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>**PRODUCT \_ SERVIDOR \_ ESTÁNDAR \_ DE ALMACENAMIENTO** (21)


</dt> <dd>

Windows Storage Server Standard Edition (instalación de experiencia de escritorio)

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>**PRODUCT \_ SERVIDOR DE \_ GRUPO \_ DE TRABAJO DE** ALMACENAMIENTO (22)


</dt> <dd>

Windows Storage Server Workgroup Edition (instalación de experiencia de escritorio)

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>**PRODUCT \_ STORAGE \_ ENTERPRISE \_ SERVER** (23)


</dt> <dd>

Storage Enterprise Server Edition

</dd> <dt>

<span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>

<span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>**PRODUCT \_ SERVER \_ FOR \_ SMALLBUSINESS** (24)


</dt> <dd>

Server For Small Business Edition

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>**PRODUCT \_ SMALLBUSINESS \_ SERVER \_ PREMIUM** (25)


</dt> <dd>

Small Business Server Premium Edition

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>

<span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>**PRODUCT \_ ENTERPRISE \_ N** (27)


</dt> <dd>

Windows Enterprise Edition

</dd> <dt>

<span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>

<span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>**PRODUCT \_ ULTIMATE \_ N** (28)


</dt> <dd>

Windows Ultimate Edition

</dd> <dt>

<span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>

<span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>**PRODUCT \_ WEB \_ SERVER \_ CORE** (29)


</dt> <dd>

Windows Server Web Server Edition (instalación server core)

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>

<span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>**PRODUCT \_ STANDARD \_ SERVER \_ V** (36)


</dt> <dd>

Windows Servidor Standard Edition sin Hyper-V

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>

<span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>**PRODUCT \_ DATACENTER \_ SERVER \_ V** (37)


</dt> <dd>

Windows Server Datacenter Edition sin Hyper-V (instalación completa)

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>

<span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>**PRODUCT \_ ENTERPRISE \_ SERVER \_ V** (38)


</dt> <dd>

Windows Servidor Enterprise Edition sin Hyper-V (instalación completa)

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>

<span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>**PRODUCT \_ DATACENTER \_ SERVER \_ CORE \_ V** (39)


</dt> <dd>

Windows Server Datacenter Edition sin Hyper-V (instalación de Server Core)

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>

<span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>**PRODUCT \_ STANDARD \_ SERVER \_ CORE \_ V** (40)


</dt> <dd>

Windows Servidor Standard Edition sin Hyper-V (instalación de Server Core)

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>**PRODUCT \_ ENTERPRISE \_ SERVER \_ CORE \_ V** (41)


</dt> <dd>

Windows Server Enterprise Edition sin Hyper-V (instalación de Server Core)

</dd> <dt>

<span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>

<span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>**PRODUCT \_ HYPERV** (42)


</dt> <dd>

Microsoft Hyper-V Server

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>**PRODUCT \_ STORAGE \_ EXPRESS \_ SERVER \_ CORE** (43)


</dt> <dd>

Storage Server Express Edition (instalación de Server Core)

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>

<span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>**PRODUCT \_ STORAGE \_ STANDARD \_ SERVER \_ CORE** (44)


</dt> <dd>

Storage Server Standard Edition (instalación de Server Core)

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>**PRODUCT \_ STORAGE \_ WORKGROUP \_ SERVER \_ CORE** (45)


</dt> <dd>

Storage Server Workgroup Edition (instalación de Server Core)

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>**PRODUCT \_ STORAGE \_ ENTERPRISE \_ SERVER \_ CORE** (46)


</dt> <dd>

Storage Server Workgroup Edition (instalación de Server Core)

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>

<span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>**PRODUCT \_ PROFESSIONAL** (48)


</dt> <dd>

Windows Professional

</dd> <dt>

<span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>

<span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>**PRODUCT \_ SB \_ SOLUTION \_ SERVER** (50)


</dt> <dd>

Windows Server Essentials (instalación de la experiencia de escritorio)

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>**PRODUCT \_ SMALLBUSINESS \_ SERVER \_ PREMIUM \_ CORE** (63)


</dt> <dd>

Small Business Server Premium (instalación de Server Core)

</dd> <dt>

<span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>

<span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>**PRODUCT \_ SERVIDOR \_ DE \_ CLÚSTER V** (64)


</dt> <dd>

Windows Servidor de clúster de proceso sin Hyper-V

</dd> <dt>

<span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>

<span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>**PRODUCT \_ CORE \_ ARM** (97)


</dt> <dd>

Windows RT

</dd> <dt>

<span id="PRODUCT_CORE"></span><span id="product_core"></span>

<span id="PRODUCT_CORE"></span><span id="product_core"></span>**PRODUCT \_ CORE** (101)


</dt> <dd>

Windows Casa

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>

<span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>**PRODUCT \_ PROFESSIONAL \_ WMC** (103)


</dt> <dd>

Windows Professional con Media Center

</dd> <dt>

<span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>

<span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>**PRODUCT \_ MOBILE \_ CORE** (104)


</dt> <dd>

Windows Mobile

</dd> <dt>

<span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>

<span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>**PRODUCT \_ IOTUAP** (123)


</dt> <dd>

Windows IoT (Internet de las cosas) Core

</dd> <dt>

<span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>

<span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>**PRODUCT \_ DATACENTER \_ NANO \_ SERVER** (143)


</dt> <dd>

Windows Server Datacenter Edition (instalación de Nano Server)

</dd> <dt>

<span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>

<span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>**PRODUCT \_ SERVIDOR \_ NANO \_ ESTÁNDAR** (144)


</dt> <dd>

Windows Server Standard Edition (instalación de Nano Server)

</dd> <dt>

<span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>

<span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>**PRODUCT \_ DATACENTER \_ WS \_ SERVER \_ CORE** (147)


</dt> <dd>

Windows Server Datacenter Edition (instalación de Server Core)

</dd> <dt>

<span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>

<span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>**PRODUCT \_ STANDARD \_ WS \_ SERVER \_ CORE** (148)


</dt> <dd>

Windows Server Standard Edition (instalación de Server Core)

</dd> </dl>

</dd> <dt>

**Organización**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows \\ \\ \\ \\ \\ \\ CurrentVersion \| RegisteredOrganization")
</dt> </dl>

Nombre de la compañía del usuario registrado del sistema operativo.

Ejemplo: "Microsoft Corporation"

</dd> <dt>

**OSArchitecture**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Arquitectura del sistema operativo, en lugar del procesador. Esta propiedad se puede localizar.

Ejemplo: 32 bits

</dd> <dt>

**OSLanguage**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| DEFAULT Panel de control configuración regional \\ \\ \\ \\ \| internacional")
</dt> </dl>

Versión de idioma del sistema operativo instalada. En la lista siguiente se enumeran los valores posibles. Ejemplo: 0x0807 (Alemán, Suiza).

<dt>

1 (0x1)
</dt> <dd>

Árabe

</dd> <dt>

4 (0x4)
</dt> <dd>

Chino (simplificado): China

</dd> <dt>

9 (0x9)
</dt> <dd>

Inglés

</dd> <dt>

1025 (0x401)
</dt> <dd>

Árabe: Emiratos Árabes Unidos

</dd> <dt>

1026 (0x402)
</dt> <dd>

Búlgaro

</dd> <dt>

1027 (0x403)
</dt> <dd>

Catalán

</dd> <dt>

1028 (0x404)
</dt> <dd>

Chino (tradicional): Taiwán

</dd> <dt>

1029 (0x405)
</dt> <dd>

Checo

</dd> <dt>

1030 (0x406)
</dt> <dd>

Danés

</dd> <dt>

1031 (0x407)
</dt> <dd>

Alemán – Alemania

</dd> <dt>

1032 (0x408)
</dt> <dd>

Griego

</dd> <dt>

1033 (0x409)
</dt> <dd>

Inglés: Estados Unidos

</dd> <dt>

1034 (0x40A)
</dt> <dd>

Español: ordenación tradicional

</dd> <dt>

1035 (0x40B)
</dt> <dd>

Finés

</dd> <dt>

1036 (0x40C)
</dt> <dd>

Francés – Francia

</dd> <dt>

1037 (0x40D)
</dt> <dd>

Hebreo

</dd> <dt>

1038 (0x40E)
</dt> <dd>

Húngaro

</dd> <dt>

1039 (0x40F)
</dt> <dd>

Islandés

</dd> <dt>

1040 (0x410)
</dt> <dd>

Italiano – Italia

</dd> <dt>

1041 (0x411)
</dt> <dd>

Japonés

</dd> <dt>

1042 (0x412)
</dt> <dd>

Coreano

</dd> <dt>

1043 (0x413)
</dt> <dd>

Neerlandés – Países Bajos

</dd> <dt>

1044 (0x414)
</dt> <dd>

Noruego: Bokmal

</dd> <dt>

1045 (0x415)
</dt> <dd>

Polaco

</dd> <dt>

1046 (0x416)
</dt> <dd>

Portugués – Brasil

</dd> <dt>

1047 (0x417)
</dt> <dd>

Rhaeto-Romanic

</dd> <dt>

1048 (0x418)
</dt> <dd>

Rumano

</dd> <dt>

1049 (0x419)
</dt> <dd>

Ruso

</dd> <dt>

1050 (0x41A)
</dt> <dd>

Croata

</dd> <dt>

1051 (0x41B)
</dt> <dd>

Eslovaco

</dd> <dt>

1052 (0x41C)
</dt> <dd>

Albanés

</dd> <dt>

1053 (0x41D)
</dt> <dd>

Sueco

</dd> <dt>

1054 (0x41E)
</dt> <dd>

Tailandés

</dd> <dt>

1055 (0x41F)
</dt> <dd>

Turco

</dd> <dt>

1056 (0x420)
</dt> <dd>

Urdu

</dd> <dt>

1057 (0x421)
</dt> <dd>

Indonesio

</dd> <dt>

1058 (0x422)
</dt> <dd>

Ucraniano

</dd> <dt>

1059 (0x423)
</dt> <dd>

Bielorruso

</dd> <dt>

1060 (0x424)
</dt> <dd>

Esloveno

</dd> <dt>

1061 (0x425)
</dt> <dd>

Estonio

</dd> <dt>

1062 (0x426)
</dt> <dd>

Letón

</dd> <dt>

1063 (0x427)
</dt> <dd>

Lituano

</dd> <dt>

1065 (0x429)
</dt> <dd>

Persa

</dd> <dt>

1066 (0x42A)
</dt> <dd>

Vietnamita

</dd> <dt>

1069 (0x42D)
</dt> <dd>

Vasco (España)

</dd> <dt>

1070 (0x42E)
</dt> <dd>

Serbio

</dd> <dt>

1071 (0x42F)
</dt> <dd>

Nordeste (Norte de Nordeste)

</dd> <dt>

1072 (0x430)
</dt> <dd>

Sutu

</dd> <dt>

1073 (0x431)
</dt> <dd>

Tsonga

</dd> <dt>

1074 (0x432)
</dt> <dd>

Setswana

</dd> <dt>

1076 (0x434)
</dt> <dd>

Xhosa

</dd> <dt>

1077 (0x435)
</dt> <dd>

Zulú

</dd> <dt>

1078 (0x436)
</dt> <dd>

Afrikáans

</dd> <dt>

1080 (0x438)
</dt> <dd>

Faroés

</dd> <dt>

1081 (0x439)
</dt> <dd>

Hindi

</dd> <dt>

1082 (0x43A)
</dt> <dd>

Maltés

</dd> <dt>

1084 (0x43C)
</dt> <dd>

Gaélico Desfila (Reino Unido)

</dd> <dt>

1085 (0x43D)
</dt> <dd>

Yidis

</dd> <dt>

1086 (0x43E)
</dt> <dd>

Malayo – Australia

</dd> <dt>

2049 (0x801)
</dt> <dd>

Árabe – Países Árabes

</dd> <dt>

2052 (0x804)
</dt> <dd>

Chino (simplificado): PRC

</dd> <dt>

2055 (0x807)
</dt> <dd>

Alemán – Suiza

</dd> <dt>

2057 (0x809)
</dt> <dd>

Inglés – Reino Unido

</dd> <dt>

2058 (0x80A)
</dt> <dd>

Español – México

</dd> <dt>

2060 (0x80C)
</dt> <dd>

Francés : Alemania

</dd> <dt>

2064 (0x810)
</dt> <dd>

Italiano – Suiza

</dd> <dt>

2067 (0x813)
</dt> <dd>

Neerlandés : Alemania

</dd> <dt>

2068 (0x814)
</dt> <dd>

Noruego : Nyno norwegian

</dd> <dt>

2070 (0x816)
</dt> <dd>

Portugués – Portugal

</dd> <dt>

2072 (0x818)
</dt> <dd>

Mosso – Reinoso

</dd> <dt>

2073 (0x819)
</dt> <dd>

Ruso: Rusia

</dd> <dt>

2074 (0x81A)
</dt> <dd>

Serbio – latino

</dd> <dt>

2077 (0x81D)
</dt> <dd>

Sueco – Estados Unidos

</dd> <dt>

3073 (0xC01)
</dt> <dd>

Árabe : Arábigo

</dd> <dt>

3076 (0xC04)
</dt> <dd>

Chino (tradicional): RAE de Hong Kong

</dd> <dt>

3079 (0xC07)
</dt> <dd>

Alemán : Francia

</dd> <dt>

3081 (0xC09)
</dt> <dd>

Inglés : Australia

</dd> <dt>

3082 (0xC0A)
</dt> <dd>

Español: ordenación internacional

</dd> <dt>

3084 (0xC0C)
</dt> <dd>

Francés – Canadá

</dd> <dt>

3098 (0xC1A)
</dt> <dd>

Serbio: cirílico

</dd> <dt>

4097 (0x1001)
</dt> <dd>

Árabe : Infiesa

</dd> <dt>

4100 (0x1004)
</dt> <dd>

Chino (simplificado): Singapur

</dd> <dt>

4103 (0x1007)
</dt> <dd>

Alemán: Alemania: Alemania

</dd> <dt>

4105 (0x1009)
</dt> <dd>

Inglés – Canadá

</dd> <dt>

4106 (0x100A)
</dt> <dd>

Español: España

</dd> <dt>

4108 (0x100C)
</dt> <dd>

Francés : Suiza

</dd> <dt>

5121 (0x1401)
</dt> <dd>

Árabe: insólo

</dd> <dt>

5127 (0x1407)
</dt> <dd>

German – Liechtenstein

</dd> <dt>

5129 (0x1409)
</dt> <dd>

Inglés : Nueva Zelanda

</dd> <dt>

5130 (0x140A)
</dt> <dd>

Español : Costa Rica

</dd> <dt>

5132 (0x140C)
</dt> <dd>

Francés: Conste

</dd> <dt>

6145 (0x1801)
</dt> <dd>

Árabe : Francia

</dd> <dt>

6153 (0x1809)
</dt> <dd>

Inglés – Irlanda

</dd> <dt>

6154 (0x180A)
</dt> <dd>

Español : España

</dd> <dt>

7169 (0x1C01)
</dt> <dd>

Árabe: insondía

</dd> <dt>

7177 (0x1C09)
</dt> <dd>

Inglés – Sudáfrica

</dd> <dt>

7178 (0x1C0A)
</dt> <dd>

Español – República De Corea del Suba

</dd> <dt>

8193 (0x2001)
</dt> <dd>

Árabe : Omán

</dd> <dt>

8201 (0x2009)
</dt> <dd>

English – Jamaica

</dd> <dt>

8202 (0x200A)
</dt> <dd>

Español: España

</dd> <dt>

9217 (0x2401)
</dt> <dd>

Árabe – Países Árabes

</dd> <dt>

9226 (0x240A)
</dt> <dd>

Español : España

</dd> <dt>

10241 (0x2801)
</dt> <dd>

Árabe – Rusia

</dd> <dt>

10249 (0x2809)
</dt> <dd>

Inglés : Leal

</dd> <dt>

10250 (0x280A)
</dt> <dd>

Español – País

</dd> <dt>

11265 (0x2C01)
</dt> <dd>

Árabe – Surábigo

</dd> <dt>

11273 (0x2C09)
</dt> <dd>

English – Trinidad

</dd> <dt>

11274 (0x2C0A)
</dt> <dd>

Español : Argentina

</dd> <dt>

12289 (0x3001)
</dt> <dd>

Árabe : insocenario

</dd> <dt>

12298 (0x300A)
</dt> <dd>

Español – Ecuatoriano

</dd> <dt>

13313 (0x3401)
</dt> <dd>

Árabe – Países Árabes

</dd> <dt>

13322 (0x340A)
</dt> <dd>

Español: México

</dd> <dt>

14337 (0x3801)
</dt> <dd>

Árabe : Ee. UU.

</dd> <dt>

14346 (0x380A)
</dt> <dd>

Español: España

</dd> <dt>

15361 (0x3C01)
</dt> <dd>

Árabe – Surábigo

</dd> <dt>

15370 (0x3C0A)
</dt> <dd>

Español: España

</dd> <dt>

16385 (0x4001)
</dt> <dd>

Árabe – Países Árabes

</dd> <dt>

16394 (0x400A)
</dt> <dd>

Español: Argentina

</dd> <dt>

17418 (0x440A)
</dt> <dd>

Español: El País

</dd> <dt>

18442 (0x480A)
</dt> <dd>

Español: Nociones

</dd> <dt>

19466 (0x4C0A)
</dt> <dd>

Español: Asínco

</dd> <dt>

20490 (0x500A)
</dt> <dd>

Español: Puerto Rico

</dd> </dl>

</dd> <dt>

**OSProductSuite**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ ProductOptions \| ProductSuite"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Small Business", "Enterprise", "BackOffice", "Communication Server", "Terminal Server", "Small Business(Restricted)", "Embedded NT", "Data Center")
</dt> </dl>

Adiciones de productos del sistema instalados y con licencia al sistema operativo. Por ejemplo, el valor de 146 (0x92) para **OSProductSuite** indica Enterprise, Terminal Services y Data Center (bits uno, cuatro y siete conjuntos). En la lista siguiente se enumeran los valores posibles.

<dt>

1 (0x1)
</dt> <dd>

Microsoft Small Business Server se instaló una vez, pero puede que se haya actualizado a otra versión de Windows.

</dd> <dt>

2 (0x2)
</dt> <dd>

Windows Server 2008 Enterprise está instalado.

</dd> <dt>

4 (0x4)
</dt> <dd>

Windows Los componentes de BackOffice están instalados.

</dd> <dt>

8 (0x8)
</dt> <dd>

Communication Server está instalado.

</dd> <dt>

16 (0x10)
</dt> <dd>

Terminal Services está instalado.

</dd> <dt>

32 (0x20)
</dt> <dd>

Microsoft Small Business Server se instala con la licencia de cliente restrictiva.

</dd> <dt>

64 (0x40)
</dt> <dd>

Windows Embedded está instalado.

</dd> <dt>

128 (0x80)
</dt> <dd>

Se instala una edición datacenter.

</dd> <dt>

256 (0x100)
</dt> <dd>

Terminal Services está instalado, pero solo se admite una sesión interactiva.

</dd> <dt>

512 (0x200)
</dt> <dd>

Windows Home Edition está instalado.

</dd> <dt>

1024 (0x400)
</dt> <dd>

Web Server Edition está instalado.

</dd> <dt>

8192 (0x2000)
</dt> <dd>

Storage Server Edition está instalado.

</dd> <dt>

16384 (0x4000)
</dt> <dd>

Compute Cluster Edition está instalado.

</dd> </dl>

</dd> <dt>

**OSType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")
</dt> </dl>

Tipo de sistema operativo. En la lista siguiente se identifican los valores posibles.

Esta propiedad se hereda de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1)


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span id="MACOS"></span><span id="macos"></span>**MACOS** (2)


</dt> <dd>

Macros

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Unix digital** (6)


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)


</dt> <dd></dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span id="AIX"></span><span id="aix"></span>**AIX** (9)


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span id="MVS"></span><span id="mvs"></span>**MVS** (10)


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span id="OS400"></span><span id="os400"></span>**OS400** (11)


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span id="OS_2"></span><span id="os_2"></span>**SO/2** (12)


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span id="WIN95"></span><span id="win95"></span>**WIN95** (16)


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span id="WIN98"></span><span id="win98"></span>**WIN98** (17)


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span id="WINCE"></span><span id="wince"></span>**WINCE** (19)


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)


</dt> <dd></dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span id="OSF"></span><span id="osf"></span>**OSF** (22)


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span id="IRIX"></span><span id="irix"></span>**IIONES** (28)


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)


</dt> <dd>

Solaris

</dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span id="U6000"></span><span id="u6000"></span>**U6000** (31)


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)


</dt> <dd></dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)


</dt> <dd></dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span id="LINUX"></span><span id="linux"></span>**LINUX** (36)


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Estaciones** (37)


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span id="OS9"></span><span id="os9"></span>**OS9** (45)


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel de MACH** (46)


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span id="QNX"></span><span id="qnx"></span>**QNX** (48)


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

<span id="OS_390"></span><span id="os_390"></span>**OS/390** (60)


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span id="VSE"></span><span id="vse"></span>**VSE** (61)


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span id="TPF"></span><span id="tpf"></span>**TPF** (62)


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherTypeDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OSType**")
</dt> </dl>

Descripción adicional de la versión actual del sistema operativo.

Esta propiedad se hereda de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**PAEEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es True,** el sistema operativo que se ejecuta en procesadores Intel habilita las extensiones de dirección física (PAE). PAE permite a las aplicaciones abordar más de 4 GB de memoria física. Cuando se habilita PAE, el sistema operativo usa la traducción de direcciones lineales de tres niveles en lugar de dos niveles. Proporcionar más memoria física a una aplicación reduce la necesidad de intercambiar memoria al archivo de página y aumenta el rendimiento. Para habilitar, PAE, use el modificador "/PAE" en el Boot.ini archivo. Para obtener más información sobre la característica extensión de dirección física, vea <https://Go.Microsoft.Com/FWLink/p/?LinkID=45912> .

</dd> <dt>

**PlusProductID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \| Plus! ProductId")
</dt> </dl>

No compatible.

</dd> <dt>

**PlusVersionNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \| Plus! VersionNumber")
</dt> </dl>

No compatible.

</dd> <dt>

**PortableOperatingSystem**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si el sistema operativo se ha arrancado desde un dispositivo USB externo. Si es true, el sistema operativo ha detectado que arranca en un dispositivo de almacenamiento conectado localmente compatible.

**Windows Server 2008 R2, Windows 7, Windows Server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows 8 y Windows Server 2012.

</dd> <dt>

**Principal**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Especifica si se trata del sistema operativo principal.

</dd> <dt>

**ProductType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Información adicional del sistema.

<dt>

<span id="Work_Station"></span><span id="work_station"></span><span id="WORK_STATION"></span>

**Estación de trabajo** (1)


</dt> <dd></dd> <dt>

<span id="Domain_Controller"></span><span id="domain_controller"></span><span id="DOMAIN_CONTROLLER"></span>

**Controlador de dominio** (2)


</dt> <dd></dd> <dt>

<span id="Server"></span><span id="server"></span><span id="SERVER"></span>

**Servidor** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**QuantumLength**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ PriorityControl \| Win32PrioritySeparation")
</dt> </dl>

No compatible

**Windows Server 2008 y Windows Vista: **

La **propiedad QuantumLength** define el número de tics de reloj por cuántico. Un cuántico es una unidad de tiempo de ejecución que el programador puede dar a una aplicación antes de cambiar a otras aplicaciones. Cuando un subproceso ejecuta un cuántico, el kernel lo adelanta y lo mueve al final de una cola para las aplicaciones con las mismas prioridades. La longitud real del cuántico de un subproceso varía según las distintas plataformas Windows subprocesos. Solo Windows NT/Windows 2000.

Los valores posibles son.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="One_tick"></span><span id="one_tick"></span><span id="ONE_TICK"></span>

**Un tic** (1)


</dt> <dd></dd> <dt>

<span id="Two_ticks"></span><span id="two_ticks"></span><span id="TWO_TICKS"></span>

**Dos pasos** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**QuantumType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

No compatible

**Windows Server 2008 y Windows Vista: **

La **propiedad QuantumType** especifica los cuánticos de longitud fija o variable. Windows de forma predeterminada en los cuánticos de longitud variable, donde la aplicación en primer plano tiene un cuanto más largo que las aplicaciones en segundo plano. Windows El servidor tiene como valor predeterminado los cuánticos de longitud fija. Un cuántico es una unidad de tiempo de ejecución que el programador puede dar a una aplicación antes de cambiar a otra aplicación. Cuando un subproceso ejecuta un cuántico, el kernel lo adelanta y lo mueve al final de una cola para las aplicaciones con las mismas prioridades. La longitud real del cuántico de un subproceso varía según las distintas plataformas Windows subprocesos.

Los valores posibles son.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

**Corregido** (1)


</dt> <dd></dd> <dt>

<span id="Variable"></span><span id="variable"></span><span id="VARIABLE"></span>

**Variable** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**RegisteredUser**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \| RegisteredOwner")
</dt> </dl>

Nombre del usuario registrado del sistema operativo.

Ejemplo: "Ben Smith"

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \| ProductId")
</dt> </dl>

Número de identificación de serie del producto del sistema operativo.

Ejemplo: "10497-OEM-0031416-71674"

</dd> <dt>

**ServicePackMajorVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Información del sistema Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **wServicePackMajor**")
</dt> </dl>

Número de versión principal del Service Pack instalado en el sistema del equipo. Si no se ha instalado ningún Service Pack, el valor es 0 (cero).

</dd> <dt>

**ServicePackMinorVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Información del sistema Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **wServicePackMinor**")
</dt> </dl>

Número de versión secundaria del Service Pack instalado en el sistema del equipo. Si no se ha instalado ningún Service Pack, el valor es 0 (cero).

</dd> <dt>

**SizeStoredInPagingFiles**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. Dmtf \| System Memory Configuración \| 001.3"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")
</dt> </dl>

Número total de kilobytes que se pueden almacenar en los archivos de paginación del sistema operativo: 0 (cero) indica que no hay archivos de paginación. Tenga en cuenta que este número no representa el tamaño físico real del archivo de paginación en el disco.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/previous-versions//aa393262(v=vs.85))

Esta propiedad se hereda de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Estado actual del objeto. Se pueden definir varios estados operativos y no operativos. Los estados operativos incluyen: "Ok", "Degraded" y "Pred Fail" (un elemento, como una unidad de disco duro habilitada para SMART, puede funcionar correctamente, pero predice un error en un futuro próximo). Los estados no operativo incluyen: "Error", "Starting", "Stopping" y "Service". El estado del servicio se aplica al trabajo administrativo, como la resilvering reflejada de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo. No todo este trabajo está en línea, pero el elemento administrado no es "correcto" ni está en uno de los demás estados.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

<dt>

<span id="OK"></span><span id="ok"></span>

**Ok** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Error** ("Error")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("Degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** ("Desconocido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Error de pred** ("error previo")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**A partir** de ("Starting")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Detención** ("Deteniendo")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servicio** ("Servicio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Estresado** ("estresado")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sin contacto** ("Sin contacto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Comm perdido** ("Comm perdido")


</dt> <dd></dd> </dl>

</dd> <dt>

**SuiteMask**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**BitMap**](../wmisdk/standard-qualifiers.md) ("0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "10"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Windows Server, Small Business Edition", "Windows Server, Enterprise Edition", "Windows Server, Backoffice Edition", "Windows Server, Communications Edition", "Microsoft Terminal Services", "Windows Server, Small Business Edition Restricted", "Windows Embedded", "Windows Server, Datacenter Edition", "Single User", "Windows Home Edition", "Windows Server, Web Edition")
</dt> </dl>

Marcas de bits que identifican los conjuntos de productos disponibles en el sistema.

Por ejemplo, para especificar Personal y BackOffice, establezca **SuiteMask** `4 | 512` en o `516` .

<dt>

1
</dt> <dd>

Pequeñas empresas

</dd> <dt>

2
</dt> <dd>

Enterprise

</dd> <dt>

4
</dt> <dd>

Backoffice

</dd> <dt>

8
</dt> <dd>

Comunicaciones

</dd> <dt>

16
</dt> <dd>

Terminal Services

</dd> <dt>

32
</dt> <dd>

Pequeña empresa restringida

</dd> <dt>

64
</dt> <dd>

Embedded Edition

</dd> <dt>

128
</dt> <dd>

Datacenter Edition

</dd> <dt>

256
</dt> <dd>

Usuario único

</dd> <dt>

512
</dt> <dd>

Home Edition

</dd> <dt>

1024
</dt> <dd>

Web Server Edition

</dd> </dl>

</dd> <dt>

**SystemDevice**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Registry Functions \| [**GetPrivateProfileString**](/windows/win32/api/winbase/nf-winbase-getprivateprofilestring)Paths \| \| TargetDevice")
</dt> </dl>

Partición de disco físico en la que está instalado el sistema operativo.

</dd> <dt>

**SystemDirectory**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Información del sistema Functions [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya))
</dt> </dl>

Directorio del sistema operativo.

Ejemplo: "C: \\ WINDOWS \\ SYSTEM32"

</dd> <dt>

**SystemDrive**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Letra de la unidad de disco en la que reside el sistema operativo. Ejemplo: "C:"

</dd> <dt>

**TotalSwapSpaceSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")
</dt> </dl>

Espacio de intercambio total en kilobytes. Este valor puede ser **NULL** (sin especificar) si el espacio de intercambio no se distingue de los archivos de página. Sin embargo, algunos sistemas operativos distinguen estos conceptos. Por ejemplo, en UNIX, se pueden intercambiar procesos completos cuando la lista de páginas libres cae y permanece por debajo de una cantidad especificada.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Esta propiedad se hereda de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**TotalVirtualMemorySize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")
</dt> </dl>

Número, en kilobytes, de memoria virtual. Por ejemplo, esto se puede calcular agregando la cantidad de RAM total a la cantidad de espacio de paginación, es decir, agregando la cantidad de memoria en o agregada por el sistema del equipo a la propiedad **SizeStoredInPagingFiles**.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Esta propiedad se hereda de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**TotalVisibleMemorySize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")
</dt> </dl>

Cantidad total, en kilobytes, de memoria física disponible para el sistema operativo. Este valor no indica necesariamente la cantidad verdadera de memoria física, sino lo que se notifica al sistema operativo como disponible para él.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Esta propiedad se hereda de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("Version"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Información del sistema Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| dwMajorVersion, dwMinorVersion")
</dt> </dl>

Número de versión del sistema operativo.

Ejemplo: "4.0"

</dd> <dt>

**WindowsDirectory**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Información del sistema Functions \| [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)")
</dt> </dl>

Windows directorio del sistema operativo.

Ejemplo: "C: \\ WINDOWS"

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ OperatingSystem de Win32** se deriva de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

Cualquier sistema operativo que se pueda instalar en un equipo que pueda ejecutar un sistema operativo basado en Windows es un descendiente o miembro de esta clase. **Win32 \_ OperatingSystem** es una clase singleton. Para obtener la instancia única, use "@" para la clave.

A diferencia de la mayoría de las demás clases WMI generadas por MgmtClassGen, el método **OperatingSystem.CreateInstance**() devolverá un objeto **OperatingSystem en** blanco. Por lo tanto, si usa C \# con MgmtClassGen, puede usar el código siguiente:


```CSharp
WMI.OperatingSystem os = new ROOT.CIMV2.win32.OperatingSystem();
```



## <a name="examples"></a>Ejemplos

Puede encontrar un ejemplo de VBScript que obtiene datos del sistema operativo y del procesador de [**Win32 \_ ComputerSystem,**](win32-computersystem.md) [**Win32 \_ Processor**](win32-processor.md)y **Win32 \_ OperatingSystem** en los ejemplos del tema Procesador [**Win32. \_**](win32-processor.md)

El [ejemplo Generate Exchange Environment Reports using PowerShell](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) PowerShell (Generar informes de entorno de Exchange con PowerShell de PowerShell) en la Galería de TechNet usa una clase **\_ OperatingSystem de Win32** como parte de una aplicación más grande para generar informes de entorno de intercambio.

El [ejemplo Get Server Uptime Using WMI](https://Gallery.TechNet.Microsoft.Com/Get-Server-Uptime-Using-WMI-15aaa8ac) (Obtener tiempo de actividad del servidor mediante WMI) de la Galería de TechNet usa la propiedad **LastBootupTime** para determinar cuánto tiempo ha estado activo el servidor. El ejemplo también usa la opción de tiempo de espera para asegurarse de que la llamada WMI no se bloqueo.

En el ejemplo de código VBScript de WMI [Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) de la Galería de TechNet se usa la clase **\_ OperatingSystem de Win32** para recuperar información del sistema operativo de varios equipos remotos.

El siguiente script obtiene las instancias de **Win32 \_ OperatingSystem** en el espacio de nombres \\ "ROOT CIMv2" predeterminado y, a continuación, muestra información sobre el sistema operativo.


```VB
On Error Resume Next
' Connect to WMI and obtain instances of Win32_OperatingSystem
For Each objOS in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

WScript.Echo "Name = " & objOS.Caption & "Version = " & objOS.Version &VBCR _
           & "Registered User = " & objOS.RegisteredUser &VBCR _
           & "Manufacturer = " & objOS.Manufacturer      
Next

if Err <> 0 Then
    WScript.Echo Err.Description
    Err.Clear
End if
```



El siguiente ejemplo de código de PowerShell muestra toda la información operativa sobre el sistema operativo actual.


```PowerShell
# get instance
$os = Get-WmiObject Win32_OperatingSystem

# output information:
"The class has {0} properties" -f $os.properties.count
"Details on this class:"
$os | Format-List *
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Sistema operativo CIM**](cim-operatingsystem.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> <dt>

[Tareas wmi: sistemas operativos](../wmisdk/wmi-tasks--operating-systems.md)
</dt> <dt>

[Tareas wmi: hardware del equipo](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> <dt>

[Tareas wmi: administración de escritorio](../wmisdk/wmi-tasks--desktop-management.md)
</dt> </dl>

 

 
