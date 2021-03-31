---
title: Propiedad IVMHardDisk HostFreeDiskSpace (VPCCOMInterfaces. h)
description: Recupera la cantidad de espacio en disco restante disponible en el host para el disco duro virtual.
ms.assetid: 08574bd3-e96d-465c-a1fc-265085fb3847
keywords:
- Propiedad HostFreeDiskSpace Virtual PC
- Propiedad HostFreeDiskSpace Virtual PC, interfaz IVMHardDisk
- Interfaz IVMHardDisk Virtual PC, propiedad HostFreeDiskSpace
topic_type:
- apiref
api_name:
- IVMHardDisk.HostFreeDiskSpace
- IVMHardDisk.get_HostFreeDiskSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e647d94ddecfdc8e0b9265b3639508b797f37861
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150996"
---
# <a name="ivmharddiskhostfreediskspace-property"></a>IVMHardDisk:: HostFreeDiskSpace (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera la cantidad de espacio en disco restante disponible en el host para el disco duro virtual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_HostFreeDiskSpace(
  [out, retval] VARIANT *freeBytes
);
```



## <a name="property-value"></a>Valor de propiedad

La cantidad de espacio en disco restante disponible en el equipo host para el archivo de imagen de disco duro actual. Este valor es una **variante** de tipo VT \_ decimal.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                            | Significado                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                                               | La operación se realizó correctamente.<br/>                                |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>                                 | El parámetro es **null**.<br/>                                   |
| <dl> <dt>HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)</dt> <dt>0x800700a1</dt> </dl> | La ruta de acceso al archivo de disco duro virtual actual no es válida.<br/> |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>                         | Se produjo un error inesperado.<br/>                            |



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

 

