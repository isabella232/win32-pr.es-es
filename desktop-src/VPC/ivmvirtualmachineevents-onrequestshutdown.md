---
title: Método IVMVirtualMachineEvents OnRequestShutdown (VPCCOMInterfaces.h)
description: Recibe la notificación de que se ha realizado una solicitud de cierre.
ms.assetid: e04131fd-5ca7-4392-9725-ba62b905324a
keywords:
- OnRequestShutdown method Virtual PC
- Método OnRequestShutdown virtual PC , interfaz IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface Virtual PC , Método OnRequestShutdown
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnRequestShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 929c9a293e760a12ace62766cbd7a0c016980fc2399cdde494402a272d90fe0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123175"
---
# <a name="ivmvirtualmachineeventsonrequestshutdown-method"></a>IVMVirtualMachineEvents::OnRequestShutdown (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recibe la notificación de que se ha realizado una solicitud de cierre.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnRequestShutdown();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Se llama a este método cada vez que la sesión de la máquina virtual está a punto de cerrarse. El programa cliente debe implementar este método de interfaz para recibir la notificación del evento **vmVirtualMachineEvent \_ RequestShutdown** que se origina en [**IVMVirtualMachine**](ivmvirtualmachine.md).

Esta notificación de eventos solo se envía cuando la sesión de máquinas virtuales está a punto de cerrarse. Las rutinas de apagado del sistema operativo, como [**IVMGuestOS::Shutdown,**](ivmguestos-shutdown.md)no despeguen este evento directamente a menos que también intenten realizar una alimentación de software fuera del hardware virtual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents se define como 9d84f560-bb67-4961-bd12-a4da780c67e4<br/>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)
</dt> </dl>

 

