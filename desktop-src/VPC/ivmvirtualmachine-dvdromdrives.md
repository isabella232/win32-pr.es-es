---
title: Propiedad IVMVirtualMachine DVDROMDrives (VPCCOMInterfaces.h)
description: Recupera una colección enumerable de unidades de CD y DVD conectadas a la máquina virtual.
ms.assetid: e9e7d912-568f-4a3d-85cf-63f6fa99cb19
keywords:
- DVDROMDrives, propiedad Virtual PC
- Propiedad DVDROMDrives Pc virtual, interfaz IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC , PROPIEDAD DVDROMDrives
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DVDROMDrives
- IVMVirtualMachine.get_DVDROMDrives
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cd7e3b101872d34b61fd893fbe794f1fac9fe9b281ad696a3d63de6c6fb9fb3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471825"
---
# <a name="ivmvirtualmachinedvdromdrives-property"></a>IVMVirtualMachine::D VDROMDrives

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera una colección enumerable de unidades de CD y DVD conectadas a la máquina virtual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_DVDROMDrives(
  [out, retval] IVMDVDDriveCollection **dvdROMCollection
);
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**IVMDVDDriveCollection.**](ivmdvddrivecollection.md)

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>     |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **NULL.**<br/>        |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | La configuración es desconocida.<br/>     |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualMachine se define como \_ f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

