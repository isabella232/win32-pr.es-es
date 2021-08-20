---
title: Método OnReset IVMVirtualMachineEvents (VPCCOMInterfaces.h)
description: Recibe la notificación de que se ha restablecido una máquina virtual.
ms.assetid: 10a66aea-9a8f-4663-8eb6-cc35f361e43f
keywords:
- Equipo virtual del método OnReset
- Método OnReset virtual PC , interfaz IVMVirtualMachineEvents
- Interfaz IVMVirtualMachineEvents Pc virtual, método OnReset
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnReset
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4101885469de59a7cd2740dc07db44101ce130df037540306f4afdab78c80fd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122908"
---
# <a name="ivmvirtualmachineeventsonreset-method"></a>IVMVirtualMachineEvents::OnReset (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recibe la notificación de que se ha restablecido una máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnReset();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Se llama a este método cuando se ha restablecido la máquina virtual. El programa cliente debe implementar este método de interfaz para recibir una notificación del evento vmVirtualMachineEvent Reset que se origina \_ en [**IVMVirtualMachine**](ivmvirtualmachine.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents se define como 9d84f560-bb67-4961-bd12-a4da780c67e4<br/>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)
</dt> </dl>

 

