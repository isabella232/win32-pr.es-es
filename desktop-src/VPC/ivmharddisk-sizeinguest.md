---
title: Propiedad IVMHardDisk SizeInGuest (VPCCOMInterfaces. h)
description: Recupera el tamaño del disco duro virtual en el sistema operativo invitado.
ms.assetid: 895598db-cd54-414c-8783-13102cfbd453
keywords:
- Propiedad SizeInGuest Virtual PC
- Propiedad SizeInGuest Virtual PC, interfaz IVMHardDisk
- Interfaz IVMHardDisk Virtual PC, propiedad SizeInGuest
topic_type:
- apiref
api_name:
- IVMHardDisk.SizeInGuest
- IVMHardDisk.get_SizeInGuest
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace142bf7c0dc612de47c8b2cb043ce24d6e9e9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150698"
---
# <a name="ivmharddisksizeinguest-property"></a>IVMHardDisk:: SizeInGuest (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera el tamaño del disco duro virtual en el sistema operativo invitado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_SizeInGuest(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a>Valor de propiedad

Tamaño, en bytes, de la imagen del disco duro. Este valor es una **variante** de tipo VT \_ decimal.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                               | Significado                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                                                  | La operación se realizó correctamente.<br/>                                                  |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>                                    | El parámetro es **null**.<br/>                                                     |
| <dl> <dt>HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró el archivo de error)</dt> <dt>0x80070002</dt> </dl> | No se encontró el archivo del disco duro virtual actual.<br/>                         |
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

 

