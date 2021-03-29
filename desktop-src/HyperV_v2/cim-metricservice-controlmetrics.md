---
description: Habilita y deshabilita la recopilación de métricas.
ms.assetid: afb90863-e70a-46e5-b1b7-d959dcacc306
title: Método ControlMetrics de la clase CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 60a7d0b34227594cf7146a988aa7e0d232f2d6cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277055"
---
# <a name="controlmetrics-method-of-the-cim_metricservice-class"></a>Método ControlMetrics de la \_ clase MetricService de CIM

Habilita y deshabilita la recopilación de métricas. **ControlMetrics** se utiliza para controlar la colección de cada tipo de métrica para un [**\_ ManagedElement CIM**](cim-managedelement.md), la colección de un tipo de métrica determinado para todos los elementos administrados o la colección de una métrica específica para un elemento administrado concreto.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ControlMetrics(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Asunto* \[ de\]
</dt> <dd>

Un [**elemento \_ ManagedElement de CIM**](cim-managedelement.md) que identifica los elementos administrados para los que se controlarán las métricas.

</dd> <dt>

*Definición* \[ de de\]
</dt> <dd>

Identifica un [**\_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) para el que se controlarán las métricas.

</dd> <dt>

*MetricCollectionEnabled* \[ de\]
</dt> <dd>

Indica la operación deseada que se va a realizar en las métricas.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

**Habilitar** (2)


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

**Deshabilitar** (3)


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**Restablecer** (4)


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

 

 




