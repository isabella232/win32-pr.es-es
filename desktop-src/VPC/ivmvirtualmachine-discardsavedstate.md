---
title: Método IVMVirtualMachine DiscardSavedState (VPCCOMInterfaces. h)
description: Descarta cualquier información de estado guardada para una máquina virtual guardada.
ms.assetid: 546d6ea9-bfa3-487d-a333-399986bdf9a1
keywords:
- Método DiscardSavedState Virtual PC
- Método DiscardSavedState Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método DiscardSavedState
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
ms.openlocfilehash: 6ce5c9cc0b07af2cc8c995d0c368d7747fa1475a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079501"
---
# <a name="ivmvirtualmachinediscardsavedstate-method"></a>IVMVirtualMachine::D método iscardSavedState

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                 | La operación se realizó correctamente.<br/>                               |
| <dl> <dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt> </dl>           | La configuración es desconocida.<br/>                               |
| <dl> <dt>**Máquina virtual \_ \_Máquina virtual \_ que ejecuta**</dt> <dt>0xA0040500</dt> </dl>           | La máquina virtual se está ejecutando.<br/>                             |
| <dl> <dt>**Máquina virtual \_ NO se ha \_ \_ guardado el \_ \_ Estado de la máquina virtual**</dt> <dt>0xA00400501</dt> </dl> | La máquina virtual no se está ejecutando, pero no tiene ningún estado guardado.<br/> |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>           | Se produjo un error inesperado.<br/>                           |



 

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

 

