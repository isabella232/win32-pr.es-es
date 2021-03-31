---
description: La \_ Asociación SessionResource de Win32 representa la relación entre una sesión y los recursos a los que la sesión proporciona acceso.
ms.assetid: 39c195cf-e70b-4e93-b46b-61ed4f08f57e
ms.tgt_platform: multiple
title: Win32_SessionResource (clase)
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
ms.openlocfilehash: 3962c8523863bb97710bf21be38906d3897beea3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807741"
---
# <a name="win32_sessionresource-class"></a>\_Clase Win32 SessionResource

La \_ Asociación SessionResource de Win32 representa la relación entre una sesión y los recursos a los que la sesión proporciona acceso.

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

Calificadores: [**invalidación**](../wmisdk/standard-qualifiers.md) ("antecedente")
</dt> </dl>

La referencia Antecedent representa los recursos usados por esta sesión.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ sesión Win32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](../wmisdk/standard-qualifiers.md) ("dependiente")
</dt> </dl>

La referencia dependiente representa la sesión que utiliza el recurso.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CimWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Cimwin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dependencia de CIM \_**](cim-dependency.md)
</dt> </dl>

 

 
