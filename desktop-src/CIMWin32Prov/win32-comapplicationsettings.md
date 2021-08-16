---
description: La clase WMI de asociación COMApplicationSettings de Win32 relaciona \_ una aplicación DCOM y sus opciones de configuración.
ms.assetid: b08eaff1-b42a-42f3-abf7-3664b6195acd
ms.tgt_platform: multiple
title: Win32_COMApplicationSettings clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMApplicationSettings
- Win32_COMApplicationSettings.Setting
- Win32_COMApplicationSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0a1126563b00861ab8b8168832f72189c3a3828378f5d89c4b74e49f68b09bd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118417915"
---
# <a name="win32_comapplicationsettings-class"></a>Clase COMApplicationSettings de Win32 \_

La clase WMI **de asociación \_ COMApplicationSettings** [de](/windows/desktop/WmiSdk/retrieving-a-class) Win32 relaciona una aplicación DCOM y sus opciones de configuración.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A563-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_COMApplicationSettings : CIM_ElementSetting
{
  Win32_DCOMApplicationSetting REF Setting;
  Win32_DCOMApplication        REF Element;
};
```

## <a name="members"></a>Miembros

La **clase \_ COMApplicationSettings de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ COMApplicationSettings de Win32** tiene estas propiedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ DCOMApplication**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplication")
</dt> </dl>

Una [**aplicación \_ DCOM de Win32**](win32-dcomapplication.md) que representa la aplicación DCOM donde se aplica la configuración.

</dd> <dt>

**Configuración**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ DCOMApplicationSetting**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplicationSetting")
</dt> </dl>

Un [**\_ DCOMApplicationSetting de Win32**](win32-dcomapplicationsetting.md) que representa los valores de configuración asociados a la aplicación DCOM.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ COMApplicationSettings de Win32** se deriva del [**elemento \_ CIMSetting**](cim-elementsetting.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

