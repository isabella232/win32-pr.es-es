---
description: Asocia una máquina virtual y sus datos de configuración de exportación.
ms.assetid: FAAE7F74-07C0-4638-ABF9-5DEDBF2B9DD6
title: Msvm_SystemExportSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemExportSettingData
- Msvm_SystemExportSettingData.ManagedElement
- Msvm_SystemExportSettingData.SettingData
- Msvm_SystemExportSettingData.IsDefault
- Msvm_SystemExportSettingData.IsCurrent
- Msvm_SystemExportSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 39e096c466dd4accc1a2c87ececd6ce23ba27cb173e6b5fa0d6728852ad59cce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811875"
---
# <a name="msvm_systemexportsettingdata-class"></a>Clase \_ SystemExportSettingData de Msvm

Asocia una máquina virtual y sus datos de configuración de exportación. Antes de llamar al [**método ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) de la clase [**Msvm \_ VirtualSystemManagementService,**](msvm-virtualsystemmanagementservice.md) se puede recuperar una instancia de [**Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) mediante esta asociación.

La sintaxis siguiente se simplifica Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemExportSettingData : CIM_ElementSettingData
{
  CIM_ComputerSystem                  REF ManagedElement;
  Msvm_VirtualSystemExportSettingData REF SettingData;
  uint16                                  IsDefault = 1;
  uint16                                  IsCurrent = 1;
  uint16                                  IsNext = 0;
};
```

## <a name="members"></a>Miembros

La **clase \_ SystemExportSettingData de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SystemExportSettingData de Msvm** tiene estas propiedades.

<dl> <dt>

**IsCurrent**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la configuración a la que se hace referencia se está utilizando actualmente en el funcionamiento del elemento o si se desconoce esta información. Esta propiedad se hereda del [**\_ elemento CIMSettingData.**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)



| Value                                                                        | Significado                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>0</dt> </dl> | Unknown<br/>     |
| <dl> <dt>1</dt> </dl> | Current<br/>     |
| <dl> <dt>2</dt> </dl> | No actual<br/> |



 

</dd> <dt>

**IsDefault**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la configuración a la que se hace referencia es una configuración predeterminada para el elemento o si se desconoce esta información. Esta propiedad se hereda del [**\_ elemento CIMSettingData.**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)



| Valor                                                                        | Significado                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>0</dt> </dl> | Unknown<br/>     |
| <dl> <dt>1</dt> </dl> | Valor predeterminado<br/>     |
| <dl> <dt>2</dt> </dl> | No predeterminado<br/> |



 

</dd> <dt>

**IsNext**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la configuración a la que se hace referencia es la siguiente configuración que se va a aplicar. Por ejemplo, la aplicación podría tener lugar en una solicitud de nueva inicialización, restablecimiento y reconfiguración. Podría ser una configuración permanente o una configuración que solo se usa una vez, como indica la marca . Si se trata de una configuración permanente, la configuración se aplica cada vez que se reinicializa el elemento administrado, hasta que esta marca se restablezca manualmente. Sin embargo, si es de un solo uso, la marca se borra automáticamente después de aplicar la configuración. Además, si se especifica esta marca (es decir, se establece en un valor distinto de 0 (desconocido),tendrá prioridad sobre los datos de configuración que se hayan especificado como predeterminados. Por ejemplo: si el elemento administrado es un sistema informático y el valor de esta marca es 1 (Es siguiente), la configuración será efectiva la próxima vez que se restablezca el sistema. Y, a menos que se cambie esta marca, se conservará para restablecimientos posteriores del sistema. Sin embargo, si esta marca se establece en 3 (Is Next For Single Use), esta configuración solo se usará una vez y la marca se restablecería después a 2 (Is Not Next). Por lo tanto, en el ejemplo anterior, si el sistema se reinicia en una sucesión rápida, la configuración no se usará en el segundo reinicio.

Esta propiedad se hereda del [**\_ elemento CIMSettingData.**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)



| Value                                                                        | Significado                           |
|------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>0</dt> </dl> | Unknown<br/>                |
| <dl> <dt>1</dt> </dl> | Is Next<br/>                |
| <dl> <dt>2</dt> </dl> | Is Not Next<br/>            |
| <dl> <dt>3</dt> </dl> | Es el siguiente para un solo uso<br/> |



 

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) \_ ("CIM ElementSettingData.ManagedElement")
</dt> </dl>

Referencia a la máquina virtual. Esta propiedad se hereda del [**\_ elemento CIMSettingData.**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) \_ ("CIM ElementSettingData.SettingData")
</dt> </dl>

Referencia a los datos de configuración de exportación de la máquina virtual. Esta propiedad se hereda del [**\_ elemento CIMSettingData.**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a **la clase \_ SystemExportSettingData de Msvm** podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

