---
description: Representa el valor de instancia de una métrica.
ms.assetid: 6b272ae8-7684-45bb-bff8-6559680cc8b6
title: CIM_BaseMetricValue clase
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
ms.openlocfilehash: 107dc3721ee32ca7f51efd563cdd6af14af483a69a5990e0b107a153b79b9351
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014703"
---
# <a name="cim_basemetricvalue-class"></a>Cim \_ BaseMetricValue (clase)

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

La **clase \_ BaseMetricValue de CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ BaseMetricValue de CIM** tiene estas propiedades.

<dl> <dt>

**BreakdownDimension**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dimensión para la que este conjunto de valores de métrica se desglosa en función de la propiedad **BreakdownDimensions** del objeto [**\_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) asociado.

</dd> <dt>

**BreakdownValue**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor de la propiedad **BreakdownDimension** definida para este valor de instancia. Por ejemplo, si **BreakdownDimension** contiene "TransactionName", esta propiedad podría dar nombre a la transacción real a la que se aplica este valor de métrica determinado.

</dd> <dt>

**Duración**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**", "**CIM \_ BaseMetricValue**.**TimeStamp**")
</dt> </dl>

Duración de tiempo durante la cual este valor de métrica es válido. Esta propiedad no debe existir para las marcas de tiempo que solo se aplican a un momento dado, pero deben definirse para los valores que se consideran válidos durante un período de tiempo determinado (por ejemplo, muestreo). Si la **propiedad Duration** existe y no es NULL, el **valor TimeStamp** debe ser el final del intervalo.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")
</dt> </dl>

Identifica de forma única una instancia de esta clase dentro del ámbito del espacio de nombres contenedor.

> [!IMPORTANT]
>
> Para garantizar la unidad dentro del espacio de nombres, el valor de la propiedad **InstanceID** debe construirse con el siguiente patrón: *OrgID*:*LocalID*
>
> *OrgID* debe incluir un nombre con derechos de autor, marca comercial o único que sea propiedad de la entidad empresarial que define **instanceID** o ser un identificador registrado asignado por una autoridad global reconocida. Este patrón es similar a la estructura de los nombres de clase de esquema. Además, para garantizar la unidad, el primer signo de dos puntos de **InstanceID** debe estar entre *orgID* y *LocalID.* Por lo *tanto, orgID* no debe contener dos puntos (':').
>
> La entidad empresarial elige *LocalID* y no se debe volver a usar para identificar los distintos elementos subyacentes del mundo real.
>
> Si no se usa el patrón anterior, la entidad de definición debe asegurarse de que el valor **instanceID** resultante no se vuelva a usar en ninguna propiedad **InstanceID** producida por este proveedor u otros proveedores para este espacio de nombres.
>
> En el caso de las instancias definidas por el Grupo de tareas de administración distribuida (DMTF), el patrón debe usarse con *el OrgID* establecido en CIM.

 

</dd> <dt>

**MeasuredElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre descriptivo para el elemento medido por la métrica.

Esta propiedad es necesaria si la definición de métrica no está asociada a un objeto [**\_ ManagedElement**](cim-managedelement.md) de CIM y se puede usar en otros casos para proporcionar información complementaria. Esto permite capturar métricas independientemente de cualquier **\_ objeto ManagedElement de CIM.**

Si hay varios objetos [**\_ ManagedElement**](cim-managedelement.md) de CIM asociados al valor de métrica, puede elegir uno de los elementos administrados para crear la información complementaria de la métrica. La propiedad no está pensada para usarse como una clave externa para consultar el elemento medido. En su lugar, se debe usar **la asociación a \_ ManagedElement** de CIM.

</dd> <dt>

**MetricDefinitionId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**Id.**")
</dt> </dl>

Clave de la instancia [**\_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) asociada a este valor de instancia.

</dd> <dt>

**MetricValue**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **requeridos**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Representación de cadena del valor de métrica. El tipo de datos original del valor de métrica se especifica en el objeto [**\_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) asociado.

</dd> <dt>

**Timestamp**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**", "**CIM \_ BaseMetricValue**.**Duración**")
</dt> </dl>

Hora a la que se calcula el valor de una instancia de métrica. Esto es diferente del momento en que se crea la instancia. Si la **propiedad Volatile** es true, este valor cambia cada vez que se toma una nueva instantánea de medida.

Una aplicación de administración puede establecer una serie temporal de datos de métricas recuperando las instancias de **\_ CIM BaseMetricValue** y ordenándolos según su **valor TimeStamp.**

</dd> <dt>

**Volátil**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

True si el **valor de TimeStamp** cambia cada vez que cambia el valor de la instancia de métrica. False si este objeto debe permanecer sin cambios y se ha creado un nuevo objeto para el **nuevo valor TimeStamp.**

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

[**CIM \_ ManagedElement**](cim-managedelement.md)
</dt> </dl>

 

