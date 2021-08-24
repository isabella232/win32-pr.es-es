---
title: Método IVMDVDDrive AttachHostDrive (VPCCOMInterfaces.h)
description: Conecta una unidad host a la unidad de DVD dentro de la máquina virtual.
ms.assetid: 68e658ba-470c-452c-8124-5bb2ec81911b
keywords:
- Pc virtual del método AttachHostDrive
- Método AttachHostDrive Virtual PC , interfaz IVMDVDDrive
- IVMDVDDrive interface Virtual PC , Método AttachHostDrive
topic_type:
- apiref
api_name:
- IVMDVDDrive.AttachHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c82229488ebb705cab1a684a207f973356d2d43177c4123ae4f456b55fbe6840
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136858"
---
# <a name="ivmdvddriveattachhostdrive-method"></a>IVMDVDDrive::AttachHostDrive (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Conecta una unidad host a la unidad de DVD dentro de la máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AttachHostDrive(
  [in] BSTR driveLetter
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*driveLetter* \[ En\]
</dt> <dd>

Letra de la unidad host que se va a adjuntar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                    | Descripción                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                          | La operación se realizó correctamente.<br/>                                                                                                                                             |
| <dl> <dt>**E \_ Invalidarg**</dt> <dt>0x80000003</dt> </dl>         | No se especificó ninguna letra de unidad o la letra de unidad especificada no es válida.<br/>                                                                                                  |
| <dl> <dt>**E \_ ERROR**</dt> <dt>0x80004005</dt> </dl>               | Se produjo un error inesperado.<br/>                                                                                                                                         |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>    | No se encontró la máquina virtual.<br/>                                                                                                                                   |
| <dl> <dt>**Máquina virtual \_ E \_ UNIDAD EN USO \_ \_ 0xA0040727**</dt> <dt></dt> </dl> | Ya hay una unidad de DVD de host o una imagen ISO conectada a esta unidad dentro de la máquina virtual, o bien la unidad host especificada ya está en uso dentro de otra máquina virtual.<br/> |
| <dl> <dt>**Máquina virtual \_ E \_ UNIDAD \_ NO VÁLIDA**</dt> <dt>0xA0040502</dt> </dl> | La ubicación del bus para esta unidad no es válida o la unidad no parece ser una unidad de DVD válida.<br/>                                                                         |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>    | Se produjo un error inesperado.<br/>                                                                                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMDVDDrive se define como \_ b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

