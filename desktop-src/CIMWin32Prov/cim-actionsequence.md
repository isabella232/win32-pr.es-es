---
description: La asociación ActionSequence de CIM define una serie de operaciones que hacen la transición del elemento de software (al que hace referencia la asociación \_ SoftwareElementActions de CIM) a su siguiente estado, o quita el elemento de software de su \_ estado actual.
ms.assetid: b539c424-bc2a-414b-b56c-72550004720f
ms.tgt_platform: multiple
title: CIM_ActionSequence clase
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
ms.openlocfilehash: a199671dd9f88cd81be50af537e156892e8cab653c70677de27c6e5df02f1d3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801085"
---
# <a name="cim_actionsequence-class"></a>Cim \_ ActionSequence (clase)

La **asociación \_ ActionSequence** de CIM define una serie de operaciones que hacen la transición del elemento de software (al que hace referencia la asociación [**\_ SoftwareElementActions**](cim-softwareelementactions.md) de CIM) a su siguiente estado, o quita el elemento de software de su estado actual.

Las acciones de estado siguiente y las acciones de desinstalación asociadas a un elemento de software determinado deben ser una secuencia continua. Dado **que \_ ACCIÓN CIMSequence** es una asociación, los bucles de la clase Acción [**CIM, \_**](cim-action.md) con roles para la acción "anterior" y la acción "siguiente", forman una secuencia.

La necesidad de una secuencia continua implica:

-   Dentro del conjunto de acciones next-state o uninstall, solo hay una acción que no tiene una instancia de la asociación **\_ Cim ActionSequence** que hace referencia a ella en el rol "siguiente". Esta es la primera acción de la secuencia.
-   Dentro del conjunto de acciones next-state o uninstall, solo hay una acción que no tiene una instancia de la asociación **\_ Cim ActionSequence** que hace referencia a ella en el rol "anterior". Esta es la última acción de la secuencia.
-   Todas las demás acciones dentro del conjunto de acciones de estado siguiente y desinstalación deben participar en dos instancias de la asociación **\_ ActionSequence** de CIM, una en un rol "anterior" y otra en el rol "siguiente".

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

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

La **clase \_ ActionSequence de CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ActionSequence de CIM** tiene estas propiedades.

<dl> <dt>

**Siguiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Acción \_ CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Máximo**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Mínimo**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Referencia a la acción siguiente.

</dd> <dt>

**Antes**
</dt> <dd> <dl> <dt>

Tipo de datos: **Acción \_ CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Máximo**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Mínimo**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Referencia a la acción anterior.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las [**clases \_ de acción**](cim-action.md) CIM que participan en esta asociación deben tener el mismo valor para la propiedad **Direction.**

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases CIM](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

