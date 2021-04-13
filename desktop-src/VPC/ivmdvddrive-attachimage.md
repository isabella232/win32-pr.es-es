---
title: Método IVMDVDDrive AttachImage (VPCCOMInterfaces. h)
description: Adjunta una imagen ISO a la unidad de DVD de la máquina virtual.
ms.assetid: 08947898-ca3f-41b6-97a3-52dc6977fc6d
keywords:
- Método AttachImage Virtual PC
- Método AttachImage Virtual PC, interfaz IVMDVDDrive
- Interfaz IVMDVDDrive Virtual PC, método AttachImage
topic_type:
- apiref
api_name:
- IVMDVDDrive.AttachImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58204545e21bd7dbf48d21acbc232b9fc5d1e3b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422559"
---
# <a name="ivmdvddriveattachimage-method"></a>IVMDVDDrive:: AttachImage (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Adjunta una imagen ISO a la unidad de DVD de la máquina virtual (VM).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AttachImage(
  [in] BSTR imagePath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*imagePath* \[ de\]
</dt> <dd>

Ruta de acceso completa a la imagen ISO que se va a adjuntar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                    | Descripción                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                          | La operación se realizó correctamente.<br/>                                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>         | El parámetro *imagePath* es un directorio.<br/>                                                         |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>            | El parámetro *imagePath* es **null**.<br/>                                                            |
| <dl> <dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt> </dl>    | No se encontró la máquina virtual.<br/>                                                                        |
| <dl> <dt>**Máquina virtual \_ \_Unidad E \_ en \_ uso**</dt> <dt>0xA0040727</dt> </dl> | Ya hay una unidad de DVD de host o una imagen ISO conectada a esta unidad.<br/>                                  |
| <dl> <dt>**Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida**</dt> <dt></dt> </dl> | La ubicación del bus para esta unidad no es válida o la unidad no parece ser una unidad de DVD válida.<br/> |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>    | Se produjo un error inesperado.<br/>                                                                 |



 

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

 

