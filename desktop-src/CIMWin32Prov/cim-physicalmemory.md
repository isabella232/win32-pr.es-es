---
description: La clase Cim PhysicalMemory representa dispositivos de memoria de bajo nivel, como SIMMS, DIMM, chips de memoria sin \_ procesar, entre otros.
ms.assetid: a25c5f00-cd85-42e6-9b26-8e9380b3c73b
ms.tgt_platform: multiple
title: CIM_PhysicalMemory clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalMemory
- CIM_PhysicalMemory.BankLabel
- CIM_PhysicalMemory.Capacity
- CIM_PhysicalMemory.Caption
- CIM_PhysicalMemory.CreationClassName
- CIM_PhysicalMemory.DataWidth
- CIM_PhysicalMemory.Description
- CIM_PhysicalMemory.FormFactor
- CIM_PhysicalMemory.HotSwappable
- CIM_PhysicalMemory.InstallDate
- CIM_PhysicalMemory.InterleavePosition
- CIM_PhysicalMemory.Manufacturer
- CIM_PhysicalMemory.MemoryType
- CIM_PhysicalMemory.Model
- CIM_PhysicalMemory.Name
- CIM_PhysicalMemory.OtherIdentifyingInfo
- CIM_PhysicalMemory.PartNumber
- CIM_PhysicalMemory.PositionInRow
- CIM_PhysicalMemory.PoweredOn
- CIM_PhysicalMemory.Removable
- CIM_PhysicalMemory.Replaceable
- CIM_PhysicalMemory.SerialNumber
- CIM_PhysicalMemory.SKU
- CIM_PhysicalMemory.Speed
- CIM_PhysicalMemory.Status
- CIM_PhysicalMemory.Tag
- CIM_PhysicalMemory.TotalWidth
- CIM_PhysicalMemory.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1b85a4e80588b98625f166f76c09aff9d52b114adcee4507eb7b81957746d88e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080489"
---
# <a name="cim_physicalmemory-class"></a>\_Clase PhysicalMemory de CIM

La **clase \_ Cim PhysicalMemory** representa dispositivos de memoria de bajo nivel, como SIMMS, DIMM, chips de memoria sin procesar, entre otros.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintaxis siguiente se simplifica a partir Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[abstract, UUID("{FAF76B7B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalMemory : CIM_Chip
{
  string   BankLabel;
  uint64   Capacity;
  string   Caption;
  string   CreationClassName;
  uint16   DataWidth;
  string   Description;
  uint16   FormFactor;
  boolean  HotSwappable;
  datetime InstallDate;
  uint32   InterleavePosition;
  string   Manufacturer;
  uint16   MemoryType;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  uint32   PositionInRow;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  uint32   Speed;
  string   Status;
  string   Tag;
  uint16   TotalWidth;
  string   Version;
};
```

## <a name="members"></a>Miembros

La **clase \_ PhysicalMemory** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ PhysicalMemory** de CIM tiene estas propiedades.

<dl> <dt>

**BankLabel**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Dispositivo de memoria DMTF \| \| 002.4")
</dt> </dl>

Banco etiquetado en el que se encuentra la memoria. Por ejemplo, "Bank 0" o "Bank A".

</dd> <dt>

**Capacity**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Capacidad total de la memoria física, en bytes.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descripción textual del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**\_ clave CIM,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nombre de la clase o subclase usada en la creación de una instancia de . Cuando se usa con otras propiedades clave de la clase , esta propiedad permite identificar de forma única todas las instancias de la clase y sus subclases.

Esta propiedad se hereda de [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**DataWidth**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")
</dt> </dl>

Ancho de datos de la memoria física, en bits. Un ancho de datos de 0 (cero) y un ancho total de 8, indica que la memoria se usa únicamente para proporcionar bits de corrección de errores.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Descripción textual del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**FormFactor**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("FormFactor"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Dispositivo de memoria DMTF \| \| 002.6")
</dt> </dl>

Factor de forma de implementación del chip. Por ejemplo, se pueden especificar valores como SIMM, TSOP o PGA.

Esta propiedad se hereda del [**\_ chip CIM**](cim-chip.md).

<dt>

0
</dt> <dd>

Unknown

</dd> <dt>

1
</dt> <dd>

Otros

</dd> <dt>

2
</dt> <dd>

Sip

</dd> <dt>

3
</dt> <dd>

DIP

</dd> <dt>

4
</dt> <dd>

ZIP

</dd> <dt>

5
</dt> <dd>

SOJ

</dd> <dt>

6
</dt> <dd>

Propietario

</dd> <dt>

7
</dt> <dd>

Simm

</dd> <dt>

8
</dt> <dd>

Dimm

</dd> <dt>

9
</dt> <dd>

Tsop

</dd> <dt>

10
</dt> <dd>

Pga

</dd> <dt>

11
</dt> <dd>

Rimm

</dd> <dt>

12
</dt> <dd>

Sodimm

</dd> <dt>

13
</dt> <dd>

SRIMM

</dd> <dt>

14
</dt> <dd>

Smd

</dd> <dt>

15
</dt> <dd>

SSMP

</dd> <dt>

16
</dt> <dd>

Qfp

</dd> <dt>

17
</dt> <dd>

Tqfp

</dd> <dt>

18
</dt> <dd>

Soic

</dd> <dt>

19
</dt> <dd>

Lcc

</dd> <dt>

20
</dt> <dd>

Plcc

</dd> <dt>

21
</dt> <dd>

Bga

</dd> <dt>

22
</dt> <dd>

FPBGA

</dd> <dt>

23
</dt> <dd>

LGA

</dd> </dl>

</dd> <dt>

**HotSwappable**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** el paquete se puede intercambiar en caliente. Un paquete físico se puede intercambiar en caliente si el elemento se puede reemplazar por uno físicamente diferente (pero equivalente) mientras el paquete que lo contiene está activado. Por ejemplo, un componente de ventilador se puede diseñar para intercambiarse en caliente. Todos los componentes que se pueden intercambiar en caliente son intrínsecamente extraíbles y reemplazables.

Esta propiedad se hereda de [**CIM \_ PhysicalComponent.**](cim-physicalcomponent.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Fecha de instalación")
</dt> </dl>

Fecha y hora en que se instaló el objeto. Esta propiedad no necesita un valor para indicar que el objeto está instalado.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**InterleavePosition**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Direcciones asignadas del dispositivo de memoria DMTF \| \| 001.7")
</dt> </dl>

Posición de la memoria física en una intercalación. Un valor de 0 indica no intercalado, 1 indica la primera posición, 2 indica la segunda posición, y así sucesivamente. Por ejemplo, en una intercalación 2:1, un valor de 1 indica que la memoria está en la posición uniforme.

</dd> <dt>

**Fabricante**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nombre de la organización responsable de generar el elemento físico. Para obtener más información, vea la **propiedad Vendor** del [**producto CIM \_**](cim-product.md).

Esta propiedad se hereda de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**MemoryType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Dispositivo de memoria DMTF \| \| 002.9")
</dt> </dl>

Tipo de memoria física.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

**DRAM** (2)


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

**DRAM sincrónica** (3)


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

**DRAM de caché** (4)


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

**EDO** (5)


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

**EDRAM** (6)


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

**VRAM** (7)


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

**SRAM** (8)


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

**RAM** (9)


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

**ROM** (10)


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

**Flash** (11)


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

**EEPROM** (12)


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

**FEPROM** (13)


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

**EPROM** (14)


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

**CDRAM** (15)


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

**3DRAM** (16)


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

**SDRAM** (17)


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

**SGRAM** (18)


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

**RDRAM** (19)


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

**DDR** (20)


</dt> <dd></dd> <dt>

<span id="DDR2"></span><span id="ddr2"></span>

**DDR2** (21)


</dt> <dd></dd> <dt>

<span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>

**DDR2 FB-DIM** (22)


</dt> <dd></dd> </dl>

</dd> <dt>

**Modelo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Nombre por el que se suele conocer el elemento físico.

Esta propiedad se hereda de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Etiqueta por la que se conoce el objeto. Cuando se subclasifica, esta propiedad se puede invalidar para que sea una propiedad de clave.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Datos adicionales, más allá de la información de etiquetas de recurso, que se pueden usar para identificar un elemento físico. Un ejemplo son los datos de código de barras asociados a un elemento , que también tiene una etiqueta de recurso. Tenga en cuenta que si solo hay datos de código de barras disponibles y es único y se puede usar como clave de elemento, esta propiedad sería NULL y los datos de código de barras se usarían como clave de clase en la **propiedad Tag.** Esta propiedad se hereda de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Partnumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Número de parte asignado por la organización que produjo o fabricó el elemento físico.

Esta propiedad se hereda de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**PositionInRow**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Direcciones asignadas del dispositivo de memoria DMTF \| \| 001.6")
</dt> </dl>

Posición de la memoria física en una fila. Por ejemplo, si se necesitan dos dispositivos de memoria de 8 bits para formar una fila de 16 bits, un valor de 2 indica que la memoria es el segundo dispositivo. Un valor de 0 es un valor no válido para esta propiedad.

</dd> <dt>

**PoweredOn**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** el elemento físico está encendido.

Esta propiedad se hereda de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Extraíble**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** este elemento está diseñado para su entrada y salida del contenedor físico en el que se encuentra normalmente, sin afectar a la función del empaquetado general. Un paquete se considera extraíble incluso si la alimentación debe estar desactivada para realizar la eliminación. Si la alimentación puede estar encendido y se ha quitado el paquete, el elemento es extraíble y se puede intercambiar en caliente. Por ejemplo, un chip de procesador no degradado es extraíble.

Esta propiedad se hereda de [**CIM \_ PhysicalComponent.**](cim-physicalcomponent.md)

</dd> <dt>

**Reemplazable**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** es posible reemplazar el elemento por uno físicamente diferente. Por ejemplo, algunos sistemas informáticos permiten que el chip del procesador principal se actualice a una de las especificaciones de reloj más altas. En este caso, se dice que el procesador es reemplazable. Todos los componentes extraíbles son inherentemente reemplazables.

Esta propiedad se hereda de [**CIM \_ PhysicalComponent.**](cim-physicalcomponent.md)

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Número asignado por el fabricante que se usa para identificar el elemento físico.

Esta propiedad se hereda de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**SKU**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Número de unidad de mantenimiento de existencias para el elemento físico.

Esta propiedad se hereda de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Velocidad**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("nanosegundos")
</dt> </dl>

Velocidad de la memoria física, en nanosegundos.

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Estado actual del objeto. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Los valores son los siguientes:

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

**Unknown** ("Unknown")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Error de pred** ("error previo")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Starting** ("Starting")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Detención** ("Detención")


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

**Tag**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**\_ Clave CIM,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Cadena arbitraria que identifica de forma única el elemento físico y actúa como clave del elemento. Esta propiedad puede contener información, como datos de etiqueta de recurso o número de serie. La clave de [**CIM \_ PhysicalElement**](cim-physicalelement.md) se coloca muy alta en la jerarquía de objetos para identificar de forma independiente el hardware o la entidad, independientemente de la colocación física en (o en) gabinetes, adaptadores, y así sucesivamente. Por ejemplo, un componente extraíble que se puede intercambiar en caliente se puede tomar de su paquete que contiene (ámbito) y no se puede usar temporalmente. El objeto sigue existiendo e incluso se puede insertar en un contenedor de ámbito diferente. La clave de un elemento físico es una cadena arbitraria que se define independientemente de la ubicación o la jerarquía orientada a la ubicación.

Esta propiedad se hereda de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**TotalWidth**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Dispositivo de memoria DMTF \| \| 002.7"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")
</dt> </dl>

Ancho total, en bits, de la memoria física, incluidos los bits de corrección de errores o de comprobación. Si no hay bits de corrección de errores, el valor de esta propiedad debe coincidir con el especificado para **la propiedad DataWidth.**

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Versión del elemento físico.

Esta propiedad se hereda de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ PhysicalMemory** de CIM se deriva de [**CIM \_ Chip**](cim-chip.md).

WMI no implementa esta clase. Para obtener clases WMI derivadas de **\_ CIM PhysicalMemory,** vea [Clases win32.](win32-provider.md)

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CIM \_ Chip**](cim-chip.md)
</dt> </dl>

 

