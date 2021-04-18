---
description: Contiene información de formato para la recompresión inteligente.
ms.assetid: 471a7b4a-e639-443b-a30e-870b747e072c
title: Estructura SCompFmt0 (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SCompFmt0
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: ad5a5277718e8d414d64a86b9c31739cf576736a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680190"
---
# <a name="scompfmt0-structure"></a>Estructura SCompFmt0

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

Contiene información de formato para la recompresión inteligente.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _SCompFmt0 {
  long          nFormatId;
  AM_MEDIA_TYPE MediaType;
} SCompFmt0;
```



## <a name="members"></a>Miembros

<dl> <dt>

**nFormatId**
</dt> <dd>

Sector debe ser cero.

</dd> <dt>

**MediaType**
</dt> <dd>

[**AM \_ Estructura de \_ tipo de medio**](/windows/win32/api/strmif/ns-strmif-am_media_type) que describe el formato de compresión.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>QEDIT. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAMTimelineGroup::GetSmartRecompressFormat**](iamtimelinegroup-getsmartrecompressformat.md)
</dt> <dt>

[**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)
</dt> </dl>

 

 




