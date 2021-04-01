---
description: Representa el valor de instancia de una métrica definida por una instancia de la \_ clase MSVM AggregationMetricDefinition.
ms.assetid: 6dfcb711-6137-492a-aff4-82facbd11949
title: Msvm_AggregationMetricValue (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AggregationMetricValue
- Msvm_AggregationMetricValue.InstanceID
- Msvm_AggregationMetricValue.Caption
- Msvm_AggregationMetricValue.Description
- Msvm_AggregationMetricValue.ElementName
- Msvm_AggregationMetricValue.MetricDefinitionId
- Msvm_AggregationMetricValue.MeasuredElementName
- Msvm_AggregationMetricValue.TimeStamp
- Msvm_AggregationMetricValue.Duration
- Msvm_AggregationMetricValue.MetricValue
- Msvm_AggregationMetricValue.BreakdownDimension
- Msvm_AggregationMetricValue.BreakdownValue
- Msvm_AggregationMetricValue.Volatile
- Msvm_AggregationMetricValue.AggregationTimeStamp
- Msvm_AggregationMetricValue.AggregationDuration
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6842e5a23fbbf7cf1d639862cf5b9737bc1ff96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083099"
---
# <a name="msvm_aggregationmetricvalue-class"></a>MSVM \_ AggregationMetricValue (clase)

Representa el valor de instancia de una métrica definida por una instancia de la clase [**MSVM \_ AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md) . Las propiedades heredadas de [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) proporcionan el valor de métrica real. Las propiedades definidas por esta clase proporcionan información sobre el intervalo sobre el que se aplicó la función de agregación.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AggregationMetricValue : CIM_AggregationMetricValue
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  string   MetricDefinitionId;
  string   MeasuredElementName;
  datetime TimeStamp;
  datetime Duration;
  string   MetricValue;
  string   BreakdownDimension;
  string   BreakdownValue;
  boolean  Volatile;
  datetime AggregationTimeStamp;
  datetime AggregationDuration;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ AggregationMetricValue** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ AggregationMetricValue** tiene estas propiedades.

<dl> <dt>

**AggregationDuration**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Representa la duración de tiempo en la que se calculó la agregación. El inicio de un intervalo de supervisión sobre el que se aplica la función de agregación se determina restando el **AggregationDuration** de **AggregationTimeStamp**. Esta propiedad se hereda de **\_ AggregationMetricValue CIM**.

</dd> <dt>

**AggregationTimeStamp**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identifica la hora en que se aplicó la función de agregación para determinar el valor de la instancia de métrica. Esto no es lo mismo que la hora en que se creó la instancia. En el caso de una instancia de **\_ AggregationMetricValue de CIM** determinada, el **AggregationTimeStamp** cambia cada vez que se aplica la función de agregación para calcular el valor. Esta propiedad se hereda de **\_ AggregationMetricValue CIM**.

</dd> <dt>

**BreakdownDimension**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica una dimensión de desglose de la matriz **BreakdownDimensions** definida en la [**\_ BaseMetricDefinition de MSVM**](msvm-basemetricdefinition.md)asociada. Esta es la dimensión en la que se divide este conjunto de valores de métricas. Esta propiedad se hereda de [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**BreakdownValue**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Define un valor de la propiedad **BreakdownDimension** definida para esta instancia de valor de métrica. Por ejemplo, si **BreakdownDimension** es "TransactionName", esta propiedad podría nombrar la transacción real a la que se aplica este valor de métrica en particular. Esta propiedad se hereda de [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Duration**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica la duración de la validez de este valor de métrica. Esta propiedad no debe existir para las marcas de tiempo que se aplican solo a un punto en el tiempo, pero debe especificarse para los valores que se consideran válidos para un determinado período de tiempo (por ejemplo, muestreo). Si la propiedad **Duration** existe y no es **null**, la propiedad **timestamp** especifica el final del intervalo. Esta propiedad se hereda de [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**
</dt> </dl>

Cadena que identifica de forma única una instancia de esta clase. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**MeasuredElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Un nombre descriptivo para el elemento al que pertenece el valor de métrica (el elemento medido). Esta propiedad se hereda de [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**MetricDefinitionId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La clave de la instancia de [**\_ BaseMetricDefinition de MSVM**](msvm-basemetricdefinition.md) para este valor. Esta propiedad se hereda de [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**MetricValue**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor de la métrica que se representa como una cadena. Esta propiedad se hereda de [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Indicaciones**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica la hora a la que se capturó o calculó el valor de métrica. Tenga en cuenta que esto es diferente del momento en que se creó la instancia. Esta propiedad se hereda de [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Volatil**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

**True** si el valor para el siguiente punto en el tiempo usará la misma instancia de la clase y simplemente cambiará los valores de propiedad (como el **valor** o la **marca** de tiempo). Si es **true**, la instancia se reutiliza. Si **es false**, las instancias existentes permanecen sin cambios y se crea una nueva instancia para el nuevo punto en el tiempo. Esta propiedad se hereda de [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

