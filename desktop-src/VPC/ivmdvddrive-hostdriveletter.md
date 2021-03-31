---
title: Propiedad IVMDVDDrive HostDriveLetter (VPCCOMInterfaces. h)
description: La letra de la unidad de host establecida para este dispositivo.
ms.assetid: e17f707f-e1cf-4302-a69e-caa5829df1af
keywords:
- Propiedad HostDriveLetter Virtual PC
- Propiedad HostDriveLetter Virtual PC, interfaz IVMDVDDrive
- Interfaz IVMDVDDrive Virtual PC, propiedad HostDriveLetter
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
ms.openlocfilehash: d60d2599b8fb73e727100111dc37d29a9d13c5d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801970"
---
# <a name="ivmdvddrivehostdriveletter-property"></a>IVMDVDDrive:: HostDriveLetter (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera la letra de la unidad de host establecida para este dispositivo.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_HostDriveLetter(
  [out, retval] BSTR *driveLetter
);
```



## <a name="property-value"></a>Valor de propiedad

Letra de la unidad.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                            | Significado                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                               | La operación se realizó correctamente.<br/>                             |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>                 | El parámetro es **null**.<br/>                                |
| <dl> <dt>E \_ ERROR</dt> <dt>0x80004005</dt> </dl>                    | Se produjo un error inesperado.<br/>                         |
| <dl> <dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt> </dl>         | No se encontró la máquina virtual.<br/>                   |
| <dl> <dt>Máquina virtual \_ E \_ medio \_ de \_ tipo incorrecto</dt> <dt>0xA00400728</dt> </dl> | El medio capturado por esta unidad de DVD no es una unidad de host.<br/> |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>         | Se produjo un error inesperado.<br/>                         |



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

 

