---
title: Estructura DLGTEMPLATEEX
description: Una plantilla de cuadro de diálogo extendido comienza con un encabezado DLGTEMPLATEEX que describe el cuadro de diálogo y especifica el número de controles del cuadro de diálogo.
ms.assetid: 9f016cc6-56e2-45d3-8773-1b405fc10d29
keywords:
- Cuadros de diálogo de estructura DLGTEMPLATEEX
topic_type:
- apiref
api_name:
- DLGTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab23b93a72edb2da6784797dd47bdfb4a839e2e9ce662adfc6ffbe09e468ac17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118503456"
---
# <a name="dlgtemplateex-structure"></a>Estructura DLGTEMPLATEEX

Una plantilla de cuadro de diálogo extendido comienza con un encabezado **DLGTEMPLATEEX** que describe el cuadro de diálogo y especifica el número de controles del cuadro de diálogo. Para cada control de un cuadro de diálogo, una plantilla de cuadro de diálogo extendido tiene un bloque de datos que usa el formato [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) para describir el control.

La **estructura DLGTEMPLATEEX** no se define en ningún archivo de encabezado estándar. La definición de estructura se proporciona aquí para explicar el formato de una plantilla extendida para un cuadro de diálogo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  WORD      dlgVer;
  WORD      signature;
  DWORD     helpID;
  DWORD     exStyle;
  DWORD     style;
  WORD      cDlgItems;
  short     x;
  short     y;
  short     cx;
  short     cy;
  sz_Or_Ord menu;
  sz_Or_Ord windowClass;
  WCHAR     title[titleLen];
  WORD      pointsize;
  WORD      weight;
  BYTE      italic;
  BYTE      charset;
  WCHAR     typeface[stringLen];
} DLGTEMPLATEEX;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dlgVer**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Número de versión de la plantilla de cuadro de diálogo extendida. Este miembro debe establecerse en 1.

</dd> <dt>

**firma**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Indica si una plantilla es una plantilla de cuadro de diálogo extendida. Si **se ha** 0xFFFF firma, se trata de una plantilla de cuadro de diálogo extendida. En este caso, el **miembro dlgVer** especifica el número de versión de la plantilla. Si **signature** es cualquier valor que no sea 0xFFFF, se trata de una plantilla de cuadro de diálogo estándar que usa las estructuras [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) y [**DLGITEMTEMPLATE.**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate)

</dd> <dt>

**helpID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Identificador de contexto de ayuda para la ventana del cuadro de diálogo. Cuando el sistema envía un [**mensaje DE AYUDA \_ DE WM,**](../shell/wm-help.md) pasa este valor en el **miembro wContextId** de la [**estructura HELPINFO.**](/windows/win32/api/winuser/ns-winuser-helpinfo)

</dd> <dt>

**exStyle**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Estilos de ventanas extendidos. Este miembro no se usa al crear cuadros de diálogo, pero las aplicaciones que usan plantillas de cuadro de diálogo pueden usarlo para crear otros tipos de ventanas. Para obtener una lista de valores, vea [**Estilos de ventana extendidos.**](/windows/desktop/winmsg/extended-window-styles)

</dd> <dt>

**style**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Estilo del cuadro de diálogo. Este miembro puede ser una combinación de valores de estilo de [ventana y](/windows/desktop/winmsg/window-styles) valores de estilo de cuadro [de diálogo](dialog-box-styles.md).

Si **style** incluye el estilo de cuadro de diálogo **\_ DS SETFONT** o **DS \_ SHELLFONT,** el encabezado  **DLGTEMPLATEEX** de la plantilla de cuadro de diálogo extendido contiene cuatro miembros adicionales **(pointsize**, weight , **italic** y **typeface)** que describen la fuente que se usará para el texto en el área cliente y los controles del cuadro de diálogo. Si es posible, el sistema crea una fuente según los valores especificados en estos miembros. A continuación, el sistema envía un [**mensaje \_ WM SETFONT**](/windows/desktop/winmsg/wm-setfont) al cuadro de diálogo y a cada control para proporcionar un identificador a la fuente.

Para obtener más información, vea [Fuentes de cuadro de diálogo](about-dialog-boxes.md).

</dd> <dt>

**cDlgItems**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Número de controles del cuadro de diálogo.

</dd> <dt>

**x**
</dt> <dd>

Tipo: **short**

</dd> <dd>

Coordenada x, en unidades de cuadro de diálogo, de la esquina superior izquierda del cuadro de diálogo.

</dd> <dt>

**y**
</dt> <dd>

Tipo: **short**

</dd> <dd>

Coordenada y, en unidades de cuadro de diálogo, de la esquina superior izquierda del cuadro de diálogo.

</dd> <dt>

**Cx**
</dt> <dd>

Tipo: **short**

</dd> <dd>

Ancho, en unidades de cuadro de diálogo, del cuadro de diálogo.

</dd> <dt>

**Cy**
</dt> <dd>

Tipo: **short**

</dd> <dd>

Alto, en unidades de cuadro de diálogo, del cuadro de diálogo.

</dd> <dt>

**Menú**
</dt> <dd>

Tipo: **sz \_ o \_ Ord**

</dd> <dd>

Matriz de longitud variable de elementos de 16 bits que identifica un recurso de menú para el cuadro de diálogo. Si el primer elemento de esta matriz 0x0000, el cuadro de diálogo no tiene ningún menú y la matriz no tiene ningún otro elemento. Si el primer elemento 0xFFFF, la matriz tiene un elemento adicional que especifica el valor ordinal de un recurso de menú en un archivo ejecutable. Si el primer elemento tiene cualquier otro valor, el sistema trata la matriz como una cadena Unicode terminada en NULL que especifica el nombre de un recurso de menú en un archivo ejecutable.

</dd> <dt>

**windowClass**
</dt> <dd>

Tipo: **sz \_ o \_ Ord**

</dd> <dd>

Matriz de longitud variable de elementos de 16 bits que identifica la clase de ventana del cuadro de diálogo. Si el primer elemento de la matriz es 0x0000, el sistema usa la clase de cuadro de diálogo predefinida para el cuadro de diálogo y la matriz no tiene ningún otro elemento. Si el primer elemento se 0xFFFF, la matriz tiene un elemento adicional que especifica el valor ordinal de una clase de ventana del sistema predefinida. Si el primer elemento tiene cualquier otro valor, el sistema trata la matriz como una cadena Unicode terminada en NULL que especifica el nombre de una clase de ventana registrada.

</dd> <dt>

**title**
</dt> <dd>

Tipo: **WCHAR \[ titleLen \]**

</dd> <dd>

Título del cuadro de diálogo. Si el primer elemento de esta matriz 0x0000, el cuadro de diálogo no tiene ningún título y la matriz no tiene ningún otro elemento.

</dd> <dt>

**pointsize**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Tamaño de punto de la fuente que se usará para el texto del cuadro de diálogo y sus controles.

Este miembro solo está presente si el **miembro de** estilo especifica **DS \_ SETFONT** o **DS \_ SHELLFONT**.

</dd> <dt>

**weight**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

El grosor de la fuente. Tenga en cuenta que, aunque puede ser cualquiera de los valores enumerados para el miembro **lfWeight** de la estructura [**LOGFONT,**](/windows/win32/api/wingdi/ns-wingdi-logfonta) cualquier valor que se utilice se cambiará automáticamente a **FW \_ NORMAL.**

Este miembro solo está presente si el **miembro de** estilo especifica **DS \_ SETFONT** o **DS \_ SHELLFONT**.

</dd> <dt>

**cursiva**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Indica si la fuente está en cursiva. Si este valor es **TRUE,** la fuente está en cursiva.

Este miembro solo está presente si el **miembro de** estilo especifica **DS \_ SETFONT** o **DS \_ SHELLFONT**.

</dd> <dt>

**Charset**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Juego de caracteres que se va a usar. Para obtener más información, vea el **miembro lfcharset** de [**LOGFONT.**](/windows/win32/api/wingdi/ns-wingdi-logfonta)

Este miembro solo está presente si el **miembro de** estilo especifica **DS \_ SETFONT** o **DS \_ SHELLFONT**.

</dd> <dt>

**Tipografía**
</dt> <dd>

Tipo: **WCHAR \[ stringLen \]**

</dd> <dd>

Nombre del tipo de letra de la fuente.

Este miembro solo está presente si el **miembro de** estilo especifica **DS \_ SETFONT** o **DS \_ SHELLFONT**.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Puede usar una plantilla de cuadro de diálogo extendida en lugar de una plantilla de cuadro de diálogo estándar en las funciones [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**DialogBoxIndirectParam,**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama) [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)y [**DialogBoxIndirect.**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)

Después del **encabezado DLGTEMPLATEEX** de una plantilla de cuadro de diálogo extendido hay una o varias estructuras [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) que describen los controles del cuadro de diálogo. El **miembro cDlgItems** de la estructura **DLGITEMTEMPLATEEX** especifica el número de estructuras **DLGITEMTEMPLATEEX** que se siguen en la plantilla.

Cada [**estructura DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) de la plantilla debe alinearse en un **límite DWORD.** Si **el** miembro de estilo especifica el estilo **\_ DS SETFONT** o **DS \_ SHELLFONT,** la primera estructura **DLGITEMTEMPLATEEX** comienza en el primer límite **DWORD** después de la cadena de tipo **de** letra. Si no se especifican estos estilos, la primera estructura comienza en el primer **límite DWORD** después de la **cadena de** título.

Las **matrices** de menús , **windowClass**, **title** y **typeface** deben estar alineadas en los límites de **WORD.**

Si especifica cadenas de caracteres en el menú **,** **windowClass**, **title** y **matrices de** tipografía, debe usar cadenas Unicode. Use la [**función MultiByteToWideChar para**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) generar estas cadenas Unicode a partir de cadenas ANSI.

Los **miembros x**, **y**, **cx** y **cy** especifican valores en unidades de cuadro de diálogo. Puede convertir estos valores en unidades de pantalla (píxeles) mediante la [**función MapDialogRect.**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md)
</dt> <dt>

[**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Cuadros de diálogo](dialog-boxes.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> </dl>

 

