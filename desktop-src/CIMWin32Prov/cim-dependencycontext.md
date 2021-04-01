---
description: La \_ relación DependencyContext de CIM asocia una \_ clase de dependencia CIM a uno o más objetos de configuración de CIM \_ . Por ejemplo, las dependencias de un equipo pueden cambiar en función de la red a la que está conectado el sistema.
ms.assetid: 9f35fc41-1bfa-4018-a54c-64c875c710d4
ms.tgt_platform: multiple
title: CIM_DependencyContext (clase)
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
ms.openlocfilehash: 69319a4f4d228d484da62411060ae3fead90bb79
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907301"
---
# <a name="cim_dependencycontext-class"></a>\_Clase DependencyContext de CIM

La **relación \_ DependencyContext de CIM** asocia una clase de [**\_ dependencia CIM**](cim-dependency.md) a uno o más objetos de [**\_ configuración de CIM**](cim-configuration.md) . Por ejemplo, las dependencias de un equipo pueden cambiar en función de la red a la que está conectado el sistema.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

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

La clase **CIM \_ DependencyContext** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ DependencyContext** tiene estas propiedades.

<dl> <dt>

**Contexto**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ configuración de CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **agregado**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Referencia al objeto de configuración que agrega la dependencia.

</dd> <dt>

**Dependencia**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ dependencia CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a una dependencia agregada.

</dd> </dl>

## <a name="remarks"></a>Observaciones

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

