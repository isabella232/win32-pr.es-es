---
title: Método IVMVirtualMachine RemoveDVDROMDrive (VPCCOMInterfaces.h)
description: Quita la unidad de CD o DVD especificada de la máquina virtual.
ms.assetid: 1c45c271-bead-41f6-8371-448d385a1288
keywords:
- RemoveDVDROMDrive method Virtual PC
- RemoveDVDROMDrive, método Virtual PC, interfaz IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC , Método RemoveDVDROMDrive
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveDVDROMDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 693d8eebe30c347b41a2b9b0b115c09f6fea75cd8744baa97aa3aca5cd0d1916
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752284"
---
# <a name="ivmvirtualmachineremovedvdromdrive-method"></a>IVMVirtualMachine::RemoveDVDROMDrive (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Quita la unidad de CD o DVD especificada de la máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RemoveDVDROMDrive(
  [in] IVMDVDDrive *dvdDrive
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dvdDrive* \[ En\]
</dt> <dd>

Unidad que se va a quitar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                            | Descripción                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                  | La operación se realizó correctamente.<br/>                              |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                    | El parámetro es **NULL.**<br/>                                 |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>            | La configuración es desconocida.<br/>                              |
| <dl> <dt>**Máquina virtual \_ E \_ MÁQUINA VIRTUAL EN EJECUCIÓN O GUARDADA \_ \_ \_ 0XA004020B**</dt> <dt></dt> </dl> | La máquina virtual está en estado en ejecución o guardado.<br/>        |
| <dl> <dt>**Máquina virtual \_ E \_ UNIDAD \_ NO VÁLIDA**</dt> <dt>0xA0040502</dt> </dl>         | La unidad especificada no está conectada a esta ubicación de bus.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>            | Se produjo un error inesperado.<br/>                          |



 

## <a name="remarks"></a>Comentarios

Solo puede quitar una unidad de CD o DVD existente de una máquina virtual detenida.

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

 

