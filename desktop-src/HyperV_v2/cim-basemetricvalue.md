---
description: Representa el valor de instancia de una métrica.
ms.assetid: 6b272ae8-7684-45bb-bff8-6559680cc8b6
title: CIM_BaseMetricValue (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BaseMetricValue
- CIM_BaseMetricValue.InstanceID
- CIM_BaseMetricValue.MetricDefinitionId
- CIM_BaseMetricValue.MeasuredElementName
- CIM_BaseMetricValue.TimeStamp
- CIM_BaseMetricValue.Duration
- CIM_BaseMetricValue.MetricValue
- CIM_BaseMetricValue.BreakdownDimension
- CIM_BaseMetricValue.BreakdownValue
- CIM_BaseMetricValue.Volatile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ca6c90a4b6b3ef3e690c13612f69480ec5f008be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002571"
---
# <a name="cim_basemetricvalue-class"></a>\_Clase BaseMetricValue de CIM

Representa el valor de instancia de una métrica.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_BaseMetricValue : CIM_ManagedElement
{
  string   InstanceID;
  string   MetricDefinitionId;
  string   MeasuredElementName;
  datetime TimeStamp;
  datetime Duration;
  string   MetricValue;
  string   BreakdownDimension;
  string   BreakdownValue;
  boolean  Volatile;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ BaseMetricValue** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ BaseMetricValue** tiene estas propiedades.

<dl> <dt>

**BreakdownDimension**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dimensión para la que este conjunto de valores de métrica se divide en función de la propiedad **BreakdownDimensions** del [**objeto \_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) asociado.

</dd> <dt>

**BreakdownValue**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor de la propiedad **BreakdownDimension** definida para este valor de instancia. Por ejemplo, si **BreakdownDimension** contiene "TransactionName", esta propiedad podría nombrar la transacción real a la que se aplica este valor de métrica en particular.

</dd> <dt>

**Duration**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**","**\_ BaseMetricValue CIM**.**Marca** de tiempo ")
</dt> </dl>

La duración de la validez de este valor de métrica. Esta propiedad no debe existir para las marcas de tiempo que solo se aplican a un punto en el tiempo, pero debe definirse para los valores que se consideran válidos durante un período de tiempo determinado (por ejemplo, muestreo). Si la propiedad duration existe y no es null, el valor de **marca** de **tiempo** debe ser el final del intervalo.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")
</dt> </dl>

Identifica de forma única una instancia de esta clase dentro del ámbito del espacio de nombres contenedor.

> [!IMPORTANT]
>
> Con el fin de garantizar la unicidad dentro del espacio de nombres, el valor de la propiedad **InstanceID** debe construirse en el patrón siguiente: *OrgID*:*LocalID*
>
> *OrgID* debe incluir un nombre con copyright, marca registrada o de otro tipo que sea propiedad de la entidad empresarial que define el **InstanceID**, o bien un identificador registrado asignado por una entidad global reconocida. Este patrón es similar a la estructura de los nombres de clase de esquema. Además, para garantizar la exclusividad, el primer signo de dos puntos en **InstanceID** debe estar entre el *OrgID* y el *LocalID*. Por lo tanto, el *OrgID* no debe contener un signo de dos puntos (': ').
>
> La entidad de negocio elige *LocalID* y no se debe volver a usar para identificar distintos elementos del mundo real subyacentes.
>
> Si no se usa el patrón anterior, la entidad de definición debe asegurarse de que el valor **InstanceID** resultante no se vuelva a usar en las propiedades **InstanceID** producidas por este proveedor u otros proveedores para este espacio de nombres.
>
> En el caso de las instancias definidas por el grupo de tareas de administración distribuida (DMTF), el patrón debe usarse con el valor de *OrgID* establecido en CIM.

 

</dd> <dt>

**MeasuredElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre descriptivo para el elemento que mide la métrica.

Esta propiedad es necesaria si la definición de la métrica no está asociada a un objeto [**\_ ManagedElement de CIM**](cim-managedelement.md) y se puede usar en otros casos para proporcionar información complementaria. Esto permite capturar las métricas independientemente de cualquier objeto **\_ ManagedElement de CIM** .

Si hay varios objetos [**de \_ ManagedElement de CIM**](cim-managedelement.md) asociados al valor de métricas, puede elegir uno de los elementos administrados para crear la información complementaria de la métrica. La propiedad no está diseñada para utilizarse como clave externa para consultar el elemento medido. En su lugar, se debe usar la asociación con el **\_ ManagedElement de CIM** .

</dd> <dt>

**MetricDefinitionId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**ID**")
</dt> </dl>

La clave de la instancia de [**\_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) que está asociada a este valor de instancia.

</dd> <dt>

**MetricValue**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Representación de cadena del valor de métrica. El tipo de datos original del valor de métrica se especifica en el objeto [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) asociado.

</dd> <dt>

**Indicaciones**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**","**\_ BaseMetricValue CIM**.**Duration**")
</dt> </dl>

La hora a la que se calcula el valor de una instancia de métrica. Esto es diferente del momento en que se crea la instancia. Si la propiedad **volatile** es true, este valor cambia cada vez que se toma una nueva instantánea de medida.

Una aplicación de administración puede establecer una serie temporal de datos de métricas mediante la recuperación de las instancias de **CIM \_ BaseMetricValue** y ordenarlas según su valor de **marca** de tiempo.

</dd> <dt>

**Volatil**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

True si el valor de **marca** de tiempo cambia cada vez que cambia el valor de la instancia de métrica. False si este objeto debe permanecer sin cambios y se ha creado un nuevo objeto para el nuevo valor de **marca** de tiempo.

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

[**ManagedElement de CIM \_**](cim-managedelement.md)
</dt> </dl>

 

