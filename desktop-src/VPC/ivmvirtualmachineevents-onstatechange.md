---
title: Método OnStateChange de IVMVirtualMachineEvents (VPCCOMInterfaces.h)
description: Recibe la notificación de que el estado de una máquina virtual ha cambiado. | Método OnStateChange de IVMVirtualMachineEvents (VPCCOMInterfaces.h)
ms.assetid: 1737bb5e-078d-4ebe-9558-de083aae1baa
keywords:
- Equipo virtual del método OnStateChange
- Método OnStateChange virtual PC , interfaz IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface Virtual PC , Método OnStateChange
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cf966d2439f3095051331b5412bc92cca9ba76e6f98c9777402ba449f2e7f44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122705"
---
# <a name="ivmvirtualmachineeventsonstatechange-method"></a>IVMVirtualMachineEvents::OnStateChange (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recibe la notificación de que el estado de una máquina virtual ha cambiado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnStateChange(
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*virtualMachineState* \[ En\]
</dt> <dd>

Nuevo estado de la máquina virtual. Para obtener una lista de valores, vea [**VMVMState.**](vmvmstate.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Se llama a este método cuando cambia el estado de esta máquina virtual. El programa cliente debe implementar este método de interfaz para recibir la notificación del evento vmVirtualMachineEvent StateChanged que se origina \_ en [**IVMVirtualMachine**](ivmvirtualmachine.md).

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

 

