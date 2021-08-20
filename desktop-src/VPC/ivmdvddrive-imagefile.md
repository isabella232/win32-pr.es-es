---
title: Propiedad ImageFile de IVMDVDDrive (VPCCOMInterfaces.h)
description: Recupera la ruta de acceso completa del conjunto de archivos de imagen para este dispositivo.
ms.assetid: e7910d37-d3a5-4291-b374-aaa67db50f1b
keywords:
- ImageFile, propiedad Virtual PC
- Propiedad ImageFile Virtual PC , interfaz IVMDVDDrive
- Interfaz IVMDVDDrive Pc virtual, propiedad ImageFile
topic_type:
- apiref
api_name:
- IVMDVDDrive.ImageFile
- IVMDVDDrive.get_ImageFile
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 275826aaea8dcb4f40427f2448a5edc86a992aefa4dc81648703a5f0a2948604
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123765"
---
# <a name="ivmdvddriveimagefile-property"></a>IVMDVDDrive::ImageFile, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera la ruta de acceso completa del conjunto de archivos de imagen para este dispositivo.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_ImageFile(
  [out, retval] BSTR *imagePath
);
```



## <a name="property-value"></a>Valor de propiedad

Ruta de acceso completa al archivo de imagen.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                            | Significado                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                               | La operación se realizó correctamente.<br/>                                  |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                 | El parámetro es **NULL.**<br/>                                     |
| <dl> <dt>E \_ ERROR</dt> <dt>0x80004005</dt> </dl>                    | Se produjo un error inesperado.<br/>                              |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>         | No se encontró la máquina virtual.<br/>                        |
| <dl> <dt>Máquina virtual \_ E \_ UNIDAD \_ NO VÁLIDA</dt> <dt>0xA0040502</dt> </dl>      | La ubicación del bus para esta unidad no es válida.<br/>                  |
| <dl> <dt>Máquina virtual \_ E \_ MEDIA WRONG TYPE \_ \_ 0xA00400728</dt> <dt></dt> </dl> | El medio capturado por esta unidad de DVD no es un archivo de imagen ISO.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>         | Se produjo un error inesperado.<br/>                              |



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

 

