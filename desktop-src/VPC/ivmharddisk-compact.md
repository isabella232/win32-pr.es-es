---
title: Método IVMHardDisk Compact (VPCCOMInterfaces.h)
description: Compacta una imagen de disco duro virtual que se expande dinámicamente.
ms.assetid: bd3ec493-1bc0-4c28-8b41-56beac3d0d6d
keywords:
- Pc virtual de método compacto
- Método compacto Virtual PC, interfaz IVMHardDisk
- IVMHardDisk interface Virtual PC , Compact method
topic_type:
- apiref
api_name:
- IVMHardDisk.Compact
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d2ae6c8bcb4237f98c8bcb47089294b202e3e9c45e51351c9818a08e2a295ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119472175"
---
# <a name="ivmharddiskcompact-method"></a>IVMHardDisk::Compact (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Compacta una imagen de disco duro virtual que se expande dinámicamente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Compact(
  [out, retval] IVMTask **compactTask
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*compactTask* \[ out, retval\]
</dt> <dd>

Objeto [**IVMTask que**](ivmtask.md) se usa para realizar un seguimiento de la finalización del proceso de compactación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                              | Descripción                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                                    | La operación se realizó correctamente.<br/>                                                                                                        |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                              | Se produjo un error inesperado.<br/>                                                                                                    |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                      | El parámetro es **NULL.**<br/>                                                                                                           |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(INFRACCIÓN \_ DE USO COMPARTIDO DE \_ ERRORES)**</dt> <dt>0x80070020</dt> </dl> | La imagen de disco duro virtual a la que hace referencia [**este objeto IVMHardDisk**](ivmharddisk.md) está en uso.<br/>                                  |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ DISK \_ FULL)**</dt> <dt>0x80070070</dt> </dl>         | El volumen host no tiene suficiente espacio para crear un archivo temporal necesario para la compactación de esta imagen de disco duro virtual.<br/>     |
| <dl> <dt>**Máquina virtual \_ E \_ APP \_ SHUTTING \_ DOWN**</dt> <dt>0xA0040209</dt> </dl>                      | La imagen de disco duro virtual no se puede compactar porque la aplicación se está cerrando.<br/>                                            |
| <dl> <dt>**Máquina virtual \_ E \_ FILE \_ READ \_ ONLY**</dt> <dt>0xA004067A</dt> </dl>                         | La imagen de disco duro virtual a la que hace referencia este [**objeto IVMHardDisk**](ivmharddisk.md) se marca como de solo lectura.<br/>                     |
| <dl> <dt>**Máquina virtual \_ E \_ ERROR DE TIPO DE \_ \_ \_ IMAGEN**</dt> <dt>DE HD 0xA004067B</dt> </dl>                   | La imagen de disco duro virtual a la que hace referencia este [**objeto IVMHardDisk**](ivmharddisk.md) debe ser un tipo de imagen **vmDiskTypeDynamic.**<br/> |
| <dl> <dt>**Máquina virtual \_ E \_ ARCHIVOS HD NO \_ \_ VÁLIDOs**</dt> <dt>0xA0040682</dt> </dl>                        | La imagen de disco duro virtual a la que hace referencia este [**objeto IVMHardDisk**](ivmharddisk.md) no parece ser una imagen válida.<br/>          |



 

## <a name="remarks"></a>Observaciones

Para compactar una imagen de disco duro que se expande dinámicamente, el espacio libre en la imagen de disco debe estar primero en cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Product<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMHardDisk se define como \_ ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

