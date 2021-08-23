---
title: Propiedad IVMDVDDrive HostDriveLetter (VPCCOMInterfaces.h)
description: Letra del conjunto de unidades host para este dispositivo.
ms.assetid: e17f707f-e1cf-4302-a69e-caa5829df1af
keywords:
- HostDriveLetter, propiedad Virtual PC
- Propiedad HostDriveLetter Pc virtual, interfaz IVMDVDDrive
- Interfaz IVMDVDDrive Pc virtual, propiedad HostDriveLetter
topic_type:
- apiref
api_name:
- IVMDVDDrive.HostDriveLetter
- IVMDVDDrive.get_HostDriveLetter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eb9105ec970331a755881d7f5b1425cf43c58f5267f5970042ce64b458070a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056873"
---
# <a name="ivmdvddrivehostdriveletter-property"></a>Propiedad IVMDVDDrive::HostDriveLetter

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera la letra del conjunto de unidades host para este dispositivo.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_HostDriveLetter(
  [out, retval] BSTR *driveLetter
);
```



## <a name="property-value"></a>Valor de propiedad

Letra de unidad.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                            | Significado                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                               | La operación se realizó correctamente.<br/>                             |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                 | El parámetro es **NULL.**<br/>                                |
| <dl> <dt>E \_ ERROR</dt> <dt>0x80004005</dt> </dl>                    | Se produjo un error inesperado.<br/>                         |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>         | No se encontró la máquina virtual.<br/>                   |
| <dl> <dt>Máquina virtual \_ E \_ MEDIA WRONG TYPE \_ \_ 0xA00400728</dt> <dt></dt> </dl> | El medio capturado por esta unidad de DVD no es una unidad host.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>         | Se produjo un error inesperado.<br/>                         |



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

 

