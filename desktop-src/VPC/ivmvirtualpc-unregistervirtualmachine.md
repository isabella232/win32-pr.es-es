---
title: Método IVMVirtualPC UnregisterVirtualMachine (VPCCOMInterfaces.h)
description: Anula el registro de una configuración de máquina virtual sin eliminar el archivo de configuración.
ms.assetid: 82ca6ef3-e9e5-471e-b2dc-0ff689a618d9
keywords:
- UnregisterVirtualMachine method Virtual PC
- UnregisterVirtualMachine method Virtual PC , IVMVirtualPC interface
- IVMVirtualPC interface Virtual PC , UnregisterVirtualMachine method
topic_type:
- apiref
api_name:
- IVMVirtualPC.UnregisterVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6173d6f43d51384af610b850ec654d185f0a8ce31a375b4dd90bd929c6455b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652735"
---
# <a name="ivmvirtualpcunregistervirtualmachine-method"></a>IVMVirtualPC::UnregisterVirtualMachine (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Anula el registro de una configuración de máquina virtual (VM) sin eliminar el archivo de configuración.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UnregisterVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*virtualMachine* \[ En\]
</dt> <dd>

Puntero a un [**objeto IVMVirtualMachine**](ivmvirtualmachine.md) que representa la configuración de máquina virtual que se va a anular el registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                        | Descripción                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                              | La operación se realizó correctamente.<br/>                                                        |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                | El *parámetro virtualMachine* era **NULL.**<br/>                                         |
| <dl> <dt>**Máquina virtual \_ E \_ MÁQUINA VIRTUAL EN \_ EJECUCIÓN**</dt> <dt>0XA0040500</dt> </dl>                        | La máquina virtual se está ejecutando.<br/>                                                                   |
| <dl> <dt>**Máquina virtual \_ E \_ HARDWARE \_ VIRTUALIZATION \_ DISABLED**</dt> <dt>0xA0040951</dt> </dl> | El procesador no admite extensiones de Virtualización acelerada por hardware (HAV).<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                        | Se produjo un error inesperado.<br/>                                                    |



 

## <a name="remarks"></a>Comentarios

Solo se pueden anular el registro de las máquinas virtuales detenidas. Los datos de unidad de deshacer o estado guardado existentes para esta configuración se conservarán cuando se anule el registro de una máquina virtual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC se define como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

