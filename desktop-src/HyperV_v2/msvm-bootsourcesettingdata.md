---
description: Representa los parámetros para establecer el origen de arranque de una máquina virtual.
ms.assetid: 21CD4B71-3D05-469E-89BB-DC2C65F5AB10
title: Msvm_BootSourceSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BootSourceSettingData
- Msvm_BootSourceSettingData.Description
- Msvm_BootSourceSettingData.Caption
- Msvm_BootSourceSettingData.InstanceID
- Msvm_BootSourceSettingData.ElementName
- Msvm_BootSourceSettingData.BootSourceType
- Msvm_BootSourceSettingData.OtherLocation
- Msvm_BootSourceSettingData.FirmwareDevicePath
- Msvm_BootSourceSettingData.BootSourceDescription
- Msvm_BootSourceSettingData.OptionalData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0403846e10df4c9bd54146eea44e8e91c06d01c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687030"
---
# <a name="msvm_bootsourcesettingdata-class"></a>MSVM \_ BootSourceSettingData (clase)

Representa los parámetros para establecer el origen de arranque de una máquina virtual. Esta clase se deriva de [**un \_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BootSourceSettingData : CIM_SettingData
{
  string Description;
  string Caption;
  string InstanceID;
  string ElementName;
  uint32 BootSourceType;
  string OtherLocation;
  string FirmwareDevicePath;
  string BootSourceDescription;
  uint8  OptionalData[];
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ BootSourceSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ BootSourceSettingData** tiene estas propiedades.

<dl> <dt>

**BootSourceDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La descripción del origen de arranque proporcionado por el firmware.

</dd> <dt>

**BootSourceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Un valor de enumeración que especifica el tipo del origen de arranque.

Estos son los valores válidos:

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Drive"></span><span id="drive"></span><span id="DRIVE"></span>

**Unidad** (1)


</dt> <dd></dd> <dt>

<span id="Network"></span><span id="network"></span><span id="NETWORK"></span>

**Red** (2)


</dt> <dd></dd> <dt>

<span id="File"></span><span id="file"></span><span id="FILE"></span>

**Archivo** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (64)
</dt> </dl>

Breve descripción textual del objeto.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una descripción textual del objeto.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar de esta instancia de SettingData. Además, el nombre para mostrar se puede usar como una propiedad de índice para una búsqueda o una consulta. (Nota: el nombre no tiene que ser único dentro de un espacio de nombres).

</dd> <dt>

**FirmwareDevicePath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La ruta de acceso nativa que el firmware utiliza para describir el dispositivo.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**
</dt> </dl>

Dentro del ámbito del espacio de nombres de la creación de instancias, InstanceID identifica de forma opaca y única una instancia de esta clase. Para garantizar la unicidad dentro del espacio de nombres, el valor de InstanceID debe construirse con el siguiente algoritmo "preferido": *OrgID*:*LocalID* donde *orgid* y *LocalID* se separan mediante dos puntos (:), y donde *OrgID* debe incluir un nombre con copyright, marca comercial o de otro tipo que sea propiedad de la entidad empresarial que está creando o definiendo el InstanceID o que es un ID (Este requisito es similar al de *SchemaName* \_ Estructura *className* de los nombres de clase de esquema.) Además, para garantizar la exclusividad, *OrgID* no debe contener dos puntos (:). Al usar este algoritmo, el primer signo de dos puntos que aparece en InstanceID debe aparecer entre *OrgID* y *LocalID*. La entidad empresarial elige *LocalID* y no se debe volver a usar para identificar distintos elementos subyacentes (del mundo real). Si no se utiliza el algoritmo preferido anterior, la entidad de definición debe asegurarse de que el InstanceID resultante no se reutiliza en ningún InstanceIDs producido por este u otros proveedores para el espacio de nombres de esta instancia. En el caso de las instancias definidas por DMTF, el algoritmo "preferido" se debe usar con el valor de *OrgID* establecido en CIM.

</dd> <dt>

**OptionalData**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Datos opcionales proporcionados por el firmware.

> [!Note]  
> Propiedad agregada en Windows 10.

 

</dd> <dt>

**OtherLocation**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La otra información de ubicación, si la hay, que el firmware usa para identificar de forma única el origen de arranque.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                                 |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SettingData de CIM \_**](cim-settingdata.md)
</dt> <dt>

[**SettingData de CIM \_**](/previous-versions//cc136911(v=vs.85))
</dt> </dl>

 

