---
title: Propiedad IVMVirtualMachine ChassisSerialNumber (VPCCOMInterfaces.h)
description: Número de serie del chasis.
ms.assetid: 03e02e6e-6819-4052-a0e0-9167eb5fdf4b
keywords:
- Pc virtual de la propiedad ChassisSerialNumber
- Interfaz IVMVirtualMachine de la propiedad ChassisSerialNumber
- Interfaz IVMVirtualMachine Pc virtual, propiedad ChassisSerialNumber
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ChassisSerialNumber
- IVMVirtualMachine.get_ChassisSerialNumber
- IVMVirtualMachine.put_ChassisSerialNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40b9922f862e52cc6b1cce3d6f508254f37ca41ec314f4312ffa159cb9cde15d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752443"
---
# <a name="ivmvirtualmachinechassisserialnumber-property"></a>Propiedad IVMVirtualMachine::ChassisSerialNumber

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera y establece el número de serie del chasis.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ChassisSerialNumber(
  [in]          BSTR chasisSerialNumber
);

HRESULT get_ChassisSerialNumber(
  [out, retval] BSTR *chassisSerialNumber
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica el número de serie del chasis.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                               | Significado                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                  | La operación se realizó correctamente.<br/>                                               |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                    | El parámetro es **NULL.**<br/>                                                  |
| <dl> <dt>E \_ Invalidarg</dt> <dt>0x80000003</dt> </dl>                 | El parámetro tiene más de 32 caracteres, una cadena vacía o no es válido.<br/> |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>            | La configuración es desconocida.<br/>                                               |
| <dl> <dt>Máquina virtual \_ E \_ MÁQUINA VIRTUAL EN EJECUCIÓN O GUARDADA \_ \_ \_ 0XA004020B</dt> <dt></dt> </dl> | La máquina virtual está en estado en ejecución o guardado.<br/>                         |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>            | Se produjo un error inesperado.<br/>                                           |



## <a name="remarks"></a>Comentarios

Esta propiedad no contendrá información válida hasta que la máquina virtual se haya iniciado por primera vez. Se devolverá una cadena vacía si se lee antes del inicio inicial.

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
</dt> </dl>

 

