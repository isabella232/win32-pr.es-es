---
title: Estructura DLGITEMTEMPLATEEX
description: Bloque de texto utilizado por una plantilla de cuadro de diálogo extendido para describir el cuadro de diálogo extendido. Para obtener una descripción del formato de una plantilla de cuadro de diálogo extendido, vea DLGTEMPLATEEX.
ms.assetid: c60fd8db-ee4b-433b-a2fb-68b9a677bac8
keywords:
- Cuadros de diálogo de la estructura DLGITEMTEMPLATEEX
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422591"
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



## <a name="members"></a>Miembros

<dl> <dt>

**helpID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Identificador del contexto de ayuda para el control. Cuando el sistema envía un mensaje de [**\_ ayuda de WM**](../shell/wm-help.md) , pasa el valor **helpID** en el miembro **dwContextId** de la estructura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) .

</dd> <dt>

**exStyle**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Los estilos extendidos de una ventana. Este miembro no se utiliza para crear controles en cuadros de diálogo, pero las aplicaciones que usan plantillas de cuadro de diálogo pueden usarlo para crear otros tipos de ventanas. Para obtener una lista de valores, vea [**estilos extendidos de ventana**](/windows/desktop/winmsg/extended-window-styles).

</dd> <dt>

**style**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

El estilo del control. Este miembro puede ser una combinación de [valores de estilo de ventana](/windows/desktop/winmsg/window-styles) ( **como WS \_ Border**) y uno o varios de los valores de estilo de [control](/windows/desktop/Controls/common-control-styles) (por ejemplo, el **\_ PUSHBUTTON de BS** y **es \_ left**).

</dd> <dt>

**x**
</dt> <dd>

Tipo: **Short**

</dd> <dd>

La coordenada x, en unidades de cuadro de diálogo, de la esquina superior izquierda del control. Esta coordenada siempre es relativa a la esquina superior izquierda del área cliente del cuadro de diálogo.

</dd> <dt>

**y**
</dt> <dd>

Tipo: **Short**

</dd> <dd>

La coordenada y, en unidades de cuadro de diálogo, de la esquina superior izquierda del control. Esta coordenada siempre es relativa a la esquina superior izquierda del área cliente del cuadro de diálogo.

</dd> <dt>

**serie**
</dt> <dd>

Tipo: **Short**

</dd> <dd>

Ancho, en unidades de cuadro de diálogo, del control.

</dd> <dt>

**CY**
</dt> <dd>

Tipo: **Short**

</dd> <dd>

Alto, en unidades de cuadro de diálogo, del control.

</dd> <dt>

**id**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Identificador del control.

</dd> <dt>

**windowClass**
</dt> <dd>

Tipo: **SZ \_ o \_ Ord**

</dd> <dd>

Matriz de longitud variable de elementos de 16 bits que especifica la clase de ventana del control. Si el primer elemento de esta matriz tiene cualquier valor distinto de 0xFFFF, el sistema trata la matriz como una cadena Unicode terminada en null que especifica el nombre de una clase de ventana registrada.

Si el primer elemento es 0xFFFF, la matriz tiene un elemento adicional que especifica el valor ordinal de una clase del sistema predefinida. El ordinal puede ser uno de los siguientes valores Atom.



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

Tipo: **SZ \_ o \_ Ord**

</dd> <dd>

Matriz de longitud variable de elementos de 16 bits que contiene el texto inicial o el identificador de recursos del control. Si el primer elemento de esta matriz es 0xFFFF, la matriz tiene un elemento adicional que especifica el valor ordinal de un recurso, como un icono, en un archivo ejecutable. Puede usar un identificador de recursos para los controles, como los controles de iconos estáticos, que cargan y muestran un icono u otro recurso en lugar de texto. Si el primer elemento es cualquier valor distinto de 0xFFFF, el sistema trata la matriz como una cadena Unicode terminada en null que especifica el texto inicial.

</dd> <dt>

**extracount**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

El número de bytes de datos de creación que siguen a este miembro. Si este valor es mayor que cero, los datos de creación comienzan en el siguiente límite de **palabras** . Estos datos de creación pueden tener cualquier tamaño y formato. El procedimiento de ventana del control debe ser capaz de interpretar los datos. Cuando el sistema crea el control, pasa un puntero a estos datos en el parámetro *lParam* del mensaje de [**\_ creación de WM**](/windows/desktop/winmsg/wm-create) que envía al control.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una plantilla extendida para un cuadro de diálogo se compone de un encabezado [**DLGTEMPLATEEX**](dlgtemplateex.md) seguido de una estructura **DLGITEMTEMPLATEEX** para cada control del cuadro de diálogo.

Cada estructura **DLGITEMTEMPLATEEX** debe estar alineada en un límite **DWORD** . Las matrices de **título** y **windowClass** de longitud variable deben alinearse en los límites de **palabras** . La matriz de datos de creación, si la hay, debe estar alineada en un límite de **palabras** .

Si especifica cadenas de caracteres en las matrices **windowClass** y **title** , debe utilizar cadenas Unicode. Utilice la función [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) para generar cadenas Unicode a partir de cadenas ANSI.

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

[**creación de WM \_**](/windows/desktop/winmsg/wm-create)
</dt> <dt>

**Vista**
</dt> <dt>

[Cuadros de diálogo](dialog-boxes.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> <dt>

[**ayuda de WM \_**](../shell/wm-help.md)
</dt> </dl>

 

