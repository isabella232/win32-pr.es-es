---
description: Asocia una máquina virtual y sus datos de configuración de exportación.
ms.assetid: FAAE7F74-07C0-4638-ABF9-5DEDBF2B9DD6
title: Msvm_SystemExportSettingData (clase)
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
ms.openlocfilehash: 8203a45bb911743bb064c1a686da0b3d8abe99bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652374"
---
# <a name="msvm_systemexportsettingdata-class"></a>MSVM \_ SystemExportSettingData (clase)

Asocia una máquina virtual y sus datos de configuración de exportación. Antes de llamar al método [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) de la clase [**\_ VirtualSystemManagementService de MSVM**](msvm-virtualsystemmanagementservice.md) , se puede recuperar una instancia de [**MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) mediante esta asociación.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

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

La clase **MSVM \_ SystemExportSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ SystemExportSettingData** tiene estas propiedades.

<dl> <dt>

**IsCurrent**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la configuración a la que se hace referencia se está utilizando actualmente en el funcionamiento del elemento o si esta información es desconocida. Esta propiedad se hereda de [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).



| Value                                                                        | Significado                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>0</dt> </dl> | Unknown<br/>     |
| <dl> <dt>1</dt> </dl> | Current<br/>     |
| <dl> <dt>2</dt> </dl> | No actual<br/> |



 

</dd> <dt>

**IsDefault**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la configuración a la que se hace referencia es un valor predeterminado para el elemento o si esta información es desconocida. Esta propiedad se hereda de [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).



| Value                                                                        | Significado                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>0</dt> </dl> | Unknown<br/>     |
| <dl> <dt>1</dt> </dl> | Valor predeterminado<br/>     |
| <dl> <dt>2</dt> </dl> | No es el valor predeterminado<br/> |



 

</dd> <dt>

**IsNext**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la configuración a la que se hace referencia es la opción siguiente que se va a aplicar. Por ejemplo, la aplicación puede tener lugar en una solicitud de reinicialización, restablecimiento y reconfiguración. Puede ser un valor de configuración permanente o una configuración usada solo una vez, como indica la marca. Si se trata de una configuración permanente, se aplica la configuración cada vez que se reinicializa el elemento administrado, hasta que esta marca se restablece manualmente. Sin embargo, si es de uso único, la marca se borra automáticamente después de aplicar la configuración. Además, si se especifica esta marca (es decir, se establece en un valor distinto de 0 (desconocido)), esto tiene prioridad sobre cualquier dato de configuración que se pueda haber especificado como predeterminado. Por ejemplo: Si el elemento administrado es un sistema informático y el valor de esta marca es 1 (es el siguiente), la configuración será efectiva la próxima vez que se restablezca el sistema. Y, a menos que se cambie esta marca, se conservará para los restablecimientos del sistema posteriores. Sin embargo, si esta marca se establece en 3 (es la siguiente para un solo uso), esta configuración solo se usará una vez y la marca se restablecerá después de la 2 (no es siguiente). Por lo tanto, en el ejemplo anterior, si el sistema se reinicia en una sucesión rápida, la configuración no se utilizará en el segundo reinicio.

Esta propiedad se hereda de [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).



| Value                                                                        | Significado                           |
|------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>0</dt> </dl> | Unknown<br/>                |
| <dl> <dt>1</dt> </dl> | Siguiente<br/>                |
| <dl> <dt>2</dt> </dl> | No es siguiente<br/>            |
| <dl> <dt>3</dt> </dl> | Siguiente para uso único<br/> |



 

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ElementSettingData. ManagedElement")
</dt> </dl>

Referencia a la máquina virtual. Esta propiedad se hereda de [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ElementSettingData. SettingData")
</dt> </dl>

Referencia a los datos de configuración de exportación de la máquina virtual. Esta propiedad se hereda de [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).

</dd> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la clase **MSVM \_ SystemExportSettingData** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

