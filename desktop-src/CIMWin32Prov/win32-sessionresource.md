---
description: La asociación SessionResource de Win32 representa la relación entre una sesión y los recursos a los que \_ la sesión proporciona acceso.
ms.assetid: 39c195cf-e70b-4e93-b46b-61ed4f08f57e
ms.tgt_platform: multiple
title: Win32_SessionResource clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SessionResource
- Win32_SessionResource.Antecedent
- Win32_SessionResource.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: 399ee8af085459b4d0995e1399f0afcbb2d138735f9aa7f3f4992e177ac04839
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119971535"
---
# <a name="win32_sessionresource-class"></a>Clase SessionResource de Win32 \_

La asociación SessionResource de Win32 representa la relación entre una sesión y los recursos a los que \_ la sesión proporciona acceso.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, AMENDMENT]
class Win32_SessionResource : CIM_Dependency
{
  Win32_LogicalElement REF Antecedent;
  Win32_Session        REF Dependent;
};
```

## <a name="members"></a>Miembros

La **clase \_ SessionResource de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SessionResource de Win32** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ LogicalElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedente")
</dt> </dl>

La referencia antecedente representa los recursos utilizados por esta sesión.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Sesión de \_ Win32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidación**](../wmisdk/standard-qualifiers.md) ("Dependiente")
</dt> </dl>

La referencia dependiente representa la sesión que usa el recurso.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 
