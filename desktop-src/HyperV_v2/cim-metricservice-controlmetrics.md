---
description: 'Método ControlMetrics de la clase CIM_MetricService: habilita y deshabilita la colección de métricas.'
ms.assetid: afb90863-e70a-46e5-b1b7-d959dcacc306
title: Método ControlMetrics de la CIM_MetricService clase
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
ms.openlocfilehash: c78f575bb68673c364fe627766b3709944c2a062e0407f927262ff019764b7d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068655"
---
# <a name="controlmetrics-method-of-the-cim_metricservice-class"></a>Método ControlMetrics de la clase \_ MetricService de CIM

Habilita y deshabilita la colección de métricas. **ControlMetrics** se usa para controlar la colección de cada tipo de métrica para un [**\_ elemento ManagedElement**](cim-managedelement.md)de CIM, la colección de un tipo determinado de métrica para todos los elementos administrados o la colección de una métrica específica para un elemento administrado específico.

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

*Asunto* \[ En\]
</dt> <dd>

Un [**elemento \_ ManagedElement de CIM**](cim-managedelement.md) que identifica los elementos administrados para los que se controlarán las métricas.

</dd> <dt>

*Definición* \[ En\]
</dt> <dd>

Identifica una [**\_ baseMetricDefinition cim**](cim-basemetricdefinition.md) para la que se controlarán las métricas.

</dd> <dt>

*MetricCollectionEnabled* \[ En\]
</dt> <dd>

Indica la operación deseada que se realizará en las métricas.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

**Habilitar** (2)


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

**Deshabilitar** (3)


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**Restablecimiento** (4)


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

 

 




