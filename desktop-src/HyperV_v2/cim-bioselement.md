---
description: Representa el software de bajo nivel que se carga en el almacenamiento no volátil y que se usa para iniciar y configurar un sistema informático (CIM \_ ComputerSystem).
ms.assetid: e34c9b00-2723-4858-805e-5e3e51a5dfd2
title: CIM_BIOSElement (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSElement
- CIM_BIOSElement.Version
- CIM_BIOSElement.Manufacturer
- CIM_BIOSElement.PrimaryBIOS
- CIM_BIOSElement.ListOfLanguages
- CIM_BIOSElement.CurrentLanguage
- CIM_BIOSElement.LoadedStartingAddress
- CIM_BIOSElement.LoadedEndingAddress
- CIM_BIOSElement.LoadUtilityInformation
- CIM_BIOSElement.ReleaseDate
- CIM_BIOSElement.RegistryURIs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f97cbb495fb8105be012c44942aeedb39377e3d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669948"
---
# <a name="cim_bioselement-class-hyper-v-management"></a>CIM_BIOSElement (clase, administración de Hyper-V)

Representa el software de bajo nivel que se carga en el almacenamiento no volátil y que se usa para iniciar y configurar un sistema informático ([**CIM \_ ComputerSystem**](cim-computersystem.md)).

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.17.0"), UMLPackagePath("CIM::Application::BIOS"), AMENDMENT]
class CIM_BIOSElement : CIM_SoftwareElement
{
  string   Version;
  string   Manufacturer;
  boolean  PrimaryBIOS;
  string   ListOfLanguages[];
  string   CurrentLanguage;
  uint64   LoadedStartingAddress;
  uint64   LoadedEndingAddress;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ BIOSElement** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ BIOSElement** tiene estas propiedades.

<dl> <dt>

**CurrentLanguage**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BIOSElement**.**ListOfLanguages**")
</dt> </dl>

Idioma seleccionado actualmente para el BIOS. Esta información se puede obtener del BIOS de administración del sistema (SMBIOS) mediante el atributo de idioma actual de la estructura de tipo 13 para indizar en la lista de cadenas que sigue a la estructura. A esta propiedad se le aplica el formato con el nombre de lenguaje ISO 639 y puede ir seguido del nombre del territorio ISO 3166 y el método de codificación.

</dd> <dt>

**ListOfLanguages**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una lista de idiomas instalables para el BIOS. Esta información se puede obtener de SMBIOS desde la lista de cadenas que sigue a la estructura de tipo 13. Se debe usar un nombre de idioma ISO 639 para especificar los idiomas instalables del BIOS. También se puede especificar el nombre del territorio ISO 3166 y el método de codificación, siguiendo el nombre del idioma.

</dd> <dt>

**LoadedEndingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS del sistema DMTF \| 001,6 ")
</dt> </dl>

Dirección final de la memoria ocupada por el BIOS.

</dd> <dt>

**LoadedStartingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS del sistema DMTF \| 001,5 ")
</dt> </dl>

Dirección inicial de la memoria ocupada por el BIOS.

</dd> <dt>

**LoadUtilityInformation**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS del sistema DMTF \| 001,7 ")
</dt> </dl>

Cadena de forma libre que describe la utilidad Flash/Load de BIOS necesaria para actualizar el objeto **CIM \_ BIOSElement** . En esta propiedad se puede indicar la versión y otra información.

</dd> <dt>

**Le**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("manufacturer"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS del sistema DMTF \| 001,2 ")
</dt> </dl>

Fabricante del elemento de software.

</dd> <dt>

**PrimaryBIOS**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS del sistema DMTF \| 001,9 ")
</dt> </dl>

True si se trata del BIOS principal del equipo; en caso contrario, false.

</dd> <dt>

**RegistryURIs**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La ubicación de publicación de los registros de atributos de BIOS a los que la implementación del BIOS cumple.

</dd> <dt>

**ReleaseDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS del sistema DMTF \| 001,8 ")
</dt> </dl>

La fecha en la que se liberó este BIOS.

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS del sistema DMTF \| 001,3 ")
</dt> </dl>

Versión de la operación. La versión de la operación debe estar en una de las siguientes formas:

-   *<major>*.*<minor>*.*<revision>*
-   *<major>*.*<minor><letter><revision>*

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

[**\_SOFTWAREELEMENT CIM**](cim-softwareelement.md)
</dt> </dl>

 

