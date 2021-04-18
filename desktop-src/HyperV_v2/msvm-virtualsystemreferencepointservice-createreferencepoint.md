---
description: Crea un punto de referencia de un sistema virtual.
ms.assetid: 9cc7665a-9562-4267-bcd0-3162e426fbad
title: Método CreateReferencePoint de la clase Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.CreateReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 08d28970288ba62346894d758ebac5ac156962ff
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105670070"
---
# <a name="createreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>Método CreateReferencePoint de la \_ clase VirtualSystemReferencePointService de MSVM

Crea un punto de referencia de un sistema virtual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CreateReferencePoint(
  [in]      Msvm_ComputerSystem              REF AffectedSystem,
  [in]      string                               ReferencePointSettings,
  [in]      uint16                               ReferencePointType,
  [in, out] Msvm_VirtualSystemReferencePoint REF ResultingReferencePoint,
  [out]     CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AffectedSystem* \[ de\]
</dt> <dd>

Un [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que hace referencia al sistema virtual afectado.

</dd> <dt>

*ReferencePointSettings* \[ de\]
</dt> <dd>

Contiene la configuración del parámetro.

</dd> <dt>

*ReferencePointType* \[ de\]
</dt> <dd>

Tipo de punto de referencia solicitado:

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Basado en el registro** (0)


</dt> <dd>

Basado en el seguimiento del registro de réplica de Hyper-V.

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT basado** (1)


</dt> <dd>

Basado en Change Tracking resistente de los discos virtuales.

</dd> </dl> </dd> <dt>

*ResultingReferencePoint* \[ in, out\]
</dt> <dd>

Punto de referencia del sistema virtual resultante

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Si la operación es de larga ejecución, opcionalmente se puede devolver un trabajo. En este caso, la instancia de la [**clase \_ MSVM VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) que representa el nuevo punto de referencia del sistema virtual se presenta a través de la Asociación [**\_ AffectedJobElement CIM**](cim-affectedjobelement.md) con el valor de la propiedad **AffectedElement** que hace referencia a la nueva instancia de la clase **MSVM \_ VirtualSystemReferencePoint** que representa el punto de referencia del sistema virtual y el valor de **ElementEffects** establecido en 5 (Create).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se ejecuta correctamente, devuelve 0; de lo contrario, devuelve un error.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Error** (2)
</dt> <dt>

**Tiempo de espera** (3)
</dt> <dt>

**Parámetro no válido** (4)
</dt> <dt>

**Estado no válido** (5)
</dt> <dt>

**Tipo no válido** (6)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Método reservado** (de no.. 32767)
</dt> <dt>

**Específico del proveedor** (32768... 65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




