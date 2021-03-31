---
description: Prueba la conectividad de red de una máquina virtual en un entorno de virtualización de red de Windows.
ms.assetid: 37d4c34d-406e-4c52-afce-b0eef754eeb3
title: Método TestNetworkConnection de la clase Msvm_VirtualSystemManagementService
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
ms.openlocfilehash: e8f15faacb1b8ad683b1ea9abfa9b91f5c376dab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153887"
---
# <a name="testnetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método TestNetworkConnection de la \_ clase VirtualSystemManagementService de MSVM

Prueba la conectividad de red de una máquina virtual en un entorno de virtualización de red de Windows.

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

*TargetNetworkAdapter* \[ de\]
</dt> <dd>

Referencia a un [**\_ EthernetPortAllocationSettingData de MSVM**](msvm-ethernetportallocationsettingdata.md) que describe el adaptador de red de destino.

</dd> <dt>

*IsSender* \[ de\]
</dt> <dd>

Indica si este método se invoca en el remitente o en el receptor.

</dd> <dt>

*SenderIP* \[ de\]
</dt> <dd>

Dirección IP del remitente.

</dd> <dt>

*ReceiverIP* \[ de\]
</dt> <dd>

Dirección Mac del remitente.

</dd> <dt>

*ReceiverMac* \[ de\]
</dt> <dd>

Dirección Mac del remitente.

</dd> <dt>

*IsolationId* \[ de\]
</dt> <dd>

IDENTIFICADOR de aislamiento.

</dd> <dt>

*SequenceNumber* \[ de\]
</dt> <dd>

IDENTIFICADOR de aislamiento.

</dd> <dt>

*RoundTripTime* \[ enuncia\]
</dt> <dd>

Tiempo de ida y vuelta.

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).

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

**Tiempo de espera** (3)
</dt> <dt>

**Parámetro no válido** (4)
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
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

