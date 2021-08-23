---
description: 'Informa de lo siguiente: las métricas disponibles para recopilarse para todas las instancias de una clase CIM, las clases CIM para las que una métrica definida por una instancia de BaseMetricDefinition de CIM está disponible para recopilarse y si una métrica determinada se está recopilando actualmente para un elemento \_ administrado.'
ms.assetid: 0115a5b5-2824-4c43-a8dc-757524c5d3dd
title: Método ShowMetricsByClass de la CIM_MetricService clase
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
ms.openlocfilehash: c70d81f153471e841803dde195f09886137f29b390298c2c7d09ce69ad1648e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694964"
---
# <a name="showmetricsbyclass-method-of-the-cim_metricservice-class"></a>Método ShowMetricsByClass de la clase \_ MetricService de CIM

Informa de lo siguiente: las métricas disponibles para recopilarse para todas las instancias de una clase CIM, las clases CIM para las que una métrica definida por una instancia de [**\_ BaseMetricDefinition**](cim-basemetricdefinition.md) de CIM está disponible para recopilarse y si una métrica determinada se está recopilando actualmente para un elemento administrado.

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

Identifica una clase CIM para la que el método devuelve referencias a instancias de [**\_ BaseMetricDefinition**](cim-basemetricdefinition.md) de CIM que definen métricas que están disponibles para capturarse para todas las instancias de la clase.

</dd> <dt>

*Definición* \[ En\]
</dt> <dd>

Identifica una instancia de [**CIM \_ BaseMetricDefinition.**](cim-basemetricdefinition.md) El método devuelve referencias a instancias de [**\_ ManagedElement**](cim-managedelement.md) de CIM para las que las métricas definidas por la instancia de **\_ BaseMetricDefinition** de CIM están disponibles para recopilarse.

</dd> <dt>

*DefinitionList* \[ out\]
</dt> <dd>

Si se ejecuta correctamente, puede contener referencias a instancias de objetos [**\_ BaseMetricDefinition**](cim-basemetricdefinition.md) de CIM que definen métricas disponibles para la recopilación para [**el elemento \_ ManagedElement**](cim-managedelement.md) de CIM identificado por el *parámetro Subject.*

</dd> <dt>

*MetricNames* \[ out\]
</dt> <dd>

Si se ejecuta correctamente, cada índice de matriz debe contener el valor de la propiedad **Name** para la instancia de [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) a la que hace referencia el índice de matriz correspondiente del *parámetro DefinitionList.*

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

Devuelve un 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

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

[**CIM \_ MetricService**](cim-metricservice.md)
</dt> </dl>

 

 




