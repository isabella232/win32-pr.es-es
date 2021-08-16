---
description: Representa un valor de métrica definido por una instancia de la clase \_ BaseMetricDefinition de Msvm.
ms.assetid: bd872f21-ab71-4ab7-88d3-b26dd2fbdbe5
title: Msvm_BaseMetricValue clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BaseMetricValue
- Msvm_BaseMetricValue.InstanceID
- Msvm_BaseMetricValue.Caption
- Msvm_BaseMetricValue.Description
- Msvm_BaseMetricValue.ElementName
- Msvm_BaseMetricValue.MetricDefinitionId
- Msvm_BaseMetricValue.MeasuredElementName
- Msvm_BaseMetricValue.TimeStamp
- Msvm_BaseMetricValue.Duration
- Msvm_BaseMetricValue.MetricValue
- Msvm_BaseMetricValue.BreakdownDimension
- Msvm_BaseMetricValue.BreakdownValue
- Msvm_BaseMetricValue.Volatile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 24d61f6068cffc83f8556637bba30de57308b6a5bcefe5b015bc185ab7811108
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790225"
---
# <a name="msvm_basemetricvalue-class"></a>Clase BaseMetricValue de Msvm \_

Representa un valor de métrica definido por una instancia de la clase [**\_ BaseMetricDefinition de Msvm.**](msvm-basemetricdefinition.md)

La sintaxis siguiente se Managed Object Format código (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BaseMetricValue : CIM_BaseMetricValue
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
};
```

## <a name="members"></a>Miembros

La **clase \_ BaseMetricValue de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ BaseMetricValue de Msvm** tiene estas propiedades.

<dl> <dt>

**BreakdownDimension**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica una dimensión de desglose de la **matriz BreakdownDimensions** definida en el objeto [**\_ BaseMetricDefinition de Msvm asociado.**](msvm-basemetricdefinition.md) Esta es la dimensión a lo largo de la cual se desglosa este conjunto de valores de métrica. Esta propiedad se hereda de [**CIM \_ BaseMetricDefinition.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**BreakdownValue**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Define un valor de la propiedad **BreakdownDimension** definida para esta instancia de valor de métrica. Por ejemplo, si **BreakdownDimension** es "TransactionName", esta propiedad podría dar nombre a la transacción real a la que se aplica este valor de métrica determinado. Esta propiedad se hereda de [**CIM \_ BaseMetricDefinition.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Duración**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica la duración de tiempo durante la que este valor de métrica es válido. Esta propiedad no debe existir para las marcas de tiempo que se aplican solo a un momento dado, sino que se debe especificar para los valores que se consideran válidos durante un período de tiempo determinado (por ejemplo, muestreo). Si la **propiedad Duration** existe y no es **Null,** la **propiedad TimeStamp** especifica el final del intervalo. Esta propiedad se hereda de [**CIM \_ BaseMetricDefinition.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

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

**MeasuredElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre descriptivo del elemento al que pertenece el valor de métrica (el elemento medido). Esta propiedad se hereda de [**CIM \_ BaseMetricDefinition.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**MetricDefinitionId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Clave de la instancia [**de \_ BaseMetricDefinition de Msvm**](msvm-basemetricdefinition.md) para este valor. Esta propiedad se hereda de [**CIM \_ BaseMetricDefinition.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**MetricValue**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor de la métrica que se representa como una cadena. Esta propiedad se hereda de [**CIM \_ BaseMetricDefinition.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Timestamp**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica la hora a la que se capturó o calculó el valor de métrica. Tenga en cuenta que esto es diferente de la hora en que se creó la instancia. Esta propiedad se hereda de [**CIM \_ BaseMetricDefinition.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Volátil**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

**True** si el valor del siguiente momento en el tiempo usará la misma instancia de clase y solo cambiará los valores de propiedad (como **Value** o **TimeStamp).** Si **es True**, se reutiliza la instancia de . Si **es False**, las instancias existentes permanecen sin cambios y se crea una nueva instancia para el nuevo momento en el tiempo. Esta propiedad se hereda de [**CIM \_ BaseMetricDefinition.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

