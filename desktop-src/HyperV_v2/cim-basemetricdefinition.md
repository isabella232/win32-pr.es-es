---
description: Representa una definición de métrica que contiene los metadatos para un \_ objeto MetricInstance de CIM.
ms.assetid: 6abfb0dc-e80b-4ca6-89d9-2e43283d0abe
title: CIM_BaseMetricDefinition (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BaseMetricDefinition
- CIM_BaseMetricDefinition.Id
- CIM_BaseMetricDefinition.Name
- CIM_BaseMetricDefinition.DataType
- CIM_BaseMetricDefinition.Calculable
- CIM_BaseMetricDefinition.Units
- CIM_BaseMetricDefinition.BreakdownDimensions
- CIM_BaseMetricDefinition.IsContinuous
- CIM_BaseMetricDefinition.ChangeType
- CIM_BaseMetricDefinition.TimeScope
- CIM_BaseMetricDefinition.GatheringType
- CIM_BaseMetricDefinition.ProgrammaticUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cac965ed1eae59f1c269d897a12e9aa116183eb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669949"
---
# <a name="cim_basemetricdefinition-class"></a>\_Clase BaseMetricDefinition de CIM

Representa una definición de métrica que contiene los metadatos para un objeto **\_ MetricInstance de CIM** .

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_BaseMetricDefinition : CIM_ManagedElement
{
  string  Id;
  string  Name;
  uint16  DataType;
  uint16  Calculable;
  string  Units;
  string  BreakdownDimensions[];
  boolean IsContinuous;
  uint16  ChangeType;
  uint16  TimeScope;
  uint16  GatheringType;
  string  ProgrammaticUnits;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ BaseMetricDefinition** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ BaseMetricDefinition** tiene estas propiedades.

<dl> <dt>

**BreakdownDimensions**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una matriz que contiene cadenas de formato libre que se pueden usar para desglosar las consultas de objetos [**\_ BaseMetricValue de CIM**](cim-basemetricvalue.md) a lo largo de una dimensión determinada. Las cadenas deben ser significativas para los usuarios finales de los datos de métricas. Además, las cadenas deben indicar qué dimensiones de división se admiten para la definición de métricas, mediante la instrumentación subyacente.

Un ejemplo es un nombre de transacción que permite el desglose del valor total de todas las transacciones en un conjunto de valores, uno para cada nombre de transacción. Otros ejemplos son un sistema de aplicaciones o un nombre de grupo de usuarios.

</dd> <dt>

**Calculado**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Características de la métrica que se usan para realizar cálculos.

<dt>

<span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>

<span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>**No calculado** (1)


</dt> <dd>

Una cadena. La aritmética no tiene sentido.

</dd> <dt>

<span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>

<span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>**Sumable** (2)


</dt> <dd>

Es razonable sumar este valor en muchas instancias de, por ejemplo, UnitOfWork, como el número de archivos procesados en un trabajo de copia de seguridad. Por ejemplo, si cada trabajo de copia de seguridad es un UnitOfWork y cada trabajo realiza una copia de seguridad de 27.000 archivos como promedio, tiene sentido decir que los trabajos de copia de seguridad de 100 procesaron 2,7 millones archivos.

</dd> <dt>

<span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>

<span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>**No sumable** (3)


</dt> <dd>

No tiene sentido sumar este valor en muchas instancias de UnitOfWork. Un ejemplo sería una métrica que mide la longitud de la cola cuando un trabajo llega a un servidor. Si cada trabajo es un UnitOfWork y el promedio de longitud de cola cuando llega cada trabajo es 33, no tiene sentido decir que la longitud de la cola para los trabajos de 100 es 3300. Tiene sentido decir que la media es 33.

</dd> </dl>

</dd> <dt>

**ChangeType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BaseMetricDefinition**.**IsContinuous**")
</dt> </dl>

Indica cómo cambia el valor de métrica mediante atributos comunes como el cambio de dirección, los valores mínimo y máximo y la semántica de ajuste.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd>

El diseñador de métricas no calificó el ChangeType.

</dd> <dt>

<span id="N_A"></span><span id="n_a"></span>

<span id="N_A"></span><span id="n_a"></span>**N/A** (2)


</dt> <dd>

Si la propiedad "IsContinuous" es "false", ChangeType no tiene sentido y debe establecerse en "N/A".

</dd> <dt>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Contador** (3)


</dt> <dd>

La métrica es una métrica de contador. Tienen valores enteros no negativos que aumentan de forma monotónica hasta alcanzar el número máximo representable y, a continuación, se ajustan y comienzan a aumentar desde 0. Estos contadores, también conocidos como contadores de sustitución incremental, se pueden usar para que la instancia cuente el número de errores de red o el número de transacciones procesadas. La única manera de que una aplicación cliente realice un seguimiento de las contornos consiste en recuperar el valor del contador en intervalos de forma adecuada.

</dd> <dt>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Medidor** (4)


</dt> <dd>

La métrica es una métrica del medidor. Tienen valores enteros o flotantes que pueden aumentar y disminuir arbitrariamente. Un medidor no debe ajustarse cuando se alcanza el número mínimo o máximo que se represente, en su lugar, el valor "se ciñe" en ese número. Los valores mínimos o máximos dentro del intervalo de valores representables en los que el valor de métrica se "palo" se pueden definir o no.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (5.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32768... 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**DataType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El tipo de datos de la métrica.

<dt>

<span id="boolean"></span><span id="BOOLEAN"></span>

**booleano** (1)


</dt> <dd></dd> <dt>

<span id="char16"></span><span id="CHAR16"></span>

**char16** (2)


</dt> <dd></dd> <dt>

<span id="datetime"></span><span id="DATETIME"></span>

**DateTime** (3)


</dt> <dd></dd> <dt>

<span id="real32"></span><span id="REAL32"></span>

**real32** (4)


</dt> <dd></dd> <dt>

<span id="real64"></span><span id="REAL64"></span>

**real64** (5)


</dt> <dd></dd> <dt>

<span id="sint16"></span><span id="SINT16"></span>

**sint16** (6)


</dt> <dd></dd> <dt>

<span id="sint32"></span><span id="SINT32"></span>

**sint32** (7)


</dt> <dd></dd> <dt>

<span id="sint64"></span><span id="SINT64"></span>

**sint64** (8)


</dt> <dd></dd> <dt>

<span id="sint8"></span><span id="SINT8"></span>

**sint8** (9)


</dt> <dd></dd> <dt>

<span id="string"></span><span id="STRING"></span>

**cadena** (10)


</dt> <dd></dd> <dt>

<span id="uint16"></span><span id="UINT16"></span>

**UInt16** (11)


</dt> <dd></dd> <dt>

<span id="uint32"></span><span id="UINT32"></span>

**UInt32** (12)


</dt> <dd></dd> <dt>

<span id="uint64"></span><span id="UINT64"></span>

**UInt64** (13)


</dt> <dd></dd> <dt>

<span id="uint8"></span><span id="UINT8"></span>

**Uint8** (14)


</dt> <dd></dd> </dl>

</dd> <dt>

**GatheringType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica cómo se recopilan los valores de métricas mediante la instrumentación subyacente.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd>

Indica que no se conoce el GatheringType.

</dd> <dt>

<span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>

<span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>**Onchange** (2)


</dt> <dd>

Indica que los valores de métrica CIM se actualizan inmediatamente cuando cambian los valores dentro del recurso medido. Los valores de las métricas onchange reflejan realmente la situación actual del recurso en cualquier momento. Un ejemplo es el número de usuarios que han iniciado sesión y que se actualizan inmediatamente a medida que los usuarios inician y cierran sesión.

</dd> <dt>

<span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>

<span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>**Periódico** (3)


</dt> <dd>

": Indica que los valores de métrica CIM se actualizan periódicamente. Por ejemplo, en una aplicación cliente, un valor de métrica que se aplica a la hora actual aparecerá como constante durante cada intervalo de recopilación y, a continuación, saltará al nuevo valor al final de cada intervalo de recopilación.

</dd> <dt>

<span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>

<span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>**Request** (4)


</dt> <dd>

Indica que el valor de métrica CIM se determina cada vez que una aplicación cliente lo lee. Los valores de las métricas de solicitud devuelven realmente la situación actual dentro del recurso si alguien la solicita. Sin embargo, no cambian el valor "unobservado" y, por lo tanto, no se recomienda suscribir los cambios de valor de las métricas de solicitud.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (5.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32768... 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Id**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

IDENTIFICADOR único de la definición de métrica. Se recomienda el UUID/GUID de Open Software Foundation (OSF).

</dd> <dt>

**IsContinuous**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

True si el valor de la métrica es continuo; en caso contrario, false.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El nombre de la métrica. Este nombre no tiene que ser único, pero debe ser descriptivo y puede contener espacios en blanco.

</dd> <dt>

**ProgrammaticUnits**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Unidades específicas de un valor. El valor de esta propiedad debe ser un valor válido del calificador de unidades de programación, tal y como se define en el Apéndice C. 1 de DSP0004 V 2.4 o posterior.

</dd> <dt>

**TimeScope**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricValue**](cim-basemetricvalue.md).**Marca** de tiempo ","**CIM \_ BaseMetricValue**.**Duration**")
</dt> </dl>

El ámbito de tiempo que se aplica al diseñador de métricas.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd>

Indica que el diseñador de métricas no calificó el ámbito de tiempo o es desconocido para el proveedor.

</dd> <dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>**Punto** (2)


</dt> <dd>

Indica que la métrica se aplica a un punto en el tiempo. En las instancias de BaseMetricValue correspondientes, TimeStamp especifica el momento dado y Duration siempre es 0.

</dd> <dt>

<span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>

<span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>**Intervalo** (3)


</dt> <dd>

Indica que la métrica se aplica a un intervalo de tiempo. En las instancias de BaseMetricValue correspondientes, TimeStamp especifica el final del intervalo de tiempo y Duration especifica su duración.

</dd> <dt>

<span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>

<span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>**StartupInterval** (4)


</dt> <dd>

Indica que la métrica se aplica a un intervalo de tiempo que comenzó en el inicio del recurso medido (es decir, el ManagedElement asociado a MetricDefForMe). En las instancias de BaseMetricValue correspondientes, TimeStamp especifica el final del intervalo de tiempo. Si Duration es 0, indica que se desconoce la hora de inicio del recurso medido. En caso contrario, Duration especifica la duración entre el inicio del recurso y la marca de tiempo.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (5.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32768... 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Unidades**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Unidades de la métrica. Algunos ejemplos son bytes, paquetes, trabajos, archivos, milisegundos y amperios.

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

 

