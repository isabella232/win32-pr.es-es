---
title: Método _ID IVMSerialPort (VPCCOMInterfaces.h)
description: Identificador interno del puerto serie.
ms.assetid: c26c18dc-5491-4edf-9338-e4f3bf431084
keywords:
- _ID virtual PC
- _ID método Virtual PC , interfaz IVMSerialPort
- IVMSerialPort interface Virtual PC , _ID método
topic_type:
- apiref
api_name:
- IVMSerialPort._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b55974319e4af48ae1a6f3554ae79557feaa5c8455e47b66e82e4d4cf02a801
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123763"
---
# <a name="ivmserialport_id-method"></a>IVMSerialPort:: \_ método de identificador

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el identificador interno del puerto serie.

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

Identificador de puerto serie.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                 | Descripción                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **NULL.**<br/>                               |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>                        |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl> | La configuración de esta máquina virtual no es válida.<br/> |



 

## <a name="remarks"></a>Comentarios

Los lenguajes de scripting no pueden hacer uso de esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPort se define como 2ce4460d-1d3f-4458-bf8b-44084b816815<br/>              |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMSerialPort**](ivmserialport.md)
</dt> </dl>

 

