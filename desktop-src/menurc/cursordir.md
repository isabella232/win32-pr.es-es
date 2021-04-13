---
title: Estructura CURSORDIR
description: Contiene las dimensiones de una imagen de cursor individual de un grupo de recursos. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: bc826fd6-74a2-470b-8d19-437cdeb0727d
keywords:
- Menús de la estructura CURSORDIR y otros recursos
topic_type:
- apiref
api_name:
- CURSORDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2434bdf90248c2f1d6c5edf9425f0f35d698cd45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422547"
---
# <a name="cursordir-structure"></a>Estructura CURSORDIR

Contiene las dimensiones de una imagen de cursor individual de un grupo de recursos. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.

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

Tipo: **Word**

</dd> <dd>

Ancho del cursor, en píxeles. Los valores aceptables son 16, 32 y 64.

</dd> <dt>

**Height**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Alto del cursor, en píxeles. Los valores aceptables son 16, 32 y 64.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura **CURSORDIR** se pasa en la estructura [**RESDIR**](resdir.md) si la estructura **RESDIR** describe un cursor.

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

**Vista**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

 





