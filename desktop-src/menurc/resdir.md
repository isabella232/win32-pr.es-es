---
title: Estructura RESDIR
description: Contiene información sobre un icono o componente de cursor individual de un grupo de recursos. Hay una estructura RESDIR para cada componente de grupo. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcestructures\resdir.htm
keywords:
- Menús de la estructura RESDIR y otros recursos
topic_type:
- apiref
api_name:
- RESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b854a4af3367131f6a559e1fef5899fae8b81107
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695885"
---
# <a name="resdir-structure"></a>Estructura RESDIR

Contiene información sobre un icono o componente de cursor individual de un grupo de recursos. Hay una estructura **RESDIR** para cada componente de grupo. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.

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

El ancho, el alto y el recuento de color del icono indicado.

</dd> <dt>

**Cursor**
</dt> <dd>

Tipo: **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

Ancho y alto del cursor indicado.

</dd> <dt>

**Planos**
</dt> <dd>

Tipo: **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

Número de planos de color del mapa de bits del icono o del cursor.

</dd> <dt>

**BitCount**
</dt> <dd>

Tipo: **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

Número de bits por píxel en el mapa de bits del icono o del cursor.

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

## <a name="remarks"></a>Observaciones

Una o varias estructuras **RESDIR** siguen inmediatamente a la estructura [**NEWHEADER**](newheader.md) del archivo. res. El miembro **ResCount** de la estructura **NEWHEADER** especifica el número de estructuras **RESDIR** . Tenga en cuenta que la estructura **RESDIR** consta de una estructura [**ICONRESDIR**](iconresdir.md) o una estructura [**CURSORDIR**](cursordir.md) seguida de los miembros **aviones**, **BitCount**, **BytesInRes** y **IconCursorId** . Si la estructura **RESDIR** contiene información sobre un cursor, las dos primeras **palabras** que escribe el compilador de recursos en el recurso de [ \_ cursor RT](/windows/desktop/menurc/resource-types) son los miembros **xHotSpot** y **yHotSpot** de la estructura [**LOCALHEADER**](localheader.md) .

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

**Vista**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

