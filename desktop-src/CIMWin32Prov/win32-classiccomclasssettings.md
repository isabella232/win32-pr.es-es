---
description: La clase WMI de asociación ClassicCOMClassSettings de Win32 relaciona una clase de Modelo de objetos componentes (COM) y la configuración utilizada para configurar instancias de \_ la clase COM.
ms.assetid: 50f253cc-b8ae-41ac-b01f-ea816f5ca3d4
ms.tgt_platform: multiple
title: Win32_ClassicCOMClassSettings clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClassSettings
- Win32_ClassicCOMClassSettings.Setting
- Win32_ClassicCOMClassSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb9c190157742aeca7c1ba6008a784005d054ca6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160330"
---
# <a name="win32_classiccomclasssettings-class"></a>Clase ClassicCOMClassSettings de Win32 \_

La clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) de asociación **\_ ClassicCOMClassSettings de Win32** relaciona una clase de Modelo de objetos componentes (COM) y la configuración utilizada para configurar instancias de la clase COM.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A564-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClassSettings : CIM_ElementSetting
{
  Win32_ClassicCOMClassSetting REF Setting;
  Win32_ClassicCOMClass        REF Element;
};
```

## <a name="members"></a>Members

La **clase \_ ClassicCOMClassSettings de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Win32 \_ ClassicCOMClassSettings** tiene estas propiedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ ClassicCOMClass**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")
</dt> </dl>

Clase [**\_ ClassicCOMClass de Win32**](win32-classiccomclass.md) que representa la clase COM donde se aplica la configuración.

</dd> <dt>

**Configuración**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ ClassicCOMClassSetting**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClassSetting")
</dt> </dl>

[**Win32 \_ ClassicCOMClassSetting que**](win32-classiccomclasssetting.md) representa los valores de configuración asociados a la clase COM.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ ClassicCOMClassSettings de Win32** se deriva del [**elemento \_ CIMSetting**](cim-elementsetting.md).

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

[**CIM \_ ElementSetting**](cim-elementsetting.md)
</dt> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

