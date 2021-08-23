---
description: Muestra las métricas especificadas.
ms.assetid: 3716b5e6-b360-4719-a0f3-60b8d39deb31
title: Método ShowMetrics de la Msvm_MetricService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 052f708f07a8e1074eeaa6c8089ccd410bb63af478072545d5db92af7933fc49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521475"
---
# <a name="showmetrics-method-of-the-msvm_metricservice-class"></a>Método ShowMetrics de la clase \_ Msvm MetricService

Muestra las métricas especificadas.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ShowMetrics(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_ManagedElement       REF ManagedElements[],
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Asunto* \[ En\]
</dt> <dd>

El parámetro Subject identifica una instancia de [**\_ ManagedElement**](cim-managedelement.md) de CIM para la que el método devuelve referencias a instancias de [**\_ BaseMetricDefinition**](cim-basemetricdefinition.md) de CIM que definen las métricas que se capturan para **el elemento \_ ManagedElement de CIM.**

</dd> <dt>

*Definición* \[ En\]
</dt> <dd>

El parámetro Definition identifica una instancia de [**CIM \_ BaseMetricDefinition.**](cim-basemetricdefinition.md) El método devuelve referencias a instancias de [**\_ ManagedElement**](cim-managedelement.md) de CIM para las que las métricas definidas por la instancia de **\_ Cim BaseMetricDefinition** están disponibles para recopilarse.

</dd> <dt>

*ManagedElements* \[ out\]
</dt> <dd>

Tras la finalización correcta del método, el parámetro *ManagedElements* puede contener referencias a \[ \] CIM [**\_ ManagedElement**](cim-managedelement.md) para las que la métrica identificada por el parámetro *Definition* está disponible para la colección.

</dd> <dt>

*DefinitionList* \[ out\]
</dt> <dd>

Una vez completado correctamente el método , el parámetro *DefinitionList* puede contener referencias a instancias de [**Cim \_ BaseMetricDefinition**](cim-basemetricdefinition.md) que definen las métricas disponibles para la recopilación para [**el elemento \_ ManagedElement**](cim-managedelement.md) de CIM identificado por el *parámetro Subject.*

</dd> <dt>

*MetricNames* \[ out\]
</dt> <dd>

Una vez completado correctamente el método , cada índice de matriz del parámetro *MetricNames* debe contener el valor de la propiedad Name para la instancia de [**\_ CIM BaseMetricDefinition**](cim-basemetricdefinition.md) a la que hace referencia el índice de matriz correspondiente del *parámetro DefinitionList.*

</dd> <dt>

*MetricCollectionEnabled* \[ out\]
</dt> <dd>

El *parámetro MetricCollectionEnabled* indica si se está recopilando una métrica para un elemento administrado.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

**Habilitar** (2)


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

**Deshabilitar** (3)


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Reservado** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Vendor Reserved** (32768..65535)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Error** (2)
</dt> <dt>

**Método reservado** (..)
</dt> <dt>

**Específico del** proveedor (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

 




