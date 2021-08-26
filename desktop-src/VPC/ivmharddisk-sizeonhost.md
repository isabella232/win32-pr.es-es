---
title: Propiedad IVMHardDisk SizeOnHost (VPCCOMInterfaces.h)
description: Tamaño del archivo de disco duro virtual en el equipo host.
ms.assetid: f787ec4b-7b4f-4d35-b07c-4844424d91cf
keywords:
- Equipo virtual de la propiedad SizeOnHost
- Propiedad SizeOnHost De PC virtual, interfaz IVMHardDisk
- IVMHardDisk interface Virtual PC , Propiedad SizeOnHost
topic_type:
- apiref
api_name:
- IVMHardDisk.SizeOnHost
- IVMHardDisk.get_SizeOnHost
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8952428665ef651d5d420bc457f1eed52f6c6ded78a7b448c8325ab09f352a9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867125"
---
# <a name="ivmharddisksizeonhost-property"></a>IVMHardDisk::SizeOnHost, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el tamaño del archivo de disco duro virtual en el equipo host.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_SizeOnHost(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a>Valor de propiedad

Tamaño, en bytes, del archivo de imagen de disco duro. Este valor es una **VARIANTE de** tipo **VT \_ DECIMAL.**

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                               | Significado                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                                  | La operación se realizó correctamente.<br/>           |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                                    | El parámetro es **NULL.**<br/>              |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                            | Se produjo un error inesperado.<br/>       |
| <dl> <dt>HRESULT \_ DESDE \_ WIN32(ARCHIVO DE ERROR \_ \_ NO \_ ENCONTRADO)</dt> <dt>0X80070002</dt> </dl> | No se encontró el archivo de imagen de disco duro.<br/> |



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

 

