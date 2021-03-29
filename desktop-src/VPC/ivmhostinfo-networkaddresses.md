---
title: Propiedad IVMHostInfo NetworkAddresses (VPCCOMInterfaces. h)
description: Recupera una colección enumerable de direcciones TCP/IP en el equipo host.
ms.assetid: 94716b82-8f35-4702-873d-64507d879dc3
keywords:
- Propiedad NetworkAddresses Virtual PC
- Propiedad NetworkAddresses Virtual PC, interfaz IVMHostInfo
- Interfaz IVMHostInfo Virtual PC, propiedad NetworkAddresses
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
ms.openlocfilehash: 824bedf8433c1025e1f4afc1e624c27606b8d0d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421893"
---
# <a name="ivmhostinfonetworkaddresses-property"></a>IVMHostInfo:: NetworkAddresses (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera una colección enumerable de direcciones TCP/IP en el equipo host.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_NetworkAddresses(
  [out, retval] VARIANT *hostAddresses
);
```



## <a name="property-value"></a>Valor de propiedad

Una matriz de direcciones TCP/IP, en notación decimal con puntos.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>     |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **null**.<br/>        |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHostInfo se define como 5b5cf343-05ad-453b-be99-adf4e27b2ebc<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

