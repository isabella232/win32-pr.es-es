---
title: Propiedad IVMHardDisk SizeInGuest (VPCCOMInterfaces.h)
description: Recupera el tamaño del disco duro virtual en el sistema operativo invitado.
ms.assetid: 895598db-cd54-414c-8783-13102cfbd453
keywords:
- SizeInGuest, propiedad Virtual PC
- SizeInGuest, propiedad Virtual PC , interfaz IVMHardDisk
- IVMHardDisk interface Virtual PC , propiedad SizeInGuest
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
ms.openlocfilehash: 8efbdcf9f5aa60a8dfdce9c71de745e0567995b90df13ffd39b5969689de099c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653295"
---
# <a name="ivmharddisksizeinguest-property"></a>Propiedad IVMHardDisk::SizeInGuest

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el tamaño del disco duro virtual en el sistema operativo invitado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_SizeInGuest(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a>Valor de propiedad

Tamaño, en bytes, de la imagen de disco duro. Este valor es una **VARIANTE de** tipo VT \_ DECIMAL.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                               | Significado                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                                  | La operación se realizó correctamente.<br/>                                                  |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                                    | El parámetro es **NULL.**<br/>                                                     |
| <dl> <dt>HRESULT \_ DESDE \_ WIN32 (ARCHIVO DE ERROR \_ \_ NO \_ ENCONTRADO)</dt> <dt>0X80070002</dt> </dl> | No se encontró el archivo de disco duro virtual actual.<br/>                         |
| <dl> <dt>Máquina virtual \_ ERROR \_ DE E HD IMAGE OPEN \_ \_ \_ 0XA004067C</dt> <dt></dt> </dl>                  | Error al intentar abrir el archivo de imagen de disco duro actual.<br/>   |
| <dl> <dt>Máquina virtual \_ E \_ HD IMAGE ACCESS \_ \_ 0xA0040681</dt> <dt></dt> </dl>                      | Error al intentar acceder al archivo de imagen de disco duro actual.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                            | Se produjo un error inesperado.<br/>                                              |



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

 

