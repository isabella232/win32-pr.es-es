---
description: Describe las capacidades de la instancia de MSVM \_ MetricService asociada.
ms.assetid: 4E24D675-8265-4B5E-9551-550510B138FE
title: Msvm_MetricServiceCapabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricServiceCapabilities
- Msvm_MetricServiceCapabilities.InstanceID
- Msvm_MetricServiceCapabilities.Caption
- Msvm_MetricServiceCapabilities.Description
- Msvm_MetricServiceCapabilities.ElementName
- Msvm_MetricServiceCapabilities.ElementNameEditSupported
- Msvm_MetricServiceCapabilities.MaxElementNameLen
- Msvm_MetricServiceCapabilities.RequestedStatesSupported
- Msvm_MetricServiceCapabilities.ElementNameMask
- Msvm_MetricServiceCapabilities.ControllableMetrics
- Msvm_MetricServiceCapabilities.MetricsControlTypes
- Msvm_MetricServiceCapabilities.ControllableManagedElements
- Msvm_MetricServiceCapabilities.ManagedElementControlTypes
- Msvm_MetricServiceCapabilities.SupportedMethods
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 635e153d3184e74ea581a045e3d6d54a5fea199f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913118"
---
# <a name="msvm_metricservicecapabilities-class"></a>MSVM \_ MetricServiceCapabilities (clase)

Describe las capacidades de la instancia de [**MSVM \_ MetricService**](msvm-metricservice.md) asociada.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricServiceCapabilities : CIM_MetricServiceCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Metric Service Capabilities";
  string  Description = "Defines Hyper-V Metric Service Capabilities";
  string  ElementName = "Hyper-V Metric Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  ControllableMetrics[];
  uint16  MetricsControlTypes[];
  string  ControllableManagedElements[];
  uint16  ManagedElementControlTypes[];
  uint16  SupportedMethods[];
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ MetricServiceCapabilities** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ MetricServiceCapabilities** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "capacidades del servicio de métricas de Hyper-V".

</dd> <dt>

**ControllableManagedElements**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **ArrayType** ("indexado")
</dt> </dl>

Identifica las instancias de la clase [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) que puede controlar la instancia de **\_ MetricService CIM** asociada. Si esta propiedad es **null**, se pueden controlar todos los elementos. Esta propiedad se hereda de **\_ MetricServiceCapabilities CIM**.

</dd> <dt>

**ControllableMetrics**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **ArrayType** ("indexado")
</dt> </dl>

Identifica las instancias de **\_ BaseMetricDefinition de CIM** que puede controlar la instancia de **\_ MetricService de CIM** asociada. Si esta propiedad es **null**, se pueden controlar todas las métricas. Esta propiedad se hereda de **\_ MetricServiceCapabilities CIM**.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "define las capacidades del servicio de métricas de Hyper-V".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "capacidades del servicio de métricas de Hyper-V".

</dd> <dt>

**ElementNameEditSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se puede modificar la propiedad **ElementName** . Esta propiedad se hereda de **\_ EnabledLogicalElementCapabilities CIM**.

</dd> <dt>

**ElementNameMask**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica las restricciones en **ElementName**, expresadas como una expresión regular. Esta propiedad se hereda de **\_ EnabledLogicalElementCapabilities CIM**.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ManagedElementControlTypes**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **ArrayType** ("indexado")
</dt> </dl>

Identifica el tipo de control admitido por la instancia de **\_ MetricService CIM** asociada para el objeto [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) identificado por el valor en el mismo índice de matriz en la propiedad **ControllableManagedElements** . Si esta propiedad es **null**, se admiten todos los tipos de control. Esta propiedad se hereda de **\_ MetricServiceCapabilities CIM**.



| Value                                                                                   | Significado                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>            | Unknown<br/>         |
| <dl> <dt>2</dt> </dl>            | Discrete<br/>        |
| <dl> <dt>3</dt> </dl>            | En bloque<br/>            |
| <dl> <dt>4</dt> </dl>            | Ambos<br/>            |
| <dl> <dt>5.. 32767</dt> </dl>     | DMTF reservado<br/>   |
| <dl> <dt>32768... 65535</dt> </dl> | Específico del proveedor<br/> |



 

</dd> <dt>

**MaxElementNameLen**
</dt> <dd> <dl> <dt>

Tipo de datos: **unit16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxValue** (256)
</dt> </dl>

Especifica la longitud máxima admitida de la propiedad **ElementName** . Esta propiedad se hereda de **\_ EnabledLogicalElementCapabilities CIM**.

</dd> <dt>

**MetricsControlTypes**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **ArrayType** ("indexado")
</dt> </dl>

Identifica el tipo de control admitido por la instancia de **\_ MetricService CIM** asociada para el **\_ BaseMetricDefinition CIM** identificado por el valor en el mismo índice de matriz en la propiedad **ControllableMetrics** . Si esta propiedad es **null**, se admiten todos los tipos de control. Esta propiedad se hereda de **\_ MetricServiceCapabilities CIM**.



| Value                                                                                   | Significado                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>            | Unknown<br/>         |
| <dl> <dt>2</dt> </dl>            | Discrete<br/>        |
| <dl> <dt>3</dt> </dl>            | En bloque<br/>            |
| <dl> <dt>4</dt> </dl>            | Ambos<br/>            |
| <dl> <dt>5.. 32767</dt> </dl>     | DMTF reservado<br/>   |
| <dl> <dt>32768... 65535</dt> </dl> | Específico del proveedor<br/> |



 

</dd> <dt>

**RequestedStatesSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **unit16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica los posibles Estados que se pueden solicitar al utilizar el método **RequestStateChange** en el elemento lógico habilitado. Esta propiedad se hereda de **\_ EnabledLogicalElementCapabilities CIM**.



| Value                                                                         | Significado              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <dt>2</dt> </dl>  | habilitado<br/>   |
| <dl> <dt>3</dt> </dl>  | Impide<br/>  |
| <dl> <dt>4</dt> </dl>  | Apagar<br/> |
| <dl> <dt>6</dt> </dl>  | Sin conexión<br/>   |
| <dl> <dt>7</dt> </dl>  | Prueba<br/>      |
| <dl> <dt>8</dt> </dl>  | Acepta<br/>     |
| <dl> <dt>9</dt> </dl>  | Modo de inactividad<br/>   |
| <dl> <dt>10</dt> </dl> | Reboot<br/>    |
| <dl> <dt>11</dt> </dl> | Reset<br/>     |



 

</dd> <dt>

**SupportedMethods**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica los métodos admitidos por el servicio de métricas. Esta propiedad se hereda de **\_ MetricServiceCapabilities CIM**.



| Value                                                                                   | Significado                                                                                         |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>2</dt> </dl>            | Se admite el método [**ControlMetrics**](controlmetrics-msvm-metricservice.md) .<br/> |
| <dl> <dt>3</dt> </dl>            | Se admite el método **ControlMetricsByClass** .<br/>                                   |
| <dl> <dt>4</dt> </dl>            | Se admite el método **ShowMetrics** .<br/>                                             |
| <dl> <dt>5</dt> </dl>            | Se admite el método **ShowMetricsByClass** .<br/>                                      |
| <dl> <dt>6</dt> </dl>            | Se admite el método **GetMetricValues** .<br/>                                         |
| <dl> <dt>7</dt> </dl>            | Se admite el método **ControlSampleTimes** .<br/>                                      |
| <dl> <dt>8.. 32767</dt> </dl>     | DMTF reservado<br/>                                                                        |
| <dl> <dt>32768... 65535</dt> </dl> | Específico del proveedor<br/>                                                                      |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_METRICSERVICECAPABILITIES CIM**](cim-metricservicecapabilities.md)
</dt> <dt>

[**MSVM \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

