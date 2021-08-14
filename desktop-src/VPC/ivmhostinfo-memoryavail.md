---
title: Propiedad IVMHostInfo MemoryAvail (VPCCOMInterfaces.h)
description: Recupera la cantidad de memoria física disponible en el equipo host, en megabytes.
ms.assetid: cb593d02-cdb9-40f6-b57f-72fc3278f1bb
keywords:
- MemoryAvail, propiedad Virtual PC
- Propiedad MemoryAvail Virtual PC , interfaz IVMHostInfo
- Interfaz IVMHostInfo pc virtual, propiedad MemoryAvail
topic_type:
- apiref
api_name:
- IVMHostInfo.MemoryAvail
- IVMHostInfo.get_MemoryAvail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc22c9808e0498b50a140951380788ed23b6d9baee32376d416f817b851077bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118345689"
---
# <a name="ivmhostinfomemoryavail-property"></a>IVMHostInfo::MemoryAvail, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera la cantidad de memoria física disponible en el equipo host, en megabytes.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_MemoryAvail(
  [out, retval] VARIANT *megabytesOfMemory
);
```



## <a name="property-value"></a>Valor de propiedad

Memoria física disponible, en megabytes. Este valor es una **VARIANTE de** tipo VT \_ DECIMAL.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>     |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **NULL.**<br/>        |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMHostInfo se define como \_ 5b5cf343-05ad-453b-be99-adf4e27b2ebc<br/>                |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

