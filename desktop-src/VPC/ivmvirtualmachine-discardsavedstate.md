---
title: Método IVMVirtualMachine DiscardSavedState (VPCCOMInterfaces.h)
description: Descarta cualquier información de estado guardada para una máquina virtual guardada.
ms.assetid: 546d6ea9-bfa3-487d-a333-399986bdf9a1
keywords:
- DiscardSavedState, método Virtual PC
- Método DiscardSavedState Para PC virtual, interfaz IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC , DiscardSavedState method
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DiscardSavedState
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff30406328ae13004505440ae2fb8b18b2e1fdf8ac19dcbfbe77b063e54df688
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471985"
---
# <a name="ivmvirtualmachinediscardsavedstate-method"></a>IVMVirtualMachine::D iscardSavedState (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Descarta cualquier información de estado guardada para una máquina virtual guardada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DiscardSavedState();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                           | Descripción                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                 | La operación se realizó correctamente.<br/>                               |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>           | La configuración es desconocida.<br/>                               |
| <dl> <dt>**Máquina virtual \_ E \_ MÁQUINA VIRTUAL EN \_ EJECUCIÓN**</dt> <dt>0XA0040500</dt> </dl>           | La máquina virtual se está ejecutando.<br/>                             |
| <dl> <dt>**Máquina virtual \_ E \_ VM NO SAVED \_ \_ \_ STATE**</dt> <dt>0xA00400501</dt> </dl> | La máquina virtual no se está ejecutando, pero no tiene ningún estado guardado.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>           | Se produjo un error inesperado.<br/>                           |



 

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

 

