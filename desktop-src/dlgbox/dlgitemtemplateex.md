---
title: Estructura DLGITEMTEMPLATEEX
description: Bloque de texto utilizado por una plantilla de cuadro de diálogo extendido para describir el cuadro de diálogo extendido. Para obtener una descripción del formato de una plantilla de cuadro de diálogo extendido, vea DLGTEMPLATEEX.
ms.assetid: c60fd8db-ee4b-433b-a2fb-68b9a677bac8
keywords:
- Cuadros de diálogo de estructura DLGITEMTEMPLATEEX
topic_type:
- apiref
api_name:
- DLGITEMTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7261fa832e5acfb4ef7d9723bc93b862947ef380
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241383"
---
# <a name="dlgitemtemplateex-structure"></a>Estructura DLGITEMTEMPLATEEX

Bloque de texto utilizado por una plantilla de cuadro de diálogo extendido para describir el cuadro de diálogo extendido. Para obtener una descripción del formato de una plantilla de cuadro de diálogo extendido, vea [**DLGTEMPLATEEX**](dlgtemplateex.md).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD     helpID;
  DWORD     exStyle;
  DWORD     style;
  short     x;
  short     y;
  short     cx;
  short     cy;
  DWORD     id;
  sz_Or_Ord windowClass;
  sz_Or_Ord title;
  WORD      extraCount;
} DLGITEMTEMPLATEEX;
```



## <a name="members"></a>Members

<dl> <dt>

**helpID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Identificador de contexto de ayuda para el control. Cuando el sistema envía un [**mensaje WM \_ HELP,**](../shell/wm-help.md) pasa el valor **helpID** en el **miembro dwContextId** de la [**estructura HELPINFO.**](/windows/win32/api/winuser/ns-winuser-helpinfo)

</dd> <dt>

**exStyle**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Estilos extendidos de una ventana. Este miembro no se usa para crear controles en cuadros de diálogo, pero las aplicaciones que usan plantillas de cuadro de diálogo pueden usarlo para crear otros tipos de ventanas. Para obtener una lista de valores, vea [**Estilos de ventana extendidos.**](/windows/desktop/winmsg/extended-window-styles)

</dd> <dt>

**style**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

El estilo del control. Este miembro puede ser una combinación de valores de estilo de ventana [(como](/windows/desktop/winmsg/window-styles) **WS \_ BORDER)** y uno o varios de los valores de estilo de [control](/windows/desktop/Controls/common-control-styles) (como **BS \_ PUSHBUTTON** y **ES \_ LEFT).**

</dd> <dt>

**x**
</dt> <dd>

Tipo: **short**

</dd> <dd>

Coordenada x, en unidades de cuadro de diálogo, de la esquina superior izquierda del control. Esta coordenada siempre es relativa a la esquina superior izquierda del área de cliente del cuadro de diálogo.

</dd> <dt>

**y**
</dt> <dd>

Tipo: **short**

</dd> <dd>

Coordenada y, en unidades de cuadro de diálogo, de la esquina superior izquierda del control. Esta coordenada siempre es relativa a la esquina superior izquierda del área de cliente del cuadro de diálogo.

</dd> <dt>

**Cx**
</dt> <dd>

Tipo: **short**

</dd> <dd>

Ancho, en unidades de cuadro de diálogo, del control.

</dd> <dt>

**Cy**
</dt> <dd>

Tipo: **short**

</dd> <dd>

Alto, en unidades de cuadro de diálogo, del control.

</dd> <dt>

**id**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Identificador de control.

</dd> <dt>

**windowClass**
</dt> <dd>

Tipo: **sz \_ o \_ ord**

</dd> <dd>

Matriz de longitud variable de elementos de 16 bits que especifica la clase de ventana del control. Si el primer elemento de esta matriz es cualquier valor distinto de 0xFFFF, el sistema trata la matriz como una cadena Unicode terminada en NULL que especifica el nombre de una clase de ventana registrada.

Si el primer elemento es 0xFFFF, la matriz tiene un elemento adicional que especifica el valor ordinal de una clase del sistema predefinida. El ordinal puede ser uno de los siguientes valores atom.



| Value                                                                             | Significado               |
|-----------------------------------------------------------------------------------|-----------------------|
| <dl> <dt>0x0080</dt> </dl> | Botón<br/>     |
| <dl> <dt>0x0081</dt> </dl> | Editar<br/>       |
| <dl> <dt>0x0082</dt> </dl> | estática<br/>     |
| <dl> <dt>0x0083</dt> </dl> | Cuadro de lista<br/>   |
| <dl> <dt>0x0084</dt> </dl> | Barra de desplazamiento<br/> |
| <dl> <dt>0x0085</dt> </dl> | Cuadro combinado<br/>  |



 

</dd> <dt>

**title**
</dt> <dd>

Tipo: **sz \_ o \_ ord**

</dd> <dd>

Matriz de longitud variable de elementos de 16 bits que contiene el texto inicial o el identificador de recursos del control. Si el primer elemento de esta matriz es 0xFFFF, la matriz tiene un elemento adicional que especifica el valor ordinal de un recurso, como un icono, en un archivo ejecutable. Puede usar un identificador de recurso para los controles, como los controles de icono estáticos, que cargan y muestran un icono u otro recurso en lugar de texto. Si el primer elemento es cualquier valor distinto de 0xFFFF, el sistema trata la matriz como una cadena Unicode terminada en NULL que especifica el texto inicial.

</dd> <dt>

**extraCount**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Número de bytes de datos de creación que siguen a este miembro. Si este valor es mayor que cero, los datos de creación comienzan en el siguiente límite **de WORD.** Estos datos de creación pueden ser de cualquier tamaño y formato. El procedimiento de ventana del control debe ser capaz de interpretar los datos. Cuando el sistema crea el control, pasa un puntero a estos datos en el parámetro *lParam* del [**mensaje CREATE \_ de WM**](/windows/desktop/winmsg/wm-create) que envía al control.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una plantilla extendida para un cuadro de diálogo consta de un encabezado [**DLGTEMPLATEEX**](dlgtemplateex.md) seguido de una **estructura DLGITEMTEMPLATEEX** para cada control del cuadro de diálogo.

Cada **estructura DLGITEMTEMPLATEEX** debe alinearse en un **límite DWORD.** Las matrices **windowClass** y **title** de longitud variable deben alinearse en los **límites de WORD.** La matriz de datos de creación, si la hay, debe alinearse en un **límite de WORD.**

Si especifica cadenas de caracteres en las **matrices windowClass** y **title,** debe usar cadenas Unicode. Use la [**función MultiByteToWideChar para**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) generar cadenas Unicode a partir de cadenas ANSI.

Los **miembros x**, **y**, **cx** y **cy** especifican valores en unidades de cuadro de diálogo. Puede convertir estos valores en unidades de pantalla (píxeles) mediante la [**función MapDialogRect.**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)

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

[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DLGTEMPLATEEX**](dlgtemplateex.md)
</dt> <dt>

[**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Cuadros de diálogo](dialog-boxes.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> <dt>

[**WM \_ HELP**](../shell/wm-help.md)
</dt> </dl>

 

