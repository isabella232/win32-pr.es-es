---
title: Propiedad IVMHardDiskConnection DeviceNumber (VPCCOMInterfaces.h)
description: Recupera el número de dispositivo al que está conectada la imagen de unidad.
ms.assetid: fea8bac6-fb25-495a-bc56-1d517b831f33
keywords:
- DeviceNumber, propiedad Virtual PC
- Propiedad DeviceNumber De PC virtual, interfaz IVMHardDiskConnection
- IVMHardDiskConnection interface Virtual PC , Propiedad DeviceNumber
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.DeviceNumber
- IVMHardDiskConnection.get_DeviceNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3326f0090983e27571b3dce2a5ba72ec1c5efc0a87b837e0fee9e7aac47aa2d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117753354"
---
# <a name="ivmharddiskconnectiondevicenumber-property"></a>IVMHardDiskConnection::D eviceNumber

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el número de dispositivo al que está conectada la imagen de unidad.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_DeviceNumber(
  [out, retval] long *vmDeviceNumber
);
```



## <a name="property-value"></a>Valor de propiedad

Número de dispositivo que corresponde a esta conexión.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                       | Significado                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                          | La operación se realizó correctamente.<br/>                                           |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>            | El parámetro es **NULL** o no es válido.<br/>                                 |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>    | La configuración actual de la máquina virtual no es válida.<br/>                 |
| <dl> <dt>Máquina virtual \_ E \_ UNIDAD \_ NO VÁLIDA</dt> <dt>0xA0040502</dt> </dl> | La ubicación del bus para esta conexión no se ha inicializado correctamente.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>    | Se produjo un error inesperado.<br/>                                       |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMHardDiskconnection se define como \_ aefa36a5-463a-46ae-9e6c-a1fb4e12e671<br/>      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> </dl>

 

