---
title: CURSORDIR (estructura)
description: Contiene las dimensiones de una imagen de cursor individual en un grupo de recursos. La definición de estructura que se proporciona aquí es solo para una explicación; no está presente en ningún archivo de encabezado estándar.
ms.assetid: bc826fd6-74a2-470b-8d19-437cdeb0727d
keywords:
- Menús de estructura CURSORDIR y otros recursos
topic_type:
- apiref
api_name:
- CURSORDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7194d6af764a9f66a2bf1a059f9c387cde13bb05728a7e96ccec470fa3650c81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602175"
---
# <a name="cursordir-structure"></a>CURSORDIR (estructura)

Contiene las dimensiones de una imagen de cursor individual en un grupo de recursos. La definición de estructura que se proporciona aquí es solo para una explicación; no está presente en ningún archivo de encabezado estándar.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  WORD Width;
  WORD Height;
} CURSORDIR;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Width**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Ancho del cursor, en píxeles. Los valores aceptables son 16, 32 y 64.

</dd> <dt>

**Height**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Alto del cursor, en píxeles. Los valores aceptables son 16, 32 y 64.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **estructura CURSORDIR** se pasa en la [**estructura RESDIR**](resdir.md) si la **estructura RESDIR** describe un cursor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**RESDIR**](resdir.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

 





