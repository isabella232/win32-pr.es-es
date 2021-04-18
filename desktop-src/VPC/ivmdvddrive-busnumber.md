---
title: Propiedad IVMDVDDrive BusNumber (VPCCOMInterfaces. h)
description: Recupera el número de bus al que está conectado este dispositivo.
ms.assetid: 8edc94da-22bc-4141-a6c7-1b18cca754fc
keywords:
- Propiedad BusNumber Virtual PC
- Propiedad BusNumber Virtual PC, interfaz IVMDVDDrive
- Interfaz IVMDVDDrive Virtual PC, propiedad BusNumber
topic_type:
- apiref
api_name:
- IVMDVDDrive.BusNumber
- IVMDVDDrive.get_BusNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056770b7eb11518645f3c28a6d45685795c7107a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676867"
---
# <a name="ivmdvddrivebusnumber-property"></a>IVMDVDDrive:: BusNumber (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera el número de bus al que está conectado este dispositivo.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_BusNumber(
  [out, retval] long *vmBusNumber
);
```



## <a name="property-value"></a>Valor de propiedad

El número de bus. Por ejemplo, en un bus IDE, este valor representaría la ubicación principal o secundaria.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                       | Significado                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                          | La operación se realizó correctamente.<br/>                                          |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>            | El parámetro es **null**.<br/>                                             |
| <dl> <dt>Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida</dt> <dt></dt> </dl> | La ubicación del bus para esta unidad de DVD no se ha inicializado correctamente.<br/> |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>    | Se produjo un error inesperado.<br/>                                      |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive se define como b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

