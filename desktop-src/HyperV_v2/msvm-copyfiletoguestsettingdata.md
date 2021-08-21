---
description: Representa los parámetros para copiar un archivo del host en el invitado.
ms.assetid: 255F4132-C212-4A3B-A9B8-3F531E7D1CF9
title: Msvm_CopyFileToGuestSettingData clase
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
ms.openlocfilehash: 6eb011ec8d03153bd5f1b7d956775327d2582410e9ca12591e19a39ddb4af5fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148844"
---
# <a name="msvm_copyfiletoguestsettingdata-class"></a>Clase \_ CopyFileToGuestSettingData de Msvm

Representa los parámetros para copiar un archivo del host en el invitado. Esta clase se deriva de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).

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

La **clase \_ CopyFileToGuestSettingData de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CopyFileToGuestSettingData de Msvm** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** ( 64 )
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

Descripción textual del objeto.

</dd> <dt>

**DestinationPath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso completa del archivo de destino que se va a copiar. Este archivo de destino debe ser accesible para el invitado y puede contener variables de entorno, que el invitado expande. Si la ruta de acceso especificada es un directorio existente en el invitado, el archivo de destino se crea en este directorio. En este caso, el nombre de archivo de **SourcePath** se usa como nombre de archivo de destino.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar de esta instancia de SettingData. Además, el nombre para mostrar se puede usar como una propiedad de índice para una búsqueda o consulta. (Nota: El nombre no tiene que ser único dentro de un espacio de nombres).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Dentro del ámbito del espacio de nombres de creación de instancias, InstanceID identifica de forma opaca e inequívoca una instancia de esta clase. Para garantizar la unidad dentro del Espacio de nombres, el valor de InstanceID debe construirse mediante el siguiente algoritmo *"preferido": OrgID:**LocalID,* donde *OrgID* y *LocalID* están separados por dos puntos (:), y donde *OrgID* debe incluir un nombre con derechos de autor, marca comercial o único que sea propiedad de la entidad empresarial que crea o define instanceID o que es un identificador registrado asignado a la entidad empresarial por una autoridad global reconocida. (Este requisito es similar a *SchemaName* \_ *Estructura ClassName* de nombres de clase de esquema). Además, para garantizar la unidad, *OrgID* no debe contener dos puntos (:). Cuando se usa este algoritmo, los primeros dos puntos que aparecen en InstanceID deben aparecer entre *OrgID* y *LocalID.* La entidad empresarial elige *LocalID* y no debe reutilizarse para identificar diferentes elementos subyacentes (reales). Si no se usa el algoritmo preferido anterior, la entidad de definición debe asegurarse de que el InstanceID resultante no se reutiliza en ningún instanceID generado por este u otros proveedores para el Espacio de nombres de esta instancia. En el caso de las instancias definidas por DMTF, el algoritmo "preferido" debe usarse con *el OrgID* establecido en CIM.

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

Ruta de acceso completa del archivo de origen que se va a copiar. Este archivo de origen debe ser accesible para el host de Hyper-V y puede contener variables de entorno, que se expanden mediante el host de Hyper-V.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                                 |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))
</dt> </dl>

 

