---
title: Método _ID IVMVirtualNetwork (VPCCOMInterfaces.h)
description: Recupera el identificador interno de la red virtual.
ms.assetid: 6f1f75be-4218-40b8-8c73-938f0801f5e5
keywords:
- _ID virtual PC
- _ID método Virtual PC , interfaz IVMVirtualNetwork
- IVMVirtualNetwork interface Virtual PC , _ID método
topic_type:
- apiref
api_name:
- IVMVirtualNetwork._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c888a6191be85bf90e9bee2d83590352c3acbf4f731e835fb5879221831b0669
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122665"
---
# <a name="ivmvirtualnetwork_id-method"></a>IVMVirtualNetwork:: \_ método de identificador

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el identificador interno de la red virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT _ID(
  [out] VARIANT *virtualNetworkID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*virtualNetworkID* \[ out\]
</dt> <dd>

Identificador de red virtual. El identificador de la red virtual de redes compartidas (NAT) es 01010101010101010101010101010101.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                 | Descripción                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>     |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **NULL.**<br/>        |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/> |



 

## <a name="remarks"></a>Comentarios

Los lenguajes de scripting no pueden hacer uso de esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualNetwork se define como \_ 431cb7a1-2469-4563-b94e-38b987adca63<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualNetwork**](ivmvirtualnetwork.md)
</dt> </dl>

 

