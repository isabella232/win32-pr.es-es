---
title: Propiedad IVMHardDiskConnection UndoHardDisk (VPCCOMInterfaces. h)
description: Recupera un objeto de disco duro correspondiente a la imagen de disco para deshacer de esta conexión.
ms.assetid: 0daec200-0bda-44cf-b97d-b9a179cb63f8
keywords:
- Propiedad UndoHardDisk Virtual PC
- Propiedad UndoHardDisk Virtual PC, interfaz IVMHardDiskConnection
- Interfaz IVMHardDiskConnection Virtual PC, propiedad UndoHardDisk
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.UndoHardDisk
- IVMHardDiskConnection.get_UndoHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0fcbd6535c0cf91e1b42549047c131c1804215c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149863"
---
# <a name="ivmharddiskconnectionundoharddisk-property"></a>IVMHardDiskConnection:: UndoHardDisk (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera un objeto de disco duro correspondiente a la imagen de disco para deshacer de esta conexión.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_UndoHardDisk(
  [out, retval] IVMHardDisk **undoHardDisk
);
```



## <a name="property-value"></a>Valor de propiedad

Un objeto [**IVMHardDisk**](ivmharddisk.md) que describe el disco duro para deshacer asociado a esta conexión.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                               | Significado                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                                                  | La operación se realizó correctamente.<br/>                                                                                                    |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>                            | Se produjo un error inesperado.<br/>                                                                                                |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>                                    | El parámetro es **null** o no es válido.<br/>                                                                                          |
| <dl> <dt>HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró el archivo de error)</dt> <dt>0x80070002</dt> </dl> | No se encontró el disco para deshacer para esta conexión.<br/>                                                                                 |
| <dl> <dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt> </dl>                            | La configuración de máquina virtual actual no es válida.<br/>                                                                          |
| <dl> <dt>Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida</dt> <dt></dt> </dl>                         | La ubicación del bus para esta conexión no se ha inicializado correctamente o el dispositivo en esta ubicación no es un disco duro válido.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDiskconnection se define como aefa36a5-463a-46ae-9e6c-a1fb4e12e671<br/>      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> </dl>

 

