---
title: Método IVMVirtualMachineEvents OnAdditionsUninstalled (VPCCOMInterfaces.h)
description: Recibe la notificación de que los componentes de integración se desinstalan en una máquina virtual.
ms.assetid: bbbc01b6-adb1-491e-a5b0-ff463dca7dfd
keywords:
- OnAdditionsUninstalled method Virtual PC
- OnAdditionsUninstalled method Virtual PC , IVMVirtualMachineEvents (interfaz)
- IVMVirtualMachineEvents interface Virtual PC , OnAdditionsUninstalled (Método OnAdditionsUninstalled)
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnAdditionsUninstalled
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd0371ea41c22f24ee2dd21e1a41166f839af8fce2aa84d58a7844d4e11f0bbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056733"
---
# <a name="ivmvirtualmachineeventsonadditionsuninstalled-method"></a>IVMVirtualMachineEvents::OnAdditionsUninstalled (Método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recibe la notificación de que los componentes de integración se desinstalan en una máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnAdditionsUninstalled();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

