---
description: Representa la definición de una métrica que se deriva de otro valor de métrica. Un \_ objeto AggregationMetricDefinition de CIM se debe asociar a los objetos de ManagedElement de CIM \_ a los que se aplica.
ms.assetid: 0059bfd6-ecf3-41f0-be6b-0ce46dfbbb18
title: CIM_AggregationMetricDefinition (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregationMetricDefinition
- CIM_AggregationMetricDefinition.ChangeType
- CIM_AggregationMetricDefinition.SimpleFunction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9a84eed5a725ebff3b39ca92bab530ef90cfca58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812734"
---
# <a name="cim_aggregationmetricdefinition-class"></a>\_Clase AggregationMetricDefinition de CIM

Representa la definición de una métrica que se deriva de otro valor de métrica. Un **objeto \_ AggregationMetricDefinition de CIM** se debe asociar a los objetos de **\_ ManagedElement de CIM** a los que se aplica.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_AggregationMetricDefinition : CIM_BaseMetricDefinition
{
  uint16 ChangeType = 5;
  uint16 SimpleFunction;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ AggregationMetricDefinition** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ AggregationMetricDefinition** tiene estas propiedades.

<dl> <dt>

**ChangeType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ChangeType"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AggregationMetricDefinition**.**IsContinuous**")
</dt> </dl>

Indica cómo cambia el valor de métrica mediante atributos comunes como el cambio de dirección, los valores mínimo y máximo y la semántica de ajuste.

<dt>

<span id="Simple_Function"></span><span id="simple_function"></span><span id="SIMPLE_FUNCTION"></span>

**Función simple** (5)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Proveedor reservado** (32768... 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**SimpleFunction**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cálculo básico realizado en una métrica subyacente para llegar al valor de esta métrica derivada. Esta propiedad es **null** cuando la propiedad **ChangeType** tiene un valor distinto de "5" (función simple).

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Mínimo** (2)


</dt> <dd>

La métrica informa del valor más bajo detectado para la entidad supervisada asociada. Esto también se conoce como límite inferior.

</dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Máximo** (3)


</dt> <dd>

La métrica informa del valor máximo detectado para la entidad supervisada asociada. Esto también se conoce como límite máximo.

</dd> <dt>

<span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>

<span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**Promedio** (4)


</dt> <dd>

La métrica informa del valor promedio de los valores de métricas subyacentes.

</dd> <dt>

<span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>

<span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>**Mediana** (5)


</dt> <dd>

La métrica informa del valor medio de los valores de métricas subyacentes.

</dd> <dt>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Modo** (6)


</dt> <dd>

la métrica informa del valor modal de los valores de métricas subyacentes.

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32768... 65535)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_BASEMETRICDEFINITION CIM**](cim-basemetricdefinition.md)
</dt> </dl>

 

