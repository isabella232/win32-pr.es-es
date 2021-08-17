---
title: Propiedad IVMHostInfo NetworkAddresses (VPCCOMInterfaces.h)
description: Recupera una colección enumerable de direcciones TCP/IP en el equipo host.
ms.assetid: 94716b82-8f35-4702-873d-64507d879dc3
keywords:
- Equipo virtual de la propiedad NetworkAddresses
- Propiedad NetworkAddresses Pc virtual, interfaz IVMHostInfo
- Interfaz IVMHostInfo pc virtual, propiedad NetworkAddresses
topic_type:
- apiref
api_name:
- IVMHostInfo.NetworkAddresses
- IVMHostInfo.get_NetworkAddresses
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19b3be88d65e567fd9586ae9f0a205eb2c55c77328d7725f59e5c80a8e63324b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117753297"
---
# <a name="ivmhostinfonetworkaddresses-property"></a>Propiedad IVMHostInfo::NetworkAddresses

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera una colección enumerable de direcciones TCP/IP en el equipo host.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_NetworkAddresses(
  [out, retval] VARIANT *hostAddresses
);
```



## <a name="property-value"></a>Valor de propiedad

Matriz de direcciones TCP/IP, en notación decimal con puntos.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>     |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **NULL.**<br/>        |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMHostInfo se define como \_ 5b5cf343-05ad-453b-be99-adf4e27b2ebc<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

