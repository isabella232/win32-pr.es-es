---
title: Método compacto IVMHardDisk (VPCCOMInterfaces. h)
description: Compacta una imagen de disco duro virtual de expansión dinámica.
ms.assetid: bd3ec493-1bc0-4c28-8b41-56beac3d0d6d
keywords:
- Método compacto Virtual PC
- Método compacto Virtual PC, interfaz IVMHardDisk
- Interfaz IVMHardDisk Virtual PC, método compacto
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
ms.openlocfilehash: 51b28b47709fdf956b679a4f16c50adde4a1b335
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803584"
---
# <a name="ivmharddiskcompact-method"></a>IVMHardDisk:: Compact (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Compacta una imagen de disco duro virtual de expansión dinámica.

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

Un objeto [**IVMTask**](ivmtask.md) que se usa para realizar el seguimiento de la finalización del proceso de compactación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                              | Descripción                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                                    | La operación se realizó correctamente.<br/>                                                                                                        |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                              | Se produjo un error inesperado.<br/>                                                                                                    |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                                      | El parámetro es **null**.<br/>                                                                                                           |
| <dl> <dt>**HRESULT \_ De \_ Win32 ( \_ \_ infracción de uso compartido de errores)**</dt> <dt>0x80070020</dt> </dl> | La imagen de disco duro virtual a la que hace referencia este objeto [**IVMHardDisk**](ivmharddisk.md) está en uso.<br/>                                  |
| <dl> <dt>**HRESULT \_ DE \_ Win32 (error de \_ disco \_ lleno)**</dt> <dt>0x80070070</dt> </dl>         | El volumen del host no tiene espacio suficiente para crear un archivo temporal necesario para la compactación de esta imagen de disco duro virtual.<br/>     |
| <dl> <dt>**Máquina virtual \_ E \_ \_ \_**</dt> <dt>0xA0040209</dt> de la aplicación </dl>                      | La imagen del disco duro virtual no se puede compactar porque la aplicación se está cerrando.<br/>                                            |
| <dl> <dt>**Máquina virtual \_ E & 0xA004067A de \_ \_ \_ solo lectura de archivos**</dt> <dt></dt> </dl>                         | La imagen de disco duro virtual a la que hace referencia este objeto [**IVMHardDisk**](ivmharddisk.md) se marca como de solo lectura.<br/>                     |
| <dl> <dt>**Máquina virtual \_ E es el \_ \_ \_ \_ tipo de imagen HD**</dt> <dt>0xA004067B</dt> </dl>                   | La imagen de disco duro virtual a la que hace referencia este objeto [**IVMHardDisk**](ivmharddisk.md) debe ser un tipo de imagen **vmDiskTypeDynamic** .<br/> |
| <dl> <dt>**Máquina virtual \_ E 0xA0040682 de \_ \_ \_ archivo HD no válido**</dt> <dt></dt> </dl>                        | Parece que la imagen de disco duro virtual a la que hace referencia este objeto [**IVMHardDisk**](ivmharddisk.md) no es una imagen válida.<br/>          |



 

## <a name="remarks"></a>Observaciones

Para compactar una imagen de disco duro de expansión dinámica, el espacio libre en la imagen de disco debe ser cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk se define como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

