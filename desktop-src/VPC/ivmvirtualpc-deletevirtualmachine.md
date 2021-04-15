---
title: Método IVMVirtualPC DeleteVirtualMachine (VPCCOMInterfaces. h)
description: Elimina una configuración de máquina virtual.
ms.assetid: fc2562f3-6a83-4a40-b800-0bc2692beae8
keywords:
- Método DeleteVirtualMachine Virtual PC
- Método DeleteVirtualMachine Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método DeleteVirtualMachine
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
ms.openlocfilehash: ee9c1591ccd736099fab04cce31c8a8b77b5fb06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695998"
---
# <a name="ivmvirtualpcdeletevirtualmachine-method"></a>IVMVirtualPC::D método eleteVirtualMachine

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Elimina una configuración de máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeleteVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*virtualMachine* \[ de\]
</dt> <dd>

Un puntero a un objeto [**IVMVirtualMachine**](ivmvirtualmachine.md) que representa la configuración de la máquina virtual que se va a eliminar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                        | Descripción                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                              | La operación se realizó correctamente.<br/>                                                        |
| <dl> <dt>**S \_ FALSO**</dt> <dt>1</dt> </dl>                                           | No se encontró la configuración especificada.<br/>                                      |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                                | El parámetro *virtualMachine* era **null**.<br/>                                         |
| <dl> <dt>**Máquina virtual \_ \_Máquina virtual \_ que ejecuta**</dt> <dt>0xA0040500</dt> </dl>                        | La máquina virtual se está ejecutando.<br/>                                                      |
| <dl> <dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt> </dl> | El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).<br/> |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                        | Se produjo un error inesperado.<br/>                                                    |



 

## <a name="remarks"></a>Observaciones

Solo se pueden eliminar las máquinas virtuales detenidas. Tenga en cuenta que los datos del estado guardado o de la unidad de deshacer existentes para esta configuración se eliminarán además del archivo de configuración.

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

 

