---
description: La relación \_ Cim DependencyContext asocia una clase de dependencia CIM con \_ uno o varios objetos de configuración \_ cim. Por ejemplo, las dependencias de un sistema informático pueden cambiar en función de la red a la que está conectado el sistema.
ms.assetid: 9f35fc41-1bfa-4018-a54c-64c875c710d4
ms.tgt_platform: multiple
title: CIM_DependencyContext clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DependencyContext
- CIM_DependencyContext.Context
- CIM_DependencyContext.Dependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 845086b7d41eb03227d6b5b47240ef4bf9e1a2c35f8049c96d5c665800b327e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924645"
---
# <a name="cim_dependencycontext-class"></a>Clase \_ DependencyContext de CIM

La **relación \_ Cim DependencyContext** asocia una clase [**de \_ dependencia CIM**](cim-dependency.md) a uno o varios objetos de configuración [**\_ cim.**](cim-configuration.md) Por ejemplo, las dependencias de un sistema informático pueden cambiar en función de la red a la que está conectado el sistema.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Aggregation, Association, UUID("{A228E208-DB22-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DependencyContext
{
  CIM_Configuration REF Context;
  CIM_Dependency    REF Dependency;
};
```

## <a name="members"></a>Miembros

La **clase \_ DependencyContext de CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ DependencyContext de CIM** tiene estas propiedades.

<dl> <dt>

**Contexto**
</dt> <dd> <dl> <dt>

Tipo de datos: **Configuración de CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Agregado**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Referencia al objeto de configuración que agrega la dependencia.

</dd> <dt>

**Dependencia**
</dt> <dd> <dl> <dt>

Tipo de datos: **dependencia CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a una dependencia agregada.

</dd> </dl>

## <a name="remarks"></a>Comentarios

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

