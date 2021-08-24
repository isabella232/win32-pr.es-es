---
title: Propiedad primaria IVMHardDisk (VPCCOMInterfaces.h)
description: Elemento primario del disco duro virtual de diferenciación.
ms.assetid: 9a400fa0-ee0d-4474-a410-82756ea544fe
keywords:
- Equipo virtual de la propiedad primaria
- Propiedad primaria Virtual PC , interfaz IVMHardDisk
- IVMHardDisk interface Virtual PC , Parent property
topic_type:
- apiref
api_name:
- IVMHardDisk.Parent
- IVMHardDisk.get_Parent
- IVMHardDisk.put_Parent
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e0ba8d56ad09f7c8263e41b17d2e107a0a441408d22ffb604e95055c57fb21d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119472105"
---
# <a name="ivmharddiskparent-property"></a>IVMHardDisk::P arent

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera y establece el elemento primario del disco duro virtual de diferenciación.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Parent(
  [in]          IVMHardDisk *parent
);

HRESULT get_Parent(
  [out, retval] IVMHardDisk **parent
);
```



## <a name="property-value"></a>Valor de propiedad

Establece el [**objeto IVMHardDisk**](ivmharddisk.md) asociado a la imagen de disco duro principal.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                                  | La operación se realizó correctamente.<br/>                                                                                                                                                                                                                                              |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                                    | El parámetro es **NULL.**<br/>                                                                                                                                                                                                                                                 |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                                               | No se trata de un disco duro de diferenciación, por lo que no tiene ningún elemento primario.<br/>                                                                                                                                                                                                                 |
| <dl> <dt>HRESULT \_ DESDE \_ WIN32(ARCHIVO DE ERROR \_ \_ NO \_ ENCONTRADO)</dt> <dt>0X80070002</dt> </dl> | El sistema no encontró el archivo de disco duro virtual primario.<br/>                                                                                                                                                                                                               |
| <dl> <dt>HRESULT \_ DESDE \_ WIN32(RUTA DE ACCESO DE ERROR \_ \_ NO \_ ENCONTRADA)</dt> <dt>0X80070003</dt> </dl> | El sistema no pudo encontrar la ruta de acceso al archivo de disco duro virtual primario.<br/>                                                                                                                                                                                                   |
| <dl> <dt>Máquina virtual \_ E \_ ERROR AL ABRIR LA \_ \_ IMAGEN \_ </dt> DE HD <dt>0XA004067C</dt> </dl>                  | Error al intentar abrir el archivo de imagen del disco duro actual.<br/>                                                                                                                                                                                               |
| <dl> <dt>Máquina virtual \_ E \_ HD IMAGE ACCESS \_ \_ 0xA0040681</dt> <dt></dt> </dl>                      | Error al intentar acceder al archivo de imagen de disco duro actual.<br/>                                                                                                                                                                                             |
| <dl> <dt>Máquina virtual \_ ERROR \_ DE COINCIDENCIA DE \_ \_ ID. \_ </dt> DE ELEMENTO PRIMARIO <dt>0XA0040685</dt> </dl>            | La imagen de disco duro virtual ubicada por el *parámetro* primario no tiene el mismo identificador que la imagen de disco secundario. Asegúrese de que la imagen de  disco duro virtual primaria ubicada por el parámetro primario es la misma imagen que se usa para crear la imagen de disco duro virtual de diferenciación.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                            | Se produjo un error inesperado.<br/>                                                                                                                                                                                                                                          |



## <a name="remarks"></a>Comentarios

Esta propiedad solo es válida con diferentes imágenes de disco duro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMHardDisk se define como \_ ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

