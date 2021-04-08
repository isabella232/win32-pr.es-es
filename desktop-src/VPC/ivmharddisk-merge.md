---
title: Método Merge de IVMHardDisk (VPCCOMInterfaces. h)
description: Combina un disco duro virtual de diferenciación con su imagen de disco principal.
ms.assetid: e2aca4d3-79c1-416a-b135-f4680c03d200
keywords:
- Merge Method Virtual PC
- Merge Method Virtual PC, interfaz IVMHardDisk
- Interfaz IVMHardDisk Virtual PC, método Merge
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
ms.openlocfilehash: bb5e4b32cb1df2f754463cee7f8275b00f86513b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996586"
---
# <a name="ivmharddiskmerge-method"></a>IVMHardDisk:: Merge (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Combina un disco duro virtual de diferenciación con su imagen de disco principal.

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

Objeto [**IVMTask**](ivmtask.md) que se usa para realizar el seguimiento de la finalización del proceso de combinación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                              | Descripción                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                                    | La operación se realizó correctamente.<br/>                                                                                                                                                                                          |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                                      | El parámetro es **null**.<br/>                                                                                                                                                                                             |
| <dl> <dt>**HRESULT \_ De \_ Win32 ( \_ \_ infracción de uso compartido de errores)**</dt> <dt>0x80070020</dt> </dl> | La imagen de disco duro virtual a la que hace referencia este objeto [**IVMHardDisk**](ivmharddisk.md) está en uso o el elemento primario de esta imagen de disco duro virtual está en uso. O bien, estas imágenes de disco duro podrían formar parte de un estado guardado.<br/> |
| <dl> <dt>**Máquina virtual \_ E es el \_ \_ \_ \_ tipo de imagen HD**</dt> <dt>0xA004067B</dt> </dl>                   | La imagen de disco duro virtual a la que hace referencia este objeto [**IVMHardDisk**](ivmharddisk.md) debe ser una imagen de disco de diferenciación.<br/>                                                                                            |
| <dl> <dt>**Máquina virtual \_ E & 0xA004067A de \_ \_ \_ solo lectura de archivos**</dt> <dt></dt> </dl>                         | El elemento primario de la imagen de disco duro virtual al que hace referencia este objeto [**IVMHardDisk**](ivmharddisk.md) está marcado como de solo lectura.<br/>                                                                                             |
| <dl> <dt>**Máquina virtual \_ \_ \_ \_ No \_ se encontró la ruta de acceso principal E**</dt> <dt>0xA0040677</dt> </dl>                 | No existe el elemento primario del disco duro virtual al que hace referencia este objeto [**IVMHardDisk**](ivmharddisk.md) .<br/>                                                                                                       |
| <dl> <dt>**Máquina virtual \_ E \_ \_ \_**</dt> <dt>0xA0040209</dt> de la aplicación </dl>                      | No se puede fusionar mediante combinación la imagen de disco duro virtual porque se está cerrando.<br/>                                                                                                                                 |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                              | Se produjo un error inesperado.<br/>                                                                                                                                                                                      |



 

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

 

