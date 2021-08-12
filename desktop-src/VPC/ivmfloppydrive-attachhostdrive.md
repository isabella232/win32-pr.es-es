---
title: Método IVMFstonepyDrive AttachHostDrive (VPCCOMInterfaces.h)
description: Conecta una unidad física del host a la unidad de disquete de la máquina virtual.
ms.assetid: 9be84e06-e38a-419a-be50-dddd0cc6d2dd
keywords:
- Equipo virtual del método AttachHostDrive
- Método AttachHostDrive Para PC virtual, interfaz IVMFstonepyDrive
- IVMFstonepyDrive interface Virtual PC , AttachHostDrive method
topic_type:
- apiref
api_name:
- IVMFloppyDrive.AttachHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8bfdfecc106acd216da5d39e7625f1fbbd9d76190eecc4c2d428595abc9e775
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118595729"
---
# <a name="ivmfloppydriveattachhostdrive-method"></a>IVMFstonepyDrive::AttachHostDrive (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Conecta una unidad física del host a la unidad de disquete de la máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AttachHostDrive(
  [in] BSTR driveLetter
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*driveLetter* \[ En\]
</dt> <dd>

La letra de unidad de la unidad de disquete física de la máquina host a se va a conectar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                 | Descripción                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>                                                                     |
| <dl> <dt>**E \_ InvalidarG**</dt> <dt>0x80000003</dt> </dl>      | El *parámetro driveLetter* es **NULL,** no es una unidad de disquete válida o la ruta de acceso especificada está vacía.<br/> |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl> | La configuración de esta máquina virtual no es válida o no se encuentra.<br/>                       |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>                                                                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMFstonepyDrive se define como \_ 661abee6-112a-4ed9-bamf-3c874969f10e<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMFstonepyDrive**](ivmfloppydrive.md)
</dt> </dl>

 

