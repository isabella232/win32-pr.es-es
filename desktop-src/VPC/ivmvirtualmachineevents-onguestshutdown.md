---
title: Método IVMVirtualMachineEvents OnGuestShutdown (VPCCOMInterfaces.h)
description: Recibe la notificación de que el sistema operativo invitado se apaga.
ms.assetid: a70c746a-f1ce-4f93-b41b-b03dc83f3da2
keywords:
- OnGuestShutdown, método Virtual PC
- OnGuestShutdown method Virtual PC , IVMVirtualMachineEvents (interfaz IVMVirtualMachineEvents)
- IVMVirtualMachineEvents interface Virtual PC , OnGuestShutdown method
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnGuestShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4da02164e22321842d09a29c4a8a286edfe548108afd927b3127886a98f6e05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056573"
---
# <a name="ivmvirtualmachineeventsonguestshutdown-method"></a>IVMVirtualMachineEvents::OnGuestShutdown (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recibe la notificación de que el sistema operativo invitado se apaga.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnGuestShutdown();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

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

 

