---
title: Propiedad IVMVirtualMachine Mouse (VPCCOMInterfaces.h)
description: Recupera el dispositivo del mouse de la máquina virtual.
ms.assetid: 917bbcc1-615d-4fd7-87e1-62abf2ece539
keywords:
- Propiedad del mouse Virtual PC
- Propiedad del mouse Virtual PC , interfaz IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC , propiedad mouse
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Mouse
- IVMVirtualMachine.get_Mouse
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ef16d32410e66e8ea3a3baf23160074cf99d97762df3402bf437d0719d6332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344659"
---
# <a name="ivmvirtualmachinemouse-property"></a>Propiedad IVMVirtualMachine::Mouse

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el dispositivo del mouse de la máquina virtual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Mouse(
  [out, retval] IVMMouse **mouse
);
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**IVMMouse.**](ivmmouse.md)

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                         | Significado                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                            | La operación se realizó correctamente.<br/>       |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>              | El parámetro es **NULL.**<br/>          |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>      | La configuración es desconocida.<br/>       |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING</dt> <dt>0xA0040206</dt> </dl> | La máquina virtual no se está ejecutando.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>      | Se produjo un error inesperado.<br/>   |



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

 

