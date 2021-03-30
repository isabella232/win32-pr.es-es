---
title: Estructura DLGTEMPLATEEX
description: Una plantilla de cuadro de diálogo extendida comienza con un encabezado DLGTEMPLATEEX que describe el cuadro de diálogo y especifica el número de controles en el cuadro de diálogo.
ms.assetid: 9f016cc6-56e2-45d3-8773-1b405fc10d29
keywords:
- Cuadros de diálogo de la estructura DLGTEMPLATEEX
topic_type:
- apiref
api_name:
- DLGTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c3db7127e23e3133e11fe9c1600d37695e3b1ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534738"
---
# <a name="dlgtemplateex-structure"></a>Estructura DLGTEMPLATEEX

Una plantilla de cuadro de diálogo extendida comienza con un encabezado **DLGTEMPLATEEX** que describe el cuadro de diálogo y especifica el número de controles en el cuadro de diálogo. Para cada control de un cuadro de diálogo, una plantilla de cuadro de diálogo extendida tiene un bloque de datos que usa el formato [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) para describir el control.

La estructura **DLGTEMPLATEEX** no está definida en ningún archivo de encabezado estándar. Aquí se proporciona la definición de la estructura para explicar el formato de una plantilla extendida para un cuadro de diálogo.

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

Tipo: **Word**

</dd> <dd>

Número de versión de la plantilla de cuadro de diálogo extendido. Este miembro debe establecerse en 1.

</dd> <dt>

**firma**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Indica si una plantilla es una plantilla de cuadro de diálogo extendida. Si la **firma** es 0xFFFF, se trata de una plantilla de cuadro de diálogo extendida. En este caso, el miembro **dlgVer** especifica el número de versión de la plantilla. Si **Signature** es cualquier valor distinto de 0xFFFF, se trata de una plantilla de cuadro de diálogo estándar que usa las estructuras [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) y [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) .

</dd> <dt>

**helpID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Identificador del contexto de ayuda para la ventana del cuadro de diálogo. Cuando el sistema envía un mensaje de [**\_ ayuda de WM**](../shell/wm-help.md) , pasa este valor en el miembro **WContextId** de la estructura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) .

</dd> <dt>

**exStyle**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Los estilos extendidos de Windows. Este miembro no se usa al crear cuadros de diálogo, pero las aplicaciones que usan plantillas de cuadro de diálogo pueden usarlo para crear otros tipos de ventanas. Para obtener una lista de valores, vea [**estilos extendidos de ventana**](/windows/desktop/winmsg/extended-window-styles).

</dd> <dt>

**style**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Estilo del cuadro de diálogo. Este miembro puede ser una combinación de [valores de estilo de ventana](/windows/desktop/winmsg/window-styles) y [valores de estilo de cuadro de diálogo](dialog-box-styles.md).

Si **Style** incluye el estilo de cuadro de diálogo **\_ SHELLFONT** de **DS \_ SETFONT** o DS, el encabezado **DLGTEMPLATEEX** de la plantilla de cuadro de diálogo extendido contiene cuatro miembros adicionales ( **Pointing**, **Weight**, **Italic** y **Font) que** describen la fuente que se va a usar para el texto en el área cliente y los controles del cuadro de diálogo. Si es posible, el sistema crea una fuente según los valores especificados en estos miembros. A continuación, el sistema envía un mensaje de [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont) al cuadro de diálogo y a cada control para proporcionar un identificador a la fuente.

Para obtener más información, vea [fuentes de cuadros de diálogo](about-dialog-boxes.md).

</dd> <dt>

**cDlgItems**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Número de controles del cuadro de diálogo.

</dd> <dt>

**x**
</dt> <dd>

Tipo: **Short**

</dd> <dd>

La coordenada x, en unidades de cuadro de diálogo, de la esquina superior izquierda del cuadro de diálogo.

</dd> <dt>

**y**
</dt> <dd>

Tipo: **Short**

</dd> <dd>

La coordenada y, en unidades de cuadro de diálogo, de la esquina superior izquierda del cuadro de diálogo.

</dd> <dt>

**serie**
</dt> <dd>

Tipo: **Short**

</dd> <dd>

Ancho, en unidades de cuadro de diálogo, del cuadro de diálogo.

</dd> <dt>

**CY**
</dt> <dd>

Tipo: **Short**

</dd> <dd>

Alto, en unidades de cuadro de diálogo, del cuadro de diálogo.

</dd> <dt>

**MENU**
</dt> <dd>

Tipo: **SZ \_ o \_ Ord**

</dd> <dd>

Matriz de longitud variable de elementos de 16 bits que identifica un recurso de menú para el cuadro de diálogo. Si el primer elemento de esta matriz es 0x0000, el cuadro de diálogo no tiene ningún menú y la matriz no tiene ningún otro elemento. Si el primer elemento es 0xFFFF, la matriz tiene un elemento adicional que especifica el valor ordinal de un recurso de menú en un archivo ejecutable. Si el primer elemento tiene cualquier otro valor, el sistema trata la matriz como una cadena Unicode terminada en null que especifica el nombre de un recurso de menú en un archivo ejecutable.

</dd> <dt>

**windowClass**
</dt> <dd>

Tipo: **SZ \_ o \_ Ord**

</dd> <dd>

Matriz de longitud variable de elementos de 16 bits que identifica la clase de ventana del cuadro de diálogo. Si el primer elemento de la matriz es 0x0000, el sistema utiliza la clase de cuadro de diálogo predefinida para el cuadro de diálogo y la matriz no tiene ningún otro elemento. Si el primer elemento es 0xFFFF, la matriz tiene un elemento adicional que especifica el valor ordinal de una clase de ventana del sistema predefinida. Si el primer elemento tiene cualquier otro valor, el sistema trata la matriz como una cadena Unicode terminada en null que especifica el nombre de una clase de ventana registrada.

</dd> <dt>

**title**
</dt> <dd>

Tipo: **WCHAR \[ titleLen \]**

</dd> <dd>

Título del cuadro de diálogo. Si el primer elemento de esta matriz es 0x0000, el cuadro de diálogo no tiene ningún título y la matriz no tiene ningún otro elemento.

</dd> <dt>

**PointSize**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Tamaño de punto de la fuente que se va a usar para el texto del cuadro de diálogo y sus controles.

Este miembro solo está presente si el miembro de **estilo** especifica **DS \_ SETFONT** o **DS \_ SHELLFONT**.

</dd> <dt>

**weight**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

El grosor de la fuente. Tenga en cuenta que, aunque puede ser cualquiera de los valores enumerados para el miembro **lfWeight** de la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) , cualquier valor que se use se cambiará automáticamente a **FW \_ normal**.

Este miembro solo está presente si el miembro de **estilo** especifica **DS \_ SETFONT** o **DS \_ SHELLFONT**.

</dd> <dt>

**cursiva**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Indica si la fuente está en cursiva. Si este valor es **true**, la fuente está en cursiva.

Este miembro solo está presente si el miembro de **estilo** especifica **DS \_ SETFONT** o **DS \_ SHELLFONT**.

</dd> <dt>

**charset**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Juego de caracteres que se va a utilizar. Para obtener más información, vea el miembro **lfcharset** de [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta).

Este miembro solo está presente si el miembro de **estilo** especifica **DS \_ SETFONT** o **DS \_ SHELLFONT**.

</dd> <dt>

**tipográfico**
</dt> <dd>

Tipo: **WCHAR \[ stringLen \]**

</dd> <dd>

Nombre del tipo de letra de la fuente.

Este miembro solo está presente si el miembro de **estilo** especifica **DS \_ SETFONT** o **DS \_ SHELLFONT**.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede usar una plantilla de cuadro de diálogo extendida en lugar de una plantilla de cuadro de diálogo estándar en las funciones [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)y [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) .

Seguir el encabezado de **DLGTEMPLATEEX** en una plantilla de cuadro de diálogo extendida es una o varias estructuras [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) que describen los controles del cuadro de diálogo. El miembro **cDlgItems** de la estructura **DLGITEMTEMPLATEEX** especifica el número de estructuras **DLGITEMTEMPLATEEX** que siguen en la plantilla.

Cada estructura [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) de la plantilla debe estar alineada en un límite **DWORD** . Si el miembro de **estilo** especifica el estilo de **DS \_ SETFONT** o **DS \_ SHELLFONT** , la primera estructura de **DLGITEMTEMPLATEEX** comienza en el primer límite **DWORD** después de la cadena de tipo de **letra** . Si no se especifican estos estilos, la primera estructura comienza en el primer límite **DWORD** después de la cadena de **título** .

Las matrices de **menú**, **windowClass**, **título** y tipo de **letra** se deben alinear en los límites de **palabras** .

Si especifica cadenas de caracteres en las matrices de **menús**, **windowClass**, **title** y tipo de **letra** , debe utilizar cadenas Unicode. Utilice la función [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) para generar estas cadenas Unicode a partir de cadenas ANSI.

Los miembros **x**, **y**, **CX** y **CY** especifican valores en las unidades del cuadro de diálogo. Puede convertir estos valores en unidades de pantalla (píxeles) mediante la función [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

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

[**WM \_**](/windows/desktop/winmsg/wm-setfont)
</dt> <dt>

**Vista**
</dt> <dt>

[Cuadros de diálogo](dialog-boxes.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**NDPTECGDI**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> </dl>

 

