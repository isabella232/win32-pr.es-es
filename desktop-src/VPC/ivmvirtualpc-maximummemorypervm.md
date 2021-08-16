---
title: Propiedad IVMVirtualPC MaximumMemoryPerVM (VPCCOMInterfaces.h)
description: Recupera la cantidad máxima permitido de memoria física por máquina virtual, en megabytes.
ms.assetid: eb30dd6c-8f37-4cf9-9ed7-47925b5b1112
keywords:
- MaximumMemoryPerVM, propiedad Virtual PC
- MaximumMemoryPerVM, propiedad Virtual PC, interfaz IVMVirtualPC
- IVMVirtualPC interface Virtual PC , MaximumMemoryPerVM property
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumMemoryPerVM
- IVMVirtualPC.get_MaximumMemoryPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e483d955548b1e90d019ecc069b8ca6169a350d8646078a7aa5b4b29b7e25d9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344312"
---
# <a name="ivmvirtualpcmaximummemorypervm-property"></a>IVMVirtualPC::MaximumMemoryPerVM, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera la cantidad máxima permitido de memoria física por máquina virtual, en megabytes.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_MaximumMemoryPerVM(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a>Valor de propiedad

Cantidad máxima permitido, en megabytes, de memoria física por máquina virtual.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                           | Significado                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                              | La operación se realizó correctamente.<br/>                                                        |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                                | El parámetro es **NULL.**<br/>                                                           |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                        | Se produjo un error inesperado.<br/>                                                    |
| <dl> <dt>Máquina virtual \_ E \_ \_ VIRTUALIZACIÓN DE HARDWARE \_ DESHABILITADA</dt> <dt>0xA0040951</dt> </dl> | El procesador no admite extensiones de virtualización acelerada de hardware (HAV).<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC se define como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

