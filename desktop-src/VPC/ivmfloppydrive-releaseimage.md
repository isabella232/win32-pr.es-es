---
title: Método IVMFstonepyDrive ReleaseImage (VPCCOMInterfaces.h)
description: Libera una imagen de disquete en el host desde la unidad de disquete.
ms.assetid: 12fc6dc4-8450-4122-b0f0-ed11cc10134c
keywords:
- ReleaseImage, método Virtual PC
- Método ReleaseImage virtual PC, interfaz IVMFstonepyDrive
- IVMFstonepyDrive interface Virtual PC , método ReleaseImage
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ReleaseImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 253e62ec35ccca5a254c6e70ef7fd1890fb6c1a52848c84d319686e0726a038d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654055"
---
# <a name="ivmfloppydrivereleaseimage-method"></a>IVMFstonepyDrive::ReleaseImage (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Libera una imagen de disquete en el host desde la unidad de disquete.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReleaseImage();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                          | Descripción                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                | La operación se realizó correctamente.<br/>                                               |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>          | La configuración de esta máquina virtual no es válida o no se encuentra.<br/> |
| <dl> <dt>**Máquina virtual \_ E \_ MEDIA WRONG TYPE \_ \_ 0xA00400728**</dt> <dt></dt> </dl>  | El medio conectado a esta unidad de disquete no es una imagen de disquete.<br/>         |
| <dl> <dt>**Máquina virtual \_ E \_ NO \_ MEDIA \_ CAPTURED**</dt> <dt>0xA00400652</dt> </dl> | No hay ningún medio conectado a esta unidad de disquete.<br/>                            |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>          | Se produjo un error inesperado.<br/>                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMFstonepyDrive se define como \_ 661abee6-112a-4ed9-tanf-3c874969f10e<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMFstonepyDrive**](ivmfloppydrive.md)
</dt> </dl>

 

