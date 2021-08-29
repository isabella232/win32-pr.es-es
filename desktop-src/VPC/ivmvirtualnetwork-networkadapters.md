---
title: Propiedad IVMVirtualNetwork NetworkAdapters (VPCCOMInterfaces.h)
description: Recupera una colección enumerable de NIC conectadas a la red virtual.
ms.assetid: d5b95831-4642-441e-93e8-34e125087a43
keywords:
- Equipo virtual de la propiedad NetworkAdapters
- Propiedad NetworkAdapters Pc virtual, interfaz IVMVirtualNetwork
- IVMVirtualNetwork interface Virtual PC , Propiedad NetworkAdapters
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.NetworkAdapters
- IVMVirtualNetwork.get_NetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76cbcf6a4c1f4aeb5f7c16d1e3a25a0081e664f0b3d71708fd85c6b457acb1b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122635"
---
# <a name="ivmvirtualnetworknetworkadapters-property"></a>IVMVirtualNetwork::NetworkAdapters, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera una colección enumerable de NIC conectadas a la red virtual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_NetworkAdapters(
  [out, retval] IVMNetworkAdapterCollection **networkInterfaceCollection
);
```



## <a name="property-value"></a>Valor de propiedad

Nuevo [**IVMNetworkAdapterCollection que**](ivmnetworkadaptercollection.md) contiene las NIC virtuales asociadas a esta red virtual.

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
| IID<br/>                      | IID IVMVirtualNetwork se define como \_ 431cb7a1-2469-4563-b94e-38b987adca63<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualNetwork**](ivmvirtualnetwork.md)
</dt> </dl>

 

