---
title: Propiedad de recuento de IVMDVDDriveCollection (VPCCOMInterfaces. h)
description: Recupera el número de unidades de CD y DVD de esta colección.
ms.assetid: 22e39c42-1f98-4680-a97e-0d329dc608e2
keywords:
- Propiedad Count Virtual PC
- Propiedad Count Virtual PC, interfaz IVMDVDDriveCollection
- Interfaz IVMDVDDriveCollection Virtual PC, propiedad Count
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection.Count
- IVMDVDDriveCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e9ea713810348c0bd78c7de307600fc6ac9adc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695965"
---
# <a name="ivmdvddrivecollectioncount-property"></a>IVMDVDDriveCollection:: Count (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera el número de unidades de CD y DVD de esta colección.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Valor de propiedad

El número de unidades de CD y DVD.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>     |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **null**.<br/>        |
| <dl> <dt>E \_ ERROR</dt> <dt>0x80004005</dt> </dl>            | Se produjo un error inesperado.<br/> |
| <dl> <dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt> </dl> | La configuración es desconocida.<br/>     |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDriveCollection se define como bc86e297-e55f-4742-9614-ad11d3131f68<br/>      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMDVDDriveCollection**](ivmdvddrivecollection.md)
</dt> </dl>

 

