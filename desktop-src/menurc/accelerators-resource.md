---
title: Recurso de ACELERAdores
description: Define uno o varios aceleradores para una aplicación. Un acelerador es una pulsación de tecla definida por la aplicación para proporcionar al usuario una forma rápida de realizar una tarea.
ms.assetid: 5953ee2d-b7a7-45d2-8445-4cba1207e272
keywords:
- Menús de recursos de ACELERAdores y otros recursos
topic_type:
- apiref
api_name:
- ACCELERATORS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2aeb09ca52438f7b2f4903e5403eeb722e5d7d7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533136"
---
# <a name="accelerators-resource"></a>Recurso de ACELERAdores

Define uno o varios aceleradores para una aplicación. Un acelerador es una pulsación de tecla definida por la aplicación para proporcionar al usuario una forma rápida de realizar una tarea.

``` syntax
acctablename ACCELERATORS [optional-statements] {event, idvalue, [type] [options]... }
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="acctablename"></span><span id="ACCTABLENAME"></span>*acctablename*
</dt> <dd>

Nombre único o un valor entero sin signo de 16 bits que identifica el recurso.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instrucciones opcionales*
</dt> <dd>

Cero o más de las instrucciones siguientes.



| .                                                        | Descripción                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Características**](characteristics-statement.md) *DWORD*     | Información definida por el usuario sobre un recurso que pueden usar las herramientas que leen y escriben archivos de recursos. Para obtener más información, vea [**características**](characteristics-statement.md). |
| [](language-statement.md) *Idioma* del idioma, *subidioma* | Especifica el idioma del recurso. Para obtener más información, vea [**Language**](language-statement.md).                                                                              |
| [**Versión**](version-statement.md) *DWORD*                     | Número de versión definido por el usuario para el recurso que pueden usar las herramientas que leen y escriben archivos de recursos. Para obtener más información, vea [**versión**](version-statement.md).              |



 

</dd> <dt>

<span id="event"></span><span id="EVENT"></span>*ceso*
</dt> <dd>

Pulsación de tecla que se va a usar como acelerador. Puede ser cualquiera de los siguientes tipos de caracteres.



| Tipo                    | Descripción                                                                                                                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "*Char*"                | Un solo carácter entre comillas dobles ("). El carácter puede ir precedido de un símbolo de intercalación (^), lo que significa que el carácter es un carácter de control.                                                                                  |
| *Carácter*             | Valor entero que representa un carácter. El parámetro de *tipo* debe ser **ASCII**.                                                                                                                                                           |
| *carácter de clave virtual* | Un valor entero que representa una clave virtual. La clave virtual de las claves alfanuméricas se puede especificar colocando la letra mayúscula o el número entre comillas dobles (por ejemplo, "9" o "C"). El parámetro de *tipo* debe ser **VIRTKEY**. |



 

</dd> <dt>

<span id="idvalue"></span><span id="IDVALUE"></span>*idvalue*
</dt> <dd>

valor entero sin signo de 16 bits que identifica el acelerador.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*automáticamente*
</dt> <dd>

Solo se requiere cuando el parámetro de *evento* es un *carácter o un* *carácter de tecla virtual*. El parámetro de *tipo* especifica **ASCII** o **VIRTKEY**; el valor entero del *evento* se interpreta en consecuencia. Cuando se especifica **VIRTKEY** y el *evento* contiene una cadena, el *evento* debe estar en mayúsculas.

</dd> <dt>

<span id="options"></span><span id="OPTIONS"></span>*Opciones*
</dt> <dd>

opciones que definen el acelerador. Este parámetro puede ser uno o varios de los valores siguientes.



| Opción                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Noinvertir**                       | Especifica que no se resalta ningún elemento de menú de nivel superior cuando se utiliza el acelerador. Esto resulta útil al definir aceleradores para acciones como el desplazamiento que no se corresponden con un elemento de menú. Si se omite **Revert** , se resaltará un elemento de menú de nivel superior (si es posible) cuando se use el acelerador. Este atributo está obsoleto y solo se conserva por compatibilidad con versiones anteriores de los archivos de recursos diseñados para Windows de 16 bits. |
| **ALTERNATIVA**                            | Hace que el acelerador se active solo si la tecla ALT está presionada. Solo se aplica a las claves virtuales.                                                                                                                                                                                                                                                                                                                                            |
| **MOVER**                          | Hace que el acelerador se active solo si la tecla Mayús está presionada. Solo se aplica a las claves virtuales                                                                                                                                                                                                                                                                                                                                           |
| [**CONTROL**](control-control.md) | Define el carácter como un carácter de control (el acelerador solo se activa si la tecla CONTROL está inactiva). Esto tiene el mismo efecto que el uso de un símbolo de intercalación (^) antes del carácter de acelerador en el parámetro de *evento* . Solo se aplica a las claves virtuales                                                                                                                                                                                           |



 

</dd> </dl>

Algunos atributos también se admiten por razones de compatibilidad con versiones anteriores. Para obtener más información, vea [atributos comunes de recursos](common-resource-attributes.md).

## <a name="remarks"></a>Observaciones

La función [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) se usa para convertir los mensajes de acelerador de la cola de la aplicación en [**mensajes de WM o de \_**](./wm-command.md) [**WM \_ SYSCOMMAND**](./wm-syscommand.md) .

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo se muestra el uso de las teclas de aceleración.

``` syntax
1 ACCELERATORS
{
  "^C",  IDDCLEAR         ; control C
  "K",   IDDCLEAR         ; shift K
  "k",   IDDELLIPSE, ALT  ; alt k
  98,    IDDRECT, ASCII   ; b
  66,    IDDSTAR, ASCII   ; B (shift b)
  "g",   IDDRECT          ; g
  "G",   IDDSTAR          ; G (shift G)
  VK_F1, IDDCLEAR, VIRTKEY                ; F1
  VK_F1, IDDSTAR, CONTROL, VIRTKEY        ; control F1
  VK_F1, IDDELLIPSE, SHIFT, VIRTKEY       ; shift F1
  VK_F1, IDDRECT, ALT, VIRTKEY            ; alt F1
  VK_F2, IDDCLEAR, ALT, SHIFT, VIRTKEY    ; alt shift F2
  VK_F2, IDDSTAR, CONTROL, SHIFT, VIRTKEY ; ctrl shift F2
  VK_F2, IDDRECT, ALT, CONTROL, VIRTKEY   ; alt control F2
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Usar aceleradores de teclado](./using-keyboard-accelerators.md)
</dt> <dt>

[**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**SUS**](characteristics-statement.md)
</dt> <dt>

[**DIÁLOGO**](dialog-resource.md)
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

 

 