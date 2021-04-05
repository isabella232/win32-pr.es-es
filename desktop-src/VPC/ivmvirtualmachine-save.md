---
title: Método Save de IVMVirtualMachine (VPCCOMInterfaces. h)
description: Guarda el estado de la máquina virtual (VM).
ms.assetid: e9f6e773-4e2d-4d7b-9624-e7864d5b248b
keywords:
- Guardar método virtual PC
- Método Save Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método Save
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
ms.openlocfilehash: 27b4dbe18b89f107657d67fb7e7b90e024b01383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803313"
---
# <a name="ivmvirtualmachinesave-method"></a>IVMVirtualMachine:: Save (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Guarda el estado de la máquina virtual (VM).

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

Un objeto [**IVMTask**](ivmtask.md) que se usa para realizar el seguimiento del progreso de finalización de la secuencia de almacenamiento de estado de la máquina virtual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                          | Descripción                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                                | La operación se realizó correctamente.<br/>                                                 |
| <dl> <dt>**E \_ ERROR**</dt> <dt>0x80004005</dt> </dl>                                     | No se pudo guardar la máquina virtual porque los discos para deshacer se marcaron para su eliminación.<br/>    |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                                  | El parámetro es **null**.<br/>                                                    |
| <dl> <dt>**HRESULT \_ DE \_ Win32 (error de \_ acceso \_ denegado)**</dt> <dt>0x80070005</dt> </dl> | El autor de la llamada debe tener permisos de acceso de ejecución para guardar el estado de esta máquina virtual.<br/> |
| <dl> <dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt> </dl>                     | La máquina virtual no se está ejecutando.<br/>                                                        |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                          | Se produjo un error inesperado.<br/>                                             |



 

## <a name="remarks"></a>Observaciones

La máquina virtual se apaga cuando la tarea **Guardar** llega a su finalización. La propiedad [**IVMVirtualMachine:: State**](ivmvirtualmachine-state.md) contendrá **vmVMState \_** al guardar mientras está en curso, seguido de **vmVMState \_ guardada** cuando se haya completado el proceso de guardado y se haya desactivado la máquina virtual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

