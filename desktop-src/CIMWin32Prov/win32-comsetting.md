---
description: La clase WMI abstracta COMSetting de Win32 representa la configuración asociada a un componente del Modelo de objetos componentes \_ (COM) o a una aplicación COM.
ms.assetid: e8cdbee8-41ab-4aff-b17b-707667138411
ms.tgt_platform: multiple
title: Win32_COMSetting clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMSetting
- Win32_COMSetting.Caption
- Win32_COMSetting.Description
- Win32_COMSetting.SettingID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2082420d4d86c9d7ab35dc03782580e5478845507be0e454f441e3784ec824a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656295"
---
# <a name="win32_comsetting-class"></a>Clase COMSetting de Win32 \_

La clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) abstracta **\_ COMSetting de Win32** representa la configuración asociada a un componente del Modelo de objetos componentes (COM) o a una aplicación COM.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[abstract, UUID("{E5D8A560-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_COMSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
};
```

## <a name="members"></a>Miembros

La **clase \_ COMSetting de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ COMSetting de Win32** tiene estas propiedades.

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

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificador por el que se conoce el objeto actual.

Esta propiedad se hereda de cim [**\_ setting**](cim-setting.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ COMSetting de Win32** se deriva de [**cim \_ setting**](cim-setting.md).

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

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

