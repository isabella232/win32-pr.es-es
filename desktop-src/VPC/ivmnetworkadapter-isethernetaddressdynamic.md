---
title: Propiedad IVMNetworkAdapter IsEthernetAddressDynamic (VPCCOMInterfaces.h)
description: Determina si la dirección Ethernet se genera dinámicamente.
ms.assetid: 7bd87868-f1d1-48e5-9e1b-04d2126f9dad
keywords:
- IsEthernetAddressDynamic, propiedad Virtual PC
- IsEthernetAddressDynamic, propiedad Virtual PC, interfaz IVMNetworkAdapter
- IVMNetworkAdapter interface Virtual PC , Propiedad IsEthernetAddressDynamic
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.IsEthernetAddressDynamic
- IVMNetworkAdapter.get_IsEthernetAddressDynamic
- IVMNetworkAdapter.put_IsEthernetAddressDynamic
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b186eac69317d0e17bf3c50fbfdb63d5e3e0074a8531b63c635913c31db9c3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136648"
---
# <a name="ivmnetworkadapterisethernetaddressdynamic-property"></a>IVMNetworkAdapter::IsEthernetAddressDynamic, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Determina si la dirección Ethernet se genera dinámicamente.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_IsEthernetAddressDynamic(
  [in]          VARIANT_BOOL isDynamic
);

HRESULT get_IsEthernetAddressDynamic(
  [out, retval] VARIANT_BOOL *isDynamic
);
```



## <a name="property-value"></a>Valor de propiedad

Establezca en VARIANT TRUE si la dirección Ethernet se debe generar \_ dinámicamente y VARIANT \_ FALSE si la dirección Ethernet es estática.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>                                                                                                                             |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **NULL.**<br/>                                                                                                                                |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | No se encontró la máquina virtual. Esto puede ocurrir si la máquina se quitó después de crear el objeto [**IVMNetworkAdapter.**](ivmnetworkadapter.md)<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>                                                                                                                         |



## <a name="remarks"></a>Comentarios

Esta propiedad debe establecerse en **TRUE** (valor predeterminado) para la mayoría de las interfaces de red virtual. Si el software del invitado requiere una dirección Ethernet estática, esta propiedad debe establecerse en **FALSE.**

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

 

