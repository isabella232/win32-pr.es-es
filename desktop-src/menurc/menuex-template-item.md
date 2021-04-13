---
title: Estructura de MENUEX_TEMPLATE_ITEM
description: Define un elemento de menú en una plantilla de menú extendida. Esta definición de estructura solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: f6e2fd0a-16b8-48e3-8597-341085a7adbd
keywords:
- MENUEX_TEMPLATE_ITEM menús de estructura y otros recursos
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_ITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca1f73d1174590db5948f54f5c51c91a8c65a8c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535085"
---
# <a name="menuex_template_item-structure"></a>Estructura del elemento de \_ plantilla MENUEX \_

Define un elemento de menú en una plantilla de menú extendida. Esta definición de estructura solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.

## <a name="syntax"></a>Sintaxis

```C++
typedef struct {
  DWORD dwType;
  DWORD dwState;
  UINT  uId;
  WORD  wFlags;
  WCHAR szText[1];
} MENUEX_TEMPLATE_ITEM;
```

## <a name="members"></a>Miembros

<dl> <dt>

**dwType**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

El tipo de elemento de menú. Este miembro puede ser una combinación de los valores de tipo (a partir de MFT) enumerados con la estructura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .

</dd> <dt>

**dwState**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Estado del elemento de menú. Este miembro puede ser una combinación de los valores de estado (empezando por MFS) enumerados con la estructura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .

</dd> <dt>

**uId**
</dt> <dd>

Tipo: **uint**

</dd> <dd>

Identificador del elemento de menú. Este es un valor definido por la aplicación que identifica el elemento de menú. En un recurso de menú extendido, los elementos que abren los menús desplegables o los submenús, así como los elementos de comando, pueden tener identificadores.

</dd> <dt>

**wFlags**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Especifica si el elemento de menú es el último elemento en la barra de menús, en el menú desplegable, en el submenú o en el menú contextual, y si es un elemento que abre un menú desplegable o un submenú. Este miembro puede tener cero o más de estos valores. En el caso de las aplicaciones de 32 bits, este miembro es una palabra; en el caso de las aplicaciones de 16 bits, es un byte.

<dt>

0x80
</dt> <dd>

La estructura define el último elemento de menú en la barra de menús, en el menú desplegable, en el submenú o en el menú contextual.

</dd> <dt>

0x01
</dt> <dd>

La estructura define un elemento que abre un menú desplegable o un submenú. Las estructuras posteriores definen los elementos de menú en el menú desplegable o submenú correspondiente.

</dd> </dl> </dd> <dt>

**szText**
</dt> <dd>

Tipo: **WCHAR**

</dd> <dd>

Texto del elemento de menú. Este miembro es una cadena Unicode terminada en null, alineada en un límite de palabras. El tamaño de la definición del elemento de menú varía en función de la longitud de esta cadena.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una plantilla de menú extendida está formada por una estructura de [**\_ \_ encabezado de plantilla de MENUEX**](menuex-template-header.md) , seguida de una o varias estructuras de **\_ \_ elemento de plantilla MENUEX** contiguas. Las estructuras de **\_ \_ elementos de plantilla MENUEX** , que son de longitud variable, se alinean en los límites **DWORD** . Para crear un menú a partir de una plantilla de menú extendida en memoria, use la función [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[**\_encabezado de plantilla MENUEX \_**](menuex-template-header.md)
</dt> <dt>

[**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

**Vista**
</dt> <dt>

[Menús](menus.md)
</dt> </dl>

 

 





