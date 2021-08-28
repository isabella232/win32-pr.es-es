---
description: Representa el software de bajo nivel que se carga en el almacenamiento no volátil y se usa para iniciar y configurar un sistema informático (CIM \_ ComputerSystem).
ms.assetid: e34c9b00-2723-4858-805e-5e3e51a5dfd2
title: CIM_BIOSElement (administración de Hyper-V)
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
ms.openlocfilehash: 78f2433d2b75e2c348fdf6e7a8ff35db56c9a0c8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879874"
---
# <a name="cim_bioselement-class-hyper-v-management"></a>CIM_BIOSElement (administración de Hyper-V)

Representa el software de bajo nivel que se carga en el almacenamiento no volátil y se usa para iniciar y configurar un sistema informático [**(CIM \_ ComputerSystem**](cim-computersystem.md)).

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

La **clase \_ BIOSElement de CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ BIOSElement de CIM** tiene estas propiedades.

<dl> <dt>

**CurrentLanguage**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BIOSElement**.**ListOfLanguages**")
</dt> </dl>

Idioma seleccionado actualmente para el BIOS. Esta información se puede obtener del BIOS de administración del sistema (SMBIOS) mediante el atributo Current Language de la estructura Type 13 para indexar en la lista de cadenas que sigue a la estructura. Esta propiedad tiene formato con el nombre de idioma ISO 639 y puede estar seguida del nombre de territorio ISO 3166 y el método de codificación.

</dd> <dt>

**ListOfLanguages**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista de idiomas instalables para el BIOS. Esta información se puede obtener de SMBIOS, de la lista de cadenas que sigue a la estructura Type 13. Se debe usar un nombre de idioma ISO 639 para especificar los idiomas instalables del BIOS. También se pueden especificar el nombre del territorio ISO 3166 y el método de codificación, siguiendo el nombre de idioma.

</dd> <dt>

**LoadedEndingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. BIOS del \| sistema DMTF \| 001.6")
</dt> </dl>

Dirección final de la memoria ocupada por el BIOS.

</dd> <dt>

**LoadedStartingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. BIOS del \| sistema DMTF \| 001.5")
</dt> </dl>

Dirección inicial de la memoria ocupada por el BIOS.

</dd> <dt>

**LoadUtilityInformation**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System BIOS \| 001.7")
</dt> </dl>

Cadena de forma libre que describe la utilidad flash/load de BIOS necesaria para actualizar el **objeto \_ BIOSElement de CIM.** La versión y otra información se pueden indicar en esta propiedad.

</dd> <dt>

**Fabricante**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. BIOS del \| sistema DMTF \| 001.2")
</dt> </dl>

Fabricante del elemento de software.

</dd> <dt>

**PrimaryBIOS**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System BIOS \| 001.9")
</dt> </dl>

True si se trata del BIOS principal del sistema informático; de lo contrario, false.

</dd> <dt>

**RegistryURIs**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ubicación de publicación de los registros de atributos de BIOS con los que se cumple la implementación del BIOS.

</dd> <dt>

**ReleaseDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System BIOS \| 001.8")
</dt> </dl>

Fecha en que se publicó este BIOS.

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System BIOS \| 001.3")
</dt> </dl>

Versión de la operación. La versión de la operación debe tener uno de los siguientes formatos:

-   *&lt; principal. &gt;**&lt; secundaria. &gt;* *&lt; revisión &gt;*
-   *&lt; principal. &gt;**&lt; revisión &gt; &lt; de letra &gt; &lt; secundaria &gt;*

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ SoftwareElement**](cim-softwareelement.md)
</dt> </dl>

 

