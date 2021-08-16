---
description: Prueba la conectividad de red de una máquina virtual en un entorno Windows virtualización de red.
ms.assetid: 37d4c34d-406e-4c52-afce-b0eef754eeb3
title: Método TestNetworkConnection de la Msvm_VirtualSystemManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.TestNetworkConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 66988944b6c4f4a97a450f63964d57084fc5886716d109e655921d8744bba721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119388385"
---
# <a name="testnetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método TestNetworkConnection de la clase \_ Msvm VirtualSystemManagementService

Prueba la conectividad de red de una máquina virtual en un entorno Windows virtualización de red.

## <a name="syntax"></a>Sintaxis


```mof
uint32 TestNetworkConnection(
  [in]  Msvm_EthernetPortAllocationSettingData REF TargetNetworkAdapter,
  [in]  boolean                                    IsSender,
  [in]  string                                     SenderIP,
  [in]  string                                     ReceiverIP,
  [in]  string                                     ReceiverMac,
  [in]  uint32                                     IsolationId,
  [in]  uint32                                     SequenceNumber,
  [out] uint32                                     RoundTripTime,
  [out] CIM_ConcreteJob                        REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TargetNetworkAdapter* \[ En\]
</dt> <dd>

Referencia a [**Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) que describe el adaptador de red de destino.

</dd> <dt>

*IsSender* \[ En\]
</dt> <dd>

Indica si este método se invoca en el remitente o en el receptor.

</dd> <dt>

*SenderIP* \[ En\]
</dt> <dd>

Dirección IP del remitente.

</dd> <dt>

*ReceiverIP* \[ En\]
</dt> <dd>

Dirección Mac del remitente.

</dd> <dt>

*ReceiverMac* \[ En\]
</dt> <dd>

Dirección Mac del remitente.

</dd> <dt>

*IsolationId* \[ En\]
</dt> <dd>

Id. de aislamiento.

</dd> <dt>

*SequenceNumber* \[ En\]
</dt> <dd>

Id. de aislamiento.

</dd> <dt>

*RoundTripTime* \[ out\]
</dt> <dd>

Tiempo de ida y vuelta.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.

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

**DMTF reservado** (..)
</dt> <dt>

**Parámetros de método activados: trabajo iniciado** (4096)
</dt> <dt>

**Método reservado** (4097..32767)
</dt> <dt>

**Específico del** proveedor (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

