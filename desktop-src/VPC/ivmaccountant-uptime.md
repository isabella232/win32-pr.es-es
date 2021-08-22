---
title: Propiedad IVMAccountant UpTime (VPCCOMInterfaces.h)
description: Recupera el número de segundos que la máquina virtual se ha estado ejecutando.
ms.assetid: 0c62d51b-fdf1-43f6-81d8-a5f0538c510f
keywords:
- UpTime, propiedad Virtual PC
- Propiedad UpTime Virtual PC , interfaz IVMAccountant
- IVMAccountant interface Virtual PC , propiedad UpTime
topic_type:
- apiref
api_name:
- IVMAccountant.UpTime
- IVMAccountant.get_UpTime
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df0c7731ab50d1967d59eb7178fb6bcee008b6d45fed69ab66279ae3fd8beb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654385"
---
# <a name="ivmaccountantuptime-property"></a>Propiedad IVMAccountant::UpTime

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el número de segundos que la máquina virtual se ha estado ejecutando.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_UpTime(
  [out, retval] long *secondsAlive
);
```



## <a name="property-value"></a>Valor de propiedad

número de segundos.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>       |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **NULL.**<br/>          |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                    | La máquina virtual no se está ejecutando.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>   |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

