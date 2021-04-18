---
title: Método IVMVirtualMachineEvents OnRequestShutdown (VPCCOMInterfaces. h)
description: Recibe la notificación de que se ha realizado una solicitud de cierre.
ms.assetid: e04131fd-5ca7-4392-9725-ba62b905324a
keywords:
- Método OnRequestShutdown Virtual PC
- Método OnRequestShutdown Virtual PC, interfaz IVMVirtualMachineEvents
- Interfaz IVMVirtualMachineEvents Virtual PC, método OnRequestShutdown
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
ms.openlocfilehash: 94dce60a7dfdb5ed5dce714e8b8eafcbd9558b95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491296"
---
# <a name="ivmvirtualmachineeventsonrequestshutdown-method"></a>IVMVirtualMachineEvents:: OnRequestShutdown (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recibe la notificación de que se ha realizado una solicitud de cierre.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnRequestShutdown();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Se llama a este método cada vez que la sesión de máquina virtual está a punto de cerrarse. El programa cliente debe implementar este método de interfaz para recibir la notificación del evento **vmVirtualMachineEvent \_ RequestShutdown** que se origina desde [**IVMVirtualMachine**](ivmvirtualmachine.md).

Esta notificación de eventos solo se envía cuando la sesión de máquinas virtuales está a punto de cerrarse. Las rutinas de apagado del sistema operativo, como [**IVMGuestOS:: Shutdown**](ivmguestos-shutdown.md), no activan este evento directamente a menos que también intenten realizar un apagado de software del hardware virtual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents se define como 9d84f560-bb67-4961-bd12-a4da780c67e4<br/>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)
</dt> </dl>

 

