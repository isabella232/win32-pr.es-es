---
title: Enumeración VMEndpointType (VPCCOMInterfaces.h)
description: Especifica el tipo de punto de conexión.
ms.assetid: b48bd860-50dc-4c8c-b65b-69c407d4612a
keywords:
- VMEndpointType (enumeración de VIRTUAL PC)
topic_type:
- apiref
api_name:
- VMEndpointType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2857dc19d6764c5c4052305d430a6ab3601493955c07f39501be4b0af10564d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136468"
---
# <a name="vmendpointtype-enumeration"></a>Enumeración VMEndpointType

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Especifica el tipo de punto de conexión.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmEndpoint_NamedPipe  = 0,
  vmEndpoint_TCPIP      = 1
} VMEndpointType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="vmEndpoint_NamedPipe"></span><span id="vmendpoint_namedpipe"></span><span id="VMENDPOINT_NAMEDPIPE"></span>**vmEndpoint \_ NamedPipe**
</dt> <dd>

Lado host.

</dd> <dt>

<span id="vmEndpoint_TCPIP"></span><span id="vmendpoint_tcpip"></span><span id="VMENDPOINT_TCPIP"></span>**vmEndpoint \_ TCPIP**
</dt> <dd>

Lado invitado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualMachine::StartCommunicationChannel**](ivmvirtualmachine-startcommunicationchannel.md)
</dt> </dl>

 

