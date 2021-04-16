---
description: Contiene información de contexto de búsqueda.
ms.assetid: 4b865563-98c2-459b-bb2b-75420d51d6a7
title: Estructura de FIND_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIND_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7d6b6dea42c008178c22f6e342a64b2f8d193ec5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659381"
---
# <a name="find_info-structure"></a>BUSCAR \_ estructura de información

Contiene información de contexto de búsqueda.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _FIND_INFO {
  TAGID     tiIndex;
  TAGID     tiCurrent;
  TAGID     tiEndIndex;
  TAG       tName;
  DWORD     dwIndexRec;
  DWORD     dwFlags;
  ULONGLONG ullKey;
  union {
    LPCTSTR szName;
    DWORD   dwName;
    GUID    *pguidName;
  };
} FIND_INFO, *PFIND_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**tiIndex**
</dt> <dd>

**TAGID** del índice que se va a buscar.

</dd> <dt>

**tiCurrent**
</dt> <dd>

**TAGID** del elemento actual que se encontró.

</dd> <dt>

**tiEndIndex**
</dt> <dd>

El **TAGID** del último registro después de FindFirst si el índice es único.

</dd> <dt>

**tName**
</dt> <dd>

Tipo del elemento que se va a buscar. Vea [tipos de etiqueta](tag-types.md).

</dd> <dt>

**dwIndexRec**
</dt> <dd>

Contador interno que se usa para realizar un seguimiento del lugar en el que debe comenzar la siguiente operación de búsqueda.

</dd> <dt>

**dwFlags**
</dt> <dd>

Este miembro puede ser 0 o **SHIMDB \_ \_ Unique index \_ key** (0x00000001), lo que indica que se trata de un índice de clave única.

</dd> <dt>

**ullKey**
</dt> <dd>

Clave de la entrada actual.

</dd> <dt>

**szName**
</dt> <dd>

La cadena actual (si el tipo de etiqueta es el **tipo de etiqueta \_ \_ STRINGREF**).

</dd> <dt>

**dwName**
</dt> <dd>

Valor **DWORD** actual (si el tipo de etiqueta es **el \_ tipo \_ de etiqueta DWORD**).

</dd> <dt>

**pguidName**
</dt> <dd>

El valor GUID actual (si el tipo de etiqueta es el **tipo de etiqueta \_ \_ Binary** y la etiqueta es **tag \_ Database \_ ID**).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbFindFirstDWORDIndexedTag**](sdbfindfirstdwordindexedtag.md)
</dt> </dl>

 

 




