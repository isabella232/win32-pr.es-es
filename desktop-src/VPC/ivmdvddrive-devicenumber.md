---
title: Propiedad IVMDVDDrive DeviceNumber (VPCCOMInterfaces. h)
description: Recupera el número de dispositivo al que está conectada esta unidad.
ms.assetid: 57b09400-e0c8-4ca2-bcd4-e6dd047daf95
keywords:
- Propiedad DeviceNumber Virtual PC
- Propiedad DeviceNumber Virtual PC, interfaz IVMDVDDrive
- Interfaz IVMDVDDrive Virtual PC, propiedad DeviceNumber
topic_type:
- apiref
api_name:
- IVMDVDDrive.DeviceNumber
- IVMDVDDrive.get_DeviceNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de189b162ed2c880819f4c8729e996236ace250a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079509"
---
# <a name="ivmdvddrivedevicenumber-property"></a>IVMDVDDrive::D propiedad eviceNumber

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera el número de dispositivo al que está conectada esta unidad.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_DeviceNumber(
  [out, retval] long *vmDeviceNumber
);
```



## <a name="property-value"></a>Valor de propiedad

El número de dispositivo. Por ejemplo, en un bus IDE, este valor representaría la ubicación principal o secundaria.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                       | Significado                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                          | La operación se realizó correctamente.<br/>                                          |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>            | El parámetro es **null**.<br/>                                             |
| <dl> <dt>Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida</dt> <dt></dt> </dl> | La ubicación del bus para esta unidad de DVD no se ha inicializado correctamente.<br/> |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>    | Se produjo un error inesperado.<br/>                                      |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive se define como b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

