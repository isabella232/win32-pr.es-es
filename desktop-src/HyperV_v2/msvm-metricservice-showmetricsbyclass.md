---
description: Muestra las métricas por clase.
ms.assetid: a08c0749-b60b-4b8a-996f-b3bbaf1fb2d3
title: Método ShowMetricsByClass de la Msvm_MetricService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 40865847b1deef877c70c1c99349c12915a464b394a38b5b804ea9139d5d0cf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147514"
---
# <a name="showmetricsbyclass-method-of-the-msvm_metricservice-class"></a>Método ShowMetricsByClass de la clase MetricService de Msvm \_

Muestra las métricas por clase.

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

*Asunto* \[ En\]
</dt> <dd>

Identifica una clase CIM para la que el método devuelve referencias a instancias de [**\_ Cim BaseMetricDefinition**](cim-basemetricdefinition.md) que definen métricas que están disponibles para capturarse para todas las instancias de la clase.

</dd> <dt>

*Definición* \[ En\]
</dt> <dd>

Identifica una instancia de [**CIM \_ BaseMetricDefinition.**](cim-basemetricdefinition.md) El método devuelve referencias a instancias de [**\_ ManagedElement de CIM**](cim-managedelement.md) para las que las métricas definidas por la instancia de **Cim \_ BaseMetricDefinition** están disponibles para recopilarse.

</dd> <dt>

*DefinitionList* \[ out\]
</dt> <dd>

Una vez completado correctamente el método , puede contener referencias a instancias de [**\_ BaseMetricDefinition cim**](cim-basemetricdefinition.md) que definen las métricas disponibles para la recopilación para [**el elemento \_ ManagedElement de CIM**](cim-managedelement.md) identificado por el parámetro *Subject.*

</dd> <dt>

*MetricNames* \[ out\]
</dt> <dd>

Tras la finalización correcta del método , cada índice de matriz contiene el valor de la propiedad **Name** para la instancia de [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) a la que hace referencia el índice de matriz correspondiente *del parámetro DefinitionList.*

</dd> <dt>

*MetricCollectionEnabled* \[ out\]
</dt> <dd>

Indica si se recopila una métrica para todas las instancias de una clase de elementos administrados.

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

**Vendor Reserved** (32768..65535)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los siguientes valores:

<dl> <dt>

**Correcto** ()
</dt> <dt>

**No compatible** ()
</dt> <dt>

**Error** ()
</dt> <dt>

**Método reservado** ()
</dt> <dt>

**Específico del** proveedor ()
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

 

 




