---
title: Propiedad IVMDVDDriveCollection Item (VPCCOMInterfaces.h)
description: Recupera el objeto de unidad de CD o DVD que corresponde al índice especificado.
ms.assetid: ecc94eea-9ddc-46c8-87e2-e67aca83eecc
keywords:
- Propiedad de elemento Virtual PC
- Propiedad de elemento Virtual PC , interfaz IVMDVDDriveCollection
- IVMDVDDriveCollection interface Virtual PC , Propiedad Item
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection.Item
- IVMDVDDriveCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55ea8cd86d45827c06f4ef3582cc0d2ff990a176e244483db52101deb596745b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117753746"
---
# <a name="ivmdvddrivecollectionitem-property"></a>IVMDVDDriveCollection::Item, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el objeto de unidad de CD o DVD que corresponde al índice especificado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Item(
  [in]          long        index,
  [out, retval] IVMDVDDrive **dvdDrive
);
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**IVMDVDDrive.**](ivmdvddrive.md)

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente. <br/>                                                      |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **NULL.**<br/>                                                          |
| <dl> <dt>E \_ ERROR</dt> <dt>0x80004005</dt> </dl>            | Se produjo un error inesperado.<br/>                                                   |
| <dl> <dt>DISP \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt> </dl>  | El índice del elemento solicitado no corresponde a un elemento de esta colección. <br/> |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | La configuración es desconocida.<br/>                                                       |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMDVDDriveCollection se define como \_ bc86e297-e55f-4742-9614-ad11d3131f68<br/>      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> <dt>

[**IVMDVDDriveCollection**](ivmdvddrivecollection.md)
</dt> </dl>

 

