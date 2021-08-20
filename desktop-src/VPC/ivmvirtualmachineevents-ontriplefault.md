---
title: Método IVMVirtualMachineEvents OnTripleFault (VPCCOMInterfaces.h)
description: Recibe la notificación de que una máquina virtual tiene un triple error.
ms.assetid: a17b1a05-3058-48ba-a196-7e9563f3e1c0
keywords:
- OnTripleFault, método Virtual PC
- Método OnTripleFault virtual PC , interfaz IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface Virtual PC , Método OnTripleFault
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnTripleFault
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9328ceff18256621a590bf0f235aca8ff12b142e4cdedf389d9d270bfde9bad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122695"
---
# <a name="ivmvirtualmachineeventsontriplefault-method"></a>IVMVirtualMachineEvents::OnTripleFault (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recibe la notificación de que una máquina virtual tiene un triple error.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnTripleFault();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Se llama a este método cuando una máquina virtual tiene un triple error. El programa cliente debe implementar este método de interfaz para recibir la notificación del evento tripleFault vmVirtualMachineEvent que se origina \_ en [**IVMVirtualMachine**](ivmvirtualmachine.md).

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

 

