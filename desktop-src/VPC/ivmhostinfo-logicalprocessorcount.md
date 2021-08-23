---
title: Propiedad IVMHostInfo LogicalProcessorCount (VPCCOMInterfaces.h)
description: Recupera el número de procesadores lógicos del equipo host.
ms.assetid: bf978a80-9a21-426a-ac18-109f20d38cbb
keywords:
- Equipo virtual de la propiedad LogicalProcessorCount
- Propiedad LogicalProcessorCount De PC virtual, interfaz IVMHostInfo
- Interfaz IVMHostInfo de EQUIPO virtual, propiedad LogicalProcessorCount
topic_type:
- apiref
api_name:
- IVMHostInfo.LogicalProcessorCount
- IVMHostInfo.get_LogicalProcessorCount
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d084f383965aa9264ce4d8492e6eaace612f9ec3be487781ce4d69ec1e43863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512135"
---
# <a name="ivmhostinfologicalprocessorcount-property"></a>IVMHostInfo::LogicalProcessorCount, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el número de procesadores lógicos del equipo host.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_LogicalProcessorCount(
  [out, retval] long *processorCount
);
```



## <a name="property-value"></a>Valor de propiedad

Número de procesadores lógicos.

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

 

