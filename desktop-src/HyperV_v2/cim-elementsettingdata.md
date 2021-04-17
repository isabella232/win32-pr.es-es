---
description: Representa una asociación entre un elemento administrado y sus datos de configuración asociados. Esta asociación también describe si se trata de una configuración predeterminada o actual.
ms.assetid: 0df2b235-76d9-4899-938b-274ec5471324
title: CIM_ElementSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSettingData
- CIM_ElementSettingData.ManagedElement
- CIM_ElementSettingData.SettingData
- CIM_ElementSettingData.IsDefault
- CIM_ElementSettingData.IsCurrent
- CIM_ElementSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e22dbd221f2e83009e4268cc0de337374e04298a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667576"
---
# <a name="cim_elementsettingdata-class"></a>\_Clase ElementSettingData de CIM

Representa una asociación entre un elemento administrado y sus datos de configuración asociados. Esta asociación también describe si se trata de una configuración predeterminada o actual.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Abstract, Version("2.19.1"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_ElementSettingData
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
  uint16                 IsDefault;
  uint16                 IsCurrent;
  uint16                 IsNext;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ ElementSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ ElementSettingData** tiene estas propiedades.

<dl> <dt>

**IsCurrent**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el elemento está usando actualmente la configuración a la que se hace referencia.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>

**Es actual** (1)


</dt> <dd></dd> <dt>

<span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>

**No es actual** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**IsDefault**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Que indica si el valor es un valor predeterminado para el elemento.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>

**Es el valor predeterminado** (1)


</dt> <dd></dd> <dt>

<span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>

**No es el valor predeterminado** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**IsNext**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Marca que indica cuándo y con qué frecuencia se aplica la configuración.

Por ejemplo, la configuración se puede aplicar en una solicitud de reinicialización, restablecimiento y reconfiguración. Puede ser un valor de configuración permanente o una configuración usada solo una vez, como indica la marca. Si se trata de una configuración permanente, se aplica la configuración cada vez que se reinicializa el elemento administrado, hasta que esta marca se restablece manualmente. Sin embargo, si es de uso único, la marca se borra automáticamente después de aplicar la configuración. Además, si esta marca se establece en un valor distinto de 0 (desconocido), esto tiene prioridad sobre una propiedad **SettingData** establecida en "default".

Si el elemento administrado es un sistema informático y el valor de esta marca es "es siguiente", el valor será efectivo la próxima vez que se restablezca el sistema. Y, a menos que se cambie esta marca, se conservará para los restablecimientos del sistema posteriores. Sin embargo, si esta marca se establece en "es siguiente para uso único", esta configuración solo se utilizará una vez y la marca se restablecerá después de la 2 (no es siguiente). Por lo tanto, en el ejemplo anterior, si el sistema se reinicia en una sucesión rápida, la configuración no se utilizará en el segundo reinicio.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>

**Es Next** (1)


</dt> <dd></dd> <dt>

<span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>

**No es Next** (2)


</dt> <dd></dd> <dt>

<span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>

**Siguiente para uso único** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ManagedElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Elemento administrado.

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ SettingData de CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Los datos de configuración asociados al elemento.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

