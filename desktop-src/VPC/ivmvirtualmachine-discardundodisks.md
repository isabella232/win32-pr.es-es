---
title: Método IVMVirtualMachine DiscardUndoDisks (VPCCOMInterfaces.h)
description: Descarta los discos de deshacer virtuales.
ms.assetid: 5c3a4b3f-ea58-498c-b7cf-54f028fa061c
keywords:
- DiscardUndoDisks method Virtual PC
- Método DiscardUndoDisks para PC virtual, interfaz IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC , DiscardUndoDisks method
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DiscardUndoDisks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997019bf25b4bcc37266c1ba39d5b1420ae44b800127f3e91bc5d9fcb4b76691
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471954"
---
# <a name="ivmvirtualmachinediscardundodisks-method"></a>IVMVirtualMachine::D iscardUndoDisks (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Descarta los discos de deshacer virtuales.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DiscardUndoDisks();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                            | Descripción                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                  | La operación se realizó correctamente.<br/>                                                                        |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>            | La configuración es desconocida.<br/>                                                                        |
| <dl> <dt>**Máquina virtual \_ E \_ MÁQUINA VIRTUAL EN EJECUCIÓN O \_ \_ \_ GUARDADA**</dt> <dt>0XA004020B</dt> </dl> | Los discos de deshacer virtuales no se pueden descartar mientras la máquina virtual se está ejecutando o en un estado guardado.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>            | Se produjo un error inesperado.<br/>                                                                    |



 

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

 

