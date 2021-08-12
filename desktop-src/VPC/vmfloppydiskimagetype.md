---
title: Enumeración VMFstonepyDiskImageType (VPCCOMInterfaces.h)
description: Especifica los formatos de disquete.
ms.assetid: 7eb504c0-dfb7-45eb-a943-b453b5f8ca63
keywords:
- VMFstonepyDiskImageType (enumeración de PC virtual)
topic_type:
- apiref
api_name:
- VMFloppyDiskImageType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b00daad9cf9abc0f713e5f3b5f530d2facd696b6f48bb17167b0d4ddecb76d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591440"
---
# <a name="vmfloppydiskimagetype-enumeration"></a>Enumeración VMFstonepyDiskImageType

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Especifica los formatos de disquete.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmFloppyDiskImage_Unknown                = 0,
  vmFloppyDiskImage_LowDensity             = 1,
  vmFloppyDiskImage_HighDensity            = 2,
  vmFloppyDiskImage_DMF                    = 3,
  vmFloppyDiskImage_LowDensitySingleSided  = 4,
  vmFloppyDiskImage_MediumDensity          = 5,
  vmFloppyDiskImage_HighDensityMSS         = 6
} VMFloppyDiskImageType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="vmFloppyDiskImage_Unknown"></span><span id="vmfloppydiskimage_unknown"></span><span id="VMFLOPPYDISKIMAGE_UNKNOWN"></span>**vmFstonepyDiskImage \_ Unknown**
</dt> <dd>

Formato desconocido.

</dd> <dt>

<span id="vmFloppyDiskImage_LowDensity"></span><span id="vmfloppydiskimage_lowdensity"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITY"></span>**vmFstonepyDiskImage \_ LowDensity**
</dt> <dd>

Formato de baja densidad (720 000).

</dd> <dt>

<span id="vmFloppyDiskImage_HighDensity"></span><span id="vmfloppydiskimage_highdensity"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITY"></span>**vmFstonepyDiskImage \_ HighDensity**
</dt> <dd>

Un formato de alta densidad (1,44 MB).

</dd> <dt>

<span id="vmFloppyDiskImage_DMF"></span><span id="vmfloppydiskimage_dmf"></span><span id="VMFLOPPYDISKIMAGE_DMF"></span>**vmFstonepyDiskImage \_ DMF**
</dt> <dd>

Formato de medio de distribución (1,68 Mb).

</dd> <dt>

<span id="vmFloppyDiskImage_LowDensitySingleSided"></span><span id="vmfloppydiskimage_lowdensitysinglesided"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITYSINGLESIDED"></span>**vmFstonepyDiskImage \_ LowDensitySingleSided**
</dt> <dd>

Formato de baja densidad de un solo lado.

</dd> <dt>

<span id="vmFloppyDiskImage_MediumDensity"></span><span id="vmfloppydiskimage_mediumdensity"></span><span id="VMFLOPPYDISKIMAGE_MEDIUMDENSITY"></span>**vmFstonepyDiskImage \_ MediumDensity**
</dt> <dd>

Formato de densidad media (1,2 MB).

</dd> <dt>

<span id="vmFloppyDiskImage_HighDensityMSS"></span><span id="vmfloppydiskimage_highdensitymss"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITYMSS"></span>**vmFstonepyDiskImage \_ HighDensityMSS**
</dt> <dd>

Un tamaño de varios sectores (MSS) de alta densidad, utilizado por el formato de distribución eXtended (XDF).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMVirtualPC::CreateFstonepyDiskImage**](ivmvirtualpc-createfloppydiskimage.md)
</dt> <dt>

[**IVMVirtualPC::GetFstonepyDiskImageType**](ivmvirtualpc-getfloppydiskimagetype.md)
</dt> </dl>

 

