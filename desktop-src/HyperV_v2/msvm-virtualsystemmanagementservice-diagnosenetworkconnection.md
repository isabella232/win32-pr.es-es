---
description: Diagnostica la conectividad de red de una máquina virtual en un Windows Network Virtualization Environment.
ms.assetid: c18f48bf-1f57-4a23-a495-462afad42750
title: Método DiagnoseNetworkConnection de la Msvm_VirtualSystemManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DiagnoseNetworkConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9c82f72a9c2a2b16ad991940fcb378c41e75fdf31e9e6f8b74f23f9d115cab93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681135"
---
# <a name="diagnosenetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método DiagnoseNetworkConnection de la clase \_ Msvm VirtualSystemManagementService

Diagnostica la conectividad de red de una máquina virtual en un Windows Network Virtualization Environment.

## <a name="syntax"></a>Sintaxis


```mof
uint32 DiagnoseNetworkConnection(
  [in]  Msvm_EthernetPortAllocationSettingData REF TargetNetworkAdapter,
  [in]  string                                     DiagnosticSettings,
  [out] string                                     DiagnosticInformation,
  [out] CIM_ConcreteJob                        REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TargetNetworkAdapter* \[ En\]
</dt> <dd>

Referencia a [**Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) que describe el adaptador de red de destino.

</dd> <dt>

*DiagnosticSettings* \[ En\]
</dt> <dd>

Configuración de diagnóstico que se usará.

</dd> <dt>

*DiagnosticInformation* \[ out\]
</dt> <dd>

Si se realiza correctamente, devuelve la información de diagnóstico.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor 0 o 4096 si se ejecuta correctamente; de lo contrario, devuelve un error.

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

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Método reservado** (4097..32767)
</dt> <dt>

**Específico del** proveedor (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1703 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

