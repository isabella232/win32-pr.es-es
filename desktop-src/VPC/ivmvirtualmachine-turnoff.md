---
title: Método IVMVirtualMachine TurnOff (VPCCOMInterfaces.h)
description: Desactiva la máquina virtual.
ms.assetid: 4ea00314-8f1e-47d9-bbb8-b5791af1fb86
keywords:
- TurnOff method Virtual PC
- Método TurnOff Virtual PC , interfaz IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC , método TurnOff
topic_type:
- apiref
api_name:
- IVMVirtualMachine.TurnOff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5351aacc3e21cd620aa31798314fd7f6728cf98653cb83cbaa2f19439d530c44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864165"
---
# <a name="ivmvirtualmachineturnoff-method"></a>IVMVirtualMachine::TurnOff (Método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Desactiva la máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT TurnOff(
  [out, retval] IVMTask **turnOffTask
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*turnOffTask* \[ out, retval\]
</dt> <dd>

Objeto [**IVMTask que**](ivmtask.md) se usa para realizar un seguimiento del progreso de finalización de la secuencia de desactivación de la máquina virtual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                          | Descripción                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                                | La operación se realizó correctamente.<br/>                                                     |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                  | El parámetro es **NULL.**<br/>                                                        |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32 (ACCESO DE ERROR \_ \_ DENEGADO)**</dt> <dt>0x80070005</dt> </dl> | El autor de la llamada debe tener permisos de acceso de ejecución para desactivar esta máquina virtual.<br/> |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING**</dt> <dt>0xA0040206</dt> </dl>                     | La máquina virtual no se está ejecutando.<br/>                                               |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                          | La configuración es desconocida.<br/>                                                     |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                          | Se produjo un error inesperado.<br/>                                                 |



 

## <a name="remarks"></a>Comentarios

Este método desactiva la máquina virtual de la misma manera que al apagar una máquina física.

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

 

