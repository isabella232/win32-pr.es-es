---
title: Método IVMVirtualMachine MergeUndoDisks (VPCCOMInterfaces.h)
description: Combina los discos de deshacer virtuales.
ms.assetid: 6445b097-220e-48c4-9a7b-1139ca7b3338
keywords:
- MergeUndoDisks, método Virtual PC
- Método MergeUndoDisks Virtual PC , interfaz IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC , método MergeUndoDisks
topic_type:
- apiref
api_name:
- IVMVirtualMachine.MergeUndoDisks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 620d30558ddb8acdd75d72955048beb34f0141206b53f3f5873e42627fb155f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998685"
---
# <a name="ivmvirtualmachinemergeundodisks-method"></a>IVMVirtualMachine::MergeUndoDisks (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Combina los discos de deshacer virtuales.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT MergeUndoDisks(
  [out, retval] IVMTask **undoMergeTask
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*undoMergeTask* \[ out, retval\]
</dt> <dd>

Objeto [**IVMTask**](ivmtask.md) que se usa para realizar un seguimiento de la creación de la imagen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                            | Descripción                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                                  | La operación se realizó correctamente.<br/>                                                                                                |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Se produjo un error inesperado.<br/>                                                                                            |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                    | El parámetro es **NULL.**<br/>                                                                                                   |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32 (RUTA DE ACCESO DE ERROR \_ \_ NO \_ ENCONTRADA)**</dt> <dt>0X80070003</dt> </dl> | El sistema no puede encontrar la ruta de acceso especificada por el *parámetro convertedDiskImagePath* o uno de los discos primarios no es válido.<br/> |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> <dt>0x80070005</dt> </dl>                               | El usuario actual no tiene acceso suficiente al archivo primario.<br/>                                                                 |
| <dl> <dt>**E \_ Identificador**</dt> <dt>0x80070006</dt> </dl>                                     | Uno de los discos primarios está en uso.<br/>                                                                                           |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                            | La configuración es desconocida.<br/>                                                                                                |
| <dl> <dt>**Máquina virtual \_ E \_ MÁQUINA VIRTUAL EN \_ EJECUCIÓN**</dt> <dt>0XA0040500</dt> </dl>                            | La máquina virtual se está ejecutando.<br/>                                                                                              |
| <dl> <dt>**Máquina virtual \_ E \_ FILE \_ READ \_ ONLY**</dt> <dt>0xA004067A</dt> </dl>                       | El elemento primario de los discos de deshacer virtuales se marca como de solo lectura.<br/>                                                                     |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Se produjo un error inesperado.<br/>                                                                                            |



 

## <a name="remarks"></a>Comentarios

**No se puede llamar a MergeUndoDisks** mientras la máquina virtual todavía se está ejecutando. Use [**IVMVirtualMachine::Save**](ivmvirtualmachine-save.md) para guardar el estado de la máquina virtual antes de llamar a **MergeUndoDisks** o [**IVMVirtualMachine::TurnOff**](ivmvirtualmachine-turnoff.md) para desactivar la máquina virtual sin guardar su estado actual de antemano.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualMachine se define como \_ f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

