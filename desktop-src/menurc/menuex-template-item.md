---
title: MENUEX_TEMPLATE_ITEM estructura
description: Define un elemento de menú en una plantilla de menú extendida. Esta definición de estructura es solo para explicación; no está presente en ningún archivo de encabezado estándar.
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
ms.openlocfilehash: 6352c7ce596a59d69b21f1ba424ac50b471e13cd97320f0df184bce2e1abd295
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733910"
---
# <a name="menuex_template_item-structure"></a>ESTRUCTURA MENUEX \_ TEMPLATE \_ ITEM

Define un elemento de menú en una plantilla de menú extendida. Esta definición de estructura es solo para explicación; no está presente en ningún archivo de encabezado estándar.

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

Tipo de elemento de menú. Este miembro puede ser una combinación de los valores de tipo (a partir de MFT) enumerados con la [**estructura MENUITEMINFO.**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)

</dd> <dt>

**dwState**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Estado del elemento de menú. Este miembro puede ser una combinación de los valores de estado (empezando por MFS) enumerados con la [**estructura MENUITEMINFO.**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)

</dd> <dt>

**Uid**
</dt> <dd>

Tipo: **UINT**

</dd> <dd>

Identificador del elemento de menú. Se trata de un valor definido por la aplicación que identifica el elemento de menú. En un recurso de menú extendido, los elementos que abren menús desplegables o submenús, así como elementos de comando, pueden tener identificadores.

</dd> <dt>

**wFlags**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Especifica si el elemento de menú es el último elemento de la barra de menús, el menú desplegable, el submenú o el menú contextual, y si es un elemento que abre un menú desplegable o un submenú. Este miembro puede ser cero o más de estos valores. Para las aplicaciones de 32 bits, este miembro es una palabra; para las aplicaciones de 16 bits, es un byte.

<dt>

0x80
</dt> <dd>

La estructura define el último elemento de menú de la barra de menús, el menú desplegable, el submenú o el menú contextual.

</dd> <dt>

0x01
</dt> <dd>

La estructura define un elemento que abre un menú desplegable o un submenú. Las estructuras posteriores definen elementos de menú en el menú desplegable o submenú correspondiente.

</dd> </dl> </dd> <dt>

**szText**
</dt> <dd>

Tipo: **WCHAR**

</dd> <dd>

Texto del elemento de menú. Este miembro es una cadena Unicode terminada en NULL, alineada en un límite de palabras. El tamaño de la definición del elemento de menú varía en función de la longitud de esta cadena.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una plantilla de menú extendida consta de una estructura [**MENUEX \_ TEMPLATE \_ HEADER**](menuex-template-header.md) seguida de una o varias estructuras **MENUEX \_ TEMPLATE ITEM contiguas. \_** Las **estructuras MENUEX \_ TEMPLATE \_ ITEM,** que tienen una longitud variable, se alinean en los **límites DWORD.** Para crear un menú a partir de una plantilla de menú extendido en memoria, use la [**función LoadMenuIndirect.**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)

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

[**ENCABEZADO DE PLANTILLA \_ MENUEX \_**](menuex-template-header.md)
</dt> <dt>

[**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Menús](menus.md)
</dt> </dl>

 

 





