---
description: La asociación de SubSession de Win32 define las relaciones entre sesiones en las que una sesión forma parte de o utiliza otra sesión, por ejemplo, cuando una sesión de Terminal usa una sesión \_ de inicio de sesión.
ms.assetid: 2269de22-b086-4f71-8b19-bc53e1c88dc7
ms.tgt_platform: multiple
title: Win32_SubSession clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SubSession
- Win32_SubSession.Antecedent
- Win32_SubSession.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: e575fddd5d869d7670aa3e42bf3f948badd7fd1b24befdf8839045c788e59634
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642655"
---
# <a name="win32_subsession-class"></a>Clase SubSession de Win32 \_

La asociación de SubSession de Win32 define las relaciones entre sesiones en las que una sesión forma parte de o utiliza otra sesión, por ejemplo, cuando una sesión de Terminal usa una sesión \_ de inicio de sesión.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, AMENDMENT]
class Win32_SubSession : CIM_Dependency
{
  Win32_Session REF Antecedent;
  Win32_Session REF Dependent;
};
```

## <a name="members"></a>Miembros

La **clase \_ SubSession de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SubSession de Win32** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Sesión de \_ Win32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) (Antecedente)
</dt> </dl>

Una [**sesión win32 \_**](win32-session.md) que describe la sesión que tiene una subsesión.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Sesión de \_ Win32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) (Dependiente)
</dt> </dl>

Una [**sesión win32 \_**](win32-session.md) que describe la sesión que es la subsesión.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CimWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Cimwin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dependencia \_ cim**](cim-dependency.md)
</dt> </dl>

 

 
