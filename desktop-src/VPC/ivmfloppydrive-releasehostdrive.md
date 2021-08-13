---
title: Método IVMFstonepyDrive ReleaseHostDrive (VPCCOMInterfaces.h)
description: Libera una unidad física en el host desde el disquete.
ms.assetid: 6d5a8e7c-684c-42bc-84e5-76d3e761b7f0
keywords:
- ReleaseHostDrive, método Virtual PC
- Método ReleaseHostDrive Virtual PC , interfaz IVMFstonepyDrive
- IVMFstonepyDrive interface Virtual PC , ReleaseHostDrive (método)
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ReleaseHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b44202754528483f88ab045b848e83a6a41a318b1e1ffed6122c2a2ac971237c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594851"
---
# <a name="ivmfloppydrivereleasehostdrive-method"></a>IVMFstonepyDrive::ReleaseHostDrive (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Libera una unidad física en el host desde el disquete.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReleaseHostDrive();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                          | Descripción                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                | La operación se realizó correctamente.<br/>                                               |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>          | La configuración de esta máquina virtual no es válida o no se encuentra.<br/> |
| <dl> <dt>**Máquina virtual \_ E \_ MEDIA WRONG TYPE \_ \_ 0xA00400728**</dt> <dt></dt> </dl>  | El medio conectado a esta unidad de disquete no es una unidad de disquete física.<br/>     |
| <dl> <dt>**Máquina virtual \_ E \_ NO \_ SE \_ CAPTURARON MEDIOS**</dt> <dt>0xA00400652</dt> </dl> | No hay ningún medio conectado a esta unidad de disquete.<br/>                            |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>          | Se produjo un error inesperado.<br/>                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMFstonepyDrive se define como \_ 661abee6-112a-4ed9-tanf-3c874969f10e<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMFstonepyDrive**](ivmfloppydrive.md)
</dt> </dl>

 

