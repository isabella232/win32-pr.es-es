---
description: La asociación Desesión de Win32 define las relaciones entre las sesiones en las que una sesión forma parte de o utiliza otra sesión, por ejemplo, donde una sesión de Terminal usa una sesión \_ de inicio de sesión.
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
ms.openlocfilehash: 540cfb4c00b5df64e4ff11a1cc462eaed03be434
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061469"
---
# <a name="win32_subsession-class"></a>Clase SubSession de Win32 \_

La asociación Desesión de Win32 define las relaciones entre las sesiones en las que una sesión forma parte de o utiliza otra sesión, por ejemplo, donde una sesión de Terminal usa una sesión \_ de inicio de sesión.

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

## <a name="members"></a>Members

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

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) (antecedente)
</dt> </dl>

Una [**sesión \_ win32**](win32-session.md) que describe la sesión que tiene una subsesión.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Sesión de \_ Win32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidación**](../wmisdk/standard-qualifiers.md) (dependiente)
</dt> </dl>

Sesión [**win32 \_**](win32-session.md) que describe la sesión que es la subsesión.

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

 

 
