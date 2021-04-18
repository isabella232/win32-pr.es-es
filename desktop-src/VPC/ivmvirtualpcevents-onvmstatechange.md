---
title: Método IVMVirtualPCEvents OnVMStateChange (VPCCOMInterfaces. h)
description: Recibe la notificación de que el estado de una máquina virtual ha cambiado. | Método IVMVirtualPCEvents OnVMStateChange (VPCCOMInterfaces. h)
ms.assetid: a79afe14-9b7d-4528-ad38-e9b5ad068561
keywords:
- Método OnVMStateChange Virtual PC
- Método OnVMStateChange Virtual PC, interfaz IVMVirtualPCEvents
- Interfaz IVMVirtualPCEvents Virtual PC, método OnVMStateChange
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
ms.openlocfilehash: d2d0a8bd9a362c558c307fb4719c95a9ba8cbf4a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698101"
---
# <a name="ivmvirtualpceventsonvmstatechange-method"></a>IVMVirtualPCEvents:: OnVMStateChange (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

*virtualMachineConfig* \[ de\]
</dt> <dd>

El nombre de la máquina virtual.

</dd> <dt>

*virtualMachineState* \[ de\]
</dt> <dd>

El nuevo estado de la máquina virtual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

El programa cliente debe implementar este método de interfaz para recibir la notificación del evento **vmVirtualPCEvent \_ VMStateChanged** que se origina desde [**IVMVirtualPC**](ivmvirtualpc.md). Para supervisar una máquina virtual concreta, use el método [**IVMVirtualMachineEvents:: OnStateChange**](ivmvirtualmachineevents-onstatechange.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualPCEvents se define como efed1ef1-3c09-41f7-a9c2-7e29fa286c9d<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualPCEvents**](ivmvirtualpcevents.md)
</dt> </dl>

 

