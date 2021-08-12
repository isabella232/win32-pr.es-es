---
title: Propiedad IVMVirtualMachine HasSSE2 (VPCCOMInterfaces.h)
description: Determina si el procesador admite el conjunto de instrucciones SSE2. | Propiedad IVMVirtualMachine HasSSE2 (VPCCOMInterfaces.h)
ms.assetid: da9860cf-d1e4-4dc4-8c4c-1b83104ffbc6
keywords:
- Equipo virtual de la propiedad HasSSE2
- Interfaz Virtual PC, IVMVirtualMachine de la propiedad HasSSE2
- IVMVirtualMachine interface Virtual PC , Propiedad HasSSE2
topic_type:
- apiref
api_name:
- IVMVirtualMachine.HasSSE2
- IVMVirtualMachine.get_HasSSE2
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f64dde4b075652899d50f4bbb41caafafdd69ec8ea9ea80d3eb165bcf14cafc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592655"
---
# <a name="ivmvirtualmachinehassse2-property"></a>IVMVirtualMachine::HasSSE2, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Determina si el procesador admite el conjunto de instrucciones SSE2.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_HasSSE2(
  [out, retval] VARIANT_BOOL *sse2Enabled
);
```



## <a name="property-value"></a>Valor de propiedad

**TRUE** si el procesador admite el conjunto de instrucciones SSE2; en caso contrario, **FALSE.**

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

