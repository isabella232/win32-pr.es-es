---
description: La clase \_ WMI Win32 AutochkSetting representa la configuración de la operación de comprobación automática de un disco.
ms.assetid: 637f4d5d-f2f0-4fe0-bbde-7804156979b7
ms.tgt_platform: multiple
title: Win32_AutochkSetting clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AutochkSetting
- Win32_AutochkSetting.Caption
- Win32_AutochkSetting.Description
- Win32_AutochkSetting.SettingID
- Win32_AutochkSetting.UserInputDelay
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6cccf1877d8812e1fee4816e80189b8404d4090a1ef15f45e840fdd6e58d8ae7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020333"
---
# <a name="win32_autochksetting-class"></a>Clase \_ AutochkSetting de Win32

La clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ Win32 AutochkSetting representa** la configuración de la operación de comprobación automática de un disco.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, AMENDMENT]
class Win32_AutochkSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 UserInputDelay;
};
```

## <a name="members"></a>Miembros

La **clase \_ AutochkSetting de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ Win32 AutochkSetting** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descripción textual del objeto actual.

Esta propiedad se hereda de cim [**\_ setting**](cim-setting.md).

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción textual del objeto actual.

Esta propiedad se hereda de cim [**\_ setting**](cim-setting.md).

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingId"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificador que se usa como parte de una clave para el objeto actual.

</dd> <dt>

**UserInputDelay**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKLM \\ \\ CurrentControlSet \\ \\ Control Session Manager \\ \\ \| AutoChkTimeOut"), [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("segundos")
</dt> </dl>

Retraso de entrada del usuario para la comprobación automática.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ AutochkSetting de Win32** se deriva de [**cim \_ setting**](cim-setting.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Configuración de CIM \_**](cim-setting.md)
</dt> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

