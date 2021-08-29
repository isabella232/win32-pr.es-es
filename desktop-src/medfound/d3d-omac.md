---
description: Contiene un código de autenticación de mensajes (MAC).
ms.assetid: be5515fd-1936-46b8-9fc8-8d1f87048c38
title: D3D_OMAC estructura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3D_OMAC
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 05cf39bccc33eb1f993b0e86cfa89fc290832b422129441d99f028f3d826c3fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449554"
---
# <a name="d3d_omac-structure"></a>Estructura D3D \_ OMAC

Contiene un código de autenticación de mensajes (MAC).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3D_OMAC {
  BYTE Omac[D3D_OMAC_SIZE];
} D3D_OMAC;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Omac**
</dt> <dd>

Matriz de bytes que contiene el valor de MAC criptográfico del mensaje.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de vídeo de Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




