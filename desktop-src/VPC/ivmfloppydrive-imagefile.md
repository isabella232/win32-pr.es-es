---
title: Propiedad ImageFile de IVMFstoneDrive (VPCCOMInterfaces.h)
description: Recupera la ruta de acceso completa del archivo de imagen al que está conectada la unidad de disquete.
ms.assetid: fc87e438-e5d4-494d-8ac2-27a4312ee81d
keywords:
- ImageFile, propiedad Virtual PC
- Propiedad ImageFile Virtual PC , interfaz IVMFstonepyDrive
- Interfaz IVMFstonepyDrive Pc virtual, propiedad ImageFile
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ImageFile
- IVMFloppyDrive.get_ImageFile
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44c76498d192954dde50e3f997fe91ce405344fc2048697ce996723aa0e6d13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118595125"
---
# <a name="ivmfloppydriveimagefile-property"></a>IVMFstonepyDrive::ImageFile, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera la ruta de acceso completa del archivo de imagen al que está conectada la unidad de disquete.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_ImageFile(
  [out, retval] BSTR *imageFile
);
```



## <a name="property-value"></a>Valor de propiedad

Ruta de acceso completa del archivo de imagen.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>                                               |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **NULL.**<br/>                                                  |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | La configuración de esta máquina virtual no es válida o no se encuentra.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>                                           |



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

 

