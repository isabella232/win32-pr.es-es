---
title: Método IVMVirtualMachineEvents OnAdditionsAvailable (VPCCOMInterfaces.h)
description: Recibe la notificación de que los componentes de integración están disponibles en una máquina virtual.
ms.assetid: c940104b-4d34-47c2-bf48-9024a7f86c46
keywords:
- OnAdditionsAvailable method Virtual PC
- Método OnAdditionsAvailable de Virtual PC, interfaz IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface Virtual PC , OnAdditionsAvailable (Método OnAdditionsAvailable)
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnAdditionsAvailable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81657563a921ca8a9aa7ef511183a56aa2d7a599e69232fcc186d7d911cb65bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056762"
---
# <a name="ivmvirtualmachineeventsonadditionsavailable-method"></a>IVMVirtualMachineEvents::OnAdditionsAvailable (Método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recibe la notificación de que los componentes de integración están disponibles en una máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnAdditionsAvailable();
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

 

