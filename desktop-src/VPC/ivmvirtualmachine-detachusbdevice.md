---
title: Método IVMVirtualMachine DetachUSBDevice (VPCCOMInterfaces.h)
description: Libera un dispositivo USB de una máquina virtual.
ms.assetid: ae2b70b1-7bf3-4a84-9f05-4e91de93fa73
keywords:
- DetachUSBDevice method Virtual PC
- DetachUSBDevice method Virtual PC , IVMVirtualMachine interface
- IVMVirtualMachine interface Virtual PC , Método DetachUSBDevice
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DetachUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e5b45821f56a9533ed851f6c73342fbd15801223832cf9bad9a380b3f97f05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344679"
---
# <a name="ivmvirtualmachinedetachusbdevice-method"></a>IVMVirtualMachine::D etachUSBDevice (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Libera un dispositivo USB de una máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DetachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*inUSBDevice* \[ En\]
</dt> <dd>

Puntero [**IVMUSBDevice**](ivmusbdevice.md) que representa el dispositivo USB que se va a desasociar de la máquina virtual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                          | Descripción                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                | La operación se realizó correctamente.<br/>       |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                  | El parámetro es **NULL.**<br/>          |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING**</dt> <dt>0xA0040206</dt> </dl>     | La máquina virtual no se está ejecutando.<br/> |
| <dl> <dt>**Máquina virtual \_ E \_ ERROR \_ DE DESASOCIÓN \_**</dt> <dt>USB 0xA00400927</dt> </dl> | Error en la operación de desasoción.<br/>        |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>          | Se produjo un error inesperado.<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualMachine se define como \_ f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

