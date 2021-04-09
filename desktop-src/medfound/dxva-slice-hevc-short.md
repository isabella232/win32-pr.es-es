---
description: Especifica los datos de control de sector.
ms.assetid: ae3399e9-b78c-473d-8ed5-e570dfb676aa
title: DXVA_Slice_HEVC_Short estructura (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_Slice_HEVC_Short
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 0d0f88e1534ef3d901023ebdee8ce9c36a8c2cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080315"
---
# <a name="dxva_slice_hevc_short-structure"></a>\_Estructura corta del segmento de DXVA \_ HEVC \_

Especifica los datos de control de sector.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _DXVA_Slice_HEVC_Short {
  UINT   BSNALunitDataLocation;
  UINT   SliceBytesInBuffer;
  USHORT wBadSliceChopping;
} DXVA_Slice_HEVC_Short, *LPDXVA_Slice_HEVC_Short;
```



## <a name="members"></a>Miembros

<dl> <dt>

**BSNALunitDataLocation**
</dt> <dd>

Especifica la ubicación de la unidad NAL.

</dd> <dt>

**SliceBytesInBuffer**
</dt> <dd>

El número de bytes del búfer de datos fragmentada que están asociados a esta estructura de datos del control de segmento.

</dd> <dt>

**wBadSliceChopping**
</dt> <dd>

Si se usa el análisis de fragmentada fuera del host, este valor indica el segmento incorrecto cortar y contiene uno de los siguientes valores:



| Requisito | Value |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Value | Descripción                                                                                                                                                                                                                                             |
| 0     | Todos los bits del segmento se encuentran en el búfer de datos de fragmentada correspondiente.                                                                                                                                                                      |
| 1     | El búfer de datos fragmentada contiene el inicio del segmento, pero no el segmento completo, porque el búfer está lleno.                                                                                                                                        |
| 2     | El búfer de datos fragmentada contiene el final del segmento. No contiene el inicio del segmento, porque el inicio del segmento se encontraba en el búfer de datos fragmentada anterior.                                                                  |
| 3     | El búfer de datos fragmentada no contiene el inicio del segmento porque el inicio del segmento se encontraba en el búfer de datos fragmentada anterior y no contiene el final del segmento porque el búfer de datos fragmentada actual también está lleno. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

**DXVA \_ El segmento \_ HEVC \_ Short** contiene datos de control de segmento que se pasan al Acelerador de hardware desde el descodificador de software del host.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation estructuras](media-foundation-structures.md)
</dt> </dl>

 

 




