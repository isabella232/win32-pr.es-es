---
title: Enumeración VMFloppyDriveAttachmentType (VPCCOMInterfaces. h)
description: Especifica lo que se adjunta a una unidad de disquete.
ms.assetid: aba1be92-bd07-4edb-ad62-f8d76dbd19b9
keywords:
- Enumeración de VMFloppyDriveAttachmentType Virtual PC
topic_type:
- apiref
api_name:
- VMFloppyDriveAttachmentType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a4a291778b2fea8039bf41fc04799a03421342f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996582"
---
# <a name="vmfloppydriveattachmenttype-enumeration"></a>Enumeración VMFloppyDriveAttachmentType

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Especifica lo que se adjunta a una unidad de disquete.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum  { 
  vmFloppyDrive_None       = 0,
  vmFloppyDrive_Image      = 1,
  vmFloppyDrive_HostDrive  = 2
} VMFloppyDriveAttachmentType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="vmFloppyDrive_None"></span><span id="vmfloppydrive_none"></span><span id="VMFLOPPYDRIVE_NONE"></span>**vmFloppyDrive \_ ninguno**
</dt> <dd>

No hay nada adjunto.

</dd> <dt>

<span id="vmFloppyDrive_Image"></span><span id="vmfloppydrive_image"></span><span id="VMFLOPPYDRIVE_IMAGE"></span>**imagen de vmFloppyDrive \_**
</dt> <dd>

Hay un archivo de imagen de disquete conectado.

</dd> <dt>

<span id="vmFloppyDrive_HostDrive"></span><span id="vmfloppydrive_hostdrive"></span><span id="VMFLOPPYDRIVE_HOSTDRIVE"></span>**vmFloppyDrive \_ HostDrive**
</dt> <dd>

Hay una unidad de disquete de host conectada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMFloppyDrive:: Attachment**](ivmfloppydrive-attachment.md)
</dt> </dl>

 

