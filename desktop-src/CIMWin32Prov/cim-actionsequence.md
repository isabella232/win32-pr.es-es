---
description: La \_ Asociación ActionSequence de CIM define una serie de operaciones que transfieren el elemento de software (al que hace referencia la \_ Asociación SOFTWAREELEMENTACTIONS de CIM) al siguiente estado o quita el elemento de software de su estado actual.
ms.assetid: b539c424-bc2a-414b-b56c-72550004720f
ms.tgt_platform: multiple
title: CIM_ActionSequence (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActionSequence
- CIM_ActionSequence.Next
- CIM_ActionSequence.Prior
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71150d1ad9785d81579d8f305fe46bc6b7e57d00
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659528"
---
# <a name="cim_actionsequence-class"></a>\_Clase ActionSequence de CIM

La **Asociación \_ ActionSequence de CIM** define una serie de operaciones que transfieren el elemento de software (al que hace referencia la Asociación [**\_ SoftwareElementActions de CIM**](cim-softwareelementactions.md) ) al siguiente estado o quita el elemento de software de su estado actual.

Las acciones de siguiente estado y las acciones de desinstalación asociadas a un elemento de software determinado deben ser una secuencia continua. Dado que **CIM \_ ActionSequence** es una asociación, los bucles de la clase de [**\_ acción CIM**](cim-action.md) , con roles para la acción "anterior" y la acción "siguiente", forman una secuencia.

La necesidad de una secuencia continua implica:

-   Dentro del conjunto de acciones de siguiente estado o desinstalación, solo hay una acción que no tiene una instancia de la Asociación **\_ ActionSequence de CIM** que hace referencia a ella en el rol "siguiente". Esta es la primera acción de la secuencia.
-   Dentro del conjunto de acciones de siguiente estado o desinstalación, solo hay una acción que no tiene una instancia de la Asociación **\_ ActionSequence de CIM** que hace referencia a ella en el rol "anterior". Esta es la última acción de la secuencia.
-   Todas las demás acciones del conjunto de acciones de siguiente estado y desinstalación deben participar en dos instancias de la **Asociación \_ ActionSequence de CIM** , una en un rol "anterior" y otra en el rol "siguiente".

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Association, UUID("{F127E50E-E3E0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ActionSequence
{
  CIM_Action REF Next;
  CIM_Action REF Prior;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ ActionSequence** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ ActionSequence** tiene estas propiedades.

<dl> <dt>

**Siguiente**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ acción de CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Referencia a la siguiente acción.

</dd> <dt>

**Anticipa**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ acción de CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Referencia a la acción anterior.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las clases de [**\_ acción CIM**](cim-action.md) que participan en esta asociación deben tener el mismo valor para la propiedad **Direction** .

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases CIM](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

