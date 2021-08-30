---
description: Representa el valor de instancia de una métrica definida por una instancia de \_ AggregationMetricDefinition de CIM.
ms.assetid: 663ef18a-0238-416f-9682-8809b271b4fc
title: CIM_AggregationMetricValue clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregationMetricValue
- CIM_AggregationMetricValue.AggregationTimeStamp
- CIM_AggregationMetricValue.AggregationDuration
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 254b2325873c2037b50f6cc0b013865589c23e2197ca113dbcc41bae6dd8a352
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041705"
---
# <a name="cim_aggregationmetricvalue-class"></a>Clase \_ AggregationMetricValue de CIM

Representa el valor de instancia de una métrica definida por una instancia de **Cim \_ AggregationMetricDefinition.**

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_AggregationMetricValue : CIM_BaseMetricValue
{
  datetime AggregationTimeStamp;
  datetime AggregationDuration;
};
```

## <a name="members"></a>Miembros

La **clase \_ Cim AggregationMetricValue** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ Cim AggregationMetricValue** tiene estas propiedades.

<dl> <dt>

**AggregationDuration**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AggregationMetricValue**.**AggregationTimeStamp**")
</dt> </dl>

Representa la duración de tiempo durante la que se calculó la agregación. El inicio de un intervalo de supervisión durante el que se aplica la función de agregación se determina restando el valor **AggregationDuration** del **valor AggregationTimestamp.**

</dd> <dt>

**AggregationTimeStamp**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AggregationMetricValue**.**Duration**")
</dt> </dl>

Hora a la que se aplicó la función de agregación para determinar el valor de la instancia de métrica. Esto es diferente del momento en que se crea la instancia. El **valor AggregationTimeStamp** cambia cada vez que se aplica la función de agregación para calcular el valor.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ BaseMetricValue**](cim-basemetricvalue.md)
</dt> </dl>

 

