---
description: Representa un dispositivo que puede usar medios para almacenar y recuperar datos.
ms.assetid: c63b1731-dbc0-4e5e-acb8-cd91b5569dd2
title: CIM_MediaAccessDevice (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice
- CIM_MediaAccessDevice.Capabilities
- CIM_MediaAccessDevice.CapabilityDescriptions
- CIM_MediaAccessDevice.ErrorMethodology
- CIM_MediaAccessDevice.CompressionMethod
- CIM_MediaAccessDevice.NumberOfMediaSupported
- CIM_MediaAccessDevice.MaxMediaSize
- CIM_MediaAccessDevice.DefaultBlockSize
- CIM_MediaAccessDevice.MaxBlockSize
- CIM_MediaAccessDevice.MinBlockSize
- CIM_MediaAccessDevice.NeedsCleaning
- CIM_MediaAccessDevice.MediaIsLocked
- CIM_MediaAccessDevice.Security
- CIM_MediaAccessDevice.LastCleaned
- CIM_MediaAccessDevice.MaxAccessTime
- CIM_MediaAccessDevice.UncompressedDataRate
- CIM_MediaAccessDevice.LoadTime
- CIM_MediaAccessDevice.UnloadTime
- CIM_MediaAccessDevice.MountCount
- CIM_MediaAccessDevice.TimeOfLastMount
- CIM_MediaAccessDevice.TotalMountTime
- CIM_MediaAccessDevice.UnitsDescription
- CIM_MediaAccessDevice.MaxUnitsBeforeCleaning
- CIM_MediaAccessDevice.UnitsUsed
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 616148f6749f3ec00d019a903e8f9046d3aba602
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689620"
---
# <a name="cim_mediaaccessdevice-class-hyper-v-management"></a>CIM_MediaAccessDevice (clase, administración de Hyper-V)

Representa un dispositivo que puede usar medios para almacenar y recuperar datos.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices"), AMENDMENT]
class CIM_MediaAccessDevice : CIM_LogicalDevice
{
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   ErrorMethodology;
  string   CompressionMethod;
  uint32   NumberOfMediaSupported;
  uint64   MaxMediaSize;
  uint64   DefaultBlockSize;
  uint64   MaxBlockSize;
  uint64   MinBlockSize;
  boolean  NeedsCleaning;
  boolean  MediaIsLocked;
  uint16   Security;
  datetime LastCleaned;
  uint64   MaxAccessTime;
  uint32   UncompressedDataRate;
  uint64   LoadTime;
  uint64   UnloadTime;
  uint64   MountCount;
  datetime TimeOfLastMount;
  uint64   TotalMountTime;
  string   UnitsDescription;
  uint64   MaxUnitsBeforeCleaning;
  uint64   UnitsUsed;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ MediaAccessDevice** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **CIM \_ MediaAccessDevice** tiene estos métodos.



| Método                                               | Descripción                                                            |
|:-----------------------------------------------------|:-----------------------------------------------------------------------|
| [**LockMedia**](cim-mediaaccessdevice-lockmedia.md) | Bloquea y desbloquea los medios extraíbles en un dispositivo de acceso a medios.<br/> |



 

### <a name="properties"></a>Propiedades

La clase **CIM \_ MediaAccessDevice** tiene estas propiedades.

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de almacenamiento DMTF \| 001,9 "," MIF. \|Dispositivos de almacenamiento DMTF \| 001,11 "," MIF. \|Dispositivos de almacenamiento DMTF \| 001,12 "," MIF. \|Discos DMTF \| 003,7 "," MIF. \|Disco de host DMTF \| 001,2 "," MIF. \|Disco de host DMTF \| 001,4 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**CapabilityDescriptions**")
</dt> </dl>

Una matriz que contiene las funciones del dispositivo de acceso a medios.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otro** (1)


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

**Acceso secuencial** (2)


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

**Acceso aleatorio** (3)


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

**Admite escritura** (4)


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

**Cifrado** (5)


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

**Compresión** (6)


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

**Admite medios** extraíbles (7)


</dt> <dd></dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

**Limpieza manual** (8)


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

**Limpieza automática** (9)


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

**Notificación inteligente** (10)


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

**Admite medios de doble cara** (11)


</dt> <dd></dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

**Predismount EJECT no requerido** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**Funcionalidades**")
</dt> </dl>

Matriz de descripciones de características para los elementos de la matriz de **funcionalidades** .

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del algoritmo o herramienta que usa el dispositivo para admitir la compresión.

Si no se especifica un tipo de compresión, se puede usar uno de los siguientes valores:

-   La compatibilidad con la compresión "desconocida" es desconocida o no se ha especificado.
-   Se admite la compresión "comprimida", pero el tipo es desconocido o no se ha especificado.
-   "No comprimido" el dispositivo no admite capacidades de compresión.

</dd> <dt>

**DefaultBlockSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **punitivo** ("byte")
</dt> </dl>

Tamaño de bloque predeterminado, en bytes, para el dispositivo.

</dd> <dt>

**ErrorMethodology**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El tipo de detección y corrección de errores admitidos por el dispositivo.

</dd> <dt>

**LastCleaned**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se limpió por última vez el dispositivo.

</dd> <dt>

**LoadTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milisegundos"), **punitivo** ("segundo \* 10 ^-3")
</dt> </dl>

El tiempo que tarda, en milisegundos, para que el dispositivo pueda leer o escribir un medio después de que el dispositivo empiece a cargarse. Por ejemplo, en el caso de las unidades de disco, es el intervalo entre un disco que no gira hasta el disco que informa de que está listo para las operaciones de lectura y escritura. En el caso de las unidades de cinta, esto se inicia cuando se inserta el medio y finaliza cuando la unidad informa de que está listo para una aplicación. Normalmente, se encuentra en el área de inicio de cinta (BOT) de la cinta.

</dd> <dt>

**MaxAccessTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milisegundos"), **punitivo** ("segundo \* 10 ^-3")
</dt> </dl>

El tiempo máximo de acceso del medio, en milisegundos. En el caso de una unidad de disco, representa la búsqueda completa y el retraso de rotación completo. En el caso de las unidades de cinta, representa una búsqueda desde el principio de la cinta hasta el punto más alejado físicamente.

</dd> <dt>

**MaxBlockSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **punitivo** ("byte")
</dt> </dl>

Tamaño máximo del bloque, en bytes, para los medios a los que tiene acceso el dispositivo.

</dd> <dt>

**MaxMediaSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de acceso secuencial \| de DMTF 001,2 "," MIF. \|Disco host DMTF \| 001,5 ")
</dt> </dl>

Tamaño máximo, en kilobytes, de los medios admitidos por este dispositivo.

</dd> <dt>

**MaxUnitsBeforeCleaning**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**UnitsDescription**")
</dt> </dl>

El número máximo de unidades que se pueden usar antes de que se limpie el dispositivo. **UnitsDescription** define el tipo de unidad.

</dd> <dt>

**MediaIsLocked**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

**true** si el medio está bloqueado en el dispositivo y no se puede expulsar; en caso contrario, **false**. En el caso de los dispositivos no extraíbles, este valor debe ser **true**.

</dd> <dt>

**MinBlockSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **punitivo** ("byte")
</dt> </dl>

Tamaño mínimo del bloque, en bytes, para los medios a los que tiene acceso el dispositivo.

</dd> <dt>

**MountCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **contador**
</dt> </dl>

El número de veces que se ha montado el medio para la transferencia de datos o para limpiar el dispositivo. Si el dispositivo no admite medios extraíbles, esta propiedad debe establecerse en cero.

</dd> <dt>

**NeedsCleaning**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

**true** si el dispositivo necesita limpieza; en caso contrario, **false**.

> [!Note]  
> La propiedad **Capabilities** indica si es posible la limpieza manual o automática.

 

</dd> <dt>

**NumberOfMediaSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si el dispositivo admite varios medios individuales, esta propiedad define el número máximo que se puede admitir o insertar.

</dd> <dt>

**Seguridad**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Discos DMTF \| 003,22 ")
</dt> </dl>

La seguridad operativa del dispositivo.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Ninguno** (3)


</dt> <dd></dd> <dt>

<span id="Read_Only"></span><span id="read_only"></span><span id="READ_ONLY"></span>

**Solo lectura** (4)


</dt> <dd></dd> <dt>

<span id="Locked_Out"></span><span id="locked_out"></span><span id="LOCKED_OUT"></span>

**Bloqueado** (5)


</dt> <dd></dd> <dt>

<span id="Boot_Bypass"></span><span id="boot_bypass"></span><span id="BOOT_BYPASS"></span>

**Omisión de arranque** (6)


</dt> <dd></dd> <dt>

<span id="Boot_Bypass_and_Read_Only"></span><span id="boot_bypass_and_read_only"></span><span id="BOOT_BYPASS_AND_READ_ONLY"></span>

**Omisión de arranque y solo lectura** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**TimeOfLastMount**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La fecha y hora más recientes en que se montó el medio en el dispositivo. Esta propiedad solo la usan los dispositivos que admiten medios extraíbles.

</dd> <dt>

**TotalMountTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El tiempo, en segundos, que los medios se han montado para la transferencia de datos o para limpiar el dispositivo. Si el dispositivo no admite medios extraíbles, esta propiedad debe establecerse en cero.

</dd> <dt>

**UncompressedDataRate**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes por segundo"), **punitivo** ("byte/segundo \* 10 ^ 3")
</dt> </dl>

La velocidad de transferencia de datos sostenida en kilobytes en la que el dispositivo puede leer y escribir en un medio. Se trata de una velocidad de datos sin procesar y sostenida. No se deben informar de las tarifas máximas con compresión en esta propiedad.

</dd> <dt>

**UnitsDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**MaxUnitsBeforeCleaning**","**\_ MediaAccessDevice CIM**.**UnitsUsed**")
</dt> </dl>

Describe el tipo de unidad de las propiedades **MaxUnitsBeforeCleaning** y **UnitsUsed** .

</dd> <dt>

**UnitsUsed**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**medidor**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**UnitsDescription**","**\_ MediaAccessDevice CIM**.**MaxUnitsBeforeCleaning**")
</dt> </dl>

El número de unidades utilizadas por el dispositivo. Esta propiedad se usa para determinar cuándo se debe limpiar el dispositivo. **UnitsDescription** define el tipo de unidad.

</dd> <dt>

**UnloadTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milisegundos"), **punitivo** ("segundo \* 10 ^-3")
</dt> </dl>

El tiempo que tarda, en milisegundos, para que el dispositivo pase de la lectura o escritura de archivos multimedia a la descarga. Por ejemplo, en el caso de las unidades de disco, es el intervalo entre un giro de disco a velocidades nominales y un disco que no gira. En el caso de las unidades de cinta, es el momento en que un medio puede pasar de su BOT a ser completamente expulsado y accesible a un elemento selector o operador humano.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LogicalDevice de CIM \_**](cim-logicaldevice.md)
</dt> </dl>

 

