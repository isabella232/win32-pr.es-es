---
title: Propiedad IVMVirtualMachine AttachedDriveTypes (VPCCOMInterfaces.h)
description: Matriz que indica el tipo de unidad conectada a cada ubicación de la máquina virtual.
ms.assetid: 6896c9cd-5448-4fbb-8c8e-eef306a5cea1
keywords:
- AttachedDriveTypes, propiedad Virtual PC
- Propiedad AttachedDriveTypes Pc virtual, interfaz IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC , AttachedDriveTypes property
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AttachedDriveTypes
- IVMVirtualMachine.get_AttachedDriveTypes
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efbb326379faacdc9f48af84f5bff38ee1d29c16c18ca89765001db3eed3ee50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123215"
---
# <a name="ivmvirtualmachineattacheddrivetypes-property"></a>IVMVirtualMachine::AttachedDriveTypes, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera una matriz que indica el tipo de unidad conectada a cada ubicación de la máquina virtual (VM).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_AttachedDriveTypes(
  [out, retval] VARIANT *driveTypes
);
```



## <a name="property-value"></a>Valor de propiedad

Variante de tipo **VT \_ ARRAY** \| **VT \_ VARIANT** que contiene entradas de tipo **VT \_ UI1.** La matriz contiene el [**valor VMDriveType**](vmdrivetype.md) de cada dispositivo conectado a cada ubicación de bus. La matriz está ordenada por \[ *busNumber* \] \[ *deviceID.* \]

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>     |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **NULL.**<br/>        |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | La configuración es desconocida.<br/>     |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/> |



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

 

