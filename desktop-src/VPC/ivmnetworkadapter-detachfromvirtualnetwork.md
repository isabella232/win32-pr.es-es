---
title: Método IVMNetworkAdapter DetachFromVirtualNetwork (VPCCOMInterfaces.h)
description: Desasoja la interfaz de red de su red virtual.
ms.assetid: f1a00ea2-2b79-4b5c-a4bd-3cab66deb0d0
keywords:
- DetachFromVirtualNetwork, método Virtual PC
- Método DetachFromVirtualNetwork De Virtual PC , interfaz IVMNetworkAdapter
- IVMNetworkAdapter interface Virtual PC , Método DetachFromVirtualNetwork
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.DetachFromVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abb97c0b2bad30cb05302b67b1b5d0569b13b4c007b79163f1ce63750b512179
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117938476"
---
# <a name="ivmnetworkadapterdetachfromvirtualnetwork-method"></a>IVMNetworkAdapter::D etachFromVirtualNetwork (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Desasoja la interfaz de red de su red virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DetachFromVirtualNetwork();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                 | Descripción                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>     |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

