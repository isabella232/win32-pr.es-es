---
description: La clase WMI de asociación SystemDesktop de Win32 \_ relaciona un sistema informático y su configuración de escritorio.
ms.assetid: 2b024660-d707-4463-8207-73df74bfa7d6
ms.tgt_platform: multiple
title: Win32_SystemDesktop clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDesktop
- Win32_SystemDesktop.Element
- Win32_SystemDesktop.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3e14cab58a445fd645b9d59c1aea713bf6c40ac0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061462"
---
# <a name="win32_systemdesktop-class"></a>Clase SystemDesktop de Win32 \_

La **clase WMI de asociación \_ SystemDesktop** [de](../wmisdk/retrieving-a-class.md) Win32 relaciona un sistema informático y su configuración de escritorio.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C506-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDesktop : Win32_SystemSetting
{
  Win32_ComputerSystem REF Element;
  Win32_Desktop        REF Setting;
};
```

## <a name="members"></a>Members

La **clase \_ SystemDesktop de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SystemDesktop de Win32** tiene estas propiedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ ComputerSystem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

Referencia a la instancia de que representa el sistema del equipo donde existe la configuración de escritorio.

</dd> <dt>

**Configuración**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ Desktop**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Desktop")
</dt> </dl>

Referencia a la instancia de que representa la configuración existente en el sistema del equipo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ SystemDesktop de Win32** se deriva de [**\_ SystemSetting de Win32.**](win32-systemsetting.md)

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

 

 
