---
title: Propiedad BusNumber de IVMDVDDrive (VPCCOMInterfaces.h)
description: Recupera el número de bus al que está conectado este dispositivo.
ms.assetid: 8edc94da-22bc-4141-a6c7-1b18cca754fc
keywords:
- BusNumber, propiedad Virtual PC
- Interfaz IVMDVDDrive de la propiedad BusNumber de Virtual PC
- Interfaz IVMDVDDrive Pc virtual, propiedad BusNumber
topic_type:
- apiref
api_name:
- IVMDVDDrive.BusNumber
- IVMDVDDrive.get_BusNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 420a3ebdb2f4b4d04532e387c0466a2938e2e51c9ffafac3b975862cddb11169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136828"
---
# <a name="ivmdvddrivebusnumber-property"></a>IVMDVDDrive::BusNumber, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el número de bus al que está conectado este dispositivo.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_BusNumber(
  [out, retval] long *vmBusNumber
);
```



## <a name="property-value"></a>Valor de propiedad

Número de bus. Por ejemplo, en un bus IDE, este valor representaría la ubicación principal o secundaria.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                       | Significado                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                          | La operación se realizó correctamente.<br/>                                          |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>            | El parámetro es **NULL.**<br/>                                             |
| <dl> <dt>Máquina virtual \_ E \_ UNIDAD \_ NO VÁLIDA</dt> <dt>0xA0040502</dt> </dl> | La ubicación del bus de esta unidad de DVD no se ha inicializado correctamente.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>    | Se produjo un error inesperado.<br/>                                      |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMDVDDrive se define como \_ b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

