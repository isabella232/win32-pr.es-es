---
description: 'Notifica lo siguiente: las métricas disponibles que se van a recopilar para todas las instancias de una clase CIM, las clases CIM para las que una métrica definida por una instancia de CIM \_ BaseMetricDefinition se pueden recopilar y si una métrica determinada se está recopilando actualmente para un elemento administrado.'
ms.assetid: 0115a5b5-2824-4c43-a8dc-757524c5d3dd
title: Método ShowMetricsByClass de la clase CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f843c835e6c92e39c4ac1f9628d0479b94a691bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910158"
---
# <a name="showmetricsbyclass-method-of-the-cim_metricservice-class"></a>Método ShowMetricsByClass de la \_ clase MetricService de CIM

Notifica lo siguiente: las métricas disponibles que se van a recopilar para todas las instancias de una clase CIM, las clases CIM para las que una métrica definida por una instancia de [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) se pueden recopilar y si una métrica determinada se está recopilando actualmente para un elemento administrado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ShowMetricsByClass(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Asunto* \[ de\]
</dt> <dd>

Identifica una clase CIM para la que el método devuelve referencias a instancias [**de \_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) que definen las métricas que están disponibles para ser capturadas para todas las instancias de la clase.

</dd> <dt>

*Definición* \[ de de\]
</dt> <dd>

Identifica una instancia de [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md). El método devuelve referencias a instancias de [**CIM \_ de CIM**](cim-managedelement.md) para las que se pueden recopilar las métricas definidas por la instancia de **\_ BaseMetricDefinition de CIM** .

</dd> <dt>

*DefinitionList* \[ enuncia\]
</dt> <dd>

Si se ejecuta correctamente, puede contener referencias a instancias de objetos [**\_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) que definen las métricas disponibles para la recopilación de los [**\_ ManagedElement de CIM**](cim-managedelement.md) identificados por el parámetro de *asunto* .

</dd> <dt>

*MetricNames* \[ enuncia\]
</dt> <dd>

Si se ejecuta correctamente, cada índice de matriz contendrá el valor de la propiedad **Name** para la instancia de [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) a la que hace referencia el índice de matriz correspondiente del parámetro *DefinitionList* .

</dd> <dt>

*MetricCollectionEnabled* \[ enuncia\]
</dt> <dd>

Indica si se va a recopilar una métrica para todas las instancias de una clase de elementos administrados.

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deshabilitado** (3)


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

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

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

[**\_METRICSERVICE CIM**](cim-metricservice.md)
</dt> </dl>

 

 




