---
description: La clase Cim Chassis representa los elementos físicos que incluyen otros elementos y proporcionan funcionalidad definible, como un escritorio, un nodo de procesamiento, UPS, almacenamiento en disco o cinta, o una combinación \_ de estos.
ms.assetid: 4c55dbff-bc4a-4cc9-8f34-29636defaa56
ms.tgt_platform: multiple
title: CIM_Chassis clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chassis
- CIM_Chassis.Caption
- CIM_Chassis.Description
- CIM_Chassis.InstallDate
- CIM_Chassis.Name
- CIM_Chassis.Status
- CIM_Chassis.CreationClassName
- CIM_Chassis.Manufacturer
- CIM_Chassis.Model
- CIM_Chassis.OtherIdentifyingInfo
- CIM_Chassis.PartNumber
- CIM_Chassis.PoweredOn
- CIM_Chassis.SerialNumber
- CIM_Chassis.SKU
- CIM_Chassis.Tag
- CIM_Chassis.Version
- CIM_Chassis.Depth
- CIM_Chassis.Height
- CIM_Chassis.HotSwappable
- CIM_Chassis.Removable
- CIM_Chassis.Replaceable
- CIM_Chassis.Weight
- CIM_Chassis.Width
- CIM_Chassis.AudibleAlarm
- CIM_Chassis.BreachDescription
- CIM_Chassis.CableManagementStrategy
- CIM_Chassis.LockPresent
- CIM_Chassis.SecurityBreach
- CIM_Chassis.ServiceDescriptions
- CIM_Chassis.ServicePhilosophy
- CIM_Chassis.VisibleAlarm
- CIM_Chassis.ChassisTypes
- CIM_Chassis.CurrentRequiredOrProduced
- CIM_Chassis.HeatGeneration
- CIM_Chassis.NumberOfPowerCords
- CIM_Chassis.TypeDescriptions
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 271f01587dc67c14464cfdb06de321d853b8b9a606a99cb1aca8fdcb0ff2ca17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835040"
---
# <a name="cim_chassis-class"></a>Cim \_ Chassis (clase)

La clase Cim Chassis representa los elementos **\_ físicos** que incluyen otros elementos y proporcionan funcionalidad definible, como un escritorio, un nodo de procesamiento, UPS, almacenamiento en disco o cinta, o una combinación de estos.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[abstract, UUID("{FAF76B72-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Chassis : CIM_PhysicalFrame
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   Manufacturer;
  string   Model;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Tag;
  string   Version;
  real32   Depth;
  real32   Height;
  boolean  HotSwappable;
  boolean  Removable;
  boolean  Replaceable;
  real32   Weight;
  real32   Width;
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  boolean  LockPresent;
  uint16   SecurityBreach;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  boolean  VisibleAlarm;
  uint16   ChassisTypes[];
  sint16   CurrentRequiredOrProduced;
  uint16   HeatGeneration;
  uint16   NumberOfPowerCords;
  string   TypeDescriptions[];
};
```

## <a name="members"></a>Miembros

La **clase CIM \_ Chassis** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ CIM Chassis** tiene estos métodos.



| Método                                                           | Descripción                                                                                                                                      |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsCompatible**](iscompatible-method-in-class-cim-chassis.md) | Comprueba si el elemento físico al que se hace referencia se puede contener o insertar en el paquete físico. No implementado por WMI.<br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ CIM Chassis** tiene estas propiedades.

<dl> <dt>

**AudibleAlarm**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** el marco está equipado con una alarma de sonido.

Esta propiedad se hereda de [**CIM \_ PhysicalFrame.**](cim-physicalframe.md)

</dd> <dt>

**BreachDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")
</dt> </dl>

Cadena de forma libre que proporciona más información si la **propiedad SecurityBreach** indica que se ha producido una infracción o algún otro evento relacionado con la seguridad.

Esta propiedad se hereda de [**CIM \_ PhysicalFrame.**](cim-physicalframe.md)

</dd> <dt>

**CableManagementStrategy**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena de forma libre que contiene información sobre cómo se conectan y agrupan los distintos cables para el marco. Con muchas redes, cables relacionados con el almacenamiento y alimentación, la administración de cables puede ser un desafío complejo y complejo. Esta propiedad de cadena contiene información para ayudar en el ensamblado y el servicio del marco.

Esta propiedad se hereda de [**CIM \_ PhysicalFrame.**](cim-physicalframe.md)

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

**ChassisTypes**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Physical Container Global Table \| 002.1"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Chassis**.**TypeDescriptions**")
</dt> </dl>

Matriz enumerada con valores enteros que indica el tipo de chasis.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1)


</dt> <dd>

Otros.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)


</dt> <dd>

Desconocido.

</dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Escritorio** (3)


</dt> <dd>

Escritorio.

</dd> <dt>

<span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>

<span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>**Escritorio de perfil bajo** (4)


</dt> <dd>

Escritorio de perfil bajo.

</dd> <dt>

<span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>

<span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>**Pizza Box** (5)


</dt> <dd>

Caja de pizza.

</dd> <dt>

<span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>

<span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>**Mini-Torre** (6)


</dt> <dd>

Mini-torre.

</dd> <dt>

<span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>

<span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>**Torre** (7)


</dt> <dd>

Torre.

</dd> <dt>

<span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>

<span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>**Portable** (8)


</dt> <dd>

Portátil.

</dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Portátil** (9)


</dt> <dd>

Equipo portátil.

</dd> <dt>

<span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>

<span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>**Notebook** (10)


</dt> <dd>

cuaderno.

</dd> <dt>

<span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>

<span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>**Hand Held** (11)


</dt> <dd>

Mantenido a mano.

</dd> <dt>

<span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>

<span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>**Estación de acoplamiento** (12)


</dt> <dd>

Estación de acoplamiento.

</dd> <dt>

<span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>

<span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>**Todo en uno** (13)


</dt> <dd>

Todo en uno.

</dd> <dt>

<span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>

<span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>**Sub notebook** (14)


</dt> <dd>

Subnotebook.

</dd> <dt>

<span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>

<span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>**Ahorro de espacio** (15)


</dt> <dd>

Ahorro de espacio.

</dd> <dt>

<span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>

<span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>**Lunch Box** (16)


</dt> <dd>

Caja de comida.

</dd> <dt>

<span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>

<span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>**Chasis del sistema principal** (17)


</dt> <dd>

Chasis del sistema principal.

</dd> <dt>

<span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>

<span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>**Chasis de expansión** (18)


</dt> <dd>

Chasis de expansión.

</dd> <dt>

<span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>

<span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>**SubChassis** (19)


</dt> <dd>

Subchassis.

</dd> <dt>

<span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>

<span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>**Chasis de expansión de bus** (20)


</dt> <dd>

Chasis de expansión de bus.

</dd> <dt>

<span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>

<span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>**Chasis periférico** (21)


</dt> <dd>

Chasis periférico.

</dd> <dt>

<span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>

<span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>**Storage chasis** (22)


</dt> <dd>

Storage chasis.

</dd> <dt>

<span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>

<span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>**Chasis de montaje en bastidor** (23)


</dt> <dd>

Chasis de montaje en bastidor.

</dd> <dt>

<span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>

<span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>**Equipo de caso sellado** (24)


</dt> <dd>

Equipo con mayúsculas y minúsculas selladas.

</dd> </dl>

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

**CurrentRequiredOrProduced**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("y a 120 volts")
</dt> </dl>

Requerido actualmente por el chasis a 120 vs. Si el chasis proporciona energía (como en el caso de un UPS), esta propiedad puede indicar el amperaje generado, como un número negativo.

</dd> <dt>

**Profundidad**
</dt> <dd> <dl> <dt>

Tipo de datos: **real32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")
</dt> </dl>

Profundidad del paquete físico, en pulgadas.

Esta propiedad se hereda de [**CIM \_ PhysicalPackage.**](cim-physicalpackage.md)

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

**HeatGeneration**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("BTU por hora")
</dt> </dl>

Cantidad de calor generado por el chasis en Btu/hora.

</dd> <dt>

**Height**
</dt> <dd> <dl> <dt>

Tipo de datos: **real32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")
</dt> </dl>

Alto del paquete físico, en pulgadas.

Esta propiedad se hereda de [**CIM \_ PhysicalPackage.**](cim-physicalpackage.md)

</dd> <dt>

**HotSwappable**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** el paquete se puede intercambiar en caliente. Un paquete físico se puede intercambiar en caliente si el elemento se puede reemplazar por uno físicamente diferente (pero equivalente) mientras el paquete que lo contiene está activado. Por ejemplo, un componente de ventilador se puede diseñar para intercambiarse en caliente. Todos los componentes que se pueden intercambiar en caliente son intrínsecamente extraíbles y reemplazables.

Esta propiedad se hereda de [**CIM \_ PhysicalPackage.**](cim-physicalpackage.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Fecha de instalación")
</dt> </dl>

Indica cuándo se instaló el objeto. La falta de un valor no indica que el objeto no está instalado.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**LockPresent**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** el marco está protegido con un bloqueo.

Esta propiedad se hereda de [**CIM \_ PhysicalFrame.**](cim-physicalframe.md)

</dd> <dt>

**Fabricante**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nombre de la organización responsable de generar el elemento físico. Para obtener más información, vea la **propiedad Vendor** del [**producto \_ CIM.**](cim-product.md)

Esta propiedad se hereda de [**CIM \_ PhysicalElement**](cim-physicalelement.md).

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

Esta propiedad se hereda de [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nombre")
</dt> </dl>

Etiqueta por la que se conoce el objeto. Cuando se subclasifica, esta propiedad se puede invalidar para que sea una propiedad de clave.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**NumberOfPowerCords**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de cables de alimentación que deben estar conectados al chasis para que todos los componentes puedan funcionar.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Datos adicionales, más allá de la información de etiquetas de recurso, que se pueden usar para identificar un elemento físico. Un ejemplo son los datos de código de barras asociados a un elemento, que también tiene una etiqueta de recurso. Tenga en cuenta que si solo hay datos de código de barras disponibles y es único y se puede usar como clave de elemento, esta propiedad sería NULL y los datos del código de barra se usarían como clave de clase en la **propiedad Tag.**

Esta propiedad se hereda de [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Partnumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Número de pieza asignado por la organización responsable de producir o fabricación del elemento físico.

Esta propiedad se hereda de [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**PoweredOn**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** el elemento físico está encendido. De lo contrario, está desactivado actualmente.

Esta propiedad se hereda de [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Extraíble**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** el paquete está diseñado para su entrada y salida del contenedor físico en el que se encuentra normalmente, sin afectar a la función del empaquetado general. Un paquete se considera extraíble incluso si la alimentación debe estar desactivada para realizar la eliminación. Si la energía puede estar encendido y el paquete quitado, el elemento es extraíble y se puede intercambiar en caliente. Por ejemplo, un chip de procesador actualizable es extraíble.

Esta propiedad se hereda de [**CIM \_ PhysicalPackage.**](cim-physicalpackage.md)

</dd> <dt>

**Reemplazable**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** es posible reemplazar el elemento por uno físicamente diferente. Por ejemplo, algunos sistemas informáticos permiten actualizar el chip del procesador principal a una de las especificaciones de reloj más altas. En este caso, se dice que el procesador es reemplazable. Todos los componentes extraíbles son intrínsecamente reemplazables.

Esta propiedad se hereda de [**CIM \_ PhysicalPackage.**](cim-physicalpackage.md)

</dd> <dt>

**SecurityBreach**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Physical Container Global Table \| 002.12"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")
</dt> </dl>

Indica si se ha intentado una infracción física del marco pero no se ha realizado correctamente, o si se ha intentado y se ha realizado correctamente.

Esta propiedad se hereda de [**CIM \_ PhysicalFrame**](cim-physicalframe.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

**Ninguna infracción** (3)


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

**Intento de infracción** (4)


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

**Brecha correcta** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Número asignado por el fabricante usado para identificar el elemento físico.

Esta propiedad se hereda de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**ServiceDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**ServiceXiaphy**")
</dt> </dl>

Cadenas de forma libre que proporcionan explicaciones detalladas de las entradas de la **matriz Service Toolbarphy.**

> [!Note]  
> Cada entrada de esta matriz está relacionada con la entrada de la matriz **ServiceMultidimensionalphy** que se encuentra en el mismo índice.

 

Esta propiedad se hereda de [**CIM \_ PhysicalFrame**](cim-physicalframe.md).

</dd> <dt>

**ServiceXiaphy**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")
</dt> </dl>

Indica si el marco se atiende desde la parte superior, frontal, posterior o lateral; y si tiene bandejas deslizantes o lados extraíbles, y si el marco es móvil (por ejemplo, con rodillos).

Esta propiedad se hereda de [**CIM \_ PhysicalFrame**](cim-physicalframe.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

**Servicio desde arriba** (2)


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

**Servicio desde el frente** (3)


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

**Servicio desde atrás** (4)


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

**Servicio desde el lado** (5)


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

**Bandejas deslizantes** (6)


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

**Lados extraíbles** (7)


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

**Moveable** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**SKU**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Número de unidad de mantenimiento de existencias para este elemento físico.

Esta propiedad se hereda de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Cadena que indica el estado actual del objeto. Se puede definir el estado operativo y no operativo. El estado operativo puede incluir "Ok", "Degraded" y "Pred Fail". "Error previo" indica que un elemento funciona correctamente, pero predice un error (por ejemplo, una unidad de disco duro habilitada para SMART).

El estado no operativo puede incluir "Error", "Starting", "Stopping" y "Service". El "servicio" se puede aplicar durante la resilvering del reflejo del disco, volver a cargar una lista de permisos de usuario u otro trabajo administrativo. No todo este trabajo está en línea, pero el elemento administrado no es "correcto" ni está en uno de los demás estados.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

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

**Tag**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**\_ clave CIM,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identifica de forma única el elemento físico y actúa como clave del elemento. Esta propiedad puede contener información, como datos de número de serie o etiqueta de recurso. La clave de [**CIM \_ PhysicalElement**](cim-physicalelement.md) se coloca muy alta en la jerarquía de objetos para identificar de forma independiente el hardware o la entidad, independientemente de la ubicación física en (o en) gabinetes, adaptadores, y así sucesivamente. Por ejemplo, un componente extraíble que se puede intercambiar en caliente se puede tomar de su paquete que contiene (ámbito) y no usarse temporalmente. El objeto sigue existiendo e incluso se puede insertar en un contenedor de ámbito diferente. La clave de un elemento físico es una cadena arbitraria que se define independientemente de la ubicación o la jerarquía orientada a la ubicación.

Esta propiedad se hereda de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**TypeDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Chassis**.**ChassisTypes**")
</dt> </dl>

Matriz de cadenas de forma libre que proporciona información sobre las entradas de la matriz **ChassisTypes.**

> [!Note]  
> Cada entrada de matriz está relacionada con la entrada de la propiedad **ChassisTypes,** que se encuentra en el mismo índice.

 

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Indica la versión del elemento físico.

Esta propiedad se hereda de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**VisibleAlarm**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** el equipo incluye una alarma visible.

Esta propiedad se hereda de [**CIM \_ PhysicalFrame**](cim-physicalframe.md).

</dd> <dt>

**Peso**
</dt> <dd> <dl> <dt>

Tipo de datos: **real32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("libras")
</dt> </dl>

Peso del paquete físico, en libras.

Esta propiedad se hereda de [**CIM \_ PhysicalPackage.**](cim-physicalpackage.md)

</dd> <dt>

**Width**
</dt> <dd> <dl> <dt>

Tipo de datos: **real32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")
</dt> </dl>

Ancho del paquete físico, en pulgadas.

Esta propiedad se hereda de [**CIM \_ PhysicalPackage.**](cim-physicalpackage.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ CIM Chassis** se deriva de [**CIM \_ PhysicalFrame**](cim-physicalframe.md).

WMI no implementa esta clase. Para obtener más información sobre las clases derivadas del **\_ chasis CIM,** vea [Clases Win32](win32-provider.md).

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

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

[**CIM \_ PhysicalFrame**](cim-physicalframe.md)
</dt> </dl>

 

