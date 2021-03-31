---
title: Propiedad de tipo IVMHardDisk (VPCCOMInterfaces. h)
description: Tipo de disco duro virtual.
ms.assetid: a855ed9b-a573-471c-ad98-521c80e9ab8c
keywords:
- Propiedad de tipo Virtual PC
- Propiedad Type Virtual PC, interfaz IVMHardDisk
- Interfaz IVMHardDisk Virtual PC, propiedad de tipo
topic_type:
- apiref
api_name:
- IVMHardDisk.Type
- IVMHardDisk.get_Type
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3757d74de5fc99972be3c7d267b15c56da6bee16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079330"
---
# <a name="ivmharddisktype-property"></a>IVMHardDisk:: Type (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera el tipo del disco duro virtual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Type(
  [out, retval] VMHardDiskType *type
);
```



## <a name="property-value"></a>Valor de propiedad

El tipo de la imagen de disco duro actual.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                               | Significado                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                                                  | La operación se realizó correctamente.<br/>                                                  |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>                                    | El parámetro es **null**.<br/>                                                     |
| <dl> <dt>HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró el archivo de error)</dt> <dt>0x80070002</dt> </dl> | No se encontró el archivo de imagen de disco duro actual.<br/>                           |
| <dl> <dt>Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida</dt> <dt></dt> </dl>                         | El tipo de la imagen de disco duro actual no es válido.<br/>                            |
| <dl> <dt>Máquina virtual \_ E \_ HD \_ Image \_ Open \_ FAIL</dt> <dt>0xA004067C</dt> </dl>                  | Se produjo un error al intentar abrir el archivo de imagen de disco duro actual.<br/>   |
| <dl> <dt>Máquina virtual \_ E 0xA0040681 de \_ \_ \_ acceso a imágenes HD</dt> <dt></dt> </dl>                      | Error al intentar obtener acceso al archivo de imagen de disco duro actual.<br/> |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>                            | Se produjo un error inesperado.<br/>                                              |



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

 

