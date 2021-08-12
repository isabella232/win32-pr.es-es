---
title: Método _ID IVMParallelPort (VPCCOMInterfaces.h)
description: Recupera el identificador interno del puerto paralelo.
ms.assetid: a0de74da-0e23-489e-8a89-8deba974e548
keywords:
- _ID virtual PC
- _ID método Virtual PC , interfaz IVMParallelPort
- IVMParallelPort interface Virtual PC , _ID método
topic_type:
- apiref
api_name:
- IVMParallelPort._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0c7b3eab7de47d182c94aa9b5fb35aef04e98495ef3e7b39d4547967f3438b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593223"
---
# <a name="ivmparallelport_id-method"></a>IVMParallelPort:: \_ método de identificador

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el identificador interno del puerto paralelo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT _ID(
  [out] long *portID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*portID* \[ out\]
</dt> <dd>

Identificador de puerto paralelo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                 | Descripción                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **NULL.**<br/>                               |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>                        |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl> | La configuración de esta máquina virtual no es válida.<br/> |



 

## <a name="remarks"></a>Observaciones

Los lenguajes de scripting no pueden hacer uso de esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMParallelPort se define como 097beecb-0a02-474f-trib6-298b22293fc6<br/>            |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMParallelPort**](ivmparallelport.md)
</dt> </dl>

 

