---
title: Recurso de cuadro de diálogo
description: Define un cuadro de diálogo. | Recurso de cuadro de diálogo
ms.assetid: d166fb7d-0fe5-4e48-a545-19acc0ff80f1
keywords:
- Menús de recursos de cuadro de diálogo y otros recursos
topic_type:
- apiref
api_name:
- DIALOG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7a1aef314406340c42c6a4aca40b76f91ac353
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678689"
---
# <a name="dialog-resource"></a>Recurso de cuadro de diálogo

Define un cuadro de diálogo. La instrucción define la posición y las dimensiones del cuadro de diálogo en la pantalla, así como el estilo del cuadro de diálogo.

> [!Note]  
> El **cuadro de diálogo** es un identificador de recurso obsoleto. Las nuevas aplicaciones deben usar [**DIALOGEX**](dialogex-resource.md).

 

``` syntax
nameID DIALOG x, y, width, height  [optional-statements] {control-statement  . . . }
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nombre único o un valor entero de 16 bits sin signo único que identifica el cuadro de diálogo.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instrucciones opcionales*
</dt> <dd>

Opciones del cuadro de diálogo. Puede ser cero o más de las instrucciones siguientes.



| .                                                        | Descripción                                                                                                                                                                                  |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Título**](caption-statement.md) de "*texto*"                    | Título del cuadro de diálogo si tiene una barra de título. Para obtener más información, consulte [**Caption**](caption-statement.md).                                                                             |
| [**Características**](characteristics-statement.md) *DWORD*     | Valor **DWORD** definido por el usuario para que lo usen las herramientas de recursos. El sistema no utiliza este valor. Para obtener más información, vea [**características**](characteristics-statement.md).                |
| [](class-statement.md) *Clase de* clase                         | Entero de 16 bits sin signo o cadena, entre comillas dobles ("), que identifica la clase del cuadro de diálogo. Para obtener más información, vea [**clase**](class-statement.md).      |
| **ExStyle =** *estilos extendidos*                                   | Estilo de ventana extendida del cuadro de diálogo. Para obtener más información, vea [**ExStyle**](exstyle-statement.md).                                                                                     |
|  *Puntuación* de fuente, tipo de *letra*                                 | Tamaño de punto y tipo de letra de la fuente. Para obtener más información, vea [**Font**](font-statement.md).                                                                                              |
| [](language-statement.md) *Idioma* del idioma, *subidioma* | Idioma del cuadro de diálogo. Para obtener más información, vea [**Language**](language-statement.md).                                                                                                |
|  *NombreMenú* de menú                                              | Menú que se va a usar. Este valor es el nombre del menú o su identificador entero.                                                                                                        |
| [](style-statement.md) *Estilos* de estilo                        | Estilos del cuadro de diálogo. Para obtener más información, vea [**Style**](style-statement.md).                                                                                                        |
| [**Versión**](version-statement.md) *DWORD*                     | Valor **DWORD** definido por el usuario. Esta instrucción está pensada para su uso por parte de herramientas de recursos adicionales y el sistema no la utiliza. Para obtener más información, vea [**versión**](version-statement.md). |



 

</dd> </dl>

Algunos atributos también se admiten por razones de compatibilidad con versiones anteriores. Para obtener más información, vea [atributos comunes de recursos](common-resource-attributes.md).

## <a name="remarks"></a>Observaciones

La función [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) devuelve las unidades base de cuadro de diálogo en píxeles. El significado exacto de las coordenadas depende del estilo definido por la instrucción de la opción de [**estilo**](style-statement.md) . En el caso de los cuadros de diálogo de estilo secundario, las coordenadas son relativas al origen de la ventana primaria, a menos que el cuadro de diálogo tenga el estilo **DS \_ ABSALIGN**; en ese caso, las coordenadas son relativas al origen de la pantalla de presentación.

No use el estilo **\_ secundario WS** con un cuadro de diálogo modal. La función [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) siempre deshabilita el elemento primario/propietario del cuadro de diálogo que se acaba de crear. Cuando una ventana primaria está deshabilitada, sus ventanas secundarias se deshabilitan implícitamente. Dado que la ventana primaria del cuadro de diálogo de estilo secundario está deshabilitada, el cuadro de diálogo de estilo secundario también es.

Si un cuadro de diálogo tiene el estilo **\_ ABSALIGN de DS** , las coordenadas del cuadro de diálogo de la esquina superior izquierda son relativas al origen de la pantalla en lugar de a la esquina superior izquierda de la ventana primaria. Normalmente se utiliza este estilo cuando se desea que el cuadro de diálogo se inicie en una parte específica de la pantalla, independientemente de dónde pueda estar la ventana primaria en la pantalla.

También se puede usar el cuadro de **diálogo** nombre como parámetro de nombre de clase para la función [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) con el fin de crear una ventana con atributos de cuadro de diálogo.

## <a name="examples"></a>Ejemplos

A continuación se muestra el uso de la instrucción **Dialog** :

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

[**ACELERADORES**](accelerators-resource.md)
</dt> <dt>

[**SUS**](characteristics-statement.md)
</dt> <dt>

[**CONTROL**](control-control.md)
</dt> <dt>

[**CreateDialog**](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[**MÓDULO**](language-statement.md)
</dt> <dt>

[**MENU**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Versión**](version-statement.md)
</dt> </dl>

 

 
