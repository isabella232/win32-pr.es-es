---
description: La clase WMI de asociación UserDesktop de Win32 relaciona una cuenta de usuario y una configuración de \_ escritorio que son específicas de ella.
ms.assetid: 5ea83ad6-bd0a-4c16-85b2-e3e61ef05903
ms.tgt_platform: multiple
title: Win32_UserDesktop clase
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126892441"
---
# <a name="win32_userdesktop-class"></a>Clase UserDesktop de Win32 \_

La clase WMI **de asociación \_ UserDesktop** [de](../wmisdk/retrieving-a-class.md) Win32 relaciona una cuenta de usuario y una configuración de escritorio que son específicas de ella.

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

## <a name="members"></a>Members

La **clase \_ UserDesktop de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ UserDesktop de Win32** tiene estas propiedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ UserAccount**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ UserAccount")
</dt> </dl>

Referencia a la instancia de que representa la cuenta de usuario cuyo escritorio se puede personalizar **mediante Configuración** propiedad de esta clase.

</dd> <dt>

**Configuración**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ Desktop**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Desktop")
</dt> </dl>

Referencia a la instancia de que representa la configuración de escritorio que sirve para personalizar un escritorio de cuenta de usuario específico.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ UserDesktop de Win32** se deriva del [**elemento \_ CIMSetting**](cim-elementsetting.md).

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

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
