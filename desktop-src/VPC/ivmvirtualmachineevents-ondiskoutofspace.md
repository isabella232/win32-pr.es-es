---
title: Método IVMVirtualMachineEvents OnDiskOutOfSpace (VPCCOMInterfaces.h)
description: Recibe la notificación de que un disco necesario para una máquina virtual tiene poco espacio libre.
ms.assetid: 1c431904-fffd-4513-8670-b9723f53edf1
keywords:
- Equipo virtual del método OnDiskOutOfSpace
- Método OnDiskOutOfSpace de PC virtual, interfaz IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface Virtual PC , OnDiskOutOfSpace method
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnDiskOutOfSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c482f0a713fda7e13436dc28d295469237273a7c607e522ce457ec908f210223
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056633"
---
# <a name="ivmvirtualmachineeventsondiskoutofspace-method"></a>IVMVirtualMachineEvents::OnDiskOutOfSpace (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recibe la notificación de que un disco necesario para una máquina virtual (VM) tiene poco espacio libre. Si el espacio disponible cae por debajo de 100 MB, este evento se recibe como una advertencia y si el espacio disponible cae por debajo de 20 MB, este evento se recibe de nuevo como un error y la máquina virtual se pausará.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnDiskOutOfSpace(
  [in] VARIANT_BOOL criticallyLow
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*criticallyLow* \[ En\]
</dt> <dd>

Establezca en **VARIANT \_ TRUE** si el disco tiene menos de 20 MB libres y en **VARIANT \_ FALSE** si el espacio disponible es superior a 20 MB pero inferior a 100 MB.

</dd> </dl>

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

 

