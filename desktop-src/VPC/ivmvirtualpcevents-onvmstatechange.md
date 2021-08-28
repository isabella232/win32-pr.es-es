---
title: Método IVMVirtualPCEvents OnVMStateChange (VPCCOMInterfaces.h)
description: Recibe la notificación de que el estado de una máquina virtual ha cambiado. | Método IVMVirtualPCEvents OnVMStateChange (VPCCOMInterfaces.h)
ms.assetid: a79afe14-9b7d-4528-ad38-e9b5ad068561
keywords:
- Equipo virtual del método OnVMStateChange
- Método OnVMStateChange para PC virtual, interfaz IVMVirtualPCEvents
- IVMVirtualPCEvents interface Virtual PC , Método OnVMStateChange
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnVMStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63516e80ce4f3b830229fdb4cd574e95378c0569a4855a73c1c528af2ec8b48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032985"
---
# <a name="ivmvirtualpceventsonvmstatechange-method"></a>IVMVirtualPCEvents::OnVMStateChange (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recibe la notificación de que el estado de una máquina virtual ha cambiado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnVMStateChange(
  [in] BSTR      virtualMachineConfig,
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*virtualMachineConfig* \[ En\]
</dt> <dd>

El nombre de la máquina virtual.

</dd> <dt>

*virtualMachineState* \[ En\]
</dt> <dd>

Nuevo estado de la máquina virtual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

El programa cliente debe implementar este método de interfaz para recibir la notificación del evento **vmVirtualPCEvent \_ VMStateChanged** que se origina en [**IVMVirtualPC**](ivmvirtualpc.md). Para supervisar una máquina virtual específica, use el [**método IVMVirtualMachineEvents::OnStateChange.**](ivmvirtualmachineevents-onstatechange.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualPCEvents se define como efed1ef1-3c09-41f7-a9c2-7e29fa286c9d<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualPCEvents**](ivmvirtualpcevents.md)
</dt> </dl>

 

