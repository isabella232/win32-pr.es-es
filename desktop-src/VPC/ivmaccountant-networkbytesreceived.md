---
title: Propiedad IVMAccountant NetworkBytesReceived (VPCCOMInterfaces.h)
description: Número total de bytes recibidos por todos los adaptadores de red virtual para esta máquina virtual.
ms.assetid: 6f6b32e6-d99b-405c-a788-ed646b3a7593
keywords:
- NetworkBytesReceived, propiedad Virtual PC
- NetworkBytesReceived, propiedad Virtual PC, interfaz IVMAccountant
- IVMAccountant interface Virtual PC , Propiedad NetworkBytesReceived
topic_type:
- apiref
api_name:
- IVMAccountant.NetworkBytesReceived
- IVMAccountant.get_NetworkBytesReceived
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 483bc038622278e23bd46688fa55695c6b11e91d7b602377ae8eb9ddaeab86c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473755"
---
# <a name="ivmaccountantnetworkbytesreceived-property"></a>Propiedad IVMAccountant::NetworkBytesReceived

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el número total de bytes recibidos por todos los adaptadores de red virtual para esta máquina virtual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_NetworkBytesReceived(
  [out, retval] VARIANT *bytesReceived
);
```



## <a name="property-value"></a>Valor de propiedad

Número total de bytes recibidos. Estos datos se devuelven como **UNA VARIANTE** de tipo **VT \_ DECIMAL.**

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>       |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **NULL.**<br/>          |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                    | La máquina virtual no se está ejecutando.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>   |



## <a name="remarks"></a>Comentarios

Tenga en cuenta que las estadísticas de E/S de red se restablecen a cero cuando una máquina virtual se ha encendido, restablecido o restaurado desde el estado guardado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMAccountant se define como \_ 6376c067-7f57-4d63-b754-06e2e4f51d73<br/>              |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMAccountant**](ivmaccountant.md)
</dt> </dl>

 

