---
description: Representa los aspectos de definición de una métrica que se deriva de otro valor de métrica.
ms.assetid: 642f53fe-e51c-4c73-babf-19adb2cf55f4
title: Msvm_AggregationMetricDefinition clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AggregationMetricDefinition
- Msvm_AggregationMetricDefinition.InstanceID
- Msvm_AggregationMetricDefinition.Caption
- Msvm_AggregationMetricDefinition.Description
- Msvm_AggregationMetricDefinition.ElementName
- Msvm_AggregationMetricDefinition.Id
- Msvm_AggregationMetricDefinition.Name
- Msvm_AggregationMetricDefinition.DataType
- Msvm_AggregationMetricDefinition.Calculable
- Msvm_AggregationMetricDefinition.Units
- Msvm_AggregationMetricDefinition.BreakdownDimensions
- Msvm_AggregationMetricDefinition.IsContinuous
- Msvm_AggregationMetricDefinition.ChangeType
- Msvm_AggregationMetricDefinition.TimeScope
- Msvm_AggregationMetricDefinition.GatheringType
- Msvm_AggregationMetricDefinition.ProgrammaticUnits
- Msvm_AggregationMetricDefinition.SimpleFunction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 50d3ffb104b32c5f9b9a4c74b7d1425ba81e78c57a8059b455fc244da0e257ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790495"
---
# <a name="msvm_aggregationmetricdefinition-class"></a>Clase Msvm \_ AggregationMetricDefinition

Representa los aspectos de definición de una métrica que se deriva de otro valor de métrica. El **objeto \_ AggregationMetricDefinition de Msvm** debe asociarse a los elementos administrados a los que se aplica.

La sintaxis siguiente se Managed Object Format código (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AggregationMetricDefinition : CIM_AggregationMetricDefinition
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
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
  uint16  SimpleFunction;
};
```

## <a name="members"></a>Miembros

La **clase \_ AggregationMetricDefinition de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ AggregationMetricDefinition de Msvm** tiene estas propiedades.

<dl> <dt>

**BreakdownDimensions**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Define una o varias cadenas que se pueden usar para refinar (dividir) consultas con los valores de métricas de una dimensión determinada. Un ejemplo es un nombre de transacción, que permite dividir el valor total de todas las transacciones en un conjunto de valores, uno para cada nombre de transacción. Otros ejemplos pueden ser el nombre del sistema de la aplicación o del grupo de usuarios. Las cadenas tienen formato libre y deben ser significativas para los usuarios finales de los datos de métrica. Las cadenas indican qué dimensiones de interrupción son compatibles con esta definición de métrica mediante la instrumentación subyacente. Esta propiedad se hereda de **CIM \_ BaseMetricDefinition.**

</dd> <dt>

**Calculable**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Describe las características de la métrica para realizar cálculos. Esta propiedad se hereda de **CIM \_ BaseMetricDefinition.** Puede ser **Null o** uno de los valores siguientes.



| Value                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span><dl> <dt>**No calculable**</dt> <dt>1</dt> </dl> | No se puede calcular el valor. Por ejemplo, una cadena.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span><dl> <dt>**Sumable**</dt> <dt>2</dt> </dl>                         | El valor se puede suman en muchas instancias. Por ejemplo, si cada trabajo de copia de seguridad es una unidad de trabajo y cada trabajo hace una copia de seguridad de 27 000 archivos de media, 100 trabajos de copia de seguridad procesaron 2 700 000 archivos.<br/>                                                                                                                                                                 |
| <span id="Non-summable_"></span><span id="non-summable_"></span><span id="NON-SUMMABLE_"></span><dl> <dt> **No sumable**</dt> <dt>3</dt> </dl>    | Este valor no se puede suman en muchas instancias. Un ejemplo sería una métrica que mide la longitud de la cola cuando un trabajo llega a un servidor. Si cada trabajo es una unidad de trabajo y la longitud media de la cola cuando llega cada trabajo es 33, no tiene sentido decir que la longitud de la cola para 100 trabajos es de 3300. Tiene sentido decir que la media es 33.<br/> |



 

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ChangeType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica cómo cambia el valor de la métrica, en forma de combinaciones típicas de atributos más específicos, como el cambio de dirección, los valores mínimos y máximos, y la semántica de ajuste. Esta propiedad se hereda de **CIM \_ BaseMetricDefinition.**



| Value                                                                                                                                                                                                                                                                       | Significado                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Desconocido**</dt> <dt>0</dt> </dl>                                                 | El diseñador de métricas no calificó **changeType.**<br/>                                                                                                                               |
| <span id="N_A"></span><span id="n_a"></span><dl> <dt>**N/A**</dt> <dt>2</dt> </dl>                                                                                       | Si la **propiedad IsContinuous** es "false", **ChangeType** no tiene sentido y debe establecerse en "N/A".<br/>                                                                             |
| <span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span><dl> <dt>**Contador**</dt> <dt>3</dt> </dl>                                                 | La métrica es una métrica de contador. Estos tienen valores enteros no negativos que aumentan hasta alcanzar el número máximo que se puede representar y, a continuación, se encapsulan y empiezan a aumentar de 0.<br/> |
| <span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span><dl> <dt>**Medidor**</dt> <dt>4</dt> </dl>                                                         | La métrica es una métrica de medidor. Tienen valores enteros o float que pueden aumentar y disminuir arbitrariamente.<br/>                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF reservado**</dt> <dt>5..32767</dt> </dl>                  |                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt> **Proveedor reservado**</dt> <dt>32768..65535</dt> </dl> | Los proveedores pueden extender la **propiedad ChangeType** en el intervalo reservado del proveedor.<br/>                                                                                                          |



 

</dd> <dt>

**DataType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de datos de la métrica. Esta propiedad se hereda de **CIM \_ BaseMetricDefinition.**

<dl> <dt>

<span id="boolean"></span><span id="BOOLEAN"></span>**booleano** (1)
</dt> <dt>

<span id="char16"></span><span id="CHAR16"></span>**char16** (2)
</dt> <dt>

<span id="datetime"></span><span id="DATETIME"></span>**datetime** (3)
</dt> <dt>

<span id="real32"></span><span id="REAL32"></span>**real32** (4)
</dt> <dt>

<span id="real64"></span><span id="REAL64"></span>**real64** (5)
</dt> <dt>

<span id="sint16"></span><span id="SINT16"></span>**sint16** (6)
</dt> <dt>

<span id="sint32"></span><span id="SINT32"></span>**sint32** (7)
</dt> <dt>

<span id="sint64"></span><span id="SINT64"></span>**sint64** (8)
</dt> <dt>

<span id="sint8"></span><span id="SINT8"></span>**sint8** (9)
</dt> <dt>

<span id="string"></span><span id="STRING"></span>**string** (10)
</dt> <dt>

<span id="uint16"></span><span id="UINT16"></span>**uint16** (11)
</dt> <dt>

<span id="uint32"></span><span id="UINT32"></span>**uint32** (12)
</dt> <dt>

<span id="uint64"></span><span id="UINT64"></span>**uint64** (13)
</dt> <dt>

<span id="uint8_"></span><span id="UINT8_"></span>**uint8** (14 )
</dt> </dl>

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**GatheringType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica cómo se recopilan los valores de métrica mediante la instrumentación subyacente. Esto permite que la aplicación cliente elija la métrica adecuada para el propósito. Esta propiedad se hereda de **CIM \_ BaseMetricDefinition.** Puede ser **Null o** uno de los valores siguientes.



| Valor                                                                                                                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Desconocido**</dt> <dt>0</dt> </dl>                                                 | No se conoce el tipo de recopilación.<br/>                                                                                                                                                                                                                               |
| <span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span><dl> <dt>**OnChange**</dt> <dt>2</dt> </dl>                                             | Los valores de métrica se actualizan inmediatamente cuando cambian los valores dentro del recurso medido.<br/>                                                                                                                                                              |
| <span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span><dl> <dt>**Periodic**</dt> <dt>3</dt> </dl>                                             | Los valores de métrica se actualizan periódicamente. Por ejemplo, para una aplicación cliente, un valor de métrica que se aplica a la hora actual aparecerá constante durante cada intervalo de recopilación y, a continuación, saltará al nuevo valor al final de cada intervalo de recopilación.<br/> |
| <span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span><dl> <dt>**OnRequest**</dt> <dt>4</dt> </dl>                                         | El valor de métrica se determina cada vez que una aplicación cliente lo lee.<br/>                                                                                                                                                                                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF Reservado**</dt> <dt>5...32767</dt> </dl>                  |                                                                                                                                                                                                                                                                           |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt> **Vendor Reserved**</dt> <dt>32768..65535</dt> </dl> |                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

**Id**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Cadena que identifica de forma única la definición de métrica. Esta propiedad se hereda de **CIM \_ BaseMetricDefinition.**

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Cadena que identifica de forma única una instancia de esta clase. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**IsContinuous**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el valor de la métrica es continuo o escalar. Las métricas de rendimiento son un ejemplo de una métrica continua. Entre los ejemplos de métricas escalares se incluyen códigos de error o estados operativos. Las métricas continuas se pueden comparar mediante la relación "mayor que". Esta propiedad se hereda de **CIM \_ BaseMetricDefinition.**

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El nombre de la métrica. Esta propiedad se hereda de **CIM \_ BaseMetricDefinition.**

</dd> <dt>

**ProgrammaticUnits**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identifica las unidades específicas de un valor. El valor de esta propiedad será un valor legal del calificador Unidades de programación tal como se define en el Apéndice C.1 de [DSP0004 V2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) o posterior. Esta propiedad se hereda de **CIM \_ BaseMetricDefinition.**

</dd> <dt>

**SimpleFunction**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Identifica el cálculo básico realizado en una métrica subyacente para llegar al valor de esta métrica derivada. Esta propiedad se hereda de **Cim \_ AggregationMetricDefinition** y será uno de los siguientes valores.

<dl> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Mínimo** (2)
</dt> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Máximo** (3)
</dt> <dt>

<span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**Promedio** (4)
</dt> <dt>

<span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>**Mediana** (5)
</dt> <dt>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Modo** (6)
</dt> </dl>

</dd> <dt>

**TimeScope**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el ámbito de tiempo al que se aplica el valor de métrica. Esta propiedad se hereda de **CIM \_ BaseMetricDefinition.**



| Value                                                                                                                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Desconocido**</dt> <dt>0</dt> </dl>                                                 | El diseñador de métricas no ha calificado el ámbito de tiempo o es desconocido para el proveedor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <dt>**Punto**</dt> <dt>2</dt> </dl>                                                         | La métrica se aplica a un momento dado. En las instancias [**de \_ BaseMetricValue de Msvm**](msvm-basemetricvalue.md) correspondientes, la propiedad **TimeStamp** especifica el momento dado y la propiedad **Duration** siempre es 0.<br/>                                                                                                                                                                                                                                                                                              |
| <span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span><dl> <dt>**Intervalo**</dt> <dt>3</dt> </dl>                                             | La métrica se aplica a un intervalo de tiempo. En las instancias [**de \_ BaseMetricValue de Msvm**](msvm-basemetricvalue.md) correspondientes, la propiedad **TimeStamp** especifica el final del intervalo de tiempo y la propiedad **Duration** especifica su duración.<br/>                                                                                                                                                                                                                                                                        |
| <span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span><dl> <dt>**StartupInterval**</dt> <dt>4</dt> </dl>                 | La métrica se aplica a un intervalo de tiempo que comenzó al inicio del recurso medido (es decir, el elemento Administrado asociado por MetricDefForMe). En las instancias [**de \_ BaseMetricValue de Msvm**](msvm-basemetricvalue.md) correspondientes, la **propiedad TimeStamp** especifica el final del intervalo de tiempo. Si la **propiedad Duration** es 0, esto indica que se desconoce el tiempo de inicio del recurso medido. De lo **contrario, Duration** especifica la duración entre el inicio del recurso y **TimeStamp**.<br/> |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF Reservado**</dt> <dt>5...32767</dt> </dl>                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt> **Vendor Reserved**</dt> <dt>32768..65535</dt> </dl> |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

**Unidades**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identifica las unidades de un valor, por ejemplo, "megabytes". Esta propiedad se hereda de **CIM \_ BaseMetricDefinition.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

