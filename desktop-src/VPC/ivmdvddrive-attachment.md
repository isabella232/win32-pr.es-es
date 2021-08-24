---
title: Propiedad IVMDVDDrive Attachment (VPCCOMInterfaces.h)
description: Recupera el tipo de medio conectado a la unidad de DVD dentro de la máquina virtual.
ms.assetid: 7ae1714d-e5e9-4f6a-85a6-c0b3c4d21820
keywords:
- Propiedad De datos adjuntos Pc virtual
- Propiedad de datos adjuntos Virtual PC , interfaz IVMDVDDrive
- IVMDVDDrive interface Virtual PC , Propiedad Attachment
topic_type:
- apiref
api_name:
- IVMDVDDrive.Attachment
- IVMDVDDrive.get_Attachment
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb1ef5263c428692ae41de0b1dadb25faec5b9229b37b9e33edcfbe9f922b92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473235"
---
# <a name="ivmdvddriveattachment-property"></a>Propiedad IVMDVDDrive::Attachment

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el tipo de medio conectado a la unidad de DVD dentro de la máquina virtual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Attachment(
  [out, retval] VMDVDDriveAttachmentType *driveAttachment
);
```



## <a name="property-value"></a>Valor de propiedad

Tipo de medio asociado. Para obtener una lista de valores, [**vea VMDVDDriveAttachmentType**](vmdvddriveattachmenttype.md).

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                       | Significado                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                          | La operación se realizó correctamente.<br/>               |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>            | El parámetro es **NULL.**<br/>                  |
| <dl> <dt>E \_ ERROR</dt> <dt>0x80004005</dt> </dl>               | Se produjo un error inesperado.<br/>           |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>    | No se encontró la máquina virtual.<br/>     |
| <dl> <dt>Máquina virtual \_ E \_ UNIDAD \_ NO VÁLIDA</dt> <dt>0xA0040502</dt> </dl> | La ubicación del bus para esta unidad no es válida.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>    | Se produjo un error inesperado.<br/>           |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMDVDDrive se define como \_ b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

