---
title: Método IVMVirtualPC UnregisterVirtualMachine (VPCCOMInterfaces. h)
description: Anula el registro de una configuración de máquina virtual sin eliminar el archivo de configuración.
ms.assetid: 82ca6ef3-e9e5-471e-b2dc-0ff689a618d9
keywords:
- Método UnregisterVirtualMachine Virtual PC
- Método UnregisterVirtualMachine Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método UnregisterVirtualMachine
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
ms.openlocfilehash: 1d74380a822253918791b78bc34ac1c796f595ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492886"
---
# <a name="ivmvirtualpcunregistervirtualmachine-method"></a>IVMVirtualPC:: UnregisterVirtualMachine (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Anula el registro de una configuración de máquina virtual (VM) sin eliminar el archivo de configuración.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UnregisterVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*virtualMachine* \[ de\]
</dt> <dd>

Un puntero a un objeto [**IVMVirtualMachine**](ivmvirtualmachine.md) que representa la configuración de la máquina virtual cuyo registro se va a anular.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                        | Descripción                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                              | La operación se realizó correctamente.<br/>                                                        |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                                | El parámetro *virtualMachine* era **null**.<br/>                                         |
| <dl> <dt>**Máquina virtual \_ \_Máquina virtual \_ que ejecuta**</dt> <dt>0xA0040500</dt> </dl>                        | La máquina virtual se está ejecutando.<br/>                                                                   |
| <dl> <dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt> </dl> | El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).<br/> |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                        | Se produjo un error inesperado.<br/>                                                    |



 

## <a name="remarks"></a>Observaciones

Solo se puede anular el registro de las máquinas virtuales detenidas. Los datos del estado guardado o de la unidad de deshacer existentes para esta configuración se conservarán cuando se anule el registro de una máquina virtual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

