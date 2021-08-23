---
title: Propiedad IVMParallelPort Name (VPCCOMInterfaces.h)
description: Nombre del puerto paralelo.
ms.assetid: 254df134-2b48-4a81-8229-0f5fbacf2e1c
keywords:
- Nombre de la propiedad Virtual PC
- Nombre de la propiedad Virtual PC , IVMParallelPort (interfaz)
- IVMParallelPort interface Virtual PC , Propiedad Name
topic_type:
- apiref
api_name:
- IVMParallelPort.Name
- IVMParallelPort.get_Name
- IVMParallelPort.put_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4e4ce0ebf800329d40352adda9fa69d1233c8e72d0a5551a710b3c943b29fb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510385"
---
# <a name="ivmparallelportname-property"></a>IVMParallelPort::Name, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera y establece el nombre del puerto paralelo.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Name(
  [in]          BSTR portName
);

HRESULT get_Name(
  [out, retval] BSTR *portName
);
```



## <a name="property-value"></a>Valor de propiedad

Establece el nombre del puerto paralelo (por ejemplo, "LPT1").

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>                              |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **NULL.**<br/>                                 |
| <dl> <dt>E \_ InvalidarG</dt> <dt>0x80000003</dt> </dl>      | El parámetro hace referencia a un puerto paralelo que no es válido.<br/> |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | La configuración de esta máquina virtual no es válida.<br/>   |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>                          |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMParallelPort se define como 097beecb-0a02-474f-trib6-298b22293fc6<br/>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMParallelPort**](ivmparallelport.md)
</dt> </dl>

 

