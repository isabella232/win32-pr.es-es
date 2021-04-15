---
description: Especifica una referencia a una superficie sin comprimir.
ms.assetid: 01F9C9F9-8EB4-49D5-91F0-89B4C40DDDC8
title: DXVA_PicEntry_HEVC estructura (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_PicEntry_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: a2c4856452d0f8010e8f97126b4e660557ea40ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648173"
---
# <a name="dxva_picentry_hevc-structure"></a>PicEntry de DXVA \_ \_ HEVC estructura

Especifica una referencia a una superficie sin comprimir.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _DXVA_PicEntry_HEVC {
  union {
    struct {
      UCHAR  Index7Bits  :7;
      UCHAR  AssociatedFlag   :1;
    };
    UCHAR  bPicEntry;
  };
} DXVA_PicEntry_HEVC, *PDXVA_PicEntry_HEVC;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Index7Bits**
</dt> <dd>

Índice que identifica una superficie sin comprimir.

</dd> <dt>

**AssociatedFlag** 
</dt> <dd>

Marca de 1 bit opcional asociada a la superficie. El significado de la marca depende del contexto. Por ejemplo, puede especificar si el marco de referencia es una referencia a largo plazo o una referencia a corto plazo.

</dd> <dt>

**bPicEntry**
</dt> <dd>

Obtiene acceso a los 8 bits completos de la Unión.

</dd> </dl>

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

 

 




