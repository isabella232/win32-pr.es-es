---
title: Método IVMVirtualMachine Save (VPCCOMInterfaces.h)
description: Guarda el estado de la máquina virtual.
ms.assetid: e9f6e773-4e2d-4d7b-9624-e7864d5b248b
keywords:
- Guardar el método Virtual PC
- Save method Virtual PC , IVMVirtualMachine interface
- IVMVirtualMachine interface Virtual PC , Save method
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Save
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 609125ed9ae8deab897163d6a841e9cb665659c2c5af76baff3a1d96fb235e92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124795"
---
# <a name="ivmvirtualmachinesave-method"></a>IVMVirtualMachine::Save (Método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Guarda el estado de la máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Save(
  [out, retval] IVMTask **saveTask
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*saveTask* \[ out, retval\]
</dt> <dd>

Objeto [**IVMTask que**](ivmtask.md) se usa para realizar un seguimiento del progreso de finalización de la secuencia de almacenamiento de estado de la máquina virtual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                          | Descripción                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                                | La operación se realizó correctamente.<br/>                                                 |
| <dl> <dt>**E \_ Error**</dt> <dt>0x80004005</dt> </dl>                                     | No se pudo guardar la máquina virtual porque los discos de deshacer se marcaron para su eliminación.<br/>    |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                  | El parámetro es **NULL.**<br/>                                                    |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ACCESO DE ERROR \_ \_ DENEGADO)**</dt> <dt>0x80070005</dt> </dl> | El autor de la llamada debe tener permisos de acceso de ejecución para guardar el estado de esta máquina virtual.<br/> |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING**</dt> <dt>0xA0040206</dt> </dl>                     | La máquina virtual no se está ejecutando.<br/>                                                        |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                          | Se produjo un error inesperado.<br/>                                             |



 

## <a name="remarks"></a>Comentarios

La máquina virtual se apaga cuando la **tarea Guardar** finaliza. La [**propiedad IVMVirtualMachine::State**](ivmvirtualmachine-state.md) contendrá **vmVMState \_ Saving** mientras el guardado está en curso, seguido de **vmVMState \_ Saved** cuando se haya completado el guardado y la máquina virtual esté desactivada.

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

 

