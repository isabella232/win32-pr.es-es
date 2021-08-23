---
title: Método IVMVirtualPC DeleteVirtualMachine (VPCCOMInterfaces.h)
description: Elimina una configuración de máquina virtual.
ms.assetid: fc2562f3-6a83-4a40-b800-0bc2692beae8
keywords:
- DeleteVirtualMachine, método Virtual PC
- DeleteVirtualMachine method Virtual PC , IVMVirtualPC interface
- IVMVirtualPC interface Virtual PC , DeleteVirtualMachine method
topic_type:
- apiref
api_name:
- IVMVirtualPC.DeleteVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a3471106beeffdfe756ad0793004b68d0a55fd14dda28a9796f4540d2503a88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471335"
---
# <a name="ivmvirtualpcdeletevirtualmachine-method"></a>IVMVirtualPC::D eleteVirtualMachine (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Elimina una configuración de máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeleteVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*virtualMachine* \[ En\]
</dt> <dd>

Puntero a un [**objeto IVMVirtualMachine**](ivmvirtualmachine.md) que representa la configuración de máquina virtual que se va a eliminar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                        | Descripción                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                              | La operación se realizó correctamente.<br/>                                                        |
| <dl> <dt>**S \_ FALSE**</dt> <dt>1</dt> </dl>                                           | No se encontró la configuración especificada.<br/>                                      |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                | El *parámetro virtualMachine* era **NULL.**<br/>                                         |
| <dl> <dt>**Máquina virtual \_ E \_ MÁQUINA VIRTUAL EN \_ EJECUCIÓN**</dt> <dt>0XA0040500</dt> </dl>                        | La máquina virtual se está ejecutando.<br/>                                                      |
| <dl> <dt>**Máquina virtual \_ E \_ \_ VIRTUALIZACIÓN DE HARDWARE \_ DESHABILITADA**</dt> <dt>0xA0040951</dt> </dl> | El procesador no admite extensiones de virtualización acelerada de hardware (HAV).<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                        | Se produjo un error inesperado.<br/>                                                    |



 

## <a name="remarks"></a>Observaciones

Solo se pueden eliminar las máquinas virtuales detenidas. Tenga en cuenta que los datos de unidad de estado guardado o deshacer existentes para esta configuración se eliminarán además del archivo de configuración.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Product<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC se define como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

