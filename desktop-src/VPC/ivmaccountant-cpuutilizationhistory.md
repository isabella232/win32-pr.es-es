---
title: Propiedad IVMAccountant CPUUtilizationHistory (VPCCOMInterfaces. h)
description: Recupera el uso de CPU reciente de esta máquina virtual (como una matriz de valores de porcentaje).
ms.assetid: f6b92b25-9455-4061-8db0-3e42f9f7391d
keywords:
- Propiedad CPUUtilizationHistory Virtual PC
- Propiedad CPUUtilizationHistory Virtual PC, interfaz IVMAccountant
- Interfaz IVMAccountant Virtual PC, propiedad CPUUtilizationHistory
topic_type:
- apiref
api_name:
- IVMAccountant.CPUUtilizationHistory
- IVMAccountant.get_CPUUtilizationHistory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfa7e91a83be7ab4c09a0b779a729745e80e1e74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492911"
---
# <a name="ivmaccountantcpuutilizationhistory-property"></a>IVMAccountant:: CPUUtilizationHistory (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera el uso de CPU reciente de esta máquina virtual (como una matriz de valores de porcentaje).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_CPUUtilizationHistory(
  [out, retval] VARIANT *percentageUtilization
);
```



## <a name="property-value"></a>Valor de propiedad

El uso de CPU reciente de esta máquina virtual. Estos datos se devuelven como una matriz de 60 elementos que representan el porcentaje de uso de CPU en cada segundo durante el último minuto. Variant Type es VT \_ array \| VT \_ UI1.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>                                           |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **null**.<br/>                                              |
| <dl> <dt>S \_ FALSO</dt> <dt>1</dt> </dl>                    | La máquina virtual no se está ejecutando. Todos los elementos de la matriz 60 se establecen en 0.<br/> |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>                                       |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMAccountant se define como 6376c067-7f57-4D63-b754-06e2e4f51d73<br/>              |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMAccountant**](ivmaccountant.md)
</dt> </dl>

 

