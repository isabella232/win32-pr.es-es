---
title: Método IVMVirtualMachine MergeUndoDisks (VPCCOMInterfaces. h)
description: Combina los discos para deshacer virtuales.
ms.assetid: 6445b097-220e-48c4-9a7b-1139ca7b3338
keywords:
- Método MergeUndoDisks Virtual PC
- Método MergeUndoDisks Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método MergeUndoDisks
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
ms.openlocfilehash: 48863bf998ebc02bac93aa9e74d8cdbe07265477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359811"
---
# <a name="ivmvirtualmachinemergeundodisks-method"></a>IVMVirtualMachine:: MergeUndoDisks (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Combina los discos para deshacer virtuales.

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

Un objeto [**IVMTask**](ivmtask.md) que se usa para realizar el seguimiento de la creación de la imagen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                            | Descripción                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                                  | La operación se realizó correctamente.<br/>                                                                                                |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                            | Se produjo un error inesperado.<br/>                                                                                            |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                                    | El parámetro es **null**.<br/>                                                                                                   |
| <dl> <dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró la ruta de acceso de error)**</dt> <dt>0x80070003</dt> </dl> | El sistema no puede encontrar la ruta de acceso especificada por el parámetro *convertedDiskImagePath* o uno de los discos primarios no es válido.<br/> |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> <dt>0x80070005</dt> </dl>                               | El usuario actual no tiene acceso suficiente al archivo primario.<br/>                                                                 |
| <dl> <dt>**E \_ ADMINISTRAR**</dt> <dt>0x80070006</dt> </dl>                                     | Uno de los discos primarios está en uso.<br/>                                                                                           |
| <dl> <dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt> </dl>                            | La configuración es desconocida.<br/>                                                                                                |
| <dl> <dt>**Máquina virtual \_ \_Máquina virtual \_ que ejecuta**</dt> <dt>0xA0040500</dt> </dl>                            | La máquina virtual se está ejecutando.<br/>                                                                                              |
| <dl> <dt>**Máquina virtual \_ E & 0xA004067A de \_ \_ \_ solo lectura de archivos**</dt> <dt></dt> </dl>                       | El elemento primario de los discos para deshacer virtual está marcado como de solo lectura.<br/>                                                                     |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                            | Se produjo un error inesperado.<br/>                                                                                            |



 

## <a name="remarks"></a>Observaciones

No se puede llamar a **MergeUndoDisks** mientras la máquina virtual sigue en ejecución. Use [**IVMVirtualMachine:: Save**](ivmvirtualmachine-save.md) para guardar el estado de la máquina virtual antes de llamar a **MergeUndoDisks** o [**IVMVirtualMachine::**](ivmvirtualmachine-turnoff.md) desactivador para desactivar la máquina virtual sin guardar su estado actual de antemano.

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

 

