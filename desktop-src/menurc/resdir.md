---
title: Estructura RESDIR
description: Contiene información sobre un icono individual o un componente de cursor en un grupo de recursos. Hay una estructura RESDIR para cada componente de grupo. La definición de estructura que se proporciona aquí es solo para una explicación; no está presente en ningún archivo de encabezado estándar.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcestructures\resdir.htm
keywords:
- Menús de estructura RESDIR y otros recursos
topic_type:
- apiref
api_name:
- RESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9033e1f30e8f497b202fa8e3f84d4ecb582bb60c166f396a50ce194c9783075
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825585"
---
# <a name="resdir-structure"></a>Estructura RESDIR

Contiene información sobre un icono individual o un componente de cursor en un grupo de recursos. Hay una estructura **RESDIR** para cada componente de grupo. La definición de estructura que se proporciona aquí es solo para una explicación; no está presente en ningún archivo de encabezado estándar.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  ICONRESDIR Icon;
  CURSORDIR  Cursor;
  CURSORDIR  Planes;
  CURSORDIR  BitCount;
  CURSORDIR  BytesInRes;
  CURSORDIR  IconCursorId;
} RESDIR;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Icono**
</dt> <dd>

Tipo: **[ **ICONRESDIR**](iconresdir.md)**

</dd> <dd>

Ancho, alto y recuento de colores del icono indicado.

</dd> <dt>

**Cursor**
</dt> <dd>

Tipo: **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

Ancho y alto del cursor indicado.

</dd> <dt>

**Aviones**
</dt> <dd>

Tipo: **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

Número de planos de color en el icono o mapa de bits del cursor.

</dd> <dt>

**BitCount**
</dt> <dd>

Tipo: **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

Número de bits por píxel en el icono o mapa de bits del cursor.

</dd> <dt>

**BytesInRes**
</dt> <dd>

Tipo: **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

Tamaño del recurso, en bytes.

</dd> <dt>

**IconCursorId**
</dt> <dd>

Tipo: **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

Icono o cursor con un identificador ordinal único.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Una o varias **estructuras RESDIR** siguen inmediatamente la [**estructura NEWHEADER**](newheader.md) en el archivo .res. El **miembro ResCount** de la **estructura NEWHEADER** especifica el número de **estructuras RESDIR.** Tenga en cuenta que la estructura **RESDIR** consta de una estructura [**ICONRESDIR**](iconresdir.md) o una estructura [**CURSORDIR**](cursordir.md) seguida de los miembros **Planes**, **BitCount**, **BytesInRes** **e IconCursorId.** Si la estructura **RESDIR** contiene información sobre un cursor, las dos primeras palabras que el compilador de recursos escribe en el recurso [RT \_ CURSOR](/windows/desktop/menurc/resource-types) son los miembros **xHotSpot** **y yHotSpot** de la [**estructura LOCALHEADER.**](localheader.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CURSORDIR**](cursordir.md)
</dt> <dt>

[**ICONRESDIR**](iconresdir.md)
</dt> <dt>

[**LOCALHEADER**](localheader.md)
</dt> <dt>

[**NEWHEADER**](newheader.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

