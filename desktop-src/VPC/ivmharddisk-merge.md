---
title: Método IVMHardDisk Merge (VPCCOMInterfaces.h)
description: Combina un disco duro virtual de diferenciación con su imagen de disco primario.
ms.assetid: e2aca4d3-79c1-416a-b135-f4680c03d200
keywords:
- Método de combinación Virtual PC
- Método de combinación Virtual PC , interfaz IVMHardDisk
- IVMHardDisk interface Virtual PC , Método Merge
topic_type:
- apiref
api_name:
- IVMHardDisk.Merge
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b1683b5a44d8418dc247dddcfde52b369c293484e5c3b19c139fe25521ac6c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998945"
---
# <a name="ivmharddiskmerge-method"></a>IVMHardDisk::Merge (Método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Combina un disco duro virtual de diferenciación con su imagen de disco primario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Merge(
  [out, retval] IVMTask **mergeTask
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mergeTask* \[ out, retval\]
</dt> <dd>

Objeto [**IVMTask**](ivmtask.md) que se usa para realizar un seguimiento de la finalización del proceso de combinación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                              | Descripción                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                                    | La operación se realizó correctamente.<br/>                                                                                                                                                                                          |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                      | El parámetro es **NULL.**<br/>                                                                                                                                                                                             |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ SHARING \_ VIOLATION) 0X80070020**</dt> <dt></dt> </dl> | La imagen de disco duro virtual a la que hace referencia este objeto [**IVMHardDisk**](ivmharddisk.md) está en uso o el elemento primario de esta imagen de disco duro virtual está en uso. O bien, estas imágenes de disco duro podrían formar parte de un estado guardado.<br/> |
| <dl> <dt>**Máquina virtual \_ E \_ ERROR DE TIPO DE \_ \_ \_ IMAGEN**</dt> <dt>DE HD 0xA004067B</dt> </dl>                   | La imagen de disco duro virtual a la que hace referencia [**este objeto IVMHardDisk**](ivmharddisk.md) debe ser una imagen de disco de diferenciación.<br/>                                                                                            |
| <dl> <dt>**Máquina virtual \_ E \_ FILE \_ READ \_ ONLY**</dt> <dt>0xA004067A</dt> </dl>                         | El elemento primario de la imagen de disco duro virtual a la que hace referencia este [**objeto IVMHardDisk**](ivmharddisk.md) se marca como de solo lectura.<br/>                                                                                             |
| <dl> <dt>**Máquina virtual \_ NO \_ SE ENCONTRÓ LA RUTA DE \_ \_ \_ ACCESO**</dt> <dt>PRIMARIA 0XA0040677</dt> </dl>                 | El elemento primario del disco duro virtual al que hace referencia este [**objeto IVMHardDisk**](ivmharddisk.md) no existe.<br/>                                                                                                       |
| <dl> <dt>**Máquina virtual \_ E \_ APP \_ SHUTTING \_ DOWN**</dt> <dt>0xA0040209</dt> </dl>                      | La imagen de disco duro virtual no se puede combinar porque la aplicación se está cerrando.<br/>                                                                                                                                 |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                              | Se produjo un error inesperado.<br/>                                                                                                                                                                                      |



 

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

 

