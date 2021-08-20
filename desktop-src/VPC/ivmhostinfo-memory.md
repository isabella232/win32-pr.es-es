---
title: Propiedad Memoria IVMHostInfo (VPCCOMInterfaces.h)
description: Recupera la cantidad total de memoria física del equipo host, en megabytes.
ms.assetid: 178013c0-cf29-4f1e-9a9d-d6a5dbd4fe2d
keywords:
- Propiedad de memoria Virtual PC
- Propiedad de memoria Virtual PC , interfaz IVMHostInfo
- IVMHostInfo interfaz De PC virtual, propiedad Memoria
topic_type:
- apiref
api_name:
- IVMHostInfo.Memory
- IVMHostInfo.get_Memory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22eeae9bcd7be7436d02f9aa116882acc4d8e0e8ee5d2703790b5e20cd4d744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117753334"
---
# <a name="ivmhostinfomemory-property"></a>IVMHostInfo::Memory, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera la cantidad total de memoria física del equipo host, en megabytes.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Memory(
  [out, retval] VARIANT *megabytesOfMemory
);
```



## <a name="property-value"></a>Valor de propiedad

Cantidad total de memoria física, en megabytes. Este valor es una **VARIANTE de** tipo VT \_ DECIMAL.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>     |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **NULL.**<br/>        |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMHostInfo se define como \_ 5b5cf343-05ad-453b-be99-adf4e27b2ebc<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

