---
description: Establece las horas del ejemplo de control.
ms.assetid: 17ffa106-8b6b-4077-895c-03400505c2a0
title: Método ControlSampleTimes de la Msvm_MetricService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlSampleTimes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ea13050c2c8e52d5786a97b3b749f10e48a73c4ecf1274e0415967ad25c9d9ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521485"
---
# <a name="controlsampletimes-method-of-the-msvm_metricservice-class"></a>Método ControlSampleTimes de la clase \_ MetricService de Msvm

Establece las horas del ejemplo de control.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ControlSampleTimes(
  [in] datetime StartSampleTime,
  [in] datetime PreferredSampleInterval,
  [in] boolean  RestartGathering
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StartSampleTime* \[ En\]
</dt> <dd>

Momento en el que se va a iniciar el muestreo de las métricas.

Un valor de 99990101000000.000000+000 indicará que el muestreo debe comenzar la próxima vez que se sincronice a la hora completa. El muestreo se sincroniza con la hora completa si los segundos desde el intervalo de muestra del módulo de medianoche en segundos es igual a 0.

</dd> <dt>

*PreferredSampleInterval* \[ En\]
</dt> <dd>

Tiempo de intervalo de ejemplo preferido. Para obtener métricas correlacionables, se recomienda elegir el intervalo de muestra de forma que el tiempo de intervalo de muestra de módulo de 3600 en segundos sea igual a 0.

Es responsabilidad de la implementación del servicio de métricas CIM decidir si se respeta el tiempo de intervalo de ejemplo solicitado.

El cliente CIM puede comprobar si los proveedores de métricas respetan o no el tiempo de intervalo de ejemplo solicitado mediante la recuperación de instancias de BaseMetricDefinition relacionadas y la comprobación del contenido de la propiedad "CIM \_ BaseMetricDefinition.SampleInterval".

</dd> <dt>

*RestartGathering* \[ En\]
</dt> <dd>

Booleano que, cuando se establece en TRUE, solicita que la recopilación de todas las métricas asociadas al servicio de métricas se vuelva a iniciar con esta llamada de método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los siguientes valores:

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

 

 




