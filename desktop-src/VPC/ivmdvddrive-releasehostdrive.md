---
title: Método IVMDVDDrive ReleaseHostDrive (VPCCOMInterfaces.h)
description: Libera una unidad host capturada de la unidad de DVD.
ms.assetid: 88bbe364-0c39-40c2-89e7-22ffd66259a2
keywords:
- Equipo virtual del método ReleaseHostDrive
- Método ReleaseHostDrive Para PC virtual, interfaz IVMDVDDrive
- IVMDVDDrive interface Virtual PC , Método ReleaseHostDrive
topic_type:
- apiref
api_name:
- IVMDVDDrive.ReleaseHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 865b9aa54304d8ddacacf048825d6c9767347f341d31524cbd4dd60d7060ae4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136808"
---
# <a name="ivmdvddrivereleasehostdrive-method"></a>IVMDVDDrive::ReleaseHostDrive (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Libera una unidad host capturada de la unidad de DVD.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReleaseHostDrive();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                         | Descripción                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                               | La operación se realizó correctamente.<br/>                                      |
| <dl> <dt>**E \_ Error**</dt> <dt>0x80004005</dt> </dl>                    | Se produjo un error inesperado.<br/>                                  |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>         | No se encontró la máquina virtual.<br/>                            |
| <dl> <dt>**Máquina virtual \_ E \_ MEDIA WRONG TYPE \_ \_ 0xA00400728**</dt> <dt></dt> </dl> | El medio capturado actualmente no es una unidad de disco host.<br/>             |
| <dl> <dt>**Máquina virtual \_ E \_ UNIDAD \_ NO VÁLIDA**</dt> <dt>0xA0040502</dt> </dl>      | No se pudo inicializar la unidad debido a una ubicación de bus no válida.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>         | Se produjo un error inesperado.<br/>                                  |



 

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

 

