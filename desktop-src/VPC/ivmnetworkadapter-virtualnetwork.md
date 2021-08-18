---
title: Propiedad IVMNetworkAdapter VirtualNetwork (VPCCOMInterfaces.h)
description: Recupera la red virtual a la que está conectada la interfaz de red.
ms.assetid: 7f52fd86-5f83-41d8-ba48-7db65e9c357c
keywords:
- VirtualNetwork, propiedad Virtual PC
- Propiedad VirtualNetwork Virtual PC , interfaz IVMNetworkAdapter
- Interfaz IVMNetworkAdapter Pc virtual, propiedad VirtualNetwork
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.VirtualNetwork
- IVMNetworkAdapter.get_VirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1bc3a3d58553d403f5e0ca6a8decbcbd3369b48450e9ec190b2f42f83de57e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136618"
---
# <a name="ivmnetworkadaptervirtualnetwork-property"></a>IVMNetworkAdapter::VirtualNetwork, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera la red virtual a la que está conectada la interfaz de red.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_VirtualNetwork(
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="property-value"></a>Valor de propiedad

Interfaz [**IVMVirtualNetwork**](ivmvirtualnetwork.md) que representa la red virtual a la que está asociada esta interfaz de red virtual.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                       | Significado                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                          | La operación se realizó correctamente.<br/>                                                  |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                            | El parámetro es **NULL.**<br/>                                                     |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                                       | Esta interfaz de red está desconectada y no está conectada a una red virtual.<br/> |
| <dl> <dt>Máquina virtual \_ E IDENTIFICADOR \_ DE \_ RED VIRTUAL \_ \_ NO</dt> <dt>VÁLIDO 0xA00400702</dt> </dl> | Esta interfaz está conectada a una red virtual con un identificador no válido.<br/>           |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                    | Se produjo un error inesperado.<br/>                                              |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMNetworkAdapter se define como \_ e32e4165-22b8-4dc0-8d57-850171ae207a<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> </dl>

 

