---
title: Propiedad IVMVirtualMachine Undoable (VPCCOMInterfaces.h)
description: Determina si las unidades de deshacer están habilitadas para los discos duros conectados a la máquina virtual.
ms.assetid: 4f591360-1229-46ae-9925-3a3d02ab3202
keywords:
- Equipo virtual de la propiedad undoable
- Propiedad undoable Virtual PC , IVMVirtualMachine (interfaz)
- IVMVirtualMachine interface Virtual PC , Propiedad undoable
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Undoable
- IVMVirtualMachine.get_Undoable
- IVMVirtualMachine.put_Undoable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7663cefb8f94809f0fd016e002102c9956066b64ca21fb79766598b592ec3dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752078"
---
# <a name="ivmvirtualmachineundoable-property"></a>Propiedad IVMVirtualMachine::Undoable

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Determina si las unidades de deshacer están habilitadas para los discos duros conectados a la máquina virtual (VM).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Undoable(
  [in]          VARIANT_BOOL enableUndo
);

HRESULT get_Undoable(
  [out, retval] VARIANT_BOOL *isUndoable
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica **VARIANT \_ TRUE si las** unidades de deshacer están habilitadas para los discos duros conectados a la máquina virtual y VARIANT FALSE **\_ en** caso contrario.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                         | Significado                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                            | La operación se realizó correctamente.<br/>     |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>      | Se produjo un error inesperado.<br/> |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>              | El parámetro es **NULL.**<br/>        |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>      | La configuración es desconocida.<br/>     |
| <dl> <dt>Máquina virtual \_ E \_ PREF \_ VM \_ ACTIVE</dt> <dt>0xA0040302</dt> </dl> | La máquina virtual se ejecuta o se guarda.<br/>       |



## <a name="remarks"></a>Comentarios

Si las unidades de deshacer están deshabilitadas, se eliminarán los archivos de unidad de deshacer existentes.

No se puede establecer esta propiedad si la máquina virtual se está ejecutando o se ha guardado.

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

 

