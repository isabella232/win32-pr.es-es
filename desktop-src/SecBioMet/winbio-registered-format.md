---
title: WINBIO_REGISTERED_FORMAT estructura (Winbio \_ types.h)
description: Especifica un formato de datos registrado como un par propietario/formato.
ms.assetid: a178840e-81cc-4dd3-9d80-a181fa7fa888
keywords:
- WINBIO_REGISTERED_FORMAT estructura Windows API de marco biométrico
- PWINBIO_REGISTERED_FORMAT puntero de estructura Windows API de marco biométrico
topic_type:
- apiref
api_name:
- WINBIO_REGISTERED_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fcf871f3fc5f258de22e033e8a388968ab58c1a35e19829bf3d02a97ca60c53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909373"
---
# <a name="winbio_registered_format-structure"></a>Estructura DE \_ FORMATO REGISTRADO \_ DE WINBIO

La **estructura FORMATO REGISTRADO \_ \_ DE WINBIO** especifica un formato de datos registrado como un par propietario/formato.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WINBIO_REGISTERED_FORMAT {
  USHORT Owner;
  USHORT Type;
} WINBIO_REGISTERED_FORMAT, *PWINBIO_REGISTERED_FORMAT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Propietario**
</dt> <dd>

Valor de propietario asignado de IBIA (Asociación internacional del sector biométrico).

</dd> <dt>

**Tipo**
</dt> <dd>

Formato asignado por el propietario.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Dado Windows admite actualmente solo lectores de huellas digitales, se deben usar los siguientes valores en la **estructura DE FORMATO REGISTRADO \_ \_ DE WINBIO.**



| Constante                                    | Significado                                                                                                               |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| PROPIETARIO DEL FORMATO WINBIO \_ ANSI \_ 381 \_ \_<br/> | Comité Inter International para estándares de tecnologías de la información (INCITS) M1 (biométrica).<br/> |
| TIPO DE FORMATO WINBIO \_ ANSI \_ 381 \_ \_<br/>  | Formato de intercambio de datos basado en imágenes ANSI INCITS 381.<br/>                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de aplicación cliente](client-application-structures.md)
</dt> <dt>

[**Constantes DE FORMATO DE WINBIO \_ ANSI \_ 381 \_**](winbio-ansi-381-format-constants.md)
</dt> <dt>

[**ENCABEZADO ANSI \_ \_ \_ 381 \_ DE WINBIO BDB**](winbio-bdb-ansi-381-header.md)
</dt> <dt>

[**ENCABEZADO WINBIO \_ BIR \_**](winbio-bir-header.md)
</dt> </dl>

 

 





