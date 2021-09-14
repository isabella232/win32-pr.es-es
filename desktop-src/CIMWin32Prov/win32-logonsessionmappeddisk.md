---
description: La clase LogonSessionMappedDisk de Win32 representa una asociación entre una sesión de inicio de sesión y los discos lógicos asignados \_ definidos dentro de la sesión.
ms.assetid: 013ae55e-6dd1-42fb-bcba-74d6afa1b905
ms.tgt_platform: multiple
title: Win32_LogonSessionMappedDisk clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogonSessionMappedDisk
- Win32_LogonSessionMappedDisk.Antecedent
- Win32_LogonSessionMappedDisk.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: 203c9dd783dece52fa19905d51ece3bc26584dc6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127273388"
---
# <a name="win32_logonsessionmappeddisk-class"></a>Clase LogonSessionMappedDisk de Win32 \_

La clase LogonSessionMappedDisk de Win32 representa una asociación entre una sesión de inicio de sesión y los discos lógicos asignados \_ definidos dentro de la sesión.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32a"), AMENDMENT]
class Win32_LogonSessionMappedDisk : CIM_Dependency
{
  Win32_LogonSession      REF Antecedent;
  Win32_MappedLogicalDisk REF Dependent;
};
```

## <a name="members"></a>Members

La **clase \_ LogonSessionMappedDisk de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ LogonSessionMappedDisk de Win32** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ LogonSession**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

La propiedad Antecedente hace referencia a una sesión de inicio de sesión.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ MappedLogicalDisk**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

La propiedad Dependiente hace referencia a un disco lógico asignado definido dentro de la sesión a la que hace referencia la propiedad Antecedente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CimWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Cimwin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Dependencia \_ cim**](cim-dependency.md)
</dt> </dl>

 

