---
title: Recurso DIALOG
description: Define un cuadro de diálogo. | Recurso DIALOG
ms.assetid: d166fb7d-0fe5-4e48-a545-19acc0ff80f1
keywords:
- Menús de recursos DIALOG y otros recursos
topic_type:
- apiref
api_name:
- DIALOG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a821bb6890a9aee8dd74c5412556bf45ca0b739a6eb12cf5d582fbb91463c2f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034353"
---
# <a name="dialog-resource"></a>Recurso DIALOG

Define un cuadro de diálogo. La instrucción define la posición y las dimensiones del cuadro de diálogo en la pantalla, así como el estilo del cuadro de diálogo.

> [!Note]  
> **DIALOG** es un identificador de recurso obsoleto. Las nuevas aplicaciones deben usar [**DIALOGEX.**](dialogex-resource.md)

 

``` syntax
nameID DIALOG x, y, width, height  [optional-statements] {control-statement  . . . }
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nombre único o un valor entero único de 16 bits sin signo que identifica el cuadro de diálogo.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*
</dt> <dd>

Opciones para el cuadro de diálogo. Puede ser cero o más de las siguientes instrucciones.



| .                                                        | Descripción                                                                                                                                                                                  |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CAPTION**](caption-statement.md) "*text*"                    | Título del cuadro de diálogo si tiene una barra de título. Para obtener más información, vea [**CAPTION**](caption-statement.md).                                                                             |
| [**CHARACTERISTICS**](characteristics-statement.md) *dword*     | Valor **DWORD** definido por el usuario para que lo usen las herramientas de recursos. El sistema no usa este valor. Para obtener más información, vea [**CHARACTERISTICS**](characteristics-statement.md).                |
| [**CLASS (clase)**](class-statement.md)                          | Entero de 16 bits sin signo o cadena, entre comillas dobles ("), que identifica la clase del cuadro de diálogo. Para obtener más información, vea [**CLASS**](class-statement.md).      |
| **EXSTYLE=** *estilos extendidos*                                   | Estilo de ventana extendido del cuadro de diálogo. Para obtener más información, [**vea EXSTYLE**](exstyle-statement.md).                                                                                     |
| **Font** *pointsize*, *typeface*                                 | Tamaño de punto y tipo de letra de la fuente. Para obtener más información, vea [**FONT**](font-statement.md).                                                                                              |
| [**Language**](language-statement.md) *language*, *sublanguage* | Idioma del cuadro de diálogo. Para obtener más información, vea [**LANGUAGE**](language-statement.md).                                                                                                |
| **MENU menuname**                                               | Menú que se va a usar. Este valor es el nombre del menú o su identificador entero.                                                                                                        |
| [**Estilos**](style-statement.md) *STYLE*                        | Estilos del cuadro de diálogo. Para obtener más información, vea [**STYLE**](style-statement.md).                                                                                                        |
| [**VERSION**](version-statement.md) *dword*                     | Valor **DWORD** definido por el usuario. Esta instrucción está pensada para su uso por herramientas de recursos adicionales y el sistema no la usa. Para obtener más información, vea [**VERSION**](version-statement.md). |



 

</dd> </dl>

Algunos atributos también se admiten por compatibilidad con versiones anteriores. Para más información, consulte [Atributos de recursos comunes.](common-resource-attributes.md)

## <a name="remarks"></a>Comentarios

La [**función GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) devuelve las unidades base del diálogo en píxeles. El significado exacto de las coordenadas depende del estilo definido por la instrucción [**de opción STYLE.**](style-statement.md) Para los cuadros de diálogo de estilo secundario, las coordenadas son relativas al origen de la ventana primaria, a menos que el cuadro de diálogo tenga el estilo **DS \_ ABSALIGN;** en ese caso, las coordenadas son relativas al origen de la pantalla.

No use el estilo **WS \_ CHILD** con un cuadro de diálogo modal. La [**función DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) siempre deshabilita el elemento primario o propietario del cuadro de diálogo recién creado. Cuando se deshabilita una ventana primaria, sus ventanas secundarias se deshabilitan implícitamente. Puesto que la ventana primaria del cuadro de diálogo de estilo secundario está deshabilitada, el cuadro de diálogo de estilo secundario también lo es.

Si un cuadro de diálogo tiene el estilo **\_ ABSALIGN de DS,** las coordenadas del diálogo de la esquina superior izquierda son relativas al origen de la pantalla en lugar de a la esquina superior izquierda de la ventana primaria. Normalmente usaría este estilo cuando quisiera que el cuadro de diálogo se iniciara en una parte específica de la pantalla, independientemente de dónde se encontrara la ventana primaria en la pantalla.

El nombre **DIALOG** también se puede usar como parámetro class-name para la [**función CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para crear una ventana con atributos de cuadro de diálogo.

## <a name="examples"></a>Ejemplos

A continuación se muestra el uso de la **instrucción DIALOG:**

``` syntax
#include <windows.h>

ErrorDialog DIALOG  10, 10, 300, 110
STYLE WS_POPUP | WS_BORDER
CAPTION "Error!" 
{
    CTEXT "Select One:", 1, 10, 10, 280, 12
    PUSHBUTTON "&Retry", 2, 75, 30, 60, 12
    PUSHBUTTON "&Abort", 3, 75, 50, 60, 12
    PUSHBUTTON "&Ignore", 4, 75, 80, 60, 12
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Usar cuadros de diálogo](../dlgbox/using-dialog-boxes.md)
</dt> <dt>

[**Aceleradores**](accelerators-resource.md)
</dt> <dt>

[**Características**](characteristics-statement.md)
</dt> <dt>

[**Control**](control-control.md)
</dt> <dt>

[**CreateDialog**](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**Cuadro de diálogo**](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[**Lengua**](language-statement.md)
</dt> <dt>

[**Menú**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Versión**](version-statement.md)
</dt> </dl>

 

 
