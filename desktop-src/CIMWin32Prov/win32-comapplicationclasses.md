---
description: La clase WMI de asociación abstracta COMApplicationClasses de Win32 relaciona un componente de Component Object Model (COM) y la aplicación \_ COM donde reside.
ms.assetid: 7c188199-86fb-45ba-b318-9d9529b831b8
ms.tgt_platform: multiple
title: Win32_COMApplicationClasses clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMApplicationClasses
- Win32_COMApplicationClasses.PartComponent
- Win32_COMApplicationClasses.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 01413128f7457049a4383c1148938e2136645337
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160316"
---
# <a name="win32_comapplicationclasses-class"></a>Clase \_ COMApplicationClasses de Win32

La clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) de asociación abstracta **\_ COMApplicationClasses de Win32** relaciona un componente de Component Object Model (COM) y la aplicación COM donde reside.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[abstract, UUID("{0F73ED51-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_COMApplicationClasses : CIM_Component
{
  Win32_COMClass       REF PartComponent;
  Win32_COMApplication REF GroupComponent;
};
```

## <a name="members"></a>Members

La **clase \_ COMApplicationClasses de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ COMApplicationClasses de Win32** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ ComApplication de Win32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ COMApplication")
</dt> </dl>

Una [**aplicación \_ COM de Win32**](win32-comapplication.md) que representa la aplicación COM que contiene el componente COM.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ COMClass**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ COMClass")
</dt> </dl>

Una [**clase \_ COMClass de Win32**](win32-comclass.md) que representa el componente COM agrupado en la aplicación COM.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ COMApplicationClasses de Win32** se deriva del [**componente CIM \_**](cim-component.md).

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

[**Componente \_ CIM**](cim-component.md)
</dt> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

