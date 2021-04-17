---
description: Asocia un elemento administrado a sus datos de configuración.
ms.assetid: 4DB78E43-E387-478E-999C-770B35925721
title: Msvm_ElementSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementSettingData
- Msvm_ElementSettingData.ManagedElement
- Msvm_ElementSettingData.SettingData
- Msvm_ElementSettingData.IsDefault
- Msvm_ElementSettingData.IsCurrent
- Msvm_ElementSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9f4d2af614e3b161f49a0d37d1e4d1ee48ce0aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686964"
---
# <a name="msvm_elementsettingdata-class"></a>MSVM \_ ElementSettingData (clase)

Asocia un elemento administrado a sus datos de configuración. Algunas de las aplicaciones más importantes de esta asociación se usan en la vinculación de una máquina virtual y los dispositivos lógicos que se han asignado a ese sistema con su información de configuración de instantánea. La información de configuración actual está asociada a la máquina virtual y sus dispositivos a través de la Asociación [**MSVM \_ SettingsDefineState**](msvm-settingsdefinestate.md) .

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementSettingData : CIM_ElementSettingData
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
  uint16                 IsDefault = 0;
  uint16                 IsCurrent = 0;
  uint16                 IsNext = 0;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ ElementSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ ElementSettingData** tiene estas propiedades.

<dl> <dt>

**IsCurrent**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica que la configuración a la que se hace referencia se está usando actualmente en el funcionamiento del elemento o que esta información es desconocida. Esta propiedad se hereda de [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata). El valor predeterminado es 0 (desconocido).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)
</dt> <dt>

<span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>**Es actual** (1)
</dt> <dt>

<span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>**No es actual** (2)
</dt> </dl>

</dd> <dt>

**IsDefault**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica que la configuración a la que se hace referencia es un valor predeterminado para el elemento o que esta información es desconocida. Esta propiedad se hereda de [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata). El valor predeterminado es 0 (desconocido).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)
</dt> <dt>

<span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>**Es el valor predeterminado** (1)
</dt> <dt>

<span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>**No es el valor predeterminado** (2)
</dt> </dl>

</dd> <dt>

**IsNext**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el valor al que se hace referencia es el siguiente valor que se va a aplicar. Esta propiedad se hereda de [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata). El valor predeterminado es 0 (desconocido).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)
</dt> <dt>

<span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>**Es Next** (1)
</dt> <dt>

<span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>**No es Next** (2)
</dt> <dt>

<span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>**Siguiente para uso único** (3)
</dt> </dl>

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a la máquina virtual o el dispositivo virtual. Esta propiedad se hereda de [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85))**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a la configuración de instantáneas para la máquina virtual o el dispositivo virtual. Esta propiedad se hereda de [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).

</dd> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la clase **MSVM \_ ElementSettingData** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Ejemplos

Consulte [consultar objetos de red](querying-networking-objects.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_ELEMENTSETTINGDATA CIM**](cim-elementsettingdata.md)
</dt> <dt>

[**\_ELEMENTSETTINGDATA CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)
</dt> <dt>

[Clases de administración de sistema virtual](virtual-system-management-classes.md)
</dt> </dl>

 

