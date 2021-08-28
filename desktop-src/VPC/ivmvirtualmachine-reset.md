---
title: Método IVMVirtualMachine Reset (VPCCOMInterfaces.h)
description: Restablece la máquina virtual.
ms.assetid: 44daf6be-66ce-4291-a535-c30369eed60f
keywords:
- Restablecer el método Virtual PC
- Restablecer método Virtual PC , IVMVirtualMachine (interfaz)
- IVMVirtualMachine interface Virtual PC , método Reset
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Reset
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9d09204afba2d5c9340350a1fad256e84f8fbf8899c544c7b52d36dfb872c91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056783"
---
# <a name="ivmvirtualmachinereset-method"></a>IVMVirtualMachine::Reset (Método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Restablece la máquina virtual (VM).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Reset(
  [out, retval] IVMTask **resetTask
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*resetTask* \[ out, retval\]
</dt> <dd>

Objeto [**IVMTask que**](ivmtask.md) se usa para realizar un seguimiento del progreso de finalización de la secuencia de restablecimiento de la máquina virtual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                          | Descripción                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                                | La operación se realizó correctamente.<br/>                                     |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                  | El parámetro es **NULL.**<br/>                                        |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32 (ACCESO DE ERROR \_ \_ DENEGADO)**</dt> <dt>0x80070005</dt> </dl> | El autor de la llamada debe tener permisos de acceso de ejecución para restablecer esta máquina virtual.<br/> |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING**</dt> <dt>0xA0040206</dt> </dl>                     | La máquina virtual no se está ejecutando.<br/>                                            |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                          | La configuración es desconocida.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                          | Se produjo un error inesperado.<br/>                                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualMachine se define como \_ f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

