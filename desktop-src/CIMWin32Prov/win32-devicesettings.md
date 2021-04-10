---
description: La \_ clase abstracta WMI DeviceSettings de Win32 relaciona un dispositivo lógico y un valor de configuración que se puede aplicar a él.
ms.assetid: 4f6c4c26-8da9-4e2c-8b8c-cec658ac08d4
ms.tgt_platform: multiple
title: Win32_DeviceSettings (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceSettings
- Win32_DeviceSettings.Setting
- Win32_DeviceSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1cd9cae29cfa608c9f3c0c36ebfe3ca7f903c809
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275053"
---
# <a name="win32_devicesettings-class"></a>\_Clase Win32 DeviceSettings

La [clase abstracta WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DeviceSettings de Win32** relaciona un dispositivo lógico y un valor de configuración que se puede aplicar a él.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{8502C4FD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceSettings : CIM_ElementSetting
{
  CIM_Setting       REF Setting;
  CIM_LogicalDevice REF Element;
};
```

## <a name="members"></a>Miembros

La **clase \_ DeviceSettings de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ DeviceSettings de Win32** tiene estas propiedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ LogicalDevice de CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("elemento"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| lógico CIM CIM \_ ")
</dt> </dl>

Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que representa las propiedades del dispositivo lógico en el que se puede aplicar la configuración.

</dd> <dt>

**Configuración**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ configuración de CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("configuración"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| configuración CIM CIM \_ ")
</dt> </dl>

[**\_ Configuración de CIM**](cim-setting.md) que representa la configuración que se puede aplicar al dispositivo lógico.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ DeviceSettings de Win32** se deriva de [**\_ ElementSetting de CIM**](cim-elementsetting.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_ELEMENTSETTING CIM**](cim-elementsetting.md)
</dt> <dt>

[Clases de hardware de sistema del equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

