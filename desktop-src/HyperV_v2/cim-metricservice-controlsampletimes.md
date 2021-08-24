---
description: Permite especificar la especificación de la recopilación de métricas a un momento dado que se debe iniciar y especificar el tiempo de intervalo de muestra preferido para la recopilación periódica de datos.
ms.assetid: 3dd6dc16-a618-49ff-bbaf-cfa25c249cf1
title: Método ControlSampleTimes de la CIM_MetricService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlSampleTimes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 833e828a7622dfcd76a7b061e3890fbe111de10a6b8c3c2d3faf0801429678f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695075"
---
# <a name="controlsampletimes-method-of-the-cim_metricservice-class"></a>Método ControlSampleTimes de la clase \_ MetricService de CIM

Permite especificar la especificación de la recopilación de métricas a un momento dado que se debe iniciar y especificar el tiempo de intervalo de muestra preferido para la recopilación periódica de datos.

Cada vez que se inicia el muestreo de métricas adicionales, se puede usar la configuración especificada por este método.

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

Momento dado en el que se va a iniciar el muestreo de las métricas.

Un valor de 99990101000000.000000+000 indicará que el muestreo debe comenzar la próxima vez que se sincronice a la hora completa. El muestreo se sincroniza con la hora completa si los segundos desde el intervalo de muestra del módulo de medianoche en segundos es igual a 0.

</dd> <dt>

*PreferredSampleInterval* \[ En\]
</dt> <dd>

Tiempo de intervalo de ejemplo preferido. Para obtener métricas correlacionables, se recomienda elegir el intervalo de muestra de forma que el tiempo del intervalo de muestra de módulo de 3600 en segundos sea igual a 0.

Es responsabilidad de la implementación del servicio de métricas CIM decidir si se respeta el tiempo de intervalo de ejemplo solicitado.

El cliente CIM puede comprobar si los proveedores de métricas respetan o no el tiempo de intervalo de ejemplo solicitado recuperando instancias de BaseMetricDefinition relacionadas y comprobando el contenido de [**\_ Cim BaseMetricDefinition**](cim-basemetricdefinition.md).**Propiedad SampleInterval.**

</dd> <dt>

*RestartGathering* \[ En\]
</dt> <dd>

**TRUE** para solicitar que la recopilación de todas las métricas asociadas al servicio de métricas se vuelva a iniciar con esta llamada de método.

</dd> </dl>

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

 

 




