---
title: Recurso ACCELERATORS
description: Define uno o varios aceleradores para una aplicación. Un acelerador es una pulsación de tecla definida por la aplicación para proporcionar al usuario una manera rápida de realizar una tarea.
ms.assetid: 5953ee2d-b7a7-45d2-8445-4cba1207e272
keywords:
- Menús de recursos ACCELERATORS y otros recursos
topic_type:
- apiref
api_name:
- ACCELERATORS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2aeb09ca52438f7b2f4903e5403eeb722e5d7d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268559"
---
# <a name="accelerators-resource"></a>Recurso ACCELERATORS

Define uno o varios aceleradores para una aplicación. Un acelerador es una pulsación de tecla definida por la aplicación para proporcionar al usuario una manera rápida de realizar una tarea.

``` syntax
acctablename ACCELERATORS [optional-statements] {event, idvalue, [type] [options]... }
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="acctablename"></span><span id="ACCTABLENAME"></span>*acctablename*
</dt> <dd>

Nombre único o un valor entero de 16 bits sin signo que identifica el recurso.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*
</dt> <dd>

Cero o más de las siguientes instrucciones.



| .                                                        | Descripción                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CHARACTERISTICS**](characteristics-statement.md) *dword*     | Información definida por el usuario sobre un recurso que pueden usar las herramientas que leen y escriben archivos de recursos. Para obtener más información, vea [**CHARACTERISTICS**](characteristics-statement.md). |
| [**Language**](language-statement.md) *Language*, *sublanguage* | Especifica el idioma del recurso. Para obtener más información, vea [**LANGUAGE**](language-statement.md).                                                                              |
| [**VERSION**](version-statement.md) *dword*                     | Número de versión definido por el usuario para el recurso que pueden usar las herramientas que leen y escriben archivos de recursos. Para obtener más información, vea [**VERSION**](version-statement.md).              |



 

</dd> <dt>

<span id="event"></span><span id="EVENT"></span>*Evento*
</dt> <dd>

Pulsación de tecla que se va a usar como acelerador. Puede ser cualquiera de los siguientes tipos de caracteres.



| Tipo                    | Descripción                                                                                                                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "*char*"                | Un solo carácter entre comillas dobles ("). El carácter puede ir precedido de un carácter de intercalación (^), lo que significa que el carácter es un carácter de control.                                                                                  |
| *Carácter*             | Valor entero que representa un carácter. El *parámetro de* tipo debe ser **ASCII.**                                                                                                                                                           |
| *carácter de clave virtual* | Valor entero que representa una clave virtual. La clave virtual para las claves alfanuméricas se puede especificar colocando la letra o el número en mayúsculas entre comillas dobles (por ejemplo, "9" o "C"). El *parámetro* de tipo debe ser **VIRTKEY.** |



 

</dd> <dt>

<span id="idvalue"></span><span id="IDVALUE"></span>*idvalue*
</dt> <dd>

un valor entero de 16 bits sin signo que identifica el acelerador.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*Tipo*
</dt> <dd>

Solo es necesario cuando *el parámetro* de evento es *un carácter* o un carácter de *clave virtual*. El *parámetro* type especifica **ASCII o** **VIRTKEY**; El valor entero del *evento* se interpreta en consecuencia. Cuando **se especifica VIRTKEY** y *el evento* contiene una cadena, el *evento* debe estar en mayúsculas.

</dd> <dt>

<span id="options"></span><span id="OPTIONS"></span>*Opciones*
</dt> <dd>

opciones que definen el acelerador. Este parámetro puede ser uno o varios de los valores siguientes.



| Opción                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **NOINVERT**                       | Especifica que no se resalta ningún elemento de menú de nivel superior cuando se usa el acelerador. Esto resulta útil al definir aceleradores para acciones como el desplazamiento que no corresponden a un elemento de menú. Si **se omite NOINVERT,** se resaltará un elemento de menú de nivel superior (si es posible) cuando se usa el acelerador. Este atributo está obsoleto y se conserva solo por compatibilidad con versiones anteriores con archivos de recursos diseñados para archivos de 16 Windows. |
| **ALT**                            | Hace que el acelerador se active solo si la tecla ALT está presionada. Solo se aplica a las claves virtuales.                                                                                                                                                                                                                                                                                                                                            |
| **CAMBIO**                          | Hace que el acelerador se active solo si la tecla MAYÚS está fuera de servicio. Solo se aplica a las claves virtuales                                                                                                                                                                                                                                                                                                                                           |
| [**CONTROL**](control-control.md) | Define el carácter como un carácter de control (el acelerador solo se activa si la tecla CONTROL está fuera de servicio). Esto tiene el mismo efecto que usar un carácter de intercalación (^) antes del carácter de acelerador en el *parámetro de* evento. Solo se aplica a las claves virtuales                                                                                                                                                                                           |



 

</dd> </dl>

Algunos atributos también se admiten por compatibilidad con versiones anteriores. Para más información, consulte [Atributos de recursos comunes.](common-resource-attributes.md)

## <a name="remarks"></a>Observaciones

La [**función TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) se usa para traducir los mensajes del acelerador de la cola de la aplicación en mensajes [**WM \_ COMMAND**](./wm-command.md) [**o WM \_ SYSCOMMAND.**](./wm-syscommand.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso de teclas de aceleración.

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

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Uso de aceleradores de teclado](./using-keyboard-accelerators.md)
</dt> <dt>

[**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**CARACTERÍSTICAS**](characteristics-statement.md)
</dt> <dt>

[**DIÁLOGO**](dialog-resource.md)
</dt> <dt>

[**LENGUA**](language-statement.md)
</dt> <dt>

[**MENÚ**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**VERSIÓN**](version-statement.md)
</dt> </dl>

 

 