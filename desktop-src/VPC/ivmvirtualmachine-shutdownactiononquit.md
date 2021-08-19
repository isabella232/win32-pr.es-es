---
title: Propiedad IVMVirtualMachine ShutdownActionOnQuit (VPCCOMInterfaces.h)
description: Acción que se va a realizar en esta máquina virtual si se está ejecutando cuando se Windows de Virtual PC.
ms.assetid: 3f6b256e-c48a-4a7c-acee-83d996e13ec7
keywords:
- ShutdownActionOnQuit, propiedad Virtual PC
- Propiedad ShutdownActionOnQuit Virtual PC , interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Pc virtual, propiedad ShutdownActionOnQuit
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ShutdownActionOnQuit
- IVMVirtualMachine.get_ShutdownActionOnQuit
- IVMVirtualMachine.put_ShutdownActionOnQuit
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c859a0f1715685e07ba13d6fb06fc99dc08f712fd20fa56a4672a2cc857b1591
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124705"
---
# <a name="ivmvirtualmachineshutdownactiononquit-property"></a>Propiedad IVMVirtualMachine::ShutdownActionOnQuit

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera y establece la acción que se va a realizar en esta máquina virtual (VM) si se está ejecutando cuando se cierra Windows equipo virtual.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ShutdownActionOnQuit(
  [in]          VMShutdownAction shutdownAction
);

HRESULT get_ShutdownActionOnQuit(
  [out, retval] VMShutdownAction *shutdownAction
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica cómo apagar esta máquina virtual si se está ejecutando cuando se cierra Windows equipo virtual. Para obtener una lista de valores, [**vea VMShutdownAction**](vmshutdownaction.md).

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>                                       |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **NULL** o no es un valor válido.<br/>                     |
| <dl> <dt>E \_ ACCESSDENIED</dt> <dt>0x80070005</dt> </dl>    | El usuario actual no tiene acceso suficiente al archivo de configuración.<br/> |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | La configuración es desconocida.<br/>                                       |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>                                   |



## <a name="remarks"></a>Comentarios

De forma predeterminada, las máquinas virtuales en ejecución se guardan Windows se cierra el equipo virtual. La acción de **apagado vmShutdownAction \_ Save** (0) guardará el estado de la máquina virtual. La **acción vmShutdownAction \_ TurnOff** (1) desactivará la máquina virtual. La **acción vmShutdownAction \_ Shutdown** (2) apagará el sistema operativo invitado si los componentes de integración están disponibles y guardará la máquina virtual en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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
</dt> <dt>

[**VMShutdownAction**](vmshutdownaction.md)
</dt> </dl>

 

