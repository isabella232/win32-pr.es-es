---
title: Propiedad IVMVirtualMachine SavedStateFilePath (VPCCOMInterfaces.h)
description: Recupera la ruta de acceso completa al archivo de estado guardado.
ms.assetid: 01bd5491-4d08-4558-ac33-01b096f057a2
keywords:
- Equipo virtual de la propiedad SavedStateFilePath
- Propiedad SavedStateFilePath Virtual PC, interfaz IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC , SavedStateFilePath property
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SavedStateFilePath
- IVMVirtualMachine.get_SavedStateFilePath
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc97bbb55ed4a784dad897fad480a2d9175db2759bba754308dc9b845f7190c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752237"
---
# <a name="ivmvirtualmachinesavedstatefilepath-property"></a>IVMVirtualMachine::SavedStateFilePath, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera la ruta de acceso completa al archivo de estado guardado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_SavedStateFilePath(
  [out, retval] BSTR *savedStateFilePath
);
```



## <a name="property-value"></a>Valor de propiedad

Ruta de acceso completa al archivo de estado guardado de la máquina virtual.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                              | Significado                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                 | La operación se realizó correctamente.<br/>                           |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                   | El parámetro es **NULL.**<br/>                              |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>           | La configuración es desconocida.<br/>                           |
| <dl> <dt>Máquina virtual \_ E \_ VM NO SAVED \_ \_ \_ STATE</dt> <dt>0xA00400501</dt> </dl> | La máquina virtual no tiene ningún archivo de estado guardado asociado.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>           | Se produjo un error inesperado.<br/>                       |



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

 

