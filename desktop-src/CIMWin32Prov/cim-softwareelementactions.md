---
description: La \_ Asociación SoftwareElementActions de CIM identifica las acciones de un elemento de software.
ms.assetid: 2f8a584c-dff0-48f8-bc5f-2b833b5c0b18
ms.tgt_platform: multiple
title: CIM_SoftwareElementActions (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementActions
- CIM_SoftwareElementActions.Action
- CIM_SoftwareElementActions.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f51cc122cdf354be9611ca1cca4ebcbe1635d14
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659441"
---
# <a name="cim_softwareelementactions-class"></a>\_Clase SoftwareElementActions de CIM

La **Asociación \_ SoftwareElementActions de CIM** identifica las acciones de un elemento de software.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[UUID("{4B82D255-E3CD-11d2-8601-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_SoftwareElementActions
{
  CIM_Action          REF Action;
  CIM_SoftwareElement REF Element;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ SoftwareElementActions** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ SoftwareElementActions** tiene estas propiedades.

<dl> <dt>

**Acción**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ acción de CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Referencia a una instancia de [**\_ acción de CIM**](cim-action.md) .

</dd> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ SoftwareElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Referencia a una instancia de [**\_ SoftwareElement de CIM**](cim-softwareelement.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

WMI no implementa esta clase. Para las clases WMI derivadas de **CIM \_ SoftwareElementActions**, vea [clases Win32](win32-provider.md).

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

