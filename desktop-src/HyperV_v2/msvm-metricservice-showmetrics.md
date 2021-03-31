---
description: Muestra las métricas especificadas.
ms.assetid: 3716b5e6-b360-4719-a0f3-60b8d39deb31
title: Método ShowMetrics de la clase Msvm_MetricService
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
ms.openlocfilehash: 9823ea61864b0d87245ebe8b171195a2fd3c411a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913125"
---
# <a name="showmetrics-method-of-the-msvm_metricservice-class"></a>Método ShowMetrics de la \_ clase MetricService de MSVM

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

*Asunto* \[ de\]
</dt> <dd>

El parámetro Subject identifica una instancia de [**CIM de CIM \_**](cim-managedelement.md) para la que el método devuelve referencias a instancias de [**\_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) que definen métricas que se capturan para el **\_ ManagedElement de CIM**.

</dd> <dt>

*Definición* \[ de de\]
</dt> <dd>

El parámetro de definición identifica una instancia de [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md). El método devuelve referencias a instancias de [**CIM \_ de CIM**](cim-managedelement.md) para las que se pueden recopilar las métricas definidas por la instancia de **\_ BaseMetricDefinition de CIM** .

</dd> <dt>

*ManagedElements* \[ enuncia\]
</dt> <dd>

Tras la finalización correcta del método, el parámetro *ManagedElements* \[ \] puede contener referencias a un [**\_ ManagedElement de CIM**](cim-managedelement.md) para el que la métrica identificada por el parámetro de *definición* está disponible para la recopilación.

</dd> <dt>

*DefinitionList* \[ enuncia\]
</dt> <dd>

Tras la finalización correcta del método, el parámetro *DefinitionList* puede contener referencias a instancias [**de \_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) que definen las métricas disponibles para la recopilación para el [**\_ ManagedElement de CIM**](cim-managedelement.md) identificado por el parámetro de *asunto* .

</dd> <dt>

*MetricNames* \[ enuncia\]
</dt> <dd>

Tras completar correctamente el método, cada índice de matriz del parámetro *MetricNames* contendrá el valor de la propiedad Name de la instancia de [**\_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) a la que hace referencia el índice de matriz correspondiente del parámetro *DefinitionList* .

</dd> <dt>

*MetricCollectionEnabled* \[ enuncia\]
</dt> <dd>

El parámetro *MetricCollectionEnabled* indica si se va a recopilar una métrica para un elemento administrado.

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

**Proveedor reservado** (32768... 65535)


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

**Específico del proveedor** (32768... 65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

 




