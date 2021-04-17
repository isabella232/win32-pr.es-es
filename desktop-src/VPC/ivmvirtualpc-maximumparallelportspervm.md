---
title: Propiedad IVMVirtualPC MaximumParallelPortsPerVM (VPCCOMInterfaces. h)
description: Recupera el número máximo de puertos paralelos por máquina virtual.
ms.assetid: c5baac59-386c-4373-a560-460750178894
keywords:
- Propiedad MaximumParallelPortsPerVM Virtual PC
- Propiedad MaximumParallelPortsPerVM Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, propiedad MaximumParallelPortsPerVM
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumParallelPortsPerVM
- IVMVirtualPC.get_MaximumParallelPortsPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57c5bed446a421190eb47630bde0d05f0cbcee7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695948"
---
# <a name="ivmvirtualpcmaximumparallelportspervm-property"></a>IVMVirtualPC:: MaximumParallelPortsPerVM (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera el número máximo de puertos paralelos por máquina virtual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_MaximumParallelPortsPerVM(
  [out, retval] long *maxPorts
);
```



## <a name="property-value"></a>Valor de propiedad

El número máximo de puertos paralelos por máquina virtual.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                           | Significado                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                                              | La operación se realizó correctamente.<br/>                                                        |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>                                | El parámetro es **null**.<br/>                                                           |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>                        | Se produjo un error inesperado.<br/>                                                    |
| <dl> <dt>Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada</dt> <dt>0xA0040951</dt> </dl> | El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

