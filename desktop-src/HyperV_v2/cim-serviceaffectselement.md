---
description: Representa una asociación entre un servicio y un elemento administrado que podría verse afectado por su ejecución.
ms.assetid: 2fd9199f-9ab0-4c42-9708-d6cd6911f77a
title: CIM_ServiceAffectsElement clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAffectsElement
- CIM_ServiceAffectsElement.AffectedElement
- CIM_ServiceAffectsElement.AffectingElement
- CIM_ServiceAffectsElement.ElementEffects
- CIM_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b8d828686a4308d9e0d76c7dd31dabd0644fdd802058fefceeec603d586e9b6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899825"
---
# <a name="cim_serviceaffectselement-class"></a>Clase \_ Cim ServiceAffectsElement

Representa una asociación entre un servicio y un elemento administrado que podría verse afectado por su ejecución.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>Miembros

La **clase CIM \_ ServiceAffectsElement** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase CIM \_ ServiceAffectsElement** tiene estas propiedades.

<dl> <dt>

**AffectedElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ManagedElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Elemento administrado que se ve afectado por el servicio.

</dd> <dt>

**AffectingElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **Servicio CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Servicio que afecta al elemento administrado.

</dd> <dt>

**ElementEffects**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ServiceAffectsElement**.**OtherElementEffectsDescriptions**")
</dt> </dl>

Efecto en el elemento administrado. Esta matriz corresponde a la **matriz OtherElementEffectsDescriptions.**

\- Uso exclusivo (2): ningún otro servicio puede tener esta asociación con el elemento .

\- Impacto en el rendimiento (3): en desuso en favor de "Consumes", "Mejora el rendimiento" o "Degrada el rendimiento". La ejecución del servicio puede mejorar o degradar el rendimiento del elemento. Esto puede ser como efecto secundario de la ejecución o como consecuencia prevista de los métodos proporcionados por el servicio.

\- Integridad de elementos (4): en desuso en favor de "Consumes", "Enhances Integrity" o "Degrades Integrity". La ejecución del servicio puede mejorar o degradar la integridad del elemento. Esto puede ser como efecto secundario de la ejecución o como consecuencia prevista de los métodos proporcionados por el servicio.

\- Administra (5): el servicio administra el elemento .

\- Consume (6): la ejecución del servicio consume parte o todo el elemento asociado como consecuencia de ejecutar el servicio. Por ejemplo, el servicio puede consumir ciclos de CPU, lo que puede afectar al rendimiento o Storage que pueden afectar tanto al rendimiento como a la integridad. (Por ejemplo, la falta de almacenamiento libre puede degradar la integridad al reducir la capacidad de guardar el estado. ) "Consumes" se puede usar solo o junto con otros valores, en particular, "Degrada el rendimiento" y "Degrada la integridad".

"Administra" y no "Consume" debe usarse para reflejar los servicios de asignación que puede proporcionar un servicio.

\- Mejora la integridad (7): el servicio puede mejorar la integridad del elemento asociado.

\- Degrada la integridad (8): el servicio puede degradar la integridad del elemento asociado.

\- Mejora el rendimiento (9): el servicio puede mejorar el rendimiento del elemento asociado.

\- Degrada el rendimiento (10): el servicio puede degradar el rendimiento del elemento asociado.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>

**Uso exclusivo** (2)


</dt> <dd></dd> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>

**Impacto en el** rendimiento (3)


</dt> <dd></dd> <dt>

<span id="Element_Integrity"></span><span id="element_integrity"></span><span id="ELEMENT_INTEGRITY"></span>

**Integridad de elementos** (4)


</dt> <dd></dd> <dt>

<span id="Manages"></span><span id="manages"></span><span id="MANAGES"></span>

**Administra** (5)


</dt> <dd></dd> <dt>

<span id="Consumes"></span><span id="consumes"></span><span id="CONSUMES"></span>

**Consume** (6)


</dt> <dd></dd> <dt>

<span id="Enhances_Integrity"></span><span id="enhances_integrity"></span><span id="ENHANCES_INTEGRITY"></span>

**Mejora la integridad** (7)


</dt> <dd></dd> <dt>

<span id="Degrades_Integrity"></span><span id="degrades_integrity"></span><span id="DEGRADES_INTEGRITY"></span>

**Degrada la integridad** (8)


</dt> <dd></dd> <dt>

<span id="Enhances_Performance"></span><span id="enhances_performance"></span><span id="ENHANCES_PERFORMANCE"></span>

**Mejora el rendimiento** (9)


</dt> <dd></dd> <dt>

<span id="Degrades_Performance"></span><span id="degrades_performance"></span><span id="DEGRADES_PERFORMANCE"></span>

**Degrada el rendimiento** (10)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Proveedor reservado** (0x8000.. 0xFFFF)


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ServiceAffectsElement**.**ElementEffects**")
</dt> </dl>

Cada elemento de la matriz proporciona información adicional para el elemento correspondiente en la **matriz ElementEffects.** Se requiere una descripción para cualquier elemento de la **matriz ElementEffects** que esté establecido en **Other** ("1").

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

