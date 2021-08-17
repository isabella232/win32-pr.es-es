---
description: Contiene información de contexto de búsqueda.
ms.assetid: 4b865563-98c2-459b-bb2b-75420d51d6a7
title: FIND_INFO estructura
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
ms.openlocfilehash: 1ee5eb66928322019a455c78d71abf5461e56b1296ae79d94b83c40c2d45379e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404788"
---
# <a name="find_info-structure"></a>Estructura \_ FIND INFO

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

TAGID **para** el índice en el que se va a buscar.

</dd> <dt>

**tiCurrent**
</dt> <dd>

TAGID **del** elemento actual que se ha ubicado.

</dd> <dt>

**tiEndIndex**
</dt> <dd>

TagID **del** último registro después de FindFirst si el índice es UNIQUE.

</dd> <dt>

**tName**
</dt> <dd>

Tipo del elemento que se va a encontrar. Vea [Tipos DE ETIQUETA.](tag-types.md)

</dd> <dt>

**dwIndexRec**
</dt> <dd>

Contador interno que se usa para realizar un seguimiento de dónde debe iniciarse la siguiente operación de búsqueda en el índice.

</dd> <dt>

**dwFlags**
</dt> <dd>

Este miembro puede ser 0 o **SHIMDB \_ INDEX UNIQUE \_ \_ KEY** (0x00000001), lo que indica que se trata de un índice de clave única.

</dd> <dt>

**ullKey**
</dt> <dd>

Clave de la entrada actual.

</dd> <dt>

**szName**
</dt> <dd>

Cadena actual (si el tipo de etiqueta es **TAG \_ TYPE \_ STRINGREF).**

</dd> <dt>

**dwName**
</dt> <dd>

Valor **DWORD** actual (si el tipo de etiqueta es **TAG \_ TYPE \_ DWORD).**

</dd> <dt>

**pguidName**
</dt> <dd>

Valor GUID actual (si el tipo de etiqueta es **TAG \_ TYPE \_ BINARY** y TAG es **TAG DATABASE \_ \_ ID**).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SdbFindFirstDWORDIndexedTag**](sdbfindfirstdwordindexedtag.md)
</dt> </dl>

 

 




