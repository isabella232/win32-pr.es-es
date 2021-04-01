---
title: Propiedad IVMAccountant gráfico (VPCCOMInterfaces. h)
description: Recupera el porcentaje de uso actual de la CPU para esta máquina virtual.
ms.assetid: 69bb61ec-af41-4bd0-95bd-4698a1d33098
keywords:
- Propiedad gráfico Virtual PC
- Propiedad gráfico Virtual PC, interfaz IVMAccountant
- Interfaz IVMAccountant Virtual PC, propiedad gráfico
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
ms.openlocfilehash: c9e38c223f47678cdb9c2d49e06452d014083c94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997051"
---
# <a name="ivmaccountantcpuutilization-property"></a>IVMAccountant:: gráfico (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera el porcentaje de uso actual de la CPU para esta máquina virtual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_CPUUtilization(
  [out, retval] long *percentageUtilization
);
```



## <a name="property-value"></a>Valor de propiedad

Porcentaje del uso actual de la CPU.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>       |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **null**.<br/>          |
| <dl> <dt>S \_ FALSO</dt> <dt>1</dt> </dl>                    | La máquina virtual no se está ejecutando.<br/> |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>   |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMAccountant se define como 6376c067-7f57-4D63-b754-06e2e4f51d73<br/>              |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMAccountant**](ivmaccountant.md)
</dt> </dl>

 

