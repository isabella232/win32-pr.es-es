---
title: Propiedad IVMHardDiskConnection BusNumber (VPCCOMInterfaces. h)
description: Recupera el número de bus al que está conectada la imagen de la unidad.
ms.assetid: 2a792930-d8c9-419d-88eb-ddec7c43c5bc
keywords:
- Propiedad BusNumber Virtual PC
- Propiedad BusNumber Virtual PC, interfaz IVMHardDiskConnection
- Interfaz IVMHardDiskConnection Virtual PC, propiedad BusNumber
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.BusNumber
- IVMHardDiskConnection.get_BusNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdc49a0d4cb284ecd1e2a1340d3b0bf8d9ed43ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491884"
---
# <a name="ivmharddiskconnectionbusnumber-property"></a>IVMHardDiskConnection:: BusNumber (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera el número de bus al que está conectada la imagen de la unidad.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_BusNumber(
  [out, retval] long *vmBusNumber
);
```



## <a name="property-value"></a>Valor de propiedad

Número de bus que corresponde a esta conexión.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                       | Significado                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                          | La operación se realizó correctamente.<br/>                                           |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>            | El parámetro es **null** o no es válido.<br/>                                 |
| <dl> <dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt> </dl>    | La configuración de máquina virtual actual no es válida.<br/>                 |
| <dl> <dt>Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida</dt> <dt></dt> </dl> | La ubicación del bus para esta conexión no se ha inicializado correctamente.<br/> |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>    | Se produjo un error inesperado.<br/>                                       |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDiskconnection se define como aefa36a5-463a-46ae-9e6c-a1fb4e12e671<br/>      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> </dl>

 

