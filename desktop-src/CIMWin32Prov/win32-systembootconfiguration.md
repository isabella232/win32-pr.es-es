---
description: La clase WMI de asociación SystemBootConfiguration de Win32 \_ relaciona un sistema informático y su configuración de arranque.
ms.assetid: 1c6bce81-84d9-4949-92da-6111b4ecc939
ms.tgt_platform: multiple
title: Win32_SystemBootConfiguration clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemBootConfiguration
- Win32_SystemBootConfiguration.Element
- Win32_SystemBootConfiguration.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 863e4103f7e87681e25ccf53679bfe006ed3ff75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061470"
---
# <a name="win32_systembootconfiguration-class"></a>Clase SystemBootConfiguration de Win32 \_

La clase WMI **de asociación \_ SystemBootConfiguration** [de](../wmisdk/retrieving-a-class.md) Win32 relaciona un sistema informático y su configuración de arranque.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en el orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C507-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemBootConfiguration : Win32_SystemSetting
{
  Win32_ComputerSystem    REF Element;
  Win32_BootConfiguration REF Setting;
};
```

## <a name="members"></a>Members

La **clase \_ SystemBootConfiguration de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SystemBootConfiguration de Win32** tiene estas propiedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ ComputerSystem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

Referencia a la instancia de que representa el sistema del equipo mediante la configuración de arranque.

</dd> <dt>

**Configuración**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ BootConfiguration**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ BootConfiguration")
</dt> </dl>

Referencia a la instancia de que representa la configuración de arranque del sistema del equipo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ SystemBootConfiguration de Win32** se deriva de [**\_ SystemSetting de Win32.**](win32-systemsetting.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SystemSetting de Win32 \_**](win32-systemsetting.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
