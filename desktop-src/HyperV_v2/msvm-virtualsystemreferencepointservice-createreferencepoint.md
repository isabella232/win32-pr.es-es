---
description: Crea un punto de referencia de un sistema virtual.
ms.assetid: 9cc7665a-9562-4267-bcd0-3162e426fbad
title: Método CreateReferencePoint de la Msvm_VirtualSystemReferencePointService clase
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
ms.openlocfilehash: fdcf4680ff10bdc8135fae4ec3bb9f81d53c26092e7196e73965ee4f4d87991f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014483"
---
# <a name="createreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>Método CreateReferencePoint de la clase \_ Msvm VirtualSystemReferencePointService

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

*AffectedSystem* \[ En\]
</dt> <dd>

[**Msvm \_ ComputerSystem que hace**](msvm-computersystem.md) referencia al sistema virtual afectado.

</dd> <dt>

*ReferencePointSettings* \[ En\]
</dt> <dd>

Contiene la configuración de parámetros.

</dd> <dt>

*ReferencePointType* \[ En\]
</dt> <dd>

Tipo de punto de referencia solicitado:

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Basado en registros** (0)


</dt> <dd>

Basado en el seguimiento de registros de réplica de Hyper-V.

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**Basado en RCT** (1)


</dt> <dd>

Basado en la resistencia Change Tracking discos virtuales.

</dd> </dl> </dd> <dt>

*ResultingReferencePoint* \[ in, out\]
</dt> <dd>

Punto de referencia del sistema virtual resultante

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación es de larga duración, opcionalmente se puede devolver un trabajo. En este caso, la instancia de la clase [**\_ Msvm VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) que representa el nuevo punto de referencia del sistema virtual se presenta a través de la asociación [**\_ AffectedJobElement**](cim-affectedjobelement.md) de CIM con el valor de la propiedad **AffectedElement** que hace referencia a la nueva instancia de la clase **\_ VirtualSystemReferencePoint de Msvm** que representa el punto de referencia del sistema virtual y el valor de **elementEffects** establecido en 5 (Crear).

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

**Tiempo de** espera (3)
</dt> <dt>

**Parámetro no válido** (4)
</dt> <dt>

**Estado no válido** (5)
</dt> <dt>

**Tipo no** válido (6)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parámetros de método activados: trabajo iniciado** (4096)
</dt> <dt>

**Método reservado** (4097..32767)
</dt> <dt>

**Específico del** proveedor (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




