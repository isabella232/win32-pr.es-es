---
description: La \_ clase WMI UserDesktop Association de Win32 relaciona una configuración de escritorio y de cuenta de usuario específica.
ms.assetid: 5ea83ad6-bd0a-4c16-85b2-e3e61ef05903
ms.tgt_platform: multiple
title: Win32_UserDesktop (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserDesktop
- Win32_UserDesktop.Element
- Win32_UserDesktop.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 39b45ee7859fea9f1068123041a87309cf40c2d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907077"
---
# <a name="win32_userdesktop-class"></a>\_Clase Win32 UserDesktop

La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ UserDesktop** Association de Win32 relaciona una configuración de escritorio y de cuenta de usuario específica.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_UserDesktop : CIM_ElementSetting
{
  Win32_UserAccount REF Element;
  Win32_Desktop     REF Setting;
};
```

## <a name="members"></a>Miembros

La **clase \_ UserDesktop de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ UserDesktop de Win32** tiene estas propiedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ cuentadeusuario**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("elemento"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ cuentadeusuario")
</dt> </dl>

Referencia a la instancia de que representa la cuenta de usuario cuyo escritorio se puede personalizar mediante la propiedad de **configuración** de esta clase.

</dd> <dt>

**Configuración**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ escritorio Win32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("configuración"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| escritorio Win32 de WMI \_ ")
</dt> </dl>

Referencia a la instancia de que representa la configuración del escritorio que sirve para personalizar un escritorio de cuenta de usuario específico.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ UserDesktop de Win32** se deriva de [**\_ ElementSetting de CIM**](cim-elementsetting.md).

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

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
