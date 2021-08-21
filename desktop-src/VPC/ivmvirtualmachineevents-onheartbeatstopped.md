---
title: Método IVMVirtualMachineEvents OnBeatStopped (VPCCOMInterfaces.h)
description: Recibe la notificación de que se ha detenido el latido de una máquina virtual.
ms.assetid: 58fc81a8-747c-47f9-98ec-38482694f533
keywords:
- Equipo virtual del método OnBeatStopped
- OnBeatStopped, método Virtual PC, interfaz IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface Virtual PC , OnBeatStopped method
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnHeartbeatStopped
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ad4af982899f2f5f5dce6d78569323fbb6a85168c81b7c88c3ee0c62b3a39f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056593"
---
# <a name="ivmvirtualmachineeventsonheartbeatstopped-method"></a>IVMVirtualMachineEvents::OnBeatStopped (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recibe la notificación de que se ha detenido el latido de una máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnHeartbeatStopped();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Se llama a este método cuando el sistema operativo invitado de esta máquina virtual se ha detenido repentinamente. El programa cliente debe implementar este método de interfaz para recibir la notificación del evento vmVirtualMachineEvent HeartbeatStopped que se origina \_ en [**IVMVirtualMachine**](ivmvirtualmachine.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents se define como 9d84f560-bb67-4961-bd12-a4da780c67e4<br/>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)
</dt> </dl>

 

