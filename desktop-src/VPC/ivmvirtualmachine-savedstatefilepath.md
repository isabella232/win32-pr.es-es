---
title: Propiedad IVMVirtualMachine SavedStateFilePath (VPCCOMInterfaces. h)
description: Recupera la ruta de acceso completa al archivo de estado guardado.
ms.assetid: 01bd5491-4d08-4558-ac33-01b096f057a2
keywords:
- Propiedad SavedStateFilePath Virtual PC
- Propiedad SavedStateFilePath Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, propiedad SavedStateFilePath
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
ms.openlocfilehash: 1e9baea53e3fce2455a2bdfa361e56b45b9b65d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150839"
---
# <a name="ivmvirtualmachinesavedstatefilepath-property"></a>IVMVirtualMachine:: SavedStateFilePath (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                                 | La operación se realizó correctamente.<br/>                           |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>                   | El parámetro es **null**.<br/>                              |
| <dl> <dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt> </dl>           | La configuración es desconocida.<br/>                           |
| <dl> <dt>Máquina virtual \_ NO se ha \_ \_ guardado el \_ \_ Estado de la máquina virtual</dt> <dt>0xA00400501</dt> </dl> | La máquina virtual no tiene ningún archivo de estado guardado asociado.<br/> |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>           | Se produjo un error inesperado.<br/>                       |



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

 

