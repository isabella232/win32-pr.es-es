---
title: Propiedad IVMUSBDevice AttachedToVM (VPCCOMInterfaces. h)
description: Recupera el nombre de la máquina virtual a la que está conectado el dispositivo USB.
ms.assetid: 214ed891-1fca-4311-945a-0ce3d05d604e
keywords:
- Propiedad AttachedToVM Virtual PC
- Propiedad AttachedToVM Virtual PC, interfaz IVMUSBDevice
- Interfaz IVMUSBDevice Virtual PC, propiedad AttachedToVM
topic_type:
- apiref
api_name:
- IVMUSBDevice.AttachedToVM
- IVMUSBDevice.get_AttachedToVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c64e265cba81858bc887cbf595426bffd1b604aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079440"
---
# <a name="ivmusbdeviceattachedtovm-property"></a>IVMUSBDevice:: AttachedToVM (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera el nombre de la máquina virtual a la que está conectado el dispositivo USB.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_AttachedToVM(
  [out, retval] BSTR *ConfigName
);
```



## <a name="property-value"></a>Valor de propiedad

El nombre de la máquina virtual (VM).

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                           | Significado                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                              | El dispositivo está conectado a la máquina virtual y se devuelve su nombre.<br/> |
| <dl> <dt>S \_ FALSO</dt> <dt>1</dt> </dl>                           | El dispositivo está conectado al host.<br/>                         |
| <dl> <dt>Máquina virtual \_ E 0xA00400929 de \_ \_ \_ máquina virtual externa USB</dt> <dt></dt> </dl> | El dispositivo está conectado a una máquina virtual en otra sesión de usuario.<br/>     |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>                | El parámetro es **null**.<br/>                                  |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMUSBDevice se define como 63C1258C-5721-4070-B86B-A6CE2AFEC0B3<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> </dl>

 

