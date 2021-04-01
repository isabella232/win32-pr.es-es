---
title: Propiedad IVMDVDDrive ImageFile (VPCCOMInterfaces. h)
description: Recupera la ruta de acceso completa del conjunto de archivos de imagen para este dispositivo.
ms.assetid: e7910d37-d3a5-4291-b374-aaa67db50f1b
keywords:
- ImageFile (propiedad, equipo virtual)
- ImageFile (propiedad, Virtual PC, interfaz IVMDVDDrive)
- Interfaz IVMDVDDrive Virtual PC, propiedad ImageFile
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
ms.openlocfilehash: 7c71ed5328e41a72c9896147c6dcd824b2bd2ab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905560"
---
# <a name="ivmdvddriveimagefile-property"></a>IVMDVDDrive:: ImageFile (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                               | La operación se realizó correctamente.<br/>                                  |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>                 | El parámetro es **null**.<br/>                                     |
| <dl> <dt>E \_ ERROR</dt> <dt>0x80004005</dt> </dl>                    | Se produjo un error inesperado.<br/>                              |
| <dl> <dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt> </dl>         | No se encontró la máquina virtual.<br/>                        |
| <dl> <dt>Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida</dt> <dt></dt> </dl>      | La ubicación del bus para esta unidad no es válida.<br/>                  |
| <dl> <dt>Máquina virtual \_ E \_ medio \_ de \_ tipo incorrecto</dt> <dt>0xA00400728</dt> </dl> | El medio capturado por esta unidad de DVD no es un archivo de imagen ISO.<br/> |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>         | Se produjo un error inesperado.<br/>                              |



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

 

