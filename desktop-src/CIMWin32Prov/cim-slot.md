---
description: La clase Ranura CIM \_ representa los conectores en los que se insertan los paquetes.
ms.assetid: bcb1bdb5-fb1a-47ed-9450-dca38edca0eb
ms.tgt_platform: multiple
title: CIM_Slot clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Slot
- CIM_Slot.Caption
- CIM_Slot.ConnectorPinout
- CIM_Slot.ConnectorType
- CIM_Slot.CreationClassName
- CIM_Slot.Description
- CIM_Slot.HeightAllowed
- CIM_Slot.InstallDate
- CIM_Slot.LengthAllowed
- CIM_Slot.Manufacturer
- CIM_Slot.MaxDataWidth
- CIM_Slot.Model
- CIM_Slot.Name
- CIM_Slot.Number
- CIM_Slot.OtherIdentifyingInfo
- CIM_Slot.PartNumber
- CIM_Slot.PoweredOn
- CIM_Slot.PurposeDescription
- CIM_Slot.SerialNumber
- CIM_Slot.SKU
- CIM_Slot.SpecialPurpose
- CIM_Slot.Status
- CIM_Slot.SupportsHotPlug
- CIM_Slot.Tag
- CIM_Slot.ThermalRating
- CIM_Slot.VccMixedVoltageSupport
- CIM_Slot.Version
- CIM_Slot.VppMixedVoltageSupport
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 910fb4a3dcd5d3d95ef524d838781bad8331d33d71fc0af8ebd358ac9dd9588e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919465"
---
# <a name="cim_slot-class"></a>Cim \_ Slot (clase)

La **clase de \_ ranura CIM** representa los conectores en los que se insertan los paquetes. Por ejemplo, un paquete físico que es una unidad de disco se puede insertar en una ranura SCA o una tarjeta (una subclase de [CIM \_ PhysicalPackage)](cim-physicalpackage.md)se puede insertar en una ranura de expansión de 16, 32 o 64 bits en una placa de hospedaje. Las ranuras PCI o PCMCIA de tipo III son ejemplos de las últimas.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintaxis siguiente se simplifica a partir Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[abstract, UUID("{FAF76B86-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Slot : CIM_PhysicalConnector
{
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  string   Description;
  real32   HeightAllowed;
  datetime InstallDate;
  real32   LengthAllowed;
  string   Manufacturer;
  uint16   MaxDataWidth;
  string   Model;
  string   Name;
  uint16   Number;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   PurposeDescription;
  string   SerialNumber;
  string   SKU;
  boolean  SpecialPurpose;
  string   Status;
  boolean  SupportsHotPlug;
  string   Tag;
  uint32   ThermalRating;
  uint16   VccMixedVoltageSupport[];
  string   Version;
  uint16   VppMixedVoltageSupport[];
};
```

## <a name="members"></a>Miembros

La **clase Slot \_ de CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Slot \_ de CIM** tiene estas propiedades.

<dl> <dt>

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

**ConnectorPinout**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena de forma libre que describe la configuración del pin y el uso de señales de un conector físico.

Esta propiedad se hereda de [**CIM \_ PhysicalConnector.**](cim-physicalconnector.md)

</dd> <dt>

**ConnectorType**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ConnectorType"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Ranura del sistema DMTF \| \| 004.2")
</dt> </dl>

Tipo de conector físico. Se especifica una matriz para permitir la descripción de combinaciones de información del conector. Por ejemplo, una entrada de matriz podría especificar RS-232, otra DB-25 y una tercera podría definir el conector como "Male".

Esta propiedad se hereda de [**CIM \_ PhysicalConnector.**](cim-physicalconnector.md)

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

Male

</dd> <dt>

3
</dt> <dd>

Female

</dd> <dt>

4
</dt> <dd>

Blindada

</dd> <dt>

5
</dt> <dd>

Sin protección

</dd> <dt>

6
</dt> <dd>

SCSI (A) Alta densidad (50 pines)

</dd> <dt>

7
</dt> <dd>

SCSI (A) Baja densidad (50 pines)

</dd> <dt>

8
</dt> <dd>

SCSI (P) Alta densidad (68 pines)

</dd> <dt>

9
</dt> <dd>

SCA-I SCSI (80 pines)

</dd> <dt>

10
</dt> <dd>

SCSI SCA-II (80 pines)

</dd> <dt>

11
</dt> <dd>

SCSI Canal de fibra (DB-9, Cobre)

</dd> <dt>

12
</dt> <dd>

SCSI Canal de fibra (fibra)

</dd> <dt>

13
</dt> <dd>

SCSI Canal de fibra SCA-II (40 pines)

</dd> <dt>

14
</dt> <dd>

SCSI Canal de fibra SCA-II (20 pines)

</dd> <dt>

15
</dt> <dd>

SCSI Canal de fibra BNC

</dd> <dt>

16
</dt> <dd>

ATA de 3 a 1/2 pulgadas (40 pines)

</dd> <dt>

17
</dt> <dd>

ATA de 2 a 1/2 pulgadas (44 pines)

</dd> <dt>

18
</dt> <dd>

ATA-2

</dd> <dt>

19
</dt> <dd>

ATA-3

</dd> <dt>

20
</dt> <dd>

ATA/66

</dd> <dt>

21
</dt> <dd>

DB-9

</dd> <dt>

22
</dt> <dd>

DB-15

</dd> <dt>

23
</dt> <dd>

DB-25

</dd> <dt>

24
</dt> <dd>

DB-36

</dd> <dt>

25
</dt> <dd>

RS-232C

</dd> <dt>

26
</dt> <dd>

RS-422

</dd> <dt>

27
</dt> <dd>

RS-423

</dd> <dt>

28
</dt> <dd>

RS-485

</dd> <dt>

29
</dt> <dd>

RS-449

</dd> <dt>

30
</dt> <dd>

V.35

</dd> <dt>

31
</dt> <dd>

X.21

</dd> <dt>

32
</dt> <dd>

IEEE-488

</dd> <dt>

33
</dt> <dd>

Aui

</dd> <dt>

34
</dt> <dd>

Categoría 3 de UTP

</dd> <dt>

35
</dt> <dd>

Categoría 4 de UTP

</dd> <dt>

36
</dt> <dd>

Categoría 5 de UTP

</dd> <dt>

37
</dt> <dd>

Bnc

</dd> <dt>

38
</dt> <dd>

RJ11

</dd> <dt>

39
</dt> <dd>

RJ45

</dd> <dt>

40
</dt> <dd>

Mic de fibra

</dd> <dt>

41
</dt> <dd>

Apple AUI

</dd> <dt>

42
</dt> <dd>

Apple GeoPort

</dd> <dt>

43
</dt> <dd>

PCI

</dd> <dt>

44
</dt> <dd>

ISA

</dd> <dt>

45
</dt> <dd>

Eisa

</dd> <dt>

46
</dt> <dd>

Vesa

</dd> <dt>

47
</dt> <dd>

PCMCIA

</dd> <dt>

48
</dt> <dd>

PCMCIA, tipo I

</dd> <dt>

49
</dt> <dd>

PCMCIA tipo II

</dd> <dt>

50
</dt> <dd>

PCMCIA Tipo III

</dd> <dt>

51
</dt> <dd>

Puerto ZV

</dd> <dt>

52
</dt> <dd>

Cardbus

</dd> <dt>

53
</dt> <dd>

USB

</dd> <dt>

54
</dt> <dd>

IEEE 1394

</dd> <dt>

55
</dt> <dd>

Hippi

</dd> <dt>

56
</dt> <dd>

HSSDC (6 pines)

</dd> <dt>

57
</dt> <dd>

Gbic

</dd> <dt>

58
</dt> <dd>

DIN

</dd> <dt>

59
</dt> <dd>

Mini-LORÓN

</dd> <dt>

60
</dt> <dd>

Micro-LORÓN

</dd> <dt>

61
</dt> <dd>

PS/2

</dd> <dt>

62
</dt> <dd>

Infrarrojos

</dd> <dt>

63
</dt> <dd>

HP-MUY

</dd> <dt>

64
</dt> <dd>

Access.bus

</dd> <dt>

65
</dt> <dd>

NuBus

</dd> <dt>

66
</dt> <dd>

Centronics

</dd> <dt>

67
</dt> <dd>

Mini-Centronics

</dd> <dt>

68
</dt> <dd>

Mini-Centronics type-14

</dd> <dt>

69
</dt> <dd>

Mini-Centronics Type-20

</dd> <dt>

70
</dt> <dd>

Mini-Centronics type-26

</dd> <dt>

71
</dt> <dd>

Bus Mouse

</dd> <dt>

72
</dt> <dd>

Adb

</dd> <dt>

73
</dt> <dd>

Agp

</dd> <dt>

74
</dt> <dd>

VME Bus

</dd> <dt>

75
</dt> <dd>

VME64

</dd> <dt>

76
</dt> <dd>

Propietario

</dd> <dt>

77
</dt> <dd>

Ranura de tarjeta de procesador propietaria

</dd> <dt>

78
</dt> <dd>

Ranura de tarjeta de memoria propietaria

</dd> <dt>

79
</dt> <dd>

Ranura de riser de E/S propietaria

</dd> <dt>

80
</dt> <dd>

PCI-66MHZ

</dd> <dt>

81
</dt> <dd>

AGP2X

</dd> <dt>

82
</dt> <dd>

AGP4X

</dd> <dt>

83
</dt> <dd>

PC-98

</dd> <dt>

84
</dt> <dd>

PC-98-Hireso

</dd> <dt>

85
</dt> <dd>

PC-H98

</dd> <dt>

86
</dt> <dd>

PC-98Note

</dd> <dt>

87
</dt> <dd>

PC-98Full

</dd> <dt>

88
</dt> <dd>

SSA SCSI

</dd> <dt>

89
</dt> <dd>

Circular

</dd> <dt>

90
</dt> <dd>

Conector IDE integrado

</dd> <dt>

91
</dt> <dd>

Conector de disquete de abordo

</dd> <dt>

92
</dt> <dd>

9 Pin Dual Inline

</dd> <dt>

93
</dt> <dd>

25 Pin Dual Inline

</dd> <dt>

94
</dt> <dd>

50 Pin Dual Inline

</dd> <dt>

95
</dt> <dd>

68 Pin Dual Inline

</dd> <dt>

96
</dt> <dd>

Conector de sonido de placa

</dd> <dt>

97
</dt> <dd>

Mini-jack

</dd> <dt>

98
</dt> <dd>

PCI-X

</dd> <dt>

99
</dt> <dd>

Sbus IEEE 1396-1993 de 32 bits

</dd> <dt>

100
</dt> <dd>

Sbus IEEE 1396-1993 de 64 bits

</dd> <dt>

101
</dt> <dd>

MCA

</dd> <dt>

102
</dt> <dd>

Gio

</dd> <dt>

103
</dt> <dd>

XIO

</dd> <dt>

104
</dt> <dd>

Hio

</dd> <dt>

105
</dt> <dd>

N ENTRELAZ

</dd> <dt>

106
</dt> <dd>

PMC

</dd> <dt>

107
</dt> <dd>

Mtrj

</dd> <dt>

108
</dt> <dd>

VF-45

</dd> <dt>

109
</dt> <dd>

E/S futuras

</dd> <dt>

110
</dt> <dd>

SC

</dd> <dt>

111
</dt> <dd>

SG

</dd> <dt>

112
</dt> <dd>

Eléctricos

</dd> <dt>

113
</dt> <dd>

Óptico

</dd> <dt>

114
</dt> <dd>

Cinta de opciones

</dd> <dt>

115
</dt> <dd>

Glm

</dd> <dt>

116
</dt> <dd>

1x9

</dd> <dt>

117
</dt> <dd>

Mini SG

</dd> <dt>

118
</dt> <dd>

LC

</dd> <dt>

119
</dt> <dd>

HSSC

</dd> <dt>

120
</dt> <dd>

VHDCI blindado (68 pines)

</dd> <dt>

121
</dt> <dd>

Infiniband

</dd> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**\_ Clave CIM,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nombre de la clase o subclase usada en la creación de una instancia de . Cuando se usa con otras propiedades clave de la clase , esta propiedad permite identificar de forma única todas las instancias de la clase y sus subclases.

Esta propiedad se hereda de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

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

**HeightAllowed**
</dt> <dd> <dl> <dt>

Tipo de datos: **real32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")
</dt> </dl>

Alto máximo, en pulgadas, de una tarjeta de adaptador que se puede insertar en la ranura.

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

**LengthAllowed**
</dt> <dd> <dl> <dt>

Tipo de datos: **real32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")
</dt> </dl>

Longitud máxima, en pulgadas, de una tarjeta adaptadora que se puede insertar en la ranura.

</dd> <dt>

**Fabricante**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Organización que produjo el elemento físico. Para obtener más información, vea la **propiedad Vendor** del [**producto CIM \_**](cim-product.md).

Esta propiedad se hereda de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**MaxDataWidth**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Ranura del sistema DMTF \| \| 004.3"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")
</dt> </dl>

Ancho máximo del bus, en bits, de las tarjetas adaptadoras que se pueden insertar en la ranura.

<dt>

<span id="8"></span>

**8** (0)


</dt> <dd></dd> <dt>

<span id="16"></span>

**16** (1)


</dt> <dd></dd> <dt>

<span id="32"></span>

**32** (2)


</dt> <dd></dd> <dt>

<span id="64"></span>

**64** (3)


</dt> <dd></dd> <dt>

<span id="128"></span>

**128** (4)


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

**Number**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de ranura física, que se puede usar como índice en una tabla de ranuras del sistema, para determinar si la ranura está ocupada físicamente.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Datos adicionales, más allá de la información de etiquetas de recurso, que se pueden usar para identificar un elemento físico. Un ejemplo son los datos de código de barras asociados a un elemento , que también tiene una etiqueta de recurso. Tenga en cuenta que si solo hay datos de código de barras disponibles y es único y se puede usar como clave de elemento, esta propiedad sería NULL y los datos de código de barras se usarían como clave de clase en la **propiedad Tag.**

Esta propiedad se hereda de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

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

**PoweredOn**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** el elemento físico está encendido.

Esta propiedad se hereda de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**PurposeDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Cim \_ Slot**.**SpecialPurpose**")
</dt> </dl>

Cadena de forma libre que describe cómo esta ranura es físicamente única y que puede contener tipos especiales de hardware. Esta propiedad solo tiene significado cuando la propiedad **SpecialPurpose** booleana correspondiente se establece en **TRUE.**

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

**SpecialPurpose**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Cim \_ Slot**.**PurposeDescription**")
</dt> </dl>

Si **es TRUE,** la ranura es físicamente única y puede contener tipos especiales de hardware (por ejemplo, una ranura de procesador de gráficos). Si **es TRUE,** **la propiedad PurposeDescription** debe especificar cómo es única la ranura o el propósito de la ranura.

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

**SupportsHotPlug**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** la ranura admite la conexión en caliente de tarjetas adaptadoras.

</dd> <dt>

**Tag**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**\_ clave CIM,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Cadena arbitraria que identifica de forma única el elemento físico y actúa como clave del elemento. Esta propiedad puede contener información, como datos de número de serie o etiqueta de recurso. La clave de [**CIM \_ PhysicalElement**](cim-physicalelement.md) se coloca muy alta en la jerarquía de objetos para identificar de forma independiente el hardware o la entidad, independientemente de la ubicación física en (o en) gabinetes, adaptadores, y así sucesivamente. Por ejemplo, un componente extraíble que se puede intercambiar en caliente se puede tomar de su paquete que contiene (ámbito) y no usarse temporalmente. El objeto sigue existiendo e incluso se puede insertar en un contenedor de ámbito diferente. La clave de un elemento físico es una cadena arbitraria que se define independientemente de la ubicación o la jerarquía orientada a la ubicación.

Esta propiedad se hereda de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Bajada de temperatura**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System Slot \| 004.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milivatios")
</dt> </dl>

Disipación térmico máxima de la ranura, en milivatios.

</dd> <dt>

**VccMixedVoltageSupport**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Ranura del sistema DMTF \| \| 004.9")
</dt> </dl>

Voltaje de cc compatible con la ranura.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

**3,3 V** (2)


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

**5 V** (3)


</dt> <dd></dd> </dl>

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

</dd> <dt>

**VppMixedVoltageSupport**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Ranura del sistema DMTF \| \| 004.10")
</dt> </dl>

Vpp voltage compatible con la ranura.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

**3,3 V** (2)


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

**5 V** (3)


</dt> <dd></dd> <dt>

<span id="12V"></span><span id="12v"></span>

**12 V** (4)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ Slot** de CIM se deriva de [**CIM \_ PhysicalConnector.**](cim-physicalconnector.md)

WMI no implementa esta clase. Para las clases WMI derivadas de **la \_ ranura CIM**, vea [Clases win32](win32-provider.md).

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

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

[**CIM \_ PhysicalConnector**](cim-physicalconnector.md)
</dt> </dl>

 

