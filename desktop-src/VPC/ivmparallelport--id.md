---
title: Método _ID IVMParallelPort (VPCCOMInterfaces. h)
description: Recupera el identificador interno del puerto paralelo.
ms.assetid: a0de74da-0e23-489e-8a89-8deba974e548
keywords:
- _ID método virtual PC
- Método _ID Virtual PC, interfaz IVMParallelPort
- Interfaz IVMParallelPort Virtual PC, método _ID
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
ms.openlocfilehash: 267061204ea92dd8f5cae37fc5cb279e7dc2b010
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695857"
---
# <a name="ivmparallelport_id-method"></a>IVMParallelPort:: \_ ID (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera el identificador interno del puerto paralelo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT _ID(
  [out] long *portID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*portID* \[ enuncia\]
</dt> <dd>

Identificador de puerto paralelo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                 | Descripción                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **null**.<br/>                               |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>                        |
| <dl> <dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt> </dl> | La configuración de esta máquina virtual no es válida.<br/> |



 

## <a name="remarks"></a>Observaciones

Esta propiedad no se puede usar en los lenguajes de scripting.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMParallelPort se define como 097beecb-0a02-474f-abd6-298b22293fc6<br/>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMParallelPort**](ivmparallelport.md)
</dt> </dl>

 

