---
description: Especifica los datos de control de segmento.
ms.assetid: ae3399e9-b78c-473d-8ed5-e570dfb676aa
title: DXVA_Slice_HEVC_Short estructura (Dxva.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172214"
---
# <a name="dxva_slice_hevc_short-structure"></a>Estructura corta \_ de HEVC de segmento \_ DXVA \_

Especifica los datos de control de segmento.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _DXVA_Slice_HEVC_Short {
  UINT   BSNALunitDataLocation;
  UINT   SliceBytesInBuffer;
  USHORT wBadSliceChopping;
} DXVA_Slice_HEVC_Short, *LPDXVA_Slice_HEVC_Short;
```



## <a name="members"></a>Members

<dl> <dt>

**BSNALunitDataLocation**
</dt> <dd>

Especifica la ubicación de la unidad NAL.

</dd> <dt>

**SliceBytesInBuffer**
</dt> <dd>

Número de bytes del búfer de datos de flujo de bits asociados a esta estructura de datos de control de segmento.

</dd> <dt>

**wBadSliceChopping**
</dt> <dd>

Si se usa el análisis de secuencia de bits fuera del host, este valor indica el corte de segmentos no válidos y contiene uno de los valores siguientes:



| Requisito | Value |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Value | Descripción                                                                                                                                                                                                                                             |
| 0     | Todos los bits del segmento se encuentran en el búfer de datos de secuencia de bits correspondiente.                                                                                                                                                                      |
| 1     | El búfer de datos de secuencia de bits contiene el inicio del segmento, pero no todo el segmento, porque el búfer está lleno.                                                                                                                                        |
| 2     | El búfer de datos de flujo de bits contiene el final del segmento. No contiene el inicio del segmento, porque el inicio del segmento se encontraba en el búfer de datos de flujo de bits anterior.                                                                  |
| 3     | El búfer de datos de flujo de bits no contiene el inicio del segmento porque el inicio del segmento se encontraba en el búfer de datos de flujo de bits anterior y no contiene el final del segmento porque el búfer de datos de secuencia de bits actual también está lleno. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

**DXVA \_ Slice \_ HEVC \_ Short contiene** datos de control de segmento que se pasan al acelerador de hardware desde el descodificador de software host.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation estructuras](media-foundation-structures.md)
</dt> </dl>

 

 




