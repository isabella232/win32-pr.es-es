---
title: Propiedad IVMAccountant CPUUtilization (VPCCOMInterfaces.h)
description: Recupera el porcentaje de uso actual de cpu para esta máquina virtual.
ms.assetid: 69bb61ec-af41-4bd0-95bd-4698a1d33098
keywords:
- CPUUtilization, propiedad Virtual PC
- CPUUtilization, propiedad Virtual PC, interfaz IVMAccountant
- IVMAccountant interface Virtual PC , PROPIEDAD CPUUtilization
topic_type:
- apiref
api_name:
- IVMAccountant.CPUUtilization
- IVMAccountant.get_CPUUtilization
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba54d7ec3a3fc447a49e9a72addd72fc5e3929b486c8fd4271276a40a7041f4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007315"
---
# <a name="ivmaccountantcpuutilization-property"></a>IVMAccountant::CPUUtilization, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el porcentaje de uso actual de cpu para esta máquina virtual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_CPUUtilization(
  [out, retval] long *percentageUtilization
);
```



## <a name="property-value"></a>Valor de propiedad

Porcentaje de uso actual de cpu.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>       |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **NULL.**<br/>          |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                    | La máquina virtual no se está ejecutando.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>   |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMAccountant se define como \_ 6376c067-7f57-4d63-b754-06e2e4f51d73<br/>              |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMAccountant**](ivmaccountant.md)
</dt> </dl>

 

