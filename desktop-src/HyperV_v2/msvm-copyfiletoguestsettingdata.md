---
description: Representa los parámetros para copiar un archivo del host en el invitado.
ms.assetid: 255F4132-C212-4A3B-A9B8-3F531E7D1CF9
title: Msvm_CopyFileToGuestSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestSettingData
- Msvm_CopyFileToGuestSettingData.Description
- Msvm_CopyFileToGuestSettingData.Caption
- Msvm_CopyFileToGuestSettingData.InstanceID
- Msvm_CopyFileToGuestSettingData.ElementName
- Msvm_CopyFileToGuestSettingData.OverwriteExisting
- Msvm_CopyFileToGuestSettingData.CreateFullPath
- Msvm_CopyFileToGuestSettingData.SourcePath
- Msvm_CopyFileToGuestSettingData.DestinationPath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 05e27340acc9dd341bec7857c164f50344abc36f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688362"
---
# <a name="msvm_copyfiletoguestsettingdata-class"></a>MSVM \_ CopyFileToGuestSettingData (clase)

Representa los parámetros para copiar un archivo del host en el invitado. Esta clase se deriva de [**un \_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[AMENDMENT]
class Msvm_CopyFileToGuestSettingData : CIM_SettingData
{
  string  Description;
  string  Caption;
  string  InstanceID;
  string  ElementName;
  boolean OverwriteExisting;
  boolean CreateFullPath;
  string  SourcePath;
  string  DestinationPath;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ CopyFileToGuestSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ CopyFileToGuestSettingData** tiene estas propiedades.

<dl> <dt>

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

**CreateFullPath**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si los directorios que faltan en la ruta de acceso del archivo de destino deben crearse antes de copiar el archivo.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una descripción textual del objeto.

</dd> <dt>

**DestinationPath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso completa del archivo de destino que se va a copiar. Este archivo de destino debe ser accesible para el invitado y puede contener variables de entorno, que se expanden mediante el invitado. Si la ruta de acceso especificada es un directorio existente en el invitado, el archivo de destino se crea en este directorio. En este caso, el nombre de archivo de **SourcePath** se utiliza como nombre de archivo de destino.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar de esta instancia de SettingData. Además, el nombre para mostrar se puede usar como una propiedad de índice para una búsqueda o una consulta. (Nota: el nombre no tiene que ser único dentro de un espacio de nombres).

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

**OverwriteExisting**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se debe sobrescribir un archivo de destino existente.

</dd> <dt>

**SourcePath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso completa del archivo de código fuente que se va a copiar. Este archivo de origen debe ser accesible para el host de Hyper-V y puede contener variables de entorno, que se expanden mediante el host de Hyper-V.

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

 

