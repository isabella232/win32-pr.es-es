---
description: Describe las capacidades de un \_ objeto MetricService de CIM.
ms.assetid: 3b4da02f-5298-46d4-876c-404baca38c03
title: CIM_MetricServiceCapabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricServiceCapabilities
- CIM_MetricServiceCapabilities.ControllableMetrics
- CIM_MetricServiceCapabilities.MetricsControlTypes
- CIM_MetricServiceCapabilities.ControllableManagedElements
- CIM_MetricServiceCapabilities.ManagedElementControlTypes
- CIM_MetricServiceCapabilities.SupportedMethods
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f878cb0e616cb710a33d350df866160fc0eebb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687710"
---
# <a name="cim_metricservicecapabilities-class"></a>\_Clase MetricServiceCapabilities de CIM

Describe las capacidades de un [**objeto \_ MetricService de CIM**](cim-metricservice.md) .

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetrics"), AMENDMENT]
class CIM_MetricServiceCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string ControllableMetrics[];
  uint16 MetricsControlTypes[];
  string ControllableManagedElements[];
  uint16 ManagedElementControlTypes[];
  uint16 SupportedMethods[];
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ MetricServiceCapabilities** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ MetricServiceCapabilities** tiene estas propiedades.

<dl> <dt>

**ControllableManagedElements**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MetricServiceCapabilities**.**ManagedElementControlTypes**")
</dt> </dl>

Una matriz que contiene los identificadores de las instancias de [**\_ ManagedElement de CIM**](cim-managedelement.md) que están controladas por el servicio de métricas. Los identificadores deben tener el formato de Web-Based URI de administración empresarial (WBEM). Para usar esta propiedad, el servicio de métricas debe admitir habilitar o deshabilitar al menos una métrica definida para la instancia de **\_ ManagedElement de CIM** .

</dd> <dt>

**ControllableMetrics**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MetricServiceCapabilities**.**MetricControlTypes**")
</dt> </dl>

Una matriz que contiene los identificadores del [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) que define las métricas administradas por el servicio de métricas. Los identificadores deben tener el formato de Web-Based URI de administración empresarial (WBEM).

Para usar esta propiedad, se debe asociar una instancia de [**\_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) a una instancia de [**\_ MetricService**](cim-metricservice.md) de CIM a través de la clase [**\_ ServiceAffectsElement de CIM**](cim-serviceaffectselement.md) . Además, el servicio de métricas debe admitir la habilitación o deshabilitación de al menos una métrica definida por la instancia de **\_ BaseMetricDefinition de CIM** .

</dd> <dt>

**ManagedElementControlTypes**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MetricServiceCapabilities**.**ControllableManagedElements**")
</dt> </dl>

Matriz que indica los tipos de control que admite el servicio de métricas para los elementos administrados de la matriz **ControllableManagedElements** . Esta matriz corresponde a la matriz **ControllableManagedElements** . Los tipos de control de esta matriz se asocian a las métricas a través de la matriz **ControllableManagedElements** .

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Discrete"></span><span id="discrete"></span><span id="DISCRETE"></span>

**Discreto** (2)


</dt> <dd></dd> <dt>

<span id="Bulk"></span><span id="bulk"></span><span id="BULK"></span>

**Bulk** (3)


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

**Ambos** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Específico del proveedor** (32768... 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**MetricsControlTypes**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MetricServiceCapabilities**.**ControllableMetrics**")
</dt> </dl>

Una matriz que indica los tipos de control que admite el servicio de métricas. Esta matriz corresponde a la matriz **ControllableMetrics** . Los tipos de control de esta matriz se asocian a las métricas a través de la matriz **ControllableMetrics** .

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Discrete"></span><span id="discrete"></span><span id="DISCRETE"></span>

**Discreto** (2)


</dt> <dd></dd> <dt>

<span id="Bulk"></span><span id="bulk"></span><span id="BULK"></span>

**Bulk** (3)


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

**Ambos** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Específico del proveedor** (32768... 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**SupportedMethods**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una matriz que contiene los nombres de los métodos admitidos por el servicio de métricas.

<dt>

<span id="ControlMetrics"></span><span id="controlmetrics"></span><span id="CONTROLMETRICS"></span>

**ControlMetrics** (2)


</dt> <dd></dd> <dt>

<span id="ControlMetricsByClass"></span><span id="controlmetricsbyclass"></span><span id="CONTROLMETRICSBYCLASS"></span>

**ControlMetricsByClass** (3)


</dt> <dd></dd> <dt>

<span id="ShowMetrics"></span><span id="showmetrics"></span><span id="SHOWMETRICS"></span>

**ShowMetrics** (4)


</dt> <dd></dd> <dt>

<span id="ShowMetricsByClass"></span><span id="showmetricsbyclass"></span><span id="SHOWMETRICSBYCLASS"></span>

**ShowMetricsByClass** (5)


</dt> <dd></dd> <dt>

<span id="GetMetricValues"></span><span id="getmetricvalues"></span><span id="GETMETRICVALUES"></span>

**GetMetricValues** (6)


</dt> <dd></dd> <dt>

<span id="ControlSampleTimes"></span><span id="controlsampletimes"></span><span id="CONTROLSAMPLETIMES"></span>

**ControlSampleTimes** (7)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Específico del proveedor** (0x8000...)


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

[**\_ENABLEDLOGICALELEMENTCAPABILITIES CIM**](cim-enabledlogicalelementcapabilities.md)
</dt> </dl>

 

