---
description: Especifica una referencia a una superficie sin comprimir.
ms.assetid: 01F9C9F9-8EB4-49D5-91F0-89B4C40DDDC8
title: DXVA_PicEntry_HEVC estructura (Dxva.h)
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
ms.openlocfilehash: 6b7b9ef471ba5d7d7c9ecd294bf2cdf1ff10a97174fe66529d1f251894f286fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117879739"
---
# <a name="dxva_picentry_hevc-structure"></a>Estructura \_ DE DXVA PicEntry \_ HEVC

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

Marca opcional de 1 bit asociada a la superficie. El significado de la marca depende del contexto. Por ejemplo, puede especificar si el marco de referencia es una referencia a largo plazo o una referencia a corto plazo.

</dd> <dt>

**bPicEntry**
</dt> <dd>

Accede a los 8 bits completos de la unión.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                           |
| Header<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation estructuras](media-foundation-structures.md)
</dt> </dl>

 

 




